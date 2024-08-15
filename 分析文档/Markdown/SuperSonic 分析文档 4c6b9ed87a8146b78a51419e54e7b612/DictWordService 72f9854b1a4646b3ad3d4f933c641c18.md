# DictWordService

`DictWordService` 是一个服务类，负责管理和处理与字典词（`DictWord`）相关的操作。这些词可能代表不同类型的语义元素，如维度、指标、实体等，用于增强系统的知识库。以下是对该类的详细解析：

### 主要功能

1. **加载字典词 (`loadDictWord`)**：
    - 初始化时从语义架构（`SemanticSchema`）中提取所有字典词，并将它们加载到知识库中。
2. **重新加载字典词 (`reloadDictWord`)**：
    - 定期检查字典词是否发生变化，如果有变化则更新知识库。
3. **获取所有字典词 (`getAllDictWords`)**：
    - 从语义架构中提取各种类型的字典词。
4. **去重 (`distinct`)**：
    - 对获取的语义元素进行去重操作，确保每个元素只出现一次。

### 方法解析

1. **`loadDictWord()`**：
    - **功能**：用于初始化时加载字典词。
    - **步骤**：
        1. 调用 `getAllDictWords()` 方法从语义架构中获取所有字典词。
        2. 将获取到的字典词保存在 `preDictWords` 中。
        3. 调用 `knowledgeBaseService.reloadAllData(dictWords)` 方法，将字典词加载到知识库中。
2. **`reloadDictWord()`**：
    - **功能**：定期重新加载字典词，以检查是否有新的字典词需要更新到知识库。
    - **步骤**：
        1. 记录开始时间。
        2. 获取当前所有的字典词，并与之前加载的字典词进行对比。
        3. 如果字典词未发生变化，直接返回。
        4. 如果有变化，更新 `preDictWords`，并调用 `knowledgeBaseService.updateOnlineKnowledge(dictWords)` 方法更新知识库。
        5. 记录并输出重新加载所花费的时间。
3. **`getAllDictWords()`**：
    - **功能**：从语义架构中提取所有类型的字典词。
    - **步骤**：
        1. 获取当前语义架构对象 `semanticSchema`。
        2. 通过调用 `addWordsByType()` 方法，将各种类型的语义元素转换为字典词并添加到词列表中。
4. **`addWordsByType(DictWordType value, List<SchemaElement> metas, List<DictWord> natures)`**：
    - **功能**：将给定类型的语义元素转换为字典词。
    - **步骤**：
        1. 调用 `distinct()` 方法对语义元素进行去重。
        2. 使用 `WordBuilderFactory.get(value).getDictWords(metas)` 将语义元素转换为字典词。
        3. 将生成的字典词添加到 `natures` 列表中。
5. **`distinct(List<SchemaElement> metas)`**：
    - **功能**：对语义元素进行去重。
    - **逻辑**：
        - 如果元素列表为空，直接返回。
        - 如果元素的类型是 `TERM`，表示术语类型，不进行去重，直接返回。
        - 否则，使用 `SchemaElement` 的 `ID` 作为键，去重后的元素列表通过映射收集并返回。

### 依赖关系

- **`SchemaService`**：用于获取当前的语义架构 `SemanticSchema`。
- **`KnowledgeBaseService`**：负责知识库的管理与更新操作。
- **`WordBuilderFactory`**：一个工厂类，根据传入的 `DictWordType` 类型，生成对应的字典词列表。

### 总结

`DictWordService` 是一个核心服务类，用于处理字典词的加载、更新和管理。它从语义架构中提取各种语义元素，并将它们转换为字典词，然后加载到系统的知识库中。这个类确保系统的知识库始终保持最新，并在需要时高效地更新字典词。