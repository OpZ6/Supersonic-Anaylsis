# SuperSonic 分析文档

作者：罗天成 

日期：2024.08.15

# 1. 文档概述

## 1.1 目的和范围

本文档旨在为SuperSonic项目提供全面的源码分析和数据流说明，帮助开发团队深入理解系统的内部工作机制。文档内容涵盖了系统架构、数据流动、关键代码结构、技术实现细节、测试与验证、以及开发建议等多个方面，确保开发团队能够快速上手并在工作中遵循最佳实践。

## 1.2 文档结构

本文档共分为8个主要部分，分别如下：

1. **项目背景**：介绍SuperSonic项目的基本信息，包括项目的背景、主要功能、及相关资源链接。
2. **系统架构概述**：提供系统的整体架构图，并解释各模块的功能及其相互关系。
3. **数据流分析**：详细描述数据在系统中的流动过程，包括关键数据处理流程及数据存储与检索方式。
4. **代码分析**：分析项目源码结构，解释核心类和方法的设计及其相互关系。
5. **关键技术**：探讨系统中使用的核心技术和算法，并阐述性能优化的相关内容。
6. **测试和验证**：介绍系统的测试框架、测试用例设计，以及性能测试与调优策略。
7. **常见问题与解决方案**：提供故障排查指南，帮助开发人员解决常见的系统问题。
8. **参考资料**：列出文档中引用的所有资源及附录内容，提供额外的技术支持。

# 2. 项目背景

## 2.1 项目简介

SuperSonic融合Chat BI（powered by LLM）和Headless BI（powered by 语义层）打造新一代的BI平台。这种融合确保了Chat BI能够与传统BI一样访问统一化治理的语义数据模型。此外，两种BI新范式都从中获得收益：

- Chat BI的Text2SQL生成通过检索语义数据模型得到增强。
- Headless BI的查询接口通过支持自然语言API得到拓展。

![image.png](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/image.png)

通过SuperSonic的问答对话界面，用户能够使用自然语言查询数据，系统会选择合适的可视化图表呈现结果。SuperSonic不需要修改或复制数据，只需要在物理数据模型之上构建逻辑语义模型（定义指标/维度/实体/标签，以及它们的业务含义、相互关系等），即可开启数据问答体验。与此同时，SuperSonic被设计为可插拔的框架，采用Java SPI机制来扩展定制功能。

![https://github.com/supersonicbi/supersonic-website/raw/main/static/img/supersonic_demo.gif](https://github.com/supersonicbi/supersonic-website/raw/main/static/img/supersonic_demo.gif)

### 项目动机

大型语言模型（LLM）如ChatGPT的出现正在重塑信息检索的方式，引领数据分析领域的一种新范式，被称为Chat BI。为了实现Chat BI，学术界和工业界主要关注利用LLM的能力将自然语言转换为SQL，通常称为Text2SQL或NL2SQL。尽管一些方法显示出有希望的结果，但它们在大规模实际应用中的可靠性还不足。

与此同时，另一种新兴范式被称为Headless BI，它专注于构建统一的语义数据模型，并引起了广泛的关注。Headless BI通过一个通用的语义层来实现，通过开放的API公开一致的数据语义。从我们的角度来看，Chat BI和Headless BI的融合有潜力在两个方面增强Text2SQL的能力：

1. 将数据语义（如业务术语、列值等）纳入提示词中，使LLM能够更好地理解语义，以减少幻觉。
2. 将高级SQL语法（如连接、公式等）的生成从LLM卸载到语义层，以减少复杂度。

为了验证上述想法，我们开发了SuperSonic项目，并将其应用在实际的内部产品中。与此同时，我们将SuperSonic作为一个可扩展的框架开源，希望能够促进数据问答对话领域的进一步发展。

### 开箱即用的特性

- 内置Chat BI界面以便*业务用户*输入数据查询。
- 内置Headless BI界面以便*分析工程师*构建语义模型。
- 内置基于规则的语义解析器，在特定场景（比如DEMO演示、集成测试）可以提升推理效率。
- 支持文本输入联想、多轮对话、查询后问题推荐等高级特征。
- 支持三级权限控制：数据集级、列级、行级。

## 2.2 项目资源

### 项目地址

[https://github.com/tencentmusic/supersonic/blob/master/README.md](https://github.com/tencentmusic/supersonic/blob/master/README.md)

### 项目DEMO

[http://117.72.46.148:9080/chat](http://117.72.46.148:9080/chat)

### 官方文档

[项目介绍](https://supersonicbi.github.io/)

### 相关社区

![image.png](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/image%201.png)

### 相关资料

[SuperSonic简介 - 天戈朱 - 博客园](https://www.cnblogs.com/tgzhu/p/17911526.html)

# 3. 系统架构概述

### 3.1 整体架构

SuperSonic的整体架构和主流程如下图所示：

![image.png](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/image%202.png)

## 3.2 模块功能

每个模块的功能及其在系统中的角色。

- **模型知识库**(Knowledge Base)： 定期从语义模型中提取相关的模式信息，构建词典和索引，以便后续的模式映射。
- **模式映射器(Schema Mapper)：** 将自然语言文本在知识库中进行匹配，为后续的语义解析提供相关信息。
- **语义解析器(Semantic Parser)：** 理解用户查询并抽取语义信息，生成语义查询语句S2SQL。
- **语义修正器(Semantic Corrector)：** 检查语义查询语句的合法性，对不合法的信息做修正和优化处理。
- **语义翻译器(Semantic Translator)：** 将语义查询语句翻译成可在物理数据模型上执行的SQL语句。
- **问答插件(Chat Plugin)：** 通过第三方工具扩展功能。给定所有配置的插件及其功能描述和示例问题，大语言模型将选择最合适的插件。
- **问答记忆(Chat Memory)：** 将历史的查询轨迹进行封装，可被召回作为few-shot样例嵌入提示词。

# 4. 数据流分析

## 4.1 数据流图

项目数据流图，展示数据在系统中的流动路径，包括输入、处理、存储和输出的过程，基于原项目框架基础上构建：

![image.png](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/image%203.png)

### 流程分析

[SuperSonic](https://supersonicbi.github.io/docs/chat-bi/问答对话/)

### 规则分析途径

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled.png)

依赖预定义规则，快速解析简单查询，适用于规则覆盖范围内的场景。

### 大模型分析途径

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%201.png)

### 1. Schema映射（提供prompt参考）

- **步骤**：
    - 用户提出自然语言查询，系统提取查询中的关键元素并映射到数据库的实际字段。
- **实现**：
    - 利用预先定义的Schema映射规则或模型，识别查询中的关键词并将其与数据库中的相应字段进行匹配。
- **示例**：
    - 查询："访问次数最高的前三个部门"
    - 映射：`访问次数 -> access_count`, `部门 -> department`

### 2. Few-shot示例（提供样本参考）

[少样本提示 – Nextra](https://www.promptingguide.ai/zh/techniques/fewshot)

- **步骤**：
    - 提供若干示例问题及其对应的SQL查询，帮助模型理解查询的结构和意图。
- **实现**：
    - 通过示例展示如何将自然语言问题转换为S2SQL语句，模型在训练过程中学习转换规则。
- **示例：**
    - 示例1: “近7天播放超过一千万的歌曲有哪些？”
        - SQL: `SELECT song_name FROM songs WHERE play_count > 10000000 AND date >= '2024-07-03'`
    - 示例2: “超音数近30天访问次数的平均数”
        - SQL: `SELECT AVG(access_count) FROM access_data WHERE datediff(day, date, '2024-07-10') <= 30`
- **作用：**
    - “标签空间和演示指定的输入文本的分布都很重要（无论标签是否对单个输入正确）”
    - 使用的格式也对性能起着关键作用，即使只是使用随机标签，这也比没有标签好得多。
    - 其他结果表明，从真实标签分布（而不是均匀分布）中选择随机标签也有帮助。

### 3. LLM解析S2SQL（利用大模型学习模仿能力识别意图构建初步查询）

- **步骤**：
    - 使用大语言模型（LLM）根据Few-shot示例生成初步的S2SQL查询。
- **实现**：
    - 利用预训练的大语言模型（如GPT-3）根据用户查询和示例生成S2SQL。
- **示例**：
    - 用户查询："访问次数最高的前三个部门"
    - 初步SQL：`SELECT department FROM access_data ORDER BY access_count DESC LIMIT 3`

### 4. 修正S2SQL（规则修正查询逻辑结构）

- **步骤**：
    - 对初步生成的S2SQL进行语法和逻辑上的校正，确保其能够正确执行。
- **实现**：
    - 利用规则或另一个模型对生成的SQL进行验证和校正，确保SQL语句逻辑正确。
- **示例**：
    - 修正后的SQL：`SELECT department, SUM(access_count) FROM access_data GROUP BY department ORDER BY SUM(access_count) DESC LIMIT 3`

### 5. 最终执行SQL（转换可执行SQL）

- **步骤**：
    - 使用headless转换S2SQL为可执行SQL，执行修正后的SQL查询，并返回结果。
- **实现**：
    - 使用数据库连接执行校正后的SQL查询，并获取结果，结果通过前端展示给用户。
- **示例**：
    - 最终SQL：`WITH temp_table AS (SELECT department, access_count FROM access_data WHERE date = '2024-07-10') SELECT department, SUM(access_count) FROM temp_table GROUP BY department ORDER BY SUM(access_count) DESC LIMIT 3`

## 4.2 运行日志相关

### 标准日志参考

```
14:25:10 [http-nio-9080-exec-7] INFO  c.t.s.h.s.f.s.i.RetrieveServiceImpl 307 - searchMetricAndDimension searchResults:[SearchResult(recommend=超音速对比所有部门得访问人数, subRecommend=访问人数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false), SearchResult(recommend=超音速对比所有部门得访问时长, subRecommend=访问时长, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false), SearchResult(recommend=超音速对比所有部门得访问次数, subRecommend=访问次数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false), SearchResult(recommend=超音速对比所有部门得访问用户数, subRecommend=访问用户数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false)]
14:25:11 [http-nio-9080-exec-6] INFO  c.t.s.h.s.f.s.i.RetrieveServiceImpl 307 - searchMetricAndDimension searchResults:[SearchResult(recommend=超音速对比所有部门得访问次数, subRecommend=访问次数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false), SearchResult(recommend=超音速对比所有部门得人均访问次数, subRecommend=人均访问次数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false)]
14:25:15 [http-nio-9080-exec-4] INFO  c.t.s.h.s.f.s.i.RetrieveServiceImpl 307 - searchMetricAndDimension searchResults:[SearchResult(recommend=超音速对所有部门得访问次数, subRecommend=访问次数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false), SearchResult(recommend=超音速对所有部门得人均访问次数, subRecommend=人均访问次数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false)]
14:25:15 [http-nio-9080-exec-5] INFO  c.t.s.h.s.f.s.i.RetrieveServiceImpl 307 - searchMetricAndDimension searchResults:[SearchResult(recommend=超音速所有部门得访问次数, subRecommend=访问次数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false), SearchResult(recommend=超音速所有部门得人均访问次数, subRecommend=人均访问次数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false)]
14:25:18 [http-nio-9080-exec-2] INFO  c.t.s.h.s.f.s.i.RetrieveServiceImpl 307 - searchMetricAndDimension searchResults:[SearchResult(recommend=超音速所有部门的访问次数, subRecommend=访问次数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false), SearchResult(recommend=超音速所有部门的人均访问次数, subRecommend=人均访问次数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false)]
14:25:20 [http-nio-9080-exec-3] INFO  c.t.s.h.s.f.s.i.RetrieveServiceImpl 307 - searchMetricAndDimension searchResults:[SearchResult(recommend=对比超音速所有部门的访问次数, subRecommend=访问次数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false), SearchResult(recommend=对比超音速所有部门的人均访问次数, subRecommend=人均访问次数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false)]
14:25:21 [http-nio-9080-exec-9] INFO  c.t.s.h.chat.parser.llm.LLMSqlParser 38 - try generating query statement for dataSetId:1
14:25:21 [http-nio-9080-exec-9] INFO  c.t.s.h.chat.parser.llm.LLMSqlParser 58 - currentRetryRound:1, start runText2SQL
14:25:24 [http-nio-9080-exec-9] INFO  c.t.s.h.c.t.DefaultSemanticTranslator 78 - parse dataSetQuery [DataSetQueryParam(sql=SELECT department, SUM(pv) FROM t_1 WHERE sys_imp_date = '2024-08-05' GROUP BY department, tables=[MetricTable(alias=t_1, metrics=[pv], dimensions=[sys_imp_date, department], where=null, aggOption=OUTER)], supportWith=true, withAlias=true)] 
14:25:24 [http-nio-9080-exec-9] INFO  c.t.s.h.c.t.DefaultSemanticTranslator 125 - parse metricQuery [MetricQueryParam(metrics=[pv], dimensions=[sys_imp_date, department], where=null, limit=null, order=null, nativeQuery=true)] isAgg [OUTER]
14:25:24 [http-nio-9080-exec-9] INFO  c.t.s.h.c.t.c.s.node.DataSourceNode 204 - dataSourceMeasures [{user_department=0, s2_pv_uv_statis=1, s2_stay_time_statis=0}]
14:25:24 [http-nio-9080-exec-9] INFO  c.t.s.h.c.t.c.sql.render.JoinRender 110 - tableView (SELECT `user_name`, `department` AS `department` FROM (SELECT `user_name`, `department` FROM `s2_user_department`) AS `user_department`) AS `src00_user_department_19d9`
14:25:24 [http-nio-9080-exec-9] INFO  c.t.s.h.c.t.c.sql.render.JoinRender 110 - tableView (SELECT `pv` AS `s2_pv_uv_statis_pv`, `imp_date` AS `sys_imp_date`, `user_name`, `imp_date` AS `imp_date` FROM (SELECT `imp_date`, `user_name`, `page`, 1 AS `pv`, `user_name` AS `user_id` FROM `s2_pv_uv_statis`) AS `s2_pv_uv_statis`) AS `src00_s2_pv_uv_statis_541d`
14:25:24 [http-nio-9080-exec-9] INFO  c.t.s.h.c.t.DefaultSemanticTranslator 78 - parse dataSetQuery [DataSetQueryParam(sql=SELECT sys_imp_date, department, SUM(pv) AS pv FROM t_1 WHERE sys_imp_date >= '2024-07-06' AND sys_imp_date <= '2024-08-04' GROUP BY sys_imp_date, department LIMIT 365, tables=[MetricTable(alias=t_1, metrics=[pv], dimensions=[sys_imp_date, department], where=null, aggOption=OUTER)], supportWith=true, withAlias=true)] 
14:25:24 [http-nio-9080-exec-9] INFO  c.t.s.h.c.t.DefaultSemanticTranslator 125 - parse metricQuery [MetricQueryParam(metrics=[pv], dimensions=[sys_imp_date, department], where=null, limit=null, order=null, nativeQuery=true)] isAgg [OUTER]
14:25:24 [http-nio-9080-exec-9] INFO  c.t.s.h.c.t.c.s.node.DataSourceNode 204 - dataSourceMeasures [{user_department=0, s2_pv_uv_statis=1, s2_stay_time_statis=0}]
14:25:24 [http-nio-9080-exec-9] INFO  c.t.s.h.c.t.c.sql.render.JoinRender 110 - tableView (SELECT `user_name`, `department` AS `department` FROM (SELECT `user_name`, `department` FROM `s2_user_department`) AS `user_department`) AS `src00_user_department_9445`
14:25:24 [http-nio-9080-exec-9] INFO  c.t.s.h.c.t.c.sql.render.JoinRender 110 - tableView (SELECT `pv` AS `s2_pv_uv_statis_pv`, `imp_date` AS `sys_imp_date`, `user_name`, `imp_date` AS `imp_date` FROM (SELECT `imp_date`, `user_name`, `page`, 1 AS `pv`, `user_name` AS `user_id` FROM `s2_pv_uv_statis`) AS `s2_pv_uv_statis`) AS `src00_s2_pv_uv_statis_864f`
14:25:24 [http-nio-9080-exec-9] INFO  c.t.s.h.c.t.DefaultSemanticTranslator 78 - parse dataSetQuery [DataSetQueryParam(sql=SELECT sys_imp_date, SUM(pv) AS pv FROM t_1 WHERE sys_imp_date >= '2024-07-06' AND sys_imp_date <= '2024-08-04' GROUP BY sys_imp_date LIMIT 365, tables=[MetricTable(alias=t_1, metrics=[pv], dimensions=[sys_imp_date], where=null, aggOption=OUTER)], supportWith=true, withAlias=true)] 
14:25:24 [http-nio-9080-exec-9] INFO  c.t.s.h.c.t.DefaultSemanticTranslator 125 - parse metricQuery [MetricQueryParam(metrics=[pv], dimensions=[sys_imp_date], where=null, limit=null, order=null, nativeQuery=true)] isAgg [OUTER]
14:25:24 [http-nio-9080-exec-9] INFO  c.t.s.h.c.t.c.s.node.DataSourceNode 204 - dataSourceMeasures [{user_department=0, s2_pv_uv_statis=1, s2_stay_time_statis=0}]
14:25:24 [http-nio-9080-exec-10] INFO  c.t.s.h.s.f.s.i.S2SemanticLayerService 106 - [queryReq:QuerySqlReq(sql=SELECT 部门, SUM(访问次数) FROM 超音数数据集 WHERE 数据日期 = '2024-08-05' GROUP BY 部门, limit=1000)]
14:25:24 [http-nio-9080-exec-10] INFO  c.t.s.h.core.cache.DefaultQueryCache 21 - query from cache, key:supersonic:dev:0:-1:1b3447fa75077e32c5e80f48133ba16d
14:25:24 [http-nio-9080-exec-10] INFO  c.t.s.h.core.executor.JdbcExecutor 41 - executing SQL: with t_1 as (SELECT `t3`.`sys_imp_date`, `t2`.`department`, `t3`.`s2_pv_uv_statis_pv` AS `pv` FROM (SELECT `user_name`, `department` FROM s2_user_department) AS `t2` LEFT JOIN (SELECT 1 AS `s2_pv_uv_statis_pv`, `imp_date` AS `sys_imp_date`, `user_name`, `imp_date` FROM s2_pv_uv_statis) AS `t3` ON `t2`.`user_name` = `t3`.`user_name`) SELECT department, SUM(pv) FROM t_1 WHERE sys_imp_date = '2024-08-05' GROUP BY department limit 1000

```

### 完整版日志分析

[完整详细日志](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/%E5%AE%8C%E6%95%B4%E8%AF%A6%E7%BB%86%E6%97%A5%E5%BF%97%207d7737e9e8b74047b2585e42c3fadcbc.md)

### 整理版日志分析

[整理版日志](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/%E6%95%B4%E7%90%86%E7%89%88%E6%97%A5%E5%BF%97%201f2a4b7e2465427c8d52ed4b8a3fdba3.md)

## 4.3 数据处理流程分析

仅含主干分析，描述主要的数据处理流程，涉及的模块和类，以及数据如何在各个流程中传递和转换。

详细分析见上述《完整版日志分析》以及《整理版日志分析》。

### 输入搜索

```css
输入：

“超音速对比所有人访问次数”

输出：

searchResults:[SearchResult(recommend=超音速对比所有人访问人数, subRecommend=访问人数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false), SearchResult(recommend=超音速对比所有人访问时长, subRecommend=访问时长, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false), SearchResult(recommend=超音速对比所有人访问次数, subRecommend=访问次数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false), SearchResult(recommend=超音速对比所有人访问用户数, subRecommend=访问用户数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false)]

possibleDataSets:[1],natureToNameMap:{_1_3_metric=访问人数, _1_2_metric=访问时长, _1_1_metric=访问次数}
```

![image.png](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/image%204.png)

```css
14:56:57 [http-nio-9080-exec-10] DEBUG c.t.s.h.s.f.s.i.RetrieveServiceImpl 103 - searchTextEntry:MatchText(regText=超音速对比所有, detectSegment=人)=[HanlpMapResult(natures=[_1_4_metric], offset=0, similarity=0.0)],queryReq:QueryReq(queryText=超音速对比所有人, chatId=1, dataSetIds=[], user=User(id=6, name=admin, displayName=admin, email=null, isAdmin=1), queryFilters=null, saveAnswer=true, text2SQLType=RULE_AND_LLM, mapModeEnum=STRICT, mapInfo=com.tencent.supersonic.headless.api.pojo.SchemaMapInfo@2b14a3bd, queryDataType=ALL, llmConfig=LLMConfig(provider=OPEN_AI, baseUrl=https://api.openai.com/v1, apiKey=kGA4i6jY7QqG5xH+S0N++SzVWVKyAHesOq7NpoFVI7pgU14eb1AM296OFiLJTNtDVfpWDpfu7o4vDG2C2yWiSA==, modelName=gpt-3.5-turbo, temperature=0.0, timeOut=60), exemplars=[])
14:56:57 [http-nio-9080-exec-10] DEBUG c.t.s.h.s.f.s.i.RetrieveServiceImpl 140 - possibleDataSets:[],dataSetInfoStat:DataSetInfoStat(dataSetCount=0, metricDataSetCount=0, dimensionDataSetCount=0, dimensionValueDataSetCount=0),contextModel:1
14:56:57 [http-nio-9080-exec-10] DEBUG c.t.s.h.s.f.s.i.RetrieveServiceImpl 276 - searchMetricAndDimension searchTextEntry:MatchText(regText=超音速对比所有, detectSegment=人)=[HanlpMapResult(natures=[_1_4_metric], offset=0, similarity=0.0)]
14:56:57 [http-nio-9080-exec-10] DEBUG c.t.s.h.s.f.s.i.RetrieveServiceImpl 304 - parseResult:HanlpMapResult(natures=[_1_4_metric], offset=0, similarity=0.0),dimensionMetricClassIds:[ModelWithSemanticType(model=1, schemaElementType=METRIC)],possibleDataSets:[1]
14:56:57 [http-nio-9080-exec-10] INFO  c.t.s.h.s.f.s.i.RetrieveServiceImpl 307 - searchMetricAndDimension searchResults:[SearchResult(recommend=超音速对比所有人均访问次数, subRecommend=人均访问次数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false)]
14:56:57 [http-nio-9080-exec-10] DEBUG c.t.s.h.s.f.s.i.RetrieveServiceImpl 117 - possibleDataSets:[1],natureToNameMap:{_1_4_metric=人均访问次数}

14:56:59 [http-nio-9080-exec-3] DEBUG c.t.s.h.s.f.s.i.RetrieveServiceImpl 103 - searchTextEntry:MatchText(regText=超音速对比所有人, detectSegment=访问)=[HanlpMapResult(natures=[_1_3_metric], offset=0, similarity=0.0), HanlpMapResult(natures=[_1_2_metric], offset=0, similarity=0.0), HanlpMapResult(natures=[_1_1_metric], offset=0, similarity=0.0), HanlpMapResult(natures=[_1_3_metric], offset=0, similarity=0.0)],queryReq:QueryReq(queryText=超音速对比所有人访问, chatId=1, dataSetIds=[], user=User(id=6, name=admin, displayName=admin, email=null, isAdmin=1), queryFilters=null, saveAnswer=true, text2SQLType=RULE_AND_LLM, mapModeEnum=STRICT, mapInfo=com.tencent.supersonic.headless.api.pojo.SchemaMapInfo@36caf6e9, queryDataType=ALL, llmConfig=LLMConfig(provider=OPEN_AI, baseUrl=https://api.openai.com/v1, apiKey=kGA4i6jY7QqG5xH+S0N++SzVWVKyAHesOq7NpoFVI7pgU14eb1AM296OFiLJTNtDVfpWDpfu7o4vDG2C2yWiSA==, modelName=gpt-3.5-turbo, temperature=0.0, timeOut=60), exemplars=[])
14:56:59 [http-nio-9080-exec-3] DEBUG c.t.s.h.s.f.s.i.RetrieveServiceImpl 140 - possibleDataSets:[],dataSetInfoStat:DataSetInfoStat(dataSetCount=0, metricDataSetCount=0, dimensionDataSetCount=0, dimensionValueDataSetCount=0),contextModel:1
14:56:59 [http-nio-9080-exec-3] DEBUG c.t.s.h.s.f.s.i.RetrieveServiceImpl 276 - searchMetricAndDimension searchTextEntry:MatchText(regText=超音速对比所有人, detectSegment=访问)=[HanlpMapResult(natures=[_1_3_metric], offset=0, similarity=0.0), HanlpMapResult(natures=[_1_2_metric], offset=0, similarity=0.0), HanlpMapResult(natures=[_1_1_metric], offset=0, similarity=0.0), HanlpMapResult(natures=[_1_3_metric], offset=0, similarity=0.0)]
14:56:59 [http-nio-9080-exec-3] DEBUG c.t.s.h.s.f.s.i.RetrieveServiceImpl 304 - parseResult:HanlpMapResult(natures=[_1_3_metric], offset=0, similarity=0.0),dimensionMetricClassIds:[ModelWithSemanticType(model=1, schemaElementType=METRIC)],possibleDataSets:[1]
14:56:59 [http-nio-9080-exec-3] DEBUG c.t.s.h.s.f.s.i.RetrieveServiceImpl 304 - parseResult:HanlpMapResult(natures=[_1_2_metric], offset=0, similarity=0.0),dimensionMetricClassIds:[ModelWithSemanticType(model=1, schemaElementType=METRIC)],possibleDataSets:[1]
14:56:59 [http-nio-9080-exec-3] DEBUG c.t.s.h.s.f.s.i.RetrieveServiceImpl 304 - parseResult:HanlpMapResult(natures=[_1_1_metric], offset=0, similarity=0.0),dimensionMetricClassIds:[ModelWithSemanticType(model=1, schemaElementType=METRIC)],possibleDataSets:[1]
14:56:59 [http-nio-9080-exec-3] DEBUG c.t.s.h.s.f.s.i.RetrieveServiceImpl 304 - parseResult:HanlpMapResult(natures=[_1_3_metric], offset=0, similarity=0.0),dimensionMetricClassIds:[ModelWithSemanticType(model=1, schemaElementType=METRIC)],possibleDataSets:[1]
14:56:59 [http-nio-9080-exec-3] INFO  c.t.s.h.s.f.s.i.RetrieveServiceImpl 307 - searchMetricAndDimension searchResults:[SearchResult(recommend=超音速对比所有人访问人数, subRecommend=访问人数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false), SearchResult(recommend=超音速对比所有人访问时长, subRecommend=访问时长, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false), SearchResult(recommend=超音速对比所有人访问次数, subRecommend=访问次数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false), SearchResult(recommend=超音速对比所有人访问用户数, subRecommend=访问用户数, modelName=超音数数据集, modelId=1, schemaElementType=METRIC, isComplete=false)]
14:56:59 [http-nio-9080-exec-3] DEBUG c.t.s.h.s.f.s.i.RetrieveServiceImpl 117 - possibleDataSets:[1],natureToNameMap:{_1_3_metric=访问人数, _1_2_metric=访问时长, _1_1_metric=访问次数}

```

对于输入语句进行实时分割，然后进行关键词（数据集、表、指标）查询匹配，给出实时推荐

[`RetrieveServiceImpl`](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/RetrieveServiceImpl%20e2beb119ba3849698912622e75c8a5bd.md)

```json
14:57:00 [scheduling-1] DEBUG c.t.s.h.s.task.DictionaryReloadTask 39 - reloadKnowledge start
14:57:00 [scheduling-1] DEBUG c.t.s.h.s.w.s.impl.DictWordService 69 - nature type:DIMENSION , nature size:15
14:57:00 [scheduling-1] DEBUG c.t.s.h.s.w.s.impl.DictWordService 69 - nature type:METRIC , nature size:18
14:57:00 [scheduling-1] DEBUG c.t.s.h.s.w.s.impl.DictWordService 69 - nature type:ENTITY , nature size:4
14:57:00 [scheduling-1] DEBUG c.t.s.h.s.w.s.impl.DictWordService 69 - nature type:VALUE , nature size:0
14:57:00 [scheduling-1] DEBUG c.t.s.h.s.w.s.impl.DictWordService 69 - nature type:TERM , nature size:6
14:57:00 [scheduling-1] DEBUG c.t.s.h.s.w.s.impl.DictWordService 44 - Dictionary hasn't been reloaded.
14:57:00 [scheduling-1] DEBUG c.t.s.h.s.task.DictionaryReloadTask 45 - reloadKnowledge end

```

[`DictWordService` ](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/DictWordService%2072f9854b1a4646b3ad3d4f933c641c18.md)

统计不同类别的词性数量，包括维度（DIMENSION，数量为15）、度量（METRIC，数量为18）、实体（ENTITY，数量为4）、值（VALUE，数量为0）、术语（TERM，数量为6），检查知识库更新

### 生成优化

```css
输入：

“超音速对比所有人访问次数”

输出：

SELECT SUM(访问次数) FROM 超音数数据集

SELECT SUM(访问次数) FROM 超音数数据集 WHERE (数据日期 >= '2024-07-31' AND 数据日期 <= '2024-08-06')

SELECT SUM(pv) FROM t_1 WHERE (sys_imp_date >= '2024-07-31' AND sys_imp_date <= '2024-08-06') -> SELECT SUM(pv) FROM t_1 WHERE (sys_imp_date >= '2024-07-31' AND sys_imp_date <= '2024-08-06')

with t_1 as (SELECT `imp_date` AS `sys_imp_date`, SUM(1) AS `pv` FROM s2_pv_uv_statis GROUP BY `imp_date`, `imp_date`) SELECT SUM(pv) FROM t_1 WHERE (sys_imp_date >= '2024-07-31' AND sys_imp_date <= '2024-08-06') limit 1000
```

![image.png](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/image%205.png)

1. [WorkflowServiceImpl](https://www.notion.so/WorkflowServiceImpl-java-ceb9292ac776466687031e5ab13643c1?pvs=21) 调启总服务（开始执行下面步骤）
    
    [`WorkflowServiceImpl.java` ](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/WorkflowServiceImpl%20java%202ea443d9c4a74616b7762a5d8fd82300.md)
    
2. `performMapping`调用`schemaMappers`元素匹配

```json
14:57:04 [http-nio-9080-exec-2] DEBUG o.s.w.s.m.m.a.RequestMappingHandlerMapping 522 - Mapped to com.tencent.supersonic.chat.server.rest.ChatQueryController#parse(ChatParseReq, HttpServletRequest, HttpServletResponse)
14:57:04 [http-nio-9080-exec-2] DEBUG o.s.w.s.m.m.a.RequestResponseBodyMethodProcessor 91 - Read "application/json;charset=UTF-8" to [ChatParseReq(queryText=超音速对比所有人访问次数, chatId=1, agentId=1, topN=10, user=null, queryFilters=null, sav (truncated)...]
14:57:04 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.mapper.BaseMatchStrategy 150 - word:访问次数,nature:_1_1_metric,frequency:100000
14:57:04 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.mapper.BaseMatchStrategy 43 - terms:[S2Term(word=访问次数, nature=_1_1_metric, offset=8, frequency=100000)],,detectDataSetIds:[]
14:57:06 [http-nio-9080-exec-2] DEBUG c.t.s.h.chat.mapper.BaseMapper 44 - after KeywordMapper,cost:772,mapInfo:{1=[SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=1, name=访问次数, bizName=pv, useCnt=0, type=METRIC, alias=[], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false), RelatedSchemaElement(dimensionId=2, isNecessary=false)], defaultAgg=SUM, dataFormatType=null, order=0.0, isTag=0, description=一段时间内用户的访问次数), similarity=1.0, detectWord=访问次数, word=访问次数, frequency=100000, isInherited=false), SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=4, name=人均访问次数, bizName=pv_avg, useCnt=0, type=METRIC, alias=[平均访问次数], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false)], defaultAgg=, dataFormatType=null, order=0.0, isTag=0, description=每个用户平均访问的次数), similarity=0.9971581297489837, detectWord=人访问次数, word=人均访问次数, frequency=100000, isInherited=false), SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=3, name=访问用户数, bizName=uv, useCnt=0, type=METRIC, alias=[UV, 访问人数], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false)], defaultAgg=count, dataFormatType=null, order=0.0, isTag=0, description=访问的用户个数), similarity=0.9953412336995052, detectWord=访问次数, word=访问用户数, frequency=100000, isInherited=false)]}
14:57:06 [http-nio-9080-exec-2] DEBUG c.t.s.h.chat.mapper.BaseMapper 33 - before QueryFilterMapper,mapInfo:{1=[SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=1, name=访问次数, bizName=pv, useCnt=0, type=METRIC, alias=[], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false), RelatedSchemaElement(dimensionId=2, isNecessary=false)], defaultAgg=SUM, dataFormatType=null, order=0.0, isTag=0, description=一段时间内用户的访问次数), similarity=1.0, detectWord=访问次数, word=访问次数, frequency=100000, isInherited=false), SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=4, name=人均访问次数, bizName=pv_avg, useCnt=0, type=METRIC, alias=[平均访问次数], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false)], defaultAgg=, dataFormatType=null, order=0.0, isTag=0, description=每个用户平均访问的次数), similarity=0.9971581297489837, detectWord=人访问次数, word=人均访问次数, frequency=100000, isInherited=false), SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=3, name=访问用户数, bizName=uv, useCnt=0, type=METRIC, alias=[UV, 访问人数], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false)], defaultAgg=count, dataFormatType=null, order=0.0, isTag=0, description=访问的用户个数), similarity=0.9953412336995052, detectWord=访问次数, word=访问用户数, frequency=100000, isInherited=false)]}
14:57:06 [http-nio-9080-exec-2] DEBUG c.t.s.h.chat.mapper.BaseMapper 44 - after QueryFilterMapper,cost:0,mapInfo:{1=[SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=1, name=访问次数, bizName=pv, useCnt=0, type=METRIC, alias=[], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false), RelatedSchemaElement(dimensionId=2, isNecessary=false)], defaultAgg=SUM, dataFormatType=null, order=0.0, isTag=0, description=一段时间内用户的访问次数), similarity=1.0, detectWord=访问次数, word=访问次数, frequency=100000, isInherited=false), SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=4, name=人均访问次数, bizName=pv_avg, useCnt=0, type=METRIC, alias=[平均访问次数], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false)], defaultAgg=, dataFormatType=null, order=0.0, isTag=0, description=每个用户平均访问的次数), similarity=0.9971581297489837, detectWord=人访问次数, word=人均访问次数, frequency=100000, isInherited=false), SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=3, name=访问用户数, bizName=uv, useCnt=0, type=METRIC, alias=[UV, 访问人数], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false)], defaultAgg=count, dataFormatType=null, order=0.0, isTag=0, description=访问的用户个数), similarity=0.9953412336995052, detectWord=访问次数, word=访问用户数, frequency=100000, isInherited=false)]}
14:57:06 [http-nio-9080-exec-2] DEBUG c.t.s.h.chat.mapper.BaseMapper 33 - before EntityMapper,mapInfo:{1=[SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=1, name=访问次数, bizName=pv, useCnt=0, type=METRIC, alias=[], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false), RelatedSchemaElement(dimensionId=2, isNecessary=false)], defaultAgg=SUM, dataFormatType=null, order=0.0, isTag=0, description=一段时间内用户的访问次数), similarity=1.0, detectWord=访问次数, word=访问次数, frequency=100000, isInherited=false), SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=4, name=人均访问次数, bizName=pv_avg, useCnt=0, type=METRIC, alias=[平均访问次数], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false)], defaultAgg=, dataFormatType=null, order=0.0, isTag=0, description=每个用户平均访问的次数), similarity=0.9971581297489837, detectWord=人访问次数, word=人均访问次数, frequency=100000, isInherited=false), SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=3, name=访问用户数, bizName=uv, useCnt=0, type=METRIC, alias=[UV, 访问人数], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false)], defaultAgg=count, dataFormatType=null, order=0.0, isTag=0, description=访问的用户个数), similarity=0.9953412336995052, detectWord=访问次数, word=访问用户数, frequency=100000, isInherited=false)]}
14:57:06 [http-nio-9080-exec-2] DEBUG c.t.s.h.chat.mapper.BaseMapper 44 - after EntityMapper,cost:0,mapInfo:{1=[SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=1, name=访问次数, bizName=pv, useCnt=0, type=METRIC, alias=[], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false), RelatedSchemaElement(dimensionId=2, isNecessary=false)], defaultAgg=SUM, dataFormatType=null, order=0.0, isTag=0, description=一段时间内用户的访问次数), similarity=1.0, detectWord=访问次数, word=访问次数, frequency=100000, isInherited=false), SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=4, name=人均访问次数, bizName=pv_avg, useCnt=0, type=METRIC, alias=[平均访问次数], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false)], defaultAgg=, dataFormatType=null, order=0.0, isTag=0, description=每个用户平均访问的次数), similarity=0.9971581297489837, detectWord=人访问次数, word=人均访问次数, frequency=100000, isInherited=false), SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=3, name=访问用户数, bizName=uv, useCnt=0, type=METRIC, alias=[UV, 访问人数], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false)], defaultAgg=count, dataFormatType=null, order=0.0, isTag=0, description=访问的用户个数), similarity=0.9953412336995052, detectWord=访问次数, word=访问用户数, frequency=100000, isInherited=false)]}

```

请求查询schema对应，匹配相关信息，便于后续查询时候调节指标生成（对knowledge base进行查询）

```dart
mapInfo:{1=[SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=1, name=访问次数, bizName=pv, useCnt=0, type=METRIC, alias=[], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false), RelatedSchemaElement(dimensionId=2, isNecessary=false)], defaultAgg=SUM, dataFormatType=null, order=0.0, isTag=0, description=一段时间内用户的访问次数), similarity=1.0, detectWord=访问次数, word=访问次数, frequency=100000, isInherited=false), SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=4, name=人均访问次数, bizName=pv_avg, useCnt=0, type=METRIC, alias=[平均访问次数], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false)], defaultAgg=, dataFormatType=null, order=0.0, isTag=0, description=每个用户平均访问的次数), similarity=0.9971581297489837, detectWord=人访问次数, word=人均访问次数, frequency=100000, isInherited=false), SchemaElementMatch(element=SchemaElement(dataSet=1, dataSetName=超音数数据集, model=2, id=3, name=访问用户数, bizName=uv, useCnt=0, type=METRIC, alias=[UV, 访问人数], schemaValueMaps=null, relatedSchemaElements=[RelatedSchemaElement(dimensionId=1, isNecessary=false)], defaultAgg=count, dataFormatType=null, order=0.0, isTag=0, description=访问的用户个数), similarity=0.9953412336995052, detectWord=访问次数, word=访问用户数, frequency=100000, isInherited=false)]}
```

1. `performParsing`调用`SemanticParser`解析指令生成请求构造SQL（67行log输出）
    
    ```dart
    14:57:06 [http-nio-9080-exec-2] DEBUG c.t.s.h.s.w.s.i.WorkflowServiceImpl 67 - RuleSqlParser result:{"queryText":"超音速对比所有人访问次数","chatId":1,"dataSetIds":[],"modelIdToDataSetIds":{"1":[1],"2":[1],"3":[1],"4":[2]},"user":{"id":6,"name":"admin","displayName":"admin","email":"null","isAdmin":1,"superAdmin":true},"saveAnswer":true,"text2SQLType":"RULE_AND_LLM","candidateQueries":[{"parseInfo":{"queryMode":"METRIC_GROUPBY","dataSet":{"dataSet":1,"dataSetName":"超音数数据集","id":1,"name":"超音数数据集","bizName":"s2","type":"DATASET","order":0.0,"isTag":0},"metrics":[{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"}],"dimensions":[{"dataSet":1,"dataSetName":"超音数数据集","model":1,"id":1,"name":"部门","bizName":"department","useCnt":0,"type":"DIMENSION","alias":[],"schemaValueMaps":[],"order":0.0,"isTag":1,"description":""}],"aggType":"NONE","filterType":"AND","dimensionFilters":[],"metricFilters":[],"orders":[],"dateInfo":{"dateMode":"RECENT","startDate":"2024-06-08","endDate":"2024-07-07","dateList":["2024-06-08","2024-06-09","2024-06-10","2024-06-11","2024-06-12","2024-06-13","2024-06-14","2024-06-15","2024-06-16","2024-06-17","2024-06-18","2024-06-19","2024-06-20","2024-06-21","2024-06-22","2024-06-23","2024-06-24","2024-06-25","2024-06-26","2024-06-27","2024-06-28","2024-06-29","2024-06-30","2024-07-01","2024-07-02","2024-07-03","2024-07-04","2024-07-05","2024-07-06","2024-07-07"],"unit":30,"period":"DAY","detectWord":"近30天","groupByDate":false,"inherited":true,"groupByTimeDimension":"sys_imp_date"},"limit":365,"score":6.0,"elementMatches":[{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},"similarity":1.0,"detectWord":"访问次数","word":"访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},"similarity":0.9971581297489837,"detectWord":"人访问次数","word":"人均访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"},"similarity":0.9953412336995052,"detectWord":"访问次数","word":"访问用户数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":1,"id":1,"name":"部门","bizName":"department","useCnt":0,"type":"DIMENSION","alias":[],"schemaValueMaps":[],"order":0.0,"isTag":1,"description":""},"similarity":1.0,"detectWord":"部门","word":"部门","frequency":100000,"inherited":true}],"properties":{},"sqlInfo":{},"sqlEvaluation":{},"queryType":"ID","dataSetId":1},"queryMode":"METRIC_GROUPBY"},{"parseInfo":{"queryMode":"METRIC_MODEL","dataSet":{"dataSet":1,"dataSetName":"超音数数据集","id":1,"name":"超音数数据集","bizName":"s2","type":"DATASET","order":0.0,"isTag":0},"metrics":[{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"}],"dimensions":[],"aggType":"NONE","filterType":"AND","dimensionFilters":[],"metricFilters":[],"orders":[],"dateInfo":{"dateMode":"RECENT","startDate":"2024-06-08","endDate":"2024-07-07","dateList":["2024-06-08","2024-06-09","2024-06-10","2024-06-11","2024-06-12","2024-06-13","2024-06-14","2024-06-15","2024-06-16","2024-06-17","2024-06-18","2024-06-19","2024-06-20","2024-06-21","2024-06-22","2024-06-23","2024-06-24","2024-06-25","2024-06-26","2024-06-27","2024-06-28","2024-06-29","2024-06-30","2024-07-01","2024-07-02","2024-07-03","2024-07-04","2024-07-05","2024-07-06","2024-07-07"],"unit":30,"period":"DAY","detectWord":"近30天","groupByDate":false,"inherited":true,"groupByTimeDimension":"sys_imp_date"},"limit":365,"score":4.0,"elementMatches":[{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},"similarity":1.0,"detectWord":"访问次数","word":"访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},"similarity":0.9971581297489837,"detectWord":"人访问次数","word":"人均访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"},"similarity":0.9953412336995052,"detectWord":"访问次数","word":"访问用户数","frequency":100000,"inherited":false}],"properties":{},"sqlInfo":{},"sqlEvaluation":{},"queryType":"ID","dataSetId":1},"queryMode":"METRIC_MODEL"}],"mapInfo":{"dataSetElementMatches":{"1":[{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},"similarity":1.0,"detectWord":"访问次数","word":"访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},"similarity":0.9971581297489837,"detectWord":"人访问次数","word":"人均访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"},"similarity":0.9953412336995052,"detectWord":"访问次数","word":"访问用户数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":1,"id":1,"name":"部门","bizName":"department","useCnt":0,"type":"DIMENSION","alias":[],"schemaValueMaps":[],"order":0.0,"isTag":1,"description":""},"similarity":1.0,"detectWord":"部门","word":"部门","frequency":100000,"inherited":true}]},"matchedDataSetInfos":[1]},"mapModeEnum":"STRICT","queryDataType":"ALL","llmConfig":{"provider":"OPEN_AI","baseUrl":"https://api.openai.com/v1","apiKey":"kGA4i6jY7QqG5xH+S0N++SzVWVKyAHesOq7NpoFVI7pgU14eb1AM296OFiLJTNtDVfpWDpfu7o4vDG2C2yWiSA==","modelName":"gpt-3.5-turbo","temperature":0.0,"timeOut":60},"exemplars":[]}
    14:57:07 [http-nio-9080-exec-2] INFO  c.t.s.h.chat.parser.llm.LLMSqlParser 58 - currentRetryRound:1, start runText2SQL
    
    //以下全部为输出
    14:57:19 [http-nio-9080-exec-2] DEBUG c.t.s.h.s.w.s.i.WorkflowServiceImpl 67 - LLMSqlParser result:{"queryText":"超音速对比所有人访问次数","chatId":1,"dataSetIds":[],"modelIdToDataSetIds":{"1":[1],"2":[1],"3":[1],"4":[2]},"user":{"id":6,"name":"admin","displayName":"admin","email":"null","isAdmin":1,"superAdmin":true},"saveAnswer":true,"text2SQLType":"RULE_AND_LLM","candidateQueries":[{"parseInfo":{"queryMode":"LLM_S2SQL","dataSet":{"dataSet":1,"dataSetName":"超音数数据集","id":1,"name":"超音数数据集","bizName":"s2","type":"DATASET","order":0.0,"isTag":0},"metrics":[],"dimensions":[],"aggType":"NONE","filterType":"AND","dimensionFilters":[],"metricFilters":[],"orders":[],"score":24.0,"elementMatches":[{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},"similarity":1.0,"detectWord":"访问次数","word":"访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},"similarity":0.9971581297489837,"detectWord":"人访问次数","word":"人均访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"},"similarity":0.9953412336995052,"detectWord":"访问次数","word":"访问用户数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":1,"id":1,"name":"部门","bizName":"department","useCnt":0,"type":"DIMENSION","alias":[],"schemaValueMaps":[],"order":0.0,"isTag":1,"description":""},"similarity":1.0,"detectWord":"部门","word":"部门","frequency":100000,"inherited":true}],"properties":{"type":"internal","CONTEXT":{"dataSetId":1,"llmReq":{"queryText":"超音速对比所有人访问次数","filterCondition":{},"schema":{"domainName":"超音数数据集","dataSetName":"超音数数据集","dataSetId":1,"fieldNameList":["访问用户数","用户","部门","访问次数","人均访问次数","停留时长","页面","数据日期"],"metrics":[{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"}],"dimensions":[{"dataSet":1,"dataSetName":"超音数数据集","model":1,"id":1,"name":"部门","bizName":"department","useCnt":0,"type":"DIMENSION","alias":[],"schemaValueMaps":[],"order":0.0,"isTag":1,"description":""}],"terms":[]},"linking":[],"currentDate":"2024-08-07","priorExts":"","sqlGenType":"1_pass_self_consistency","llmConfig":{"provider":"OPEN_AI","baseUrl":"https://api.openai.com/v1","apiKey":"kGA4i6jY7QqG5xH+S0N++SzVWVKyAHesOq7NpoFVI7pgU14eb1AM296OFiLJTNtDVfpWDpfu7o4vDG2C2yWiSA==","modelName":"gpt-3.5-turbo","temperature":0.0,"timeOut":60},"exemplars":[]},"llmResp":{"query":"超音速对比所有人访问次数","modelName":"超音数数据集","dbSchema":"Table: 超音数数据集, Metrics: [访问次数 COMMENT '一段时间内用户的访问次数' AGGREGATE 'SUM',人均访问次数 COMMENT '每个用户平均访问的次数',访问用户数 COMMENT '访问的用户个数' AGGREGATE 'COUNT',], Dimensions: [部门,]","sqlOutput":"SELECT SUM(访问次数) FROM 超音数数据集","sqlRespMap":{"SELECT SUM(访问次数) FROM 超音数数据集":{"sqlWeight":1.0,"fewShots":[{"question":"今年以来发行的歌曲中，有哪些在近7天播放超过一千万的 (补充信息:。当前的日期是2023-08-12) ","dbSchema":"Table: 歌曲库, Columns = [\"发行日期\", \"歌曲语言\", \"歌曲来源\", \"歌曲流派\", \"歌曲名\", \"歌曲版本\", \"歌曲类型\", \"发行时间\", \"数据日期\"]","sql":"SELECT 歌曲名 FROM 歌曲库 WHERE datediff('year', 发行日期, '2023-08-12') <= 0 AND datediff('day', 数据日期, '2023-08-12') <= 7 AND 结算播放量 > 10000000"},{"question":"超音数近半年每个月的平均访问次数 (补充信息:。当前的日期是2023-09-04) ","dbSchema":"Table: 超音数产品, Columns = [\"用户名\", \"部门\", \"模块\", \"访问时长\", \"访问次数\", \"访问人数\", \"数据日期\"]","sql":"SELECT MONTH(数据日期), AVG(访问次数) FROM 超音数产品 WHERE datediff('year', 数据日期, '2023-09-04') <= 0.5 GROUP BY MONTH(数据日期)"},{"question":"我想要近半年签约的播放量前十的歌手有哪些 (补充信息:。当前的日期是2023-09-11) ","dbSchema":"Table: 艺人库, Columns = [\"播放量层级\", \"播放量单调性\", \"播放量方差\", \"播放量突增类型\", \"播放量集中度\", \"歌手名\", \"歌手等级\", \"歌手类型\", \"歌手来源\", \"签约日期\", \"MPPM潮流人等级\", \"结算播放量\", \"运营播放量\", \"历史累计结算播放量\", \"有播放量歌曲数\", \"历史累计运营播放量\", \"付费用户结算播放量\", \"结算播放量占比\", \"运营播放份额\", \"免费用户结算播放占比\", \"完播量\", \"数据日期\"]","sql":"SELECT 歌手名 FROM 艺人库 WHERE datediff('year', 签约日期, '2023-09-11') <= 0.5 ORDER BY 结算播放量 DESC LIMIT 10"},{"question":"播放量大于1万的歌曲有多少 (补充信息:。当前的日期是2023-07-31) ","dbSchema":"Table: 歌曲库, Columns = [\"歌曲名\", \"歌曲版本\", \"歌曲类型\", \"MPPM歌曲ID\", \"是否严选窄口径歌曲\", \"是否严选宽口径歌曲\", \"是否潮流人歌曲\", \"超声波歌曲ID\", \"C音歌曲ID\", \"C音歌曲MID\", \"结算播放量\", \"运营播放量\", \"分享量\", \"收藏量\", \"运营搜播量\", \"结算搜播量\", \"拉新用户数\", \"拉活用户数\", \"分享率\", \"结算播放份额\", \"数据日期\"]","sql":"SELECT 歌曲名 FROM 歌曲库 WHERE 结算播放量 > 10000"},{"question":"超音数访问次数大于1k的部门是哪些 (补充信息:。当前的日期是2023-09-14) ","dbSchema":"Table: 超音数产品, Columns = [\"部门\", \"模块\", \"用户名\", \"访问次数\", \"访问人数\", \"访问时长\", \"数据日期\"]","sql":"SELECT 部门 FROM 超音数产品 WHERE 访问次数 > 1000"}]}}},"linkingValues":[]}},"sqlInfo":{"s2SQL":"SELECT SUM(访问次数) FROM 超音数数据集"},"sqlEvaluation":{},"queryType":"ID","dataSetId":1},"queryMode":"LLM_S2SQL"},{"parseInfo":{"queryMode":"METRIC_GROUPBY","dataSet":{"dataSet":1,"dataSetName":"超音数数据集","id":1,"name":"超音数数据集","bizName":"s2","type":"DATASET","order":0.0,"isTag":0},"metrics":[{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"}],"dimensions":[{"dataSet":1,"dataSetName":"超音数数据集","model":1,"id":1,"name":"部门","bizName":"department","useCnt":0,"type":"DIMENSION","alias":[],"schemaValueMaps":[],"order":0.0,"isTag":1,"description":""}],"aggType":"NONE","filterType":"AND","dimensionFilters":[],"metricFilters":[],"orders":[],"dateInfo":{"dateMode":"RECENT","startDate":"2024-06-08","endDate":"2024-07-07","dateList":["2024-06-08","2024-06-09","2024-06-10","2024-06-11","2024-06-12","2024-06-13","2024-06-14","2024-06-15","2024-06-16","2024-06-17","2024-06-18","2024-06-19","2024-06-20","2024-06-21","2024-06-22","2024-06-23","2024-06-24","2024-06-25","2024-06-26","2024-06-27","2024-06-28","2024-06-29","2024-06-30","2024-07-01","2024-07-02","2024-07-03","2024-07-04","2024-07-05","2024-07-06","2024-07-07"],"unit":30,"period":"DAY","detectWord":"近30天","groupByDate":false,"inherited":true,"groupByTimeDimension":"sys_imp_date"},"limit":365,"score":6.0,"elementMatches":[{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},"similarity":1.0,"detectWord":"访问次数","word":"访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},"similarity":0.9971581297489837,"detectWord":"人访问次数","word":"人均访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"},"similarity":0.9953412336995052,"detectWord":"访问次数","word":"访问用户数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":1,"id":1,"name":"部门","bizName":"department","useCnt":0,"type":"DIMENSION","alias":[],"schemaValueMaps":[],"order":0.0,"isTag":1,"description":""},"similarity":1.0,"detectWord":"部门","word":"部门","frequency":100000,"inherited":true}],"properties":{},"sqlInfo":{},"sqlEvaluation":{},"queryType":"ID","dataSetId":1},"queryMode":"METRIC_GROUPBY"},{"parseInfo":{"queryMode":"METRIC_MODEL","dataSet":{"dataSet":1,"dataSetName":"超音数数据集","id":1,"name":"超音数数据集","bizName":"s2","type":"DATASET","order":0.0,"isTag":0},"metrics":[{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"}],"dimensions":[],"aggType":"NONE","filterType":"AND","dimensionFilters":[],"metricFilters":[],"orders":[],"dateInfo":{"dateMode":"RECENT","startDate":"2024-06-08","endDate":"2024-07-07","dateList":["2024-06-08","2024-06-09","2024-06-10","2024-06-11","2024-06-12","2024-06-13","2024-06-14","2024-06-15","2024-06-16","2024-06-17","2024-06-18","2024-06-19","2024-06-20","2024-06-21","2024-06-22","2024-06-23","2024-06-24","2024-06-25","2024-06-26","2024-06-27","2024-06-28","2024-06-29","2024-06-30","2024-07-01","2024-07-02","2024-07-03","2024-07-04","2024-07-05","2024-07-06","2024-07-07"],"unit":30,"period":"DAY","detectWord":"近30天","groupByDate":false,"inherited":true,"groupByTimeDimension":"sys_imp_date"},"limit":365,"score":4.0,"elementMatches":[{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},"similarity":1.0,"detectWord":"访问次数","word":"访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},"similarity":0.9971581297489837,"detectWord":"人访问次数","word":"人均访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"},"similarity":0.9953412336995052,"detectWord":"访问次数","word":"访问用户数","frequency":100000,"inherited":false}],"properties":{},"sqlInfo":{},"sqlEvaluation":{},"queryType":"ID","dataSetId":1},"queryMode":"METRIC_MODEL"}],"mapInfo":{"dataSetElementMatches":{"1":[{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},"similarity":1.0,"detectWord":"访问次数","word":"访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},"similarity":0.9971581297489837,"detectWord":"人访问次数","word":"人均访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"},"similarity":0.9953412336995052,"detectWord":"访问次数","word":"访问用户数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":1,"id":1,"name":"部门","bizName":"department","useCnt":0,"type":"DIMENSION","alias":[],"schemaValueMaps":[],"order":0.0,"isTag":1,"description":""},"similarity":1.0,"detectWord":"部门","word":"部门","frequency":100000,"inherited":true}]},"matchedDataSetInfos":[1]},"mapModeEnum":"STRICT","queryDataType":"ALL","llmConfig":{"provider":"OPEN_AI","baseUrl":"https://api.openai.com/v1","apiKey":"kGA4i6jY7QqG5xH+S0N++SzVWVKyAHesOq7NpoFVI7pgU14eb1AM296OFiLJTNtDVfpWDpfu7o4vDG2C2yWiSA==","modelName":"gpt-3.5-turbo","temperature":0.0,"timeOut":60},"exemplars":[]}
    14:57:19 [http-nio-9080-exec-2] DEBUG c.t.s.h.s.w.s.i.WorkflowServiceImpl 67 - QueryTypeParser result:{"queryText":"超音速对比所有人访问次数","chatId":1,"dataSetIds":[],"modelIdToDataSetIds":{"1":[1],"2":[1],"3":[1],"4":[2]},"user":{"id":6,"name":"admin","displayName":"admin","email":"null","isAdmin":1,"superAdmin":true},"saveAnswer":true,"text2SQLType":"RULE_AND_LLM","candidateQueries":[{"parseInfo":{"queryMode":"LLM_S2SQL","dataSet":{"dataSet":1,"dataSetName":"超音数数据集","id":1,"name":"超音数数据集","bizName":"s2","type":"DATASET","order":0.0,"isTag":0},"metrics":[],"dimensions":[],"aggType":"NONE","filterType":"AND","dimensionFilters":[],"metricFilters":[],"orders":[],"score":24.0,"elementMatches":[{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},"similarity":1.0,"detectWord":"访问次数","word":"访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},"similarity":0.9971581297489837,"detectWord":"人访问次数","word":"人均访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"},"similarity":0.9953412336995052,"detectWord":"访问次数","word":"访问用户数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":1,"id":1,"name":"部门","bizName":"department","useCnt":0,"type":"DIMENSION","alias":[],"schemaValueMaps":[],"order":0.0,"isTag":1,"description":""},"similarity":1.0,"detectWord":"部门","word":"部门","frequency":100000,"inherited":true}],"properties":{"type":"internal","CONTEXT":{"dataSetId":1,"llmReq":{"queryText":"超音速对比所有人访问次数","filterCondition":{},"schema":{"domainName":"超音数数据集","dataSetName":"超音数数据集","dataSetId":1,"fieldNameList":["访问用户数","用户","部门","访问次数","人均访问次数","停留时长","页面","数据日期"],"metrics":[{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"}],"dimensions":[{"dataSet":1,"dataSetName":"超音数数据集","model":1,"id":1,"name":"部门","bizName":"department","useCnt":0,"type":"DIMENSION","alias":[],"schemaValueMaps":[],"order":0.0,"isTag":1,"description":""}],"terms":[]},"linking":[],"currentDate":"2024-08-07","priorExts":"","sqlGenType":"1_pass_self_consistency","llmConfig":{"provider":"OPEN_AI","baseUrl":"https://api.openai.com/v1","apiKey":"kGA4i6jY7QqG5xH+S0N++SzVWVKyAHesOq7NpoFVI7pgU14eb1AM296OFiLJTNtDVfpWDpfu7o4vDG2C2yWiSA==","modelName":"gpt-3.5-turbo","temperature":0.0,"timeOut":60},"exemplars":[]},"llmResp":{"query":"超音速对比所有人访问次数","modelName":"超音数数据集","dbSchema":"Table: 超音数数据集, Metrics: [访问次数 COMMENT '一段时间内用户的访问次数' AGGREGATE 'SUM',人均访问次数 COMMENT '每个用户平均访问的次数',访问用户数 COMMENT '访问的用户个数' AGGREGATE 'COUNT',], Dimensions: [部门,]","sqlOutput":"SELECT SUM(访问次数) FROM 超音数数据集","sqlRespMap":{"SELECT SUM(访问次数) FROM 超音数数据集":{"sqlWeight":1.0,"fewShots":[{"question":"今年以来发行的歌曲中，有哪些在近7天播放超过一千万的 (补充信息:。当前的日期是2023-08-12) ","dbSchema":"Table: 歌曲库, Columns = [\"发行日期\", \"歌曲语言\", \"歌曲来源\", \"歌曲流派\", \"歌曲名\", \"歌曲版本\", \"歌曲类型\", \"发行时间\", \"数据日期\"]","sql":"SELECT 歌曲名 FROM 歌曲库 WHERE datediff('year', 发行日期, '2023-08-12') <= 0 AND datediff('day', 数据日期, '2023-08-12') <= 7 AND 结算播放量 > 10000000"},{"question":"超音数近半年每个月的平均访问次数 (补充信息:。当前的日期是2023-09-04) ","dbSchema":"Table: 超音数产品, Columns = [\"用户名\", \"部门\", \"模块\", \"访问时长\", \"访问次数\", \"访问人数\", \"数据日期\"]","sql":"SELECT MONTH(数据日期), AVG(访问次数) FROM 超音数产品 WHERE datediff('year', 数据日期, '2023-09-04') <= 0.5 GROUP BY MONTH(数据日期)"},{"question":"我想要近半年签约的播放量前十的歌手有哪些 (补充信息:。当前的日期是2023-09-11) ","dbSchema":"Table: 艺人库, Columns = [\"播放量层级\", \"播放量单调性\", \"播放量方差\", \"播放量突增类型\", \"播放量集中度\", \"歌手名\", \"歌手等级\", \"歌手类型\", \"歌手来源\", \"签约日期\", \"MPPM潮流人等级\", \"结算播放量\", \"运营播放量\", \"历史累计结算播放量\", \"有播放量歌曲数\", \"历史累计运营播放量\", \"付费用户结算播放量\", \"结算播放量占比\", \"运营播放份额\", \"免费用户结算播放占比\", \"完播量\", \"数据日期\"]","sql":"SELECT 歌手名 FROM 艺人库 WHERE datediff('year', 签约日期, '2023-09-11') <= 0.5 ORDER BY 结算播放量 DESC LIMIT 10"},{"question":"播放量大于1万的歌曲有多少 (补充信息:。当前的日期是2023-07-31) ","dbSchema":"Table: 歌曲库, Columns = [\"歌曲名\", \"歌曲版本\", \"歌曲类型\", \"MPPM歌曲ID\", \"是否严选窄口径歌曲\", \"是否严选宽口径歌曲\", \"是否潮流人歌曲\", \"超声波歌曲ID\", \"C音歌曲ID\", \"C音歌曲MID\", \"结算播放量\", \"运营播放量\", \"分享量\", \"收藏量\", \"运营搜播量\", \"结算搜播量\", \"拉新用户数\", \"拉活用户数\", \"分享率\", \"结算播放份额\", \"数据日期\"]","sql":"SELECT 歌曲名 FROM 歌曲库 WHERE 结算播放量 > 10000"},{"question":"超音数访问次数大于1k的部门是哪些 (补充信息:。当前的日期是2023-09-14) ","dbSchema":"Table: 超音数产品, Columns = [\"部门\", \"模块\", \"用户名\", \"访问次数\", \"访问人数\", \"访问时长\", \"数据日期\"]","sql":"SELECT 部门 FROM 超音数产品 WHERE 访问次数 > 1000"}]}}},"linkingValues":[]}},"sqlInfo":{"s2SQL":"SELECT SUM(访问次数) FROM 超音数数据集","correctS2SQL":"SELECT SUM(访问次数) FROM 超音数数据集"},"sqlEvaluation":{},"queryType":"METRIC","dataSetId":1},"queryMode":"LLM_S2SQL"},{"parseInfo":{"queryMode":"METRIC_GROUPBY","dataSet":{"dataSet":1,"dataSetName":"超音数数据集","id":1,"name":"超音数数据集","bizName":"s2","type":"DATASET","order":0.0,"isTag":0},"metrics":[{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"}],"dimensions":[{"bizName":"sys_imp_date","order":0.0,"isTag":0},{"dataSet":1,"dataSetName":"超音数数据集","model":1,"id":1,"name":"部门","bizName":"department","useCnt":0,"type":"DIMENSION","alias":[],"schemaValueMaps":[],"order":0.0,"isTag":1,"description":""}],"aggType":"NONE","filterType":"AND","dimensionFilters":[],"metricFilters":[],"orders":[],"dateInfo":{"dateMode":"RECENT","startDate":"2024-06-08","endDate":"2024-07-07","dateList":["2024-06-08","2024-06-09","2024-06-10","2024-06-11","2024-06-12","2024-06-13","2024-06-14","2024-06-15","2024-06-16","2024-06-17","2024-06-18","2024-06-19","2024-06-20","2024-06-21","2024-06-22","2024-06-23","2024-06-24","2024-06-25","2024-06-26","2024-06-27","2024-06-28","2024-06-29","2024-06-30","2024-07-01","2024-07-02","2024-07-03","2024-07-04","2024-07-05","2024-07-06","2024-07-07"],"unit":30,"period":"DAY","detectWord":"近30天","groupByDate":false,"inherited":true,"groupByTimeDimension":"sys_imp_date"},"limit":365,"score":6.0,"elementMatches":[{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},"similarity":1.0,"detectWord":"访问次数","word":"访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},"similarity":0.9971581297489837,"detectWord":"人访问次数","word":"人均访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"},"similarity":0.9953412336995052,"detectWord":"访问次数","word":"访问用户数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":1,"id":1,"name":"部门","bizName":"department","useCnt":0,"type":"DIMENSION","alias":[],"schemaValueMaps":[],"order":0.0,"isTag":1,"description":""},"similarity":1.0,"detectWord":"部门","word":"部门","frequency":100000,"inherited":true}],"properties":{},"sqlInfo":{"s2SQL":"SELECT sys_imp_date, 部门, SUM(访问次数) AS 访问次数 FROM 超音数数据集 WHERE sys_imp_date >= '2024-07-08' AND sys_imp_date <= '2024-08-06' GROUP BY sys_imp_date, 部门 LIMIT 365","correctS2SQL":"SELECT sys_imp_date, 部门, SUM(访问次数) AS 访问次数 FROM 超音数数据集 WHERE sys_imp_date >= '2024-07-08' AND sys_imp_date <= '2024-08-06' GROUP BY sys_imp_date, 部门 LIMIT 365"},"sqlEvaluation":{},"queryType":"METRIC","dataSetId":1},"queryMode":"METRIC_GROUPBY"},{"parseInfo":{"queryMode":"METRIC_MODEL","dataSet":{"dataSet":1,"dataSetName":"超音数数据集","id":1,"name":"超音数数据集","bizName":"s2","type":"DATASET","order":0.0,"isTag":0},"metrics":[{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"}],"dimensions":[{"bizName":"sys_imp_date","order":0.0,"isTag":0}],"aggType":"NONE","filterType":"AND","dimensionFilters":[],"metricFilters":[],"orders":[],"dateInfo":{"dateMode":"RECENT","startDate":"2024-06-08","endDate":"2024-07-07","dateList":["2024-06-08","2024-06-09","2024-06-10","2024-06-11","2024-06-12","2024-06-13","2024-06-14","2024-06-15","2024-06-16","2024-06-17","2024-06-18","2024-06-19","2024-06-20","2024-06-21","2024-06-22","2024-06-23","2024-06-24","2024-06-25","2024-06-26","2024-06-27","2024-06-28","2024-06-29","2024-06-30","2024-07-01","2024-07-02","2024-07-03","2024-07-04","2024-07-05","2024-07-06","2024-07-07"],"unit":30,"period":"DAY","detectWord":"近30天","groupByDate":false,"inherited":true,"groupByTimeDimension":"sys_imp_date"},"limit":365,"score":4.0,"elementMatches":[{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},"similarity":1.0,"detectWord":"访问次数","word":"访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},"similarity":0.9971581297489837,"detectWord":"人访问次数","word":"人均访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"},"similarity":0.9953412336995052,"detectWord":"访问次数","word":"访问用户数","frequency":100000,"inherited":false}],"properties":{},"sqlInfo":{"s2SQL":"SELECT sys_imp_date, SUM(访问次数) AS 访问次数 FROM 超音数数据集 WHERE sys_imp_date >= '2024-07-08' AND sys_imp_date <= '2024-08-06' GROUP BY sys_imp_date LIMIT 365","correctS2SQL":"SELECT sys_imp_date, SUM(访问次数) AS 访问次数 FROM 超音数数据集 WHERE sys_imp_date >= '2024-07-08' AND sys_imp_date <= '2024-08-06' GROUP BY sys_imp_date LIMIT 365"},"sqlEvaluation":{},"queryType":"METRIC","dataSetId":1},"queryMode":"METRIC_MODEL"}],"mapInfo":{"dataSetElementMatches":{"1":[{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":1,"name":"访问次数","bizName":"pv","useCnt":0,"type":"METRIC","alias":[],"relatedSchemaElements":[{"dimensionId":1,"necessary":false},{"dimensionId":2,"necessary":false}],"defaultAgg":"SUM","order":0.0,"isTag":0,"description":"一段时间内用户的访问次数"},"similarity":1.0,"detectWord":"访问次数","word":"访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":4,"name":"人均访问次数","bizName":"pv_avg","useCnt":0,"type":"METRIC","alias":["平均访问次数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"","order":0.002841870251016343,"isTag":0,"description":"每个用户平均访问的次数"},"similarity":0.9971581297489837,"detectWord":"人访问次数","word":"人均访问次数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":2,"id":3,"name":"访问用户数","bizName":"uv","useCnt":0,"type":"METRIC","alias":["UV","访问人数"],"relatedSchemaElements":[{"dimensionId":1,"necessary":false}],"defaultAgg":"count","order":0.004658766300494777,"isTag":0,"description":"访问的用户个数"},"similarity":0.9953412336995052,"detectWord":"访问次数","word":"访问用户数","frequency":100000,"inherited":false},{"element":{"dataSet":1,"dataSetName":"超音数数据集","model":1,"id":1,"name":"部门","bizName":"department","useCnt":0,"type":"DIMENSION","alias":[],"schemaValueMaps":[],"order":0.0,"isTag":1,"description":""},"similarity":1.0,"detectWord":"部门","word":"部门","frequency":100000,"inherited":true}]},"matchedDataSetInfos":[1]},"mapModeEnum":"STRICT","queryDataType":"ALL","llmConfig":{"provider":"OPEN_AI","baseUrl":"https://api.openai.com/v1","apiKey":"kGA4i6jY7QqG5xH+S0N++SzVWVKyAHesOq7NpoFVI7pgU14eb1AM296OFiLJTNtDVfpWDpfu7o4vDG2C2yWiSA==","modelName":"gpt-3.5-turbo","temperature":0.0,"timeOut":60},"exemplars":[]}
    ```
    
    [`LMSqlParser` + `QueryTypeParser`](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/LMSqlParser%20+%20QueryTypeParser%207e5d1fd081ad45ddb28584192f1e36e9.md)
    
    使用大模型生成S2SQL，并进行投票选出可信度最高回答作为结果，同时传递给大模型聊天解析的相关信息。
    

![image.png](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/image%206.png)

1. `performCorrecting`调用`SemanticCorrector` 校正SQL

```json
14:57:19 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.c.BaseSemanticCorrector 35 - sqlCorrection:SchemaCorrector sql:SqlInfo(s2SQL=SELECT SUM(访问次数) FROM 超音数数据集, correctS2SQL=SELECT SUM(访问次数) FROM 超音数数据集, querySQL=null, sourceId=null)
14:57:19 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.c.BaseSemanticCorrector 35 - sqlCorrection:TimeCorrector sql:SqlInfo(s2SQL=SELECT SUM(访问次数) FROM 超音数数据集, correctS2SQL=SELECT SUM(访问次数) FROM 超音数数据集 WHERE (数据日期 >= '2024-07-31' AND 数据日期 <= '2024-08-06'), querySQL=null, sourceId=null)
14:57:19 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.c.BaseSemanticCorrector 35 - sqlCorrection:SelectCorrector sql:SqlInfo(s2SQL=SELECT SUM(访问次数) FROM 超音数数据集, correctS2SQL=SELECT SUM(访问次数) FROM 超音数数据集 WHERE (数据日期 >= '2024-07-31' AND 数据日期 <= '2024-08-06'), querySQL=null, sourceId=null)
14:57:19 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.c.BaseSemanticCorrector 35 - sqlCorrection:WhereCorrector sql:SqlInfo(s2SQL=SELECT SUM(访问次数) FROM 超音数数据集, correctS2SQL=SELECT SUM(访问次数) FROM 超音数数据集 WHERE (数据日期 >= '2024-07-31' AND 数据日期 <= '2024-08-06'), querySQL=null, sourceId=null)
14:57:19 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.c.BaseSemanticCorrector 35 - sqlCorrection:GroupByCorrector sql:SqlInfo(s2SQL=SELECT SUM(访问次数) FROM 超音数数据集, correctS2SQL=SELECT SUM(访问次数) FROM 超音数数据集 WHERE (数据日期 >= '2024-07-31' AND 数据日期 <= '2024-08-06'), querySQL=null, sourceId=null)
14:57:19 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.c.BaseSemanticCorrector 35 - sqlCorrection:AggCorrector sql:SqlInfo(s2SQL=SELECT SUM(访问次数) FROM 超音数数据集, correctS2SQL=SELECT SUM(访问次数) FROM 超音数数据集 WHERE (数据日期 >= '2024-07-31' AND 数据日期 <= '2024-08-06'), querySQL=null, sourceId=null)
14:57:19 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.c.BaseSemanticCorrector 35 - sqlCorrection:HavingCorrector sql:SqlInfo(s2SQL=SELECT SUM(访问次数) FROM 超音数数据集, correctS2SQL=SELECT SUM(访问次数) FROM 超音数数据集 WHERE (数据日期 >= '2024-07-31' AND 数据日期 <= '2024-08-06'), querySQL=null, sourceId=null)
14:57:19 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.c.BaseSemanticCorrector 35 - sqlCorrection:GrammarCorrector sql:SqlInfo(s2SQL=SELECT SUM(访问次数) FROM 超音数数据集, correctS2SQL=SELECT SUM(访问次数) FROM 超音数数据集 WHERE (数据日期 >= '2024-07-31' AND 数据日期 <= '2024-08-06'), querySQL=null, sourceId=null)
```

```dart
sql:SqlInfo(

s2SQL=SELECT SUM(访问次数) FROM 超音数数据集, 
correctS2SQL=SELECT SUM(访问次数) FROM 超音数数据集 WHERE (数据日期 >= '2024-07-31' AND 数据日期 <= '2024-08-06'), 

querySQL=null, sourceId=null)
```

1. `performProcessing`调用`ResultProcessor`将查询上下文和校正后的信息进行最终处理，生成 `ParseResp` 对象

![image.png](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/image%207.png)

[`ParseInfoProcessor` +Sql`InfoProcessor` ](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/ParseInfoProcessor%20+SqlInfoProcessor%204c8e24102f0c47828239e4d358b79e57.md)

[`SchemaServiceImpl`](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/SchemaServiceImpl%203bca859b985045c885d018bd76368224.md)

```json
14:57:19 [http-nio-9080-exec-2] DEBUG c.t.s.h.s.w.s.impl.SchemaServiceImpl 451 - statInfos:[]
14:57:19 [http-nio-9080-exec-2] DEBUG c.t.s.h.s.w.s.impl.SchemaServiceImpl 273 - typeIdAndStatPair:{}

14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.s.utils.QueryReqConverter 173 - dataSetId:1,convert name to bizName before:SELECT SUM(访问次数) FROM 超音数数据集 WHERE (数据日期 >= '2024-07-31' AND 数据日期 <= '2024-08-06')
14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.s.utils.QueryReqConverter 175 - dataSetId:1,convert name to bizName after:SELECT SUM(pv) FROM 超音数数据集 WHERE (sys_imp_date >= '2024-07-31' AND sys_imp_date <= '2024-08-06')
14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.s.utils.QueryReqConverter 243 - correctTableName after:SELECT SUM(pv) FROM t_1 WHERE (sys_imp_date >= '2024-07-31' AND sys_imp_date <= '2024-08-06')
14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.s.utils.QueryReqConverter 79 - replaceOrderAggSameAlias SELECT SUM(pv) FROM t_1 WHERE (sys_imp_date >= '2024-07-31' AND sys_imp_date <= '2024-08-06') -> SELECT SUM(pv) FROM t_1 WHERE (sys_imp_date >= '2024-07-31' AND sys_imp_date <= '2024-08-06')
14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.s.utils.QueryReqConverter 125 - QueryReqConverter queryStructReq[{"dataSetId":1"modelIds":[],"groups":[],"aggregators":[{"column":"pv","func":UNKNOWN,"nameCh":"null","args":null,"alias":null}],"orders":[],"dimensionFilters":[],"metricFilters":[],"params":[],"dateInfo":{"dateMode":BETWEEN,"startDate":"2024-08-06","endDate":"2024-07-31","dateList":[],"unit":1,"period":"DAY","text":"null"},"limit":2000,"cacheInfo":{"cache":true}}]

14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.u.SysTimeDimensionBuilder 19 - addSysTimeDimension before:[Dim(name=部门, type=categorical, expr=null, dateFormat=yyyy-MM-dd, typeParams=null, isCreateDimension=1, bizName=department, description=null, isTag=0)], engineAdaptor:com.tencent.supersonic.headless.core.adaptor.db.MysqlAdaptor@486b5958
14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.u.SysTimeDimensionBuilder 19 - addSysTimeDimension before:[Dim(name=, type=time, expr=null, dateFormat=yyyy-MM-dd, typeParams=DimensionTimeTypeParams(isPrimary=true, timeGranularity=day), isCreateDimension=0, bizName=imp_date, description=null, isTag=0), Dim(name=, type=categorical, expr=page, dateFormat=yyyy-MM-dd, typeParams=null, isCreateDimension=0, bizName=page, description=null, isTag=0)], engineAdaptor:com.tencent.supersonic.headless.core.adaptor.db.MysqlAdaptor@486b5958
14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.u.SysTimeDimensionBuilder 29 - addSysTimeDimension after:[Dim(name=, type=time, expr=null, dateFormat=yyyy-MM-dd, typeParams=DimensionTimeTypeParams(isPrimary=true, timeGranularity=day), isCreateDimension=0, bizName=imp_date, description=null, isTag=0), Dim(name=, type=categorical, expr=page, dateFormat=yyyy-MM-dd, typeParams=null, isCreateDimension=0, bizName=page, description=null, isTag=0), Dim(name=null, type=time, expr=imp_date, dateFormat=yyyy-MM-dd, typeParams=DimensionTimeTypeParams(isPrimary=true, timeGranularity=day), isCreateDimension=0, bizName=sys_imp_date, description=null, isTag=0), Dim(name=null, type=time, expr=DATE_FORMAT(DATE_SUB(imp_date, INTERVAL (DAYOFWEEK(imp_date) - 2) DAY), '%Y-%m-%d'), dateFormat=yyyy-MM-dd, typeParams=DimensionTimeTypeParams(isPrimary=false, timeGranularity=week), isCreateDimension=0, bizName=sys_imp_week, description=null, isTag=0), Dim(name=null, type=time, expr=DATE_FORMAT(imp_date, '%Y-%m') , dateFormat=yyyy-MM-dd, typeParams=DimensionTimeTypeParams(isPrimary=false, timeGranularity=month), isCreateDimension=0, bizName=sys_imp_month, description=null, isTag=0)], engineAdaptor:com.tencent.supersonic.headless.core.adaptor.db.MysqlAdaptor@486b5958
14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.u.SysTimeDimensionBuilder 19 - addSysTimeDimension before:[Dim(name=, type=time, expr=null, dateFormat=yyyy-MM-dd, typeParams=DimensionTimeTypeParams(isPrimary=true, timeGranularity=day), isCreateDimension=0, bizName=imp_date, description=null, isTag=0), Dim(name=页面, type=categorical, expr=page, dateFormat=yyyy-MM-dd, typeParams=null, isCreateDimension=1, bizName=page, description=null, isTag=0)], engineAdaptor:com.tencent.supersonic.headless.core.adaptor.db.MysqlAdaptor@486b5958
14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.u.SysTimeDimensionBuilder 29 - addSysTimeDimension after:[Dim(name=, type=time, expr=null, dateFormat=yyyy-MM-dd, typeParams=DimensionTimeTypeParams(isPrimary=true, timeGranularity=day), isCreateDimension=0, bizName=imp_date, description=null, isTag=0), Dim(name=页面, type=categorical, expr=page, dateFormat=yyyy-MM-dd, typeParams=null, isCreateDimension=1, bizName=page, description=null, isTag=0), Dim(name=null, type=time, expr=imp_date, dateFormat=yyyy-MM-dd, typeParams=DimensionTimeTypeParams(isPrimary=true, timeGranularity=day), isCreateDimension=0, bizName=sys_imp_date, description=null, isTag=0), Dim(name=null, type=time, expr=DATE_FORMAT(DATE_SUB(imp_date, INTERVAL (DAYOFWEEK(imp_date) - 2) DAY), '%Y-%m-%d'), dateFormat=yyyy-MM-dd, typeParams=DimensionTimeTypeParams(isPrimary=false, timeGranularity=week), isCreateDimension=0, bizName=sys_imp_week, description=null, isTag=0), Dim(name=null, type=time, expr=DATE_FORMAT(imp_date, '%Y-%m') , dateFormat=yyyy-MM-dd, typeParams=DimensionTimeTypeParams(isPrimary=false, timeGranularity=month), isCreateDimension=0, bizName=sys_imp_month, description=null, isTag=0)], engineAdaptor:com.tencent.supersonic.headless.core.adaptor.db.MysqlAdaptor@486b5958

14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.t.DefaultSemanticTranslator 51 - SemanticConverter before [QueryParam(groups=[], aggregators=[{"column":"pv","func":UNKNOWN,"nameCh":"null","args":null,"alias":null}], orders=[], dimensionFilters=[], metricFilters=[], dateInfo={"dateMode":BETWEEN,"startDate":"2024-08-06","endDate":"2024-07-31","dateList":[],"unit":1,"period":"DAY","text":"null"}, limit=2000, queryType=METRIC, s2SQL=null, correctS2SQL=null, dataSetId=1, dataSetName=null, modelIds=[], params=[], metrics=[pv], dimensions=null, where=null, order=null, nativeQuery=false)]
14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.t.DefaultSemanticTranslator 54 - SemanticConverter accept [com.tencent.supersonic.headless.core.translator.converter.DefaultDimValueConverter]
14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.t.DefaultSemanticTranslator 54 - SemanticConverter accept [com.tencent.supersonic.headless.core.translator.converter.SqlVariableParseConverter]
14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.t.DefaultSemanticTranslator 58 - SemanticConverter after QueryParam(groups=[], aggregators=[{"column":"pv","func":UNKNOWN,"nameCh":"null","args":null,"alias":null}], orders=[], dimensionFilters=[], metricFilters=[], dateInfo={"dateMode":BETWEEN,"startDate":"2024-08-06","endDate":"2024-07-31","dateList":[],"unit":1,"period":"DAY","text":"null"}, limit=2000, queryType=METRIC, s2SQL=null, correctS2SQL=null, dataSetId=1, dataSetName=null, modelIds=[], params=[], metrics=[pv], dimensions=null, where=null, order=null, nativeQuery=false) DataSetQueryParam(sql=SELECT SUM(pv) FROM t_1 WHERE (sys_imp_date >= '2024-07-31' AND sys_imp_date <= '2024-08-06'), tables=[MetricTable(alias=t_1, metrics=[pv], dimensions=[sys_imp_date], where=null, aggOption=DEFAULT)], supportWith=true, withAlias=true) MetricQueryParam(metrics=null, dimensions=null, where=null, limit=null, order=null, nativeQuery=false)
14:57:20 [http-nio-9080-exec-2] INFO  c.t.s.h.c.t.DefaultSemanticTranslator 78 - parse dataSetQuery [DataSetQueryParam(sql=SELECT SUM(pv) FROM t_1 WHERE (sys_imp_date >= '2024-07-31' AND sys_imp_date <= '2024-08-06'), tables=[MetricTable(alias=t_1, metrics=[pv], dimensions=[sys_imp_date], where=null, aggOption=DEFAULT)], supportWith=true, withAlias=true)] 
14:57:20 [http-nio-9080-exec-2] INFO  c.t.s.h.c.t.DefaultSemanticTranslator 125 - parse metricQuery [MetricQueryParam(metrics=[pv], dimensions=[sys_imp_date], where=null, limit=null, order=null, nativeQuery=false)] isAgg [DEFAULT]
```

开始转换字段，翻译映射，构造结构请求，实现translator框架前置部分

```json
14:57:20 [http-nio-9080-exec-2] INFO  c.t.s.h.c.t.c.s.node.DataSourceNode 204 - dataSourceMeasures [{user_department=0, s2_pv_uv_statis=1, s2_stay_time_statis=0}]
14:57:20 [http-nio-9080-exec-2] DEBUG c.t.s.h.c.t.c.s.node.DataSourceNode 229 - baseDataSource  match all 
```

[`DataSourceNode`](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/DataSourceNode%20954ee82014a245c7884242789df541c8.md)

最后检查所有映射关系资源是否真实存在，确保查询可靠

### Apache Calcite优化

参考4.2 整理版日志文档中Apache Calcite部分，进行三轮优化过程，以及参考6 关键技术部分。

[Calcite相关日志分析](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Calcite%E7%9B%B8%E5%85%B3%E6%97%A5%E5%BF%97%E5%88%86%E6%9E%90%20623f6c72ba094a31b12d7a8e3aa23bdd.md)

### 最终查询

![image.png](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/image%208.png)

```json
14:57:22 [http-nio-9080-exec-6] INFO  c.t.s.h.core.executor.JdbcExecutor 41 - executing SQL: with t_1 as (SELECT `imp_date` AS `sys_imp_date`, SUM(1) AS `pv` FROM s2_pv_uv_statis GROUP BY `imp_date`, `imp_date`) SELECT SUM(pv) FROM t_1 WHERE (sys_imp_date >= '2024-07-31' AND sys_imp_date <= '2024-08-06') limit 1000
14:57:22 [http-nio-9080-exec-6] ERROR c.alibaba.druid.filter.FilterManager 117 - load filter error, filter not found : 'stat'
14:57:22 [http-nio-9080-exec-6] WARN  c.alibaba.druid.pool.DruidDataSource 1236 - removeAbandoned is true, not use in production.
14:57:22 [http-nio-9080-exec-6] INFO  c.alibaba.druid.pool.DruidDataSource 985 - {dataSource-2,1@数据实例} inited
14:57:22 [http-nio-9080-exec-6] DEBUG o.s.b.f.xml.XmlBeanDefinitionReader 393 - Loaded 11 bean definitions from class path resource [org/springframework/jdbc/support/sql-error-codes.xml]

14:57:22 [http-nio-9080-exec-6] DEBUG o.s.jdbc.core.JdbcTemplate 440 - Executing SQL query [with t_1 as (SELECT `imp_date` AS `sys_imp_date`, SUM(1) AS `pv`
FROM
s2_pv_uv_statis
GROUP BY `imp_date`, `imp_date`)
SELECT SUM(pv) FROM t_1 WHERE (sys_imp_date >= '2024-07-31' AND sys_imp_date <= '2024-08-06') limit 1000]
14:57:22 [http-nio-9080-exec-6] DEBUG o.s.jdbc.datasource.DataSourceUtils 115 - Fetching JDBC Connection from DataSource
```

[`JdbcExecutor`](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/JdbcExecutor%202cd9b3d123e7415fa3f0a6526464fe15.md)

优化并执行SQL查询

### 缓存相关

```json
14:57:22 [http-nio-9080-exec-6] INFO  c.t.s.h.core.cache.DefaultQueryCache 21 - query from cache, key:supersonic:dev:0:-1:f7b1b5e688abc7568ab130888606780a
14:57:22 [ForkJoinPool.commonPool-worker-20] DEBUG c.t.s.h.c.cache.CaffeineCacheManager 25 - [put caffeineCache] key:supersonic:dev:0:-1:f7b1b5e688abc7568ab130888606780a, value:SemanticQueryResp(columns=[QueryColumn(name=访问次数, type=DECIMAL, nameEn=SUM(pv), showType=NUMBER, authorized=true, dataFormatType=null, dataFormat=null, comment=null)], sql=with t_1 as (SELECT `imp_date` AS `sys_imp_date`, SUM(1) AS `pv`
FROM
s2_pv_uv_statis
GROUP BY `imp_date`, `imp_date`)
SELECT SUM(pv) FROM t_1 WHERE (sys_imp_date >= '2024-07-31' AND sys_imp_date <= '2024-08-06') limit 1000, queryAuthorization=null, useCache=false)
14:57:22 [http-nio-9080-exec-6] DEBUG c.t.s.h.core.cache.DefaultQueryCache 36 - put to cache, key: supersonic:dev:0:-1:f7b1b5e688abc7568ab130888606780a
```

包括查询缓存，以及生成后存入缓存操作，具体剩余可参考4.2 整理版日志内容

## 4.4  前后端交互（网络抓包）

——示例 "超音速所有部门访问次数” 

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%202.png)

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%203.png)

1. 在用户输入对话的过程中，出现多达7个search网络请求：

根据官方手册判断，这是增强用户体验的一种联想功能。通过实时捕获用户输入并进行联想推荐，可以帮助用户更快找到他们需要的信息。这种机制会在用户每次输入时触发一个搜索请求，以便动态生成相关建议。

- 实时联想原理：
    - 先对文本进行分词
    - 然后再进行并行分段探测
    - 选取探测文本最长的、且有联想结果的那项进行返回

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%204.png)

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%205.png)

1. 点击发送对话后，先出现parse请求：
- 解析步骤 (Parse Request):
    - 用户查询文本被传递给大模型。
    - 大模型解析查询文本并生成相应的SQL查询。
    1. 步骤 1：请求参数解析
    
    ```json
    {
        "code": 200,
        "msg": "success",
        "data": {
            "chatId": 1,
            "queryText": "超音速所有部门访问次数",
            "queryId": 55,
            "state": "COMPLETED",
            "selectedParses": [...]
        }
    }
    ```
    
    - **chatId**: 当前会话的ID (1)。
    - **queryText**: 用户查询的文本 ("超音速所有部门访问次数")。
    - **queryId**: 当前查询的ID (55)。
    - **state**: 解析状态 ("COMPLETED")。
    1. 步骤 2：大模型请求
    
    ```json
    {
        "llmReq": {
            "queryText": "超音速所有部门访问次数",
            "schema": {
                "domainName": "超音数数据集",
                "dataSetName": "超音数数据集",
                "fieldNameList": [...],
                "metrics": [...],
                "dimensions": [...]
            },
            "llmConfig": {
                "modelName": "gpt-3.5-turbo",
                "baseUrl": "https://api.openai.com/v1",
                "apiKey": "...",
                "provider": "OPEN_AI",
                "temperature": 0.0,
                "timeOut": 60
            }
        }
    }
    ```
    
    - **queryText**: 用户查询文本。
    - **schema**: 数据集的结构信息。
        - **domainName**: 数据集域名 ("超音数数据集")。
        - **dataSetName**: 数据集名称 ("超音数数据集")。
        - **fieldNameList**: 数据集字段列表。
        - **metrics**: 度量指标列表。
        - **dimensions**: 维度列表。
    - **llmConfig**: 大模型配置 (使用 GPT-3.5-turbo)。
    1.  步骤 3：大模型响应
    
    ```json
    {
        "llmResp": {
            "query": "超音速所有部门访问次数",
            "sqlOutput": "SELECT 部门, SUM(访问次数) AS 超音速所有部门访问次数 FROM 超音数数据集 GROUP BY 部门"
        }
    }
    ```
    
    - **query**: 解析后的查询文本。
    - **sqlOutput**: 大模型生成的SQL查询：
        
        ```sql
        SELECT 部门, SUM(访问次数) AS 超音速所有部门访问次数 FROM 超音数数据集 GROUP BY 部门
        ```
        
    - 解析参数说明：
    1. **code**: 表示请求的状态码，200表示成功。
    2. **msg**: 请求的消息，通常是 "success" 表示成功。
    3. **data**: 包含请求的详细数据。
        - **chatId**: 当前会话的ID。
        - **queryText**: 用户输入的查询文本，如 "超音速部门用书数量分布"。
        - **queryId**: 当前查询的唯一标识符。
        - **state**: 当前解析的状态，这里是 "COMPLETED" 表示解析已完成。
        - **selectedParses**: 包含大模型生成的多个解析结果。
    4. **llmReq**: 向大模型发送的请求。
    - **queryText**: 用户输入的查询文本。
    - **schema**: 数据集的结构信息。
        - **domainName**: 数据集的域名。
        - **dataSetName**: 数据集名称。
        - **fieldNameList**: 数据集中的字段列表。
        - **metrics**: 度量指标列表。
        - **dimensions**: 维度列表。
    - **llmConfig**: 大模型的配置信息。
        - **modelName**: 使用的模型名称，如 "gpt-3.5-turbo"。
        - **baseUrl**: API 基础 URL。
        - **apiKey**: 用于身份验证的 API 密钥。
        - **provider**: 提供商名称。
        - **temperature**: 输出的随机性。
        - **timeOut**: 请求的超时时间。
    1. **llmResp**: 大模型返回的响应。
    - **query**: 大模型解析后的查询文本。
    - **modelName**: 使用的模型名称。
    - **dbSchema**: 数据库模式，包含表名、字段和注释信息。
    - **sqlOutput**: 大模型生成的 SQL 查询。
    - **sqlRespMap**: SQL 查询响应映射。
1. 随后出现execute请求：
- 执行步骤 (Execute Request):
    - 生成的SQL查询在数据库中执行。
    - 返回查询结果，包括列信息和状态。
    1. 步骤 4：执行SQL查询
    
    ```json
    {
        "code": 200,
        "msg": "success",
        "data": {
            "querySql": "with t_1 as (...) SELECT department, SUM(pv) FROM t_1 WHERE (sys_imp_date >= '2024-07-04' AND sys_imp_date <= '2024-07-10') GROUP BY department limit 1000",
            "queryState": "SUCCESS",
            "queryColumns": [...]
        }
    }
    ```
    
    - **querySql**: 执行的SQL查询：
        
        ```sql
        with t_1 as (
            SELECT `t3`.`sys_imp_date`, `t2`.`department`, `t3`.`s2_pv_uv_statis_pv` AS `pv`
            FROM
            (SELECT `user_name`, `department` FROM s2_user_department) AS `t2`
            LEFT JOIN (SELECT 1 AS `s2_pv_uv_statis_pv`, `imp_date` AS `sys_imp_date`, `user_name`, `imp_date` FROM s2_pv_uv_statis) AS `t3`
            ON `t2`.`user_name` = `t3`.`user_name`
        )
        SELECT department, SUM(pv)
        FROM t_1
        WHERE (sys_imp_date >= '2024-07-04' AND sys_imp_date <= '2024-07-10')
        GROUP BY department
        limit 1000
        ```
        
    - **queryState**: 查询状态 ("SUCCESS")。
    - **queryColumns**: 查询结果的列信息。
    
    ### 执行参数说明：
    
    1. **code**: 请求状态码，200表示成功。
    2. **msg**: 请求消息，通常是 "success" 表示成功。
    3. **data**: 执行的详细数据。
        - **querySql**: 要执行的 SQL 查询。
        - **queryState**: 查询状态，"SUCCESS" 表示成功。
        - **queryColumns**: 查询结果的列信息。
            - **name**: 列名称，如 "部门"。
            - **type**: 列类型，如 "VARCHAR"。
            - **nameEn**: 英文列名，如 "department"。
            - **showType**: 显示类型，如 "CATEGORY"。
            - **authorized**: 是否授权访问。
        - **chatContext**: 当前会话的上下文信息。
            - **id**: 会话ID。
            - **queryMode**: 查询模式，如 "LLM_S2SQL"。
            - **dataSet**: 数据集信息。
                - **dataSet**: 数据集ID。
                - **dataSetName**: 数据集名称，如 "超音数数据集"。
                - **bizName**: 业务名称，如 "s2"。
                - **type**: 数据集类型，如 "DATASET"。
            - **metrics**: 度量指标列表。
            - **dimensions**: 维度列表。
                - **dataSet**: 数据集ID。
                - **dataSetName**: 数据集名称。
                - **model**: 模型ID。
                - **id**: 维度ID。
                - **name**: 维度名称，如 "部门"。
                - **bizName**: 业务名称，如 "department"。
                - **isTag**: 是否为标签维度。
            - **dateInfo**: 日期信息。
                - **dateMode**: 日期模式，如 "BETWEEN"。
                - **startDate**: 起始日期，如 "2024-07-10"。
                - **endDate**: 结束日期，如 "2024-07-10"。
                - **groupByTimeDimension**: 按时间维度分组的字段，如 "sys_imp_date"。
1. 每轮查询请求结束后，一次getAll?agentId= 的查询，获取当前聊天信息
2. 如果更改查询参数，再点击重新检索，出现两个query请求：

根据之前用户对话调用LLM识别到的维度参数数据，经过调整参数生成并执行 SQL直接查询。

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%206.png)

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%207.png)

### 抓包内容分析

结构化显示所有抓包内容，解析所有参数：

[网络抓包内容分析](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/%E7%BD%91%E7%BB%9C%E6%8A%93%E5%8C%85%E5%86%85%E5%AE%B9%E5%88%86%E6%9E%90%207ebd5fe038d54b1b93f246bc3e2ceb60.md)

## 4.5 LLM生成流程

### 总结构：

（**提示词 + 少样本提示 + 用户问题增强 + 关键词映射）**

```java
String promptStr = String.format(INSTRUCTION, exemplarsStr, questionAugmented, dataSemanticsStr);
```

### 提示词：

```java
    private static final String INSTRUCTION = ""
            + "#Role: You are a data analyst experienced in SQL languages.\n"
            + "#Task: You will be provided a natural language query asked by business users,"
            + "please convert it to a SQL query so that relevant answer could be returned to the user "
            + "by executing the SQL query against underlying database.\n"
            + "#Rules:"
            + "1.ALWAYS use `数据日期` as the date field."
            + "2.ALWAYS use `datediff()` as the date function."
            + "3.DO NOT specify date filter in the where clause if not explicitly mentioned in the query."
            + "4.ONLY respond with the converted SQL statement.\n"
            + "#Exemplars:\n%s"
            + "#UserQuery: %s "
            + "#Schema: %s "
            + "#SQL: ";
```

翻译：

+“#角色:你是一名有SQL语言经验的数据分析师。”
+“#Task:您将获得由业务用户提出的自然语言查询，”
+“请将其转换为SQL查询，以便将相关答案返回给用户”

+“通过对底层数据库执行SQL查询。\n"

+“#规则:“

+“1。始终使用'数据日期'作为日期字段。"
+”2。总是使用' datediff() '作为日期函数。"
+”3。如果查询中没有明确提到，不要在where子句中指定日期过滤器。
+”4。只响应转换后的SQL语句。\n"

### 少样本提示+自一致性投票：

`ResponseHelper.selfConsistencyVote` 方法负责处理自[一致投票。](https://www.notion.so/cae82e2fe6a24c49931c385191cfbf66?pvs=21)
对于数据集，有特殊的已有构建问题和对应S2SQL语句。

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%208.png)

1. 生成多个 Prompt（作为不同的样本以及提供不同思路）
    
    首先，我们生成了多个 Prompt，每个 Prompt 包含了一组不同的 SQL 示例（few-shot exemplars）。目的是为模型提供参考。
    
2. 并行执行推理
    
    并行地执行这些 Prompt，每个 Prompt 都会通过 ChatLanguageModel 生成一个 SQL 查询。
    
3. 汇总结果并进行投票
    
    将这些生成的 SQL 查询进行汇总，通过投票机制选出最合适 SQL 查询。通过`selfConsistencyVote` 方法对所有生成的 SQL 结果进行投票，选择得票最多的结果作为最终的 SQL 查询。
    
4. 举例说明
    
    假设我们有一个用户查询 “所有部门的访问次数”，我们会生成多个 Prompt，每个 Prompt 包含不同的 SQL 示例。然后，我们并行地将这些 Prompt 发送给模型进行 SQL 生成。最后，我们对所有生成的 SQL 进行投票，选择得票最多的 SQL 作为最终的 SQL 查询。
    
    ### 示例：
    
    1. 用户查询: “所有部门的访问次数”
    2. 生成的 Prompt 列表:
        - Prompt 1: 包含 SQL 示例 A, B, C
        - Prompt 2: 包含 SQL 示例 D, E, F
        - ...
    3. 并行地将这些 Prompt 发送给模型:
        - 模型返回 SQL 查询 1, 2, 3, ...
    4. 对所有生成的 SQL 进行投票:
        - SQL 查询 1 得到 3 票
        - SQL 查询 2 得到 2 票
        - SQL 查询 3 得到 5 票
    5. 选择得票最多的 SQL 查询 3 作为最终的 SQL 查询

### 用户问题增强：

`promptHelper`类中得`buildAugmentedQuestion` 函数通过添加更多上下文信息（如链接值、当前日期、业务术语等）来增强用户的查询问题。有助于模型生成更准确的 SQL 查询，结合了多个辅助方法来构建最终的增强问题字符串。

1. 提取链接的值
    
    函数首先从 `LLMReq` 对象中提取 `linking` 值，这些值表示与查询相关的上下文信息。
    

```java
List<LLMReq.ElementValue> linkedValues = llmReq.getLinking();
```

1. 获取当前日期
    
    获取当前日期字符串以加入到增强的问题中。
    

```java
String currentDate = llmReq.getCurrentDate();
```

1. 获取先前的扩展信息
    
    提取任何先前的扩展信息（`priorExts`），这通常是与当前查询相关的历史或附加信息。
    

```java
String priorExts = llmReq.getPriorExts();
```

1. 构建链接值字符串
    
    遍历 `linkedValues` 列表，并为每个值生成一个描述字符串。例如，如果 `linkedValues` 包含一个字段名为“部门”，字段值为“销售”的元素，它会生成“‘销售’是一个‘部门’”。
    

```java
List<String> priorLinkingList = new ArrayList<>();
for (LLMReq.ElementValue value : linkedValues) {
    String fieldName = value.getFieldName();
    String fieldValue = value.getFieldValue();
    priorLinkingList.add("‘" + fieldValue + "‘是一个‘" + fieldName + "‘");
}
String linkingListStr = String.join("，", priorLinkingList);
```

1. 生成当前日期字符串
    
    生成表示当前日期的字符串。
    

```java
String currentDataStr = "当前的日期是" + currentDate;
```

1. 构建业务术语字符串
    
    调用 `buildTermStr` 函数以构建与查询相关的业务术语的字符串。
    

```java
String termStr = buildTermStr(llmReq);
```

它遍历 `LLMReq` 对象中的术语列表，并为每个术语生成描述字符串。

```java
private String buildTermStr(LLMReq llmReq) {
    List<LLMReq.Term> terms = llmReq.getSchema().getTerms();
    StringBuilder termsDesc = new StringBuilder();
    if (!CollectionUtils.isEmpty(terms)) {
        termsDesc.append("相关业务术语：");
        for (int idx = 0; idx < terms.size(); idx++) {
            LLMReq.Term term = terms.get(idx);
            String name = term.getName();
            String description = term.getDescription();
            List<String> alias = term.getAlias();
            String descPart = StringUtils.isBlank(description) ? "" : String.format("，它通常是指<%s>", description);
            String aliasPart = CollectionUtils.isEmpty(alias) ? "" : String.format("，类似的表达还有%s", alias);
            termsDesc.append(String.format("%d.<%s>是业务术语%s%s；", idx + 1, name, descPart, aliasPart));
        }
        if (termsDesc.length() > 0) {
            termsDesc.setLength(termsDesc.length() - 1);
        }
    }

    return termsDesc.toString();
}
```

1. 拼接增强问题字符串
    
    将用户的原始查询问题与上述生成的字符串拼接在一起，形成一个增强版的问题字符串。
    

```java
return String.format("%s (补充信息:%s;%s;%s;%s)", llmReq.getQueryText(),
        linkingListStr, currentDataStr, termStr, priorExts);
```

1. 示例

完整示例：假设我们有以下 `LLMReq` 对象：

```java
LLMReq llmReq = new LLMReq();
llmReq.setQueryText("所有部门的访问次数");
llmReq.setCurrentDate("2024-07-12");
llmReq.setPriorExts("过去一年的数据");
llmReq.setLinking(Arrays.asList(
    new LLMReq.ElementValue("部门", "销售"),
    new LLMReq.ElementValue("部门", "市场")
));
```

执行 `buildAugmentedQuestion` 函数后，返回的增强问题字符串如下：

```php
所有部门的访问次数 (补充信息:‘销售’是一个‘部门’，‘市场’是一个‘部门’；当前的日期是2024-07-12；相关业务术语：1.<术语1>是业务术语，类似的表达还有...；过去一年的数据)
```

### 关键词映射：

`buildSchemaStr` 函数的主要目的是生成一个字符串，该字符串描述了数据集的表结构，包括表名、指标（metrics）和维度（dimensions）通过遍历数据集的指标和维度列表，生成一个包含表名、指标和维度的描述字符串。这个字符串用于提供给LLM模型以增强生成SQL查询时的上下文信息。

1. 获取表名
    
    函数首先从 `LLMReq` 对象中获取数据集的名称。
    

```java
String tableStr = llmReq.getSchema().getDataSetName();
```

1. 构建指标字符串
    
    通过遍历 `llmReq` 对象中的 `metrics` 列表，构建一个描述所有指标的字符串。对于每个指标，函数会添加其名称、描述和默认聚合函数（如果存在）。
    

```java
StringBuilder metricStr = new StringBuilder();

llmReq.getSchema().getMetrics().stream().forEach(
    metric -> {
        metricStr.append(metric.getName());
        if (StringUtils.isNotEmpty(metric.getDescription())) {
            metricStr.append(" COMMENT '" + metric.getDescription() + "'");
        }
        if (StringUtils.isNotEmpty(metric.getDefaultAgg())) {
            metricStr.append(" AGGREGATE '" + metric.getDefaultAgg().toUpperCase() + "'");
        }
        metricStr.append(",");
    }
);
```

1. 构建维度字符串
    
    以类似的方式处理 `dimensions` 列表，构建一个描述所有维度的字符串。对于每个维度，函数会添加其名称和描述（如果存在）。
    

```java
StringBuilder dimensionStr = new StringBuilder();

llmReq.getSchema().getDimensions().stream().forEach(
    dimension -> {
        dimensionStr.append(dimension.getName());
        if (StringUtils.isNotEmpty(dimension.getDescription())) {
            dimensionStr.append(" COMMENT '" + dimension.getDescription() + "'");
        }
        dimensionStr.append(",");
    }
);
```

1. 格式化字符串
    
    函数使用字符串模板将表名、指标和维度字符串组合成一个完整的描述字符串。
    

```java
String template = "Table: %s, Metrics: [%s], Dimensions: [%s]";
return String.format(template, tableStr, metricStr, dimensionStr);
```

1. 示例

假设我们有以下 `LLMReq` 对象：

```java
LLMReq llmReq = new LLMReq();
llmReq.setSchema(new Schema());
llmReq.getSchema().setDataSetName("订单数据集");

Metric metric1 = new Metric();
metric1.setName("销售额");
metric1.setDescription("总销售额");
metric1.setDefaultAgg("SUM");

Metric metric2 = new Metric();
metric2.setName("订单数");
metric2.setDescription("总订单数");
metric2.setDefaultAgg("COUNT");

llmReq.getSchema().setMetrics(Arrays.asList(metric1, metric2));

Dimension dimension1 = new Dimension();
dimension1.setName("地区");
dimension1.setDescription("销售地区");

Dimension dimension2 = new Dimension();
dimension2.setName("销售日期");
dimension2.setDescription("订单销售日期");

llmReq.getSchema().setDimensions(Arrays.asList(dimension1, dimension2));
```

执行 `buildSchemaStr` 函数后返回如下：

```css
Table: 订单数据集, Metrics: [销售额 COMMENT '总销售额' AGGREGATE 'SUM',订单数 COMMENT '总订单数' AGGREGATE 'COUNT',], Dimensions: [地区 COMMENT '销售地区',销售日期 COMMENT '订单销售日期',]
```

### 寻问框架生成代码：

为了构建最终的询问 `promptStr`，我们需要结合提供的 `INSTRUCTION` 模板、示例数据、增强的问题和数据模式。以下是具体步骤和生成的 `promptStr` 示例：

### 1. INSTRUCTION 模板

```java
private static final String INSTRUCTION = ""
        + "#Role: You are a data analyst experienced in SQL languages.\n"
        + "#Task: You will be provided a natural language query asked by business users,"
        + "please convert it to a SQL query so that relevant answer could be returned to the user "
        + "by executing the SQL query against underlying database.\n"
        + "#Rules:"
        + "1.ALWAYS use `数据日期` as the date field."
        + "2.ALWAYS use `datediff()` as the date function."
        + "3.DO NOT specify date filter in the where clause if not explicitly mentioned in the query."
        + "4.ONLY respond with the converted SQL statement.\n"
        + "#Exemplars:\n%s"
        + "#UserQuery: %s "
        + "#Schema: %s "
        + "#SQL: ";
```

### 2. 示例数据

```java
String exemplarsStr =
        "#UserQuery: 超音数访问次数大于1k的部门是哪些 (补充信息:。当前的日期是2023-09-14)\n#Schema: Table: 超音数产品, Metrics: [访问次数 AGGREGATE 'SUM'], Dimensions: [部门]\n#SQL: SELECT 部门 FROM 超音数产品 WHERE 访问次数 > 1000\n" +
        "#UserQuery: 超音数pv最高的用户有哪些 (补充信息:。当前的日期是2023-08-31)\n#Schema: Table: 超音数产品, Metrics: [访问次数 AGGREGATE 'SUM'], Dimensions: [用户名]\n#SQL: SELECT 用户名 FROM 超音数产品 ORDER BY 访问次数 DESC LIMIT 1\n" +
        "#UserQuery: 超音数近半年哪个月的访问次数汇总最高 (补充信息:。当前的日期是2023-09-04)\n#Schema: Table: 超音数产品, Metrics: [访问次数 AGGREGATE 'SUM'], Dimensions: [数据日期]\n#SQL: SELECT MONTH(数据日期), SUM(访问次数) FROM 超音数产品 WHERE datediff('year', 数据日期, '2023-09-04') <= 0.5 GROUP BY MONTH(数据日期) ORDER BY SUM(访问次数) DESC LIMIT 1\n" +
        "#UserQuery: 超音数近半年每个月的平均访问次数 (补充信息:。当前的日期是2023-09-04)\n#Schema: Table: 超音数产品, Metrics: [访问次数 AGGREGATE 'AVG'], Dimensions: [数据日期]\n#SQL: SELECT MONTH(数据日期), AVG(访问次数) FROM 超音数产品 WHERE datediff('year', 数据日期, '2023-09-04') <= 0.5 GROUP BY MONTH(数据日期)\n" +
        "#UserQuery: 今年以来发行的歌曲中，有哪些在近7天播放超过一千万的 (补充信息:。当前的日期是2023-08-12)\n#Schema: Table: 歌曲库, Metrics: [结算播放量 AGGREGATE 'SUM'], Dimensions: [发行日期, 数据日期]\n#SQL: SELECT 歌曲名 FROM 歌曲库 WHERE datediff('year', 发行日期, '2023-08-12') <= 0 AND datediff('day', 数据日期, '2023-08-12') <= 7 AND 结算播放量 > 10000000\n";
```

### 3. 增强的问题

```java
String questionAugmented = "超音数所有部门访问次数 (补充信息:当前的日期是2023-09-14;)";
```

### 4. 数据模式

```java
String dataSemanticsStr = "Table: 超音数数据集, Metrics: [访问次数 AGGREGATE 'SUM'], Dimensions: [部门]";
```

### 5. 最终的 `promptStr`

```java
String promptStr = String.format(INSTRUCTION, exemplarsStr, questionAugmented, dataSemanticsStr);
```

### 完整的 `promptStr` 示例

```java
String promptStr = String.format(
    "#Role: You are a data analyst experienced in SQL languages.\n" +
    "#Task: You will be provided a natural language query asked by business users, " +
    "please convert it to a SQL query so that relevant answer could be returned to the user " +
    "by executing the SQL query against underlying database.\n" +
    "#Rules:\n" +
    "1.ALWAYS use `数据日期` as the date field.\n" +
    "2.ALWAYS use `datediff()` as the date function.\n" +
    "3.DO NOT specify date filter in the where clause if not explicitly mentioned in the query.\n" +
    "4.ONLY respond with the converted SQL statement.\n" +
    "#Exemplars:\n%s" +
    "#UserQuery: %s " +
    "#Schema: %s " +
    "#SQL: ",
    exemplarsStr, questionAugmented, dataSemanticsStr
);
```

### 示例结果

```java
#Role: You are a data analyst experienced in SQL languages.
#Task: You will be provided a natural language query asked by business users, please convert it to a SQL query so that relevant answer could be returned to the user by executing the SQL query against underlying database.
#Rules:
1.ALWAYS use `数据日期` as the date field.
2.ALWAYS use `datediff()` as the date function.
3.DO NOT specify date filter in the where clause if not explicitly mentioned in the query.
4.ONLY respond with the converted SQL statement.
#Exemplars:
#UserQuery: 超音数访问次数大于1k的部门是哪些 (补充信息:。当前的日期是2023-09-14)
#Schema: Table: 超音数产品, Metrics: [访问次数 AGGREGATE 'SUM'], Dimensions: [部门]
#SQL: SELECT 部门 FROM 超音数产品 WHERE 访问次数 > 1000
#UserQuery: 超音数pv最高的用户有哪些 (补充信息:。当前的日期是2023-08-31)
#Schema: Table: 超音数产品, Metrics: [访问次数 AGGREGATE 'SUM'], Dimensions: [用户名]
#SQL: SELECT 用户名 FROM 超音数产品 ORDER BY 访问次数 DESC LIMIT 1
#UserQuery: 超音数近半年哪个月的访问次数汇总最高 (补充信息:。当前的日期是2023-09-04)
#Schema: Table: 超音数产品, Metrics: [访问次数 AGGREGATE 'SUM'], Dimensions: [数据日期]
#SQL: SELECT MONTH(数据日期), SUM(访问次数) FROM 超音数产品 WHERE datediff('year', 数据日期, '2023-09-04') <= 0.5 GROUP BY MONTH(数据日期) ORDER BY SUM(访问次数) DESC LIMIT 1
#UserQuery: 超音数近半年每个月的平均访问次数 (补充信息:。当前的日期是2023-09-04)
#Schema: Table: 超音数产品, Metrics: [访问次数 AGGREGATE 'AVG'], Dimensions: [数据日期]
#SQL: SELECT MONTH(数据日期), AVG(访问次数) FROM 超音数产品 WHERE datediff('year', 数据日期, '2023-09-04') <= 0.5 GROUP BY MONTH(数据日期)
#UserQuery: 今年以来发行的歌曲中，有哪些在近7天播放超过一千万的 (补充信息:。当前的日期是2023-08-12)
#Schema: Table: 歌曲库, Metrics: [结算播放量 AGGREGATE 'SUM'], Dimensions: [发行日期, 数据日期]
#SQL: SELECT 歌曲名 FROM 歌曲库 WHERE datediff('year', 发行日期, '2023-08-12') <= 0 AND datediff('day', 数据日期, '2023-08-12') <= 7 AND 结算播放量 > 10000000
#UserQuery: 超音数所有部门访问次数 (补充信息:当前的日期是2023-09-14;)
#Schema: Table: 超音数数据集, Metrics: [访问次数 AGGREGATE 'SUM'], Dimensions: [部门]
#SQL:
```

## 4.6 数据存储与检索

本项目系统默认使用H2内存数据库，重启后会丢失数据，可以重新自行配置到MYSQL等数据库中，默认配置文件均已配置，具体参考8 常见问题。

根据项目日志观察分析，所有信息均完整存储数据库中，所有显示信息均通过反复查询数据库调取。

![image.png](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/image%209.png)

### 反复出现数据库查询示例

包含查询指标、聊天记录等：

```css
14:28:27 [http-nio-9080-exec-1] DEBUG org.mybatis.spring.SqlSessionUtils 49 - Creating a new SqlSession
14:28:27 [http-nio-9080-exec-1] DEBUG org.mybatis.spring.SqlSessionUtils 49 - SqlSession [org.apache.ibatis.session.defaults.DefaultSqlSession@428ba2f6] was not registered for synchronization because synchronization is not active
14:28:27 [http-nio-9080-exec-1] DEBUG o.s.jdbc.datasource.DataSourceUtils 115 - Fetching JDBC Connection from DataSource
14:28:27 [http-nio-9080-exec-1] DEBUG o.m.s.t.SpringManagedTransaction 49 - JDBC Connection [com.mysql.cj.jdbc.ConnectionImpl@3404ed53] will not be managed by Spring
14:28:27 [http-nio-9080-exec-1] DEBUG c.t.s.c.s.p.m.C.selectList_COUNT 135 - ==>  Preparing: SELECT count(0) FROM s2_chat_query WHERE (chat_id = ? AND user_name = ?)
14:28:27 [http-nio-9080-exec-1] DEBUG c.t.s.c.s.p.m.C.selectList_COUNT 135 - ==> Parameters: 1(Long), admin(String)
14:28:27 [http-nio-9080-exec-1] DEBUG c.t.s.c.s.p.m.C.selectList_COUNT 135 - <==      Total: 1
14:28:27 [http-nio-9080-exec-1] DEBUG c.t.s.c.s.p.m.C.selectList 135 - ==>  Preparing: SELECT question_id,agent_id,create_time,user_name,query_state,chat_id,score,feedback,query_text,query_result,similar_queries,parse_time_cost FROM s2_chat_query WHERE (chat_id = ? AND user_name = ?) ORDER BY question_id DESC LIMIT ?
14:28:27 [http-nio-9080-exec-1] DEBUG c.t.s.c.s.p.m.C.selectList 135 - ==> Parameters: 1(Long), admin(String), 3(Integer)
14:28:27 [http-nio-9080-exec-1] DEBUG c.t.s.c.s.p.m.C.selectList 135 - <==      Total: 3
14:28:27 [http-nio-9080-exec-1] DEBUG org.mybatis.spring.SqlSessionUtils 49 - Closing non transactional SqlSession [org.apache.ibatis.session.defaults.DefaultSqlSession@428ba2f6]

```

这段日志记录展示了一个后端服务在处理HTTP请求过程中与数据库的交互。具体步骤如下：

1. **创建新的SqlSession**：
    - `Creating a new SqlSession`：日志显示正在创建一个新的SQL会话（SqlSession）。这是与数据库交互的第一步，涉及到建立一个数据库会话环境。
2. **SqlSession注册情况**：
    - `SqlSession [org.apache.ibatis.session.defaults.DefaultSqlSession@428ba2f6] was not registered for synchronization because synchronization is not active`：这说明创建的SqlSession没有注册同步，因为当前环境没有激活同步操作。这通常意味着该操作不在事务管理之下。
3. **获取数据库连接**：
    - `Fetching JDBC Connection from DataSource`：从数据源获取JDBC连接，这是执行SQL命令前的准备步骤。
4. **JDBC连接管理**：
    - `JDBC Connection [com.mysql.cj.jdbc.ConnectionImpl@3404ed53] will not be managed by Spring`：表明获取的JDBC连接不会被Spring框架管理。通常这种情况出现在手动管理数据库连接或在非标准事务环境下操作时。
5. **执行SQL查询**（计数查询）：
    - `Preparing: SELECT count(0) FROM s2_chat_query WHERE (chat_id = ? AND user_name = ?)`：准备执行一个SQL查询，计算符合特定条件（chat_id和user_name）的记录数。
    - `Parameters: 1(Long), admin(String)`：指明SQL查询中使用的参数，这里使用了聊天ID为1和用户名为"admin"。
    - `Total: 1`：查询结果显示，有1条记录满足条件。
6. **执行SQL查询**（选择列表）：
    - `Preparing: SELECT question_id, agent_id, create_time, user_name, query_state, chat_id, score, feedback, query_text, query_result, similar_queries, parse_time_cost FROM s2_chat_query WHERE (chat_id = ? AND user_name = ?) ORDER BY question_id DESC LIMIT ?`：准备执行一个更复杂的SQL查询，选择多个字段，条件同上，并按question_id降序排列，限制返回结果数为3。
    - `Parameters: 1(Long), admin(String), 3(Integer)`：SQL查询使用的参数，包括聊天ID、用户名以及返回的最大记录数。
    - `Total: 3`：查询结果显示，有3条记录满足条件。
7. **关闭SqlSession**：
    - `Closing non transactional SqlSession [org.apache.ibatis.session.defaults.DefaultSqlSession@428ba2f6]`：日志记录了非事务性SqlSession的关闭操作，表明此次数据库会话结束。

# 5. 代码分析

## 5.1 源码结构

.github：负责项目的GitHub配置，包括Issue模板和工作流配置。

- **ISSUE_TEMPLATE**：存放各种问题模板，用于用户在提交Bug、增强请求、功能请求和问题请求时使用。
- **workflows**：存放持续集成配置文件，用于不同操作系统（如CentOS、Mac、Ubuntu、Windows）上的CI配置。
- **PULL_REQUEST_TEMPLATE.md**：Pull Request的模板文件，规范提交PR时的信息。

.idea：存放项目的IDE配置文件，通常用于JetBrains系列的IDE（如IntelliJ IDEA）。

- **.gitignore**：忽略IDE生成的临时文件。
- **compiler.xml、encodings.xml、jarRepositories.xml、misc.xml、vcs.xml、workspace.xml**：IDE的各种配置文件。

assembly：负责项目的打包和构建脚本。

- **bin**：存放不同平台的构建和启动脚本。
- **build**：存放构建相关的配置文件和打包结果。

auth：负责项目的认证和授权功能。

- **api**：认证API的源码和目标文件。
- **authentication**：认证模块的源码和目标文件。
- **authorization**：授权模块的源码和目标文件。
- **target**：构建过程中的临时文件和结果文件。

benchmark：负责性能测试和基准测试。

- **data**：存放用于基准测试的数据文件。
- **benchmark.md、benchmark.py、requirements.txt**：基准测试的说明、脚本和依赖文件。

chat：负责聊天功能的实现。

- **api**：聊天API的源码和目标文件。
- **server**：聊天服务器的源码和目标文件。
- **target**：构建过程中的临时文件和结果文件。

checkstyle：存放代码风格检查的配置文件。

- **checkstyle.xml**：Checkstyle配置文件。

common：存放项目的公共代码和模块。

- **src**：主代码和测试代码。
- **target**：构建过程中的临时文件和结果文件。

docker：负责项目的Docker配置和相关脚本。

- **docker-build.bat、docker-build.sh**：Docker构建脚本。
- **docker-compose.yml、Dockerfile**：Docker编排文件和Docker镜像配置文件

evaluation：负责模型评估和数据处理。

- **config、data**：存放评估过程中的配置文件和数据文件。
- **各个Python脚本**：实现评估和数据处理的功能。

headless：负责无头模式下的功能实现。

- **api、chat、core、server**：各模块的源码和目标文件。
- **target**：构建过程中的临时文件和结果文件。

launchers：存放项目的启动器相关代码和配置。

- **chat、common、headless、standalone**：各个启动器模块的源码和目标文件。
- **target**：构建过程中的临时文件和结果文件。

logs：存放项目运行过程中的日志文件。

- **各种.log和.log.gz文件**：不同模块和功能的日志文件。

target：存放构建过程中的临时文件和结果文件。

- **checkstyle相关文件**：代码风格检查的结果文件。

webapp：负责Web应用的前端部分。

- **node_modules**：前端依赖的模块。
- **packages**：前端项目包。
- **各个脚本和配置文件**：前端开发和生产环境的启动脚本和配置文件。

其他：

- **.flattened-pom.xml**：扁平化的Maven配置文件。
- **.gitignore**：Git忽略文件。
- **CHANGELOG.md**：项目变更日志。
- **LICENSE**：项目的许可证。
- **pom.xml**：Maven主配置文件。
- **README.md、README_CN.md、README_JP.md**：项目的说明文档，分别用英文、中文和日文编写。

## 5.2 模块位置

- 项目接口（ChatBI Interface）:

`chat/server/src/main/java/com/tencent/supersonic/chat/server/service/impl/`

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%209.png)

- 可视化对话（Visualization Chats）:

`webapp/packages/chat-sdk/src/Chat`

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2010.png)

- **模式映射器(Schema Mapper)：**

将自然语言文本在知识库中进行匹配，为后续的语义解析提供相关信息。

`headless/chat/src/main/java/com/tencent/supersonic/headless/chat/mapper`

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2011.png)

- **模型知识库(Knowledge Base)：**

定期从语义模型中提取相关的模式信息，构建词典和索引，以便后续的模式映射。

`headless/chat/src/main/java/com/tencent/supersonic/headless/chat/knowledge`

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2012.png)

- **语义解析器(Semantic Parser)：**

理解用户查询并抽取语义信息，生成语义查询语句S2SQL。

`headless/chat/src/main/java/com/tencent/supersonic/headless/chat/parser`

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2013.png)

- **问答记忆(Chat Memory)：**

将历史的查询轨迹进行封装，可被召回作为few-shot样例嵌入提示词。

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2014.png)

- **问答插件(Chat Plugin)：**

通过第三方工具扩展功能给定所有配置的插件及其功能描述和示例问。

`chat/server/src/main/java/com/tencent/supersonic/chat/server/plugin`

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2015.png)

- **语义修正器(Semantic Corrector)：**

检查语义查询语句的合法性，对不合法的信息做修正和优化处理。

`headless/chat/src/main/java/com/tencent/supersonic/headless/chat/corrector`

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2016.png)

- **语义翻译器(Semantic Translator)** + （Semantic Data Model）:

将语义查询语句翻译成可在物理数据模型上执行的SQL语句。

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2017.png)

## 5.3 模块依赖关系

具体联系请参考4.1 数据流图，以及4.2 数据流详细分析。

# 6. 关键技术

## 6.1 大模型相关技术

### 少样本提示：

[少样本提示 – Nextra](https://www.promptingguide.ai/zh/techniques/fewshot)

### 自一致性：

[自我一致性 – Nextra](https://www.promptingguide.ai/zh/techniques/consistency)

[ICLR 2023 | Self-Consistency: Google超简单方法改善大模型推理能力_self-consistency improves chain of thought reasoni-CSDN博客](https://blog.csdn.net/qq_16949707/article/details/131532600)

[arxiv.org](https://arxiv.org/pdf/2203.11171)

[PET-SQL：具有跨一致性的大模型Prompt增强两阶段Text-to-SQL框架！ - 文章 - 开发者社区 - 火山引擎](https://developer.volcengine.com/articles/7389112187136000036)

## 6.2 SQL解析框架 Apache Calcite

主要负责语义翻译模块，将优化后S2SQL解析为可执行SQL语句并进行合理优化

### 主要功能

1. **SQL 解析和验证**：
    - Calcite 可以解析标准 SQL 语法，并将其转换为内部的抽象语法树 (AST) 或者关系表达式 (RelNode)。
    - 它还可以验证 SQL 查询的合法性，例如检查语法错误、检查字段或表的存在性。
2. **查询优化**：
    - Calcite 提供了一套优化规则，可以对查询进行逻辑优化。比如它会将查询中的某些操作重写为更高效的形式，或者消除冗余的计算。
    - 它支持自定义的优化规则，允许开发者根据特定需求进行扩展。
3. **查询计划生成**：
    - Calcite 将优化后的查询表达式转换为物理查询计划，即将查询转换为可在特定数据库引擎或执行环境中运行的形式。
4. **多数据源支持**：
    - Calcite 支持对多种异构数据源的访问，如关系型数据库、NoSQL 数据库、文件系统等，并可以将它们统一为一个 SQL 接口。

### 其他资料

[Apache Calcite 快速入门指南](https://strongduanmu.com/blog/apache-calcite-quick-start-guide.html)

[Apache Calcite教程-SQL解析-Calcite SQL解析_java使用apcahe calcite 解析sql-CSDN博客](https://blog.csdn.net/QXC1281/article/details/89481346)

[segmentfault.com](https://segmentfault.com/a/1190000043345921)

[](https://segmentfault.com/a/1190000040829100)

## 6.3 大模型交互框架 langchain4j

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2018.png)

[LangChain中文网:500页中文文档教程，助力大模型LLM应用开发从入门到精通](https://www.langchain.com.cn/)

[Introduction | LangChain4j](https://docs.langchain4j.dev/intro/)

[https://github.com/langchain4j/langchain4j/](https://github.com/langchain4j/langchain4j/)

### OPENAI协议样例（Supersonic使用）

[OpenAI | LangChain4j](https://docs.langchain4j.dev/integrations/language-models/open-ai)

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2019.png)

### 可参考SQL交互库（包含Fewshot模板，源代码具有参考价值）

提供了LLM生成SQL的便捷方式，跟Supersonic的获取基础模板后自行修正不一样，是连接数据库后更直接的调用大模型能力生成，效果有待验证，但实现逻辑直接。Supersonic项目中使用的是简单的问询模板。

LangChain 的 SQL 代理提供了一个高级的方式来与 SQL 数据库进行交互。这个代理的设计使得用户可以更灵活地操作数据库，具体优势包括：

1. **智能问答能力**：SQL 代理可以根据数据库的模式和内容回答关于数据库结构或特定表的问题，这使得用户在不直接查看数据库结构的情况下，也能快速了解和操作数据库内容。
2. **错误恢复**：在执行查询时，如果发生错误，SQL 代理可以捕获错误回溯（backtrace），并重新生成正确的查询。这个功能对于调试和优化查询非常有用，帮助用户避免常见的错误并提高查询效率。
3. **迭代查询**：有时候回答一个问题需要多次查询数据库。SQL 代理能够根据用户问题的需要，自动进行多次查询，直到找到满意的答案。
4. **效率优化**：代理能够智能地只从相关的表中检索必要的模式信息，有效地节约资源和令牌使用，提高查询效率。

为了初始化这个代理，你需要使用 `create_sql_agent` 构造函数。这个函数是基于 `SQLDatabaseToolkit` 来构建的，包含了以下工具和功能：

- **创建和执行查询**：允许用户定义和执行SQL查询。
- **检查查询语法**：自动检查SQL查询的语法正确性，帮助用户避免语法错误。
- **检索表描述**：能够提供数据库表的结构和描述信息，帮助用户更好地理解数据存储的细节。
- **等等**：包括更多有助于数据库管理和数据检索的工具和功能。

实现：

- **数据库连接**：首先，SQL 代理需要与数据库建立连接。这通常通过提供数据库的连接字符串（包括数据库的类型、服务器地址、端口号、数据库名、用户名和密码等）来实现。连接一旦建立，代理就可以发送查询命令和接收数据。
- **发送查询**：用户通过代理输入查询请求，代理则将这些请求转化为适合数据库的 SQL 语句。这一过程可能涉及到解析用户的自然语言查询，转换为结构化的 SQL 查询。
- **执行查询**：SQL 代理使用 SQLDatabaseToolkit 的功能来执行构建的 SQL 查询。这包括对 SQL 语句的语法进行检查以确保其正确性，然后将其发送到数据库服务器执行。
- **错误处理与恢复**：如果查询过程中出现错误，SQL 代理可以捕捉到这些错误（例如，语法错误、执行超时等）。代理可以基于错误的类型进行适当的调整或重试策略，如修改查询语句或调整查询参数。
- **数据接收和处理**：查询执行后，数据库会返回数据。SQL 代理接收这些数据，并根据用户的需求进行处理和格式化，以便用户可以理解和使用这些数据。
- **多次查询支持**：对于复杂的问题，可能需要多次查询才能得到完整的答案。SQL 代理可以根据初次查询的结果决定是否需要进一步的查询，并连续执行多个查询。
- **资源和权限管理**：SQL 代理还需要管理与数据库交互时的权限和资源使用，确保数据安全性和访问效率。这可能涉及到限制某些类型的查询或调整查询频率和数据加载量。

[代理商 | LangChain中文网:500页中文文档教程，助力大模型LLM应用开发从入门到精通](https://www.langchain.com.cn/use_cases/sql/agents)

[SQL Database | 🦜️🔗 LangChain](https://python.langchain.com/v0.2/docs/integrations/toolkits/sql_database/)

## 6.4 自动文档框架 Swagger

[超详细！使用swagger自动生成Api文档（swagger-ui）_swagger生成api 前端-CSDN博客](https://blog.csdn.net/zhanggonglalala/article/details/98070986)

### 参考内容

项目使用了内置了swagger自动api文档说明，启动后查看，便于后续分析调用。

http://localhost:9080/swagger-ui/index.html

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2020.png)

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2021.png)

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2022.png)

框架结构：

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2023.png)

具体接口：

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2024.png)

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2025.png)

### 导出

API文档导出

[segmentfault.com](https://segmentfault.com/a/1190000044881763)

[http://localhost:9080/v3/api-docs](http://localhost:9080/v3/api-docs)

[Swagger API.html](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Swagger_API.html)

# 7. 测试和验证

## 7.1 LLM配置验证

使用简单对话”来闲聊“直接验证即可

[配置LLM](https://supersonicbi.github.io/docs/系统部署/配置llm/)

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2026.png)

## 7.2 Mysql数据库验证

[配置DB](https://supersonicbi.github.io/docs/系统部署/配置db/)

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2027.png)

## 7.3 大模型LLM输出验证

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2028.png)

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2029.png)

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2030.png)

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2031.png)

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2032.png)

Schema + Few-shot + LLM解析：已经验证完毕

# 8. 常见问题与解决方案

## 8.1 常见疑问

### 官方FAQ?

[FAQ](https://supersonicbi.github.io/docs/faq/)

- [项目有没有体验的地址？](https://supersonicbi.github.io/docs/faq/#%E9%A1%B9%E7%9B%AE%E6%9C%89%E6%B2%A1%E6%9C%89%E4%BD%93%E9%AA%8C%E7%9A%84%E5%9C%B0%E5%9D%80)
- [初始启动后为什么能显示DEMO问答对话？](https://supersonicbi.github.io/docs/faq/#%E5%88%9D%E5%A7%8B%E5%90%AF%E5%8A%A8%E5%90%8E%E4%B8%BA%E4%BB%80%E4%B9%88%E8%83%BD%E6%98%BE%E7%A4%BAdemo%E9%97%AE%E7%AD%94%E5%AF%B9%E8%AF%9D)
- [是否自带大模型服务？](https://supersonicbi.github.io/docs/faq/#%E6%98%AF%E5%90%A6%E8%87%AA%E5%B8%A6%E5%A4%A7%E6%A8%A1%E5%9E%8B%E6%9C%8D%E5%8A%A1)
- [支持哪些大模型服务？](https://supersonicbi.github.io/docs/faq/#%E6%94%AF%E6%8C%81%E5%93%AA%E4%BA%9B%E5%A4%A7%E6%A8%A1%E5%9E%8B%E6%9C%8D%E5%8A%A1)
- [是否支持文本知识库？](https://supersonicbi.github.io/docs/faq/#%E6%98%AF%E5%90%A6%E6%94%AF%E6%8C%81%E6%96%87%E6%9C%AC%E7%9F%A5%E8%AF%86%E5%BA%93)
- [是否支持多轮对话？](https://supersonicbi.github.io/docs/faq/#%E6%98%AF%E5%90%A6%E6%94%AF%E6%8C%81%E5%A4%9A%E8%BD%AE%E5%AF%B9%E8%AF%9D)
- [重启系统后为什么配置的助理/模型数据丢失了？](https://supersonicbi.github.io/docs/faq/#%E9%87%8D%E5%90%AF%E7%B3%BB%E7%BB%9F%E5%90%8E%E4%B8%BA%E4%BB%80%E4%B9%88%E9%85%8D%E7%BD%AE%E7%9A%84%E5%8A%A9%E7%90%86%E6%A8%A1%E5%9E%8B%E6%95%B0%E6%8D%AE%E4%B8%A2%E5%A4%B1%E4%BA%86)
- [系统默认的账号和密码是什么？](https://supersonicbi.github.io/docs/faq/#%E7%B3%BB%E7%BB%9F%E9%BB%98%E8%AE%A4%E7%9A%84%E8%B4%A6%E5%8F%B7%E5%92%8C%E5%AF%86%E7%A0%81%E6%98%AF%E4%BB%80%E4%B9%88)
- [如果要用我自己的数据进行测试，我至少需要经过哪些步骤](https://supersonicbi.github.io/docs/faq/#%E5%A6%82%E6%9E%9C%E8%A6%81%E7%94%A8%E6%88%91%E8%87%AA%E5%B7%B1%E7%9A%84%E6%95%B0%E6%8D%AE%E8%BF%9B%E8%A1%8C%E6%B5%8B%E8%AF%95%E6%88%91%E8%87%B3%E5%B0%91%E9%9C%80%E8%A6%81%E7%BB%8F%E8%BF%87%E5%93%AA%E4%BA%9B%E6%AD%A5%E9%AA%A4)
- [是否可以提供接口供第三方应用调用？](https://supersonicbi.github.io/docs/faq/#%E6%98%AF%E5%90%A6%E5%8F%AF%E4%BB%A5%E6%8F%90%E4%BE%9B%E6%8E%A5%E5%8F%A3%E4%BE%9B%E7%AC%AC%E4%B8%89%E6%96%B9%E5%BA%94%E7%94%A8%E8%B0%83%E7%94%A8)
- [有哪些国内的大模型服务对接？](https://supersonicbi.github.io/docs/faq/#%E6%9C%89%E5%93%AA%E4%BA%9B%E5%9B%BD%E5%86%85%E7%9A%84%E5%A4%A7%E6%A8%A1%E5%9E%8B%E6%9C%8D%E5%8A%A1%E5%AF%B9%E6%8E%A5)
- [【语义模型】和【数据集】有什么区别？](https://supersonicbi.github.io/docs/faq/#%E8%AF%AD%E4%B9%89%E6%A8%A1%E5%9E%8B%E5%92%8C%E6%95%B0%E6%8D%AE%E9%9B%86%E6%9C%89%E4%BB%80%E4%B9%88%E5%8C%BA%E5%88%AB)
- [是否可以定制few-shot示例？](https://supersonicbi.github.io/docs/faq/#%E6%98%AF%E5%90%A6%E5%8F%AF%E4%BB%A5%E5%AE%9A%E5%88%B6few-shot%E7%A4%BA%E4%BE%8B)
- [使用ollama时，问答出现"在Python中xxxx"的如下图错误？](https://supersonicbi.github.io/docs/faq/#%E4%BD%BF%E7%94%A8ollama%E6%97%B6%E9%97%AE%E7%AD%94%E5%87%BA%E7%8E%B0%E5%9C%A8python%E4%B8%ADxxxx%E7%9A%84%E5%A6%82%E4%B8%8B%E5%9B%BE%E9%94%99%E8%AF%AF)

### S2SQL歧义指正？

一般意义上S2SQL指[阿里巴巴Text2SQL模型](https://www.notion.so/cae82e2fe6a24c49931c385191cfbf66?pvs=21)，主要指代的是Question-Schema interaction graph Encoder使用的是传统意义上的深度学习神经网络模型，但是进行了编译器结构优化和效率。

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2033.png)

此处对于说明文档中的S2SQL个人判断不是一个概念，更可能的解释是Structured to SQL，在此仅仅只是名字重合。

"Structured to SQL"的意思是将结构化的查询语句或数据转换为SQL语句。这个过程包括从文本或语句中解析出维度、维度值和指标等信息，并构造成一个初始的SQL查询（S2SQL），然后经过修正和优化，最终生成可以在数据库引擎上执行的SQL代码。

这个解析和转换过程在数据库查询、报表生成、数据分析等领域非常常见，旨在自动化地将用户输入的结构化或半结构化数据转换为可执行的SQL查询，从而简化用户与数据库的交互。

### 项目中数据集指代什么？

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2034.png)

数据集指代概念就是数据库概念中一样，但是supersonic项目中想要使用数据集比较繁琐，需要经过：

1、数据库连接（目前发现必须指定具体数据库）

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2035.png)

2、语义建模（选择连接数据库，添加所需表，数据建模连接相关表，添加便于后续查询的标签对象，最后再进行权限管理）

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2036.png)

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2037.png)

3、助手设置（进入工具管理，指定数据集，但测试下来发现不指定即默认情况下会关联所有可能的数据模型）

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2038.png)

- **连接问题（可行性分析）：**

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2039.png)

**官方教程指定了数据库，所以可能针对每一个数据库都要单独创建连接**

在JDBC连接字符串中，通常会指定一个默认的数据库名称，这样在连接到数据库服务器后，所有操作都会在这个默认数据库中进行。在你的连接字符串中，`sakila`是默认的数据库：

```bash
jdbc:mysql://localhost:3306/sakila?useUnicode=true&characterEncoding=UTF-8&useSSL=false&allowMultiQueries=true
```

如果你想连接到MySQL服务器而不指定默认的数据库，可以省略数据库名称。这样你可以在连接后选择要使用的数据库，或者在每个SQL查询中显式指定数据库名称。修改后的连接字符串如下：

```ruby
jdbc:mysql://localhost:3306/?useUnicode=true&characterEncoding=UTF-8&useSSL=false&allowMultiQueries=true
```

在这种情况下，你需要在每个SQL查询中指定数据库，或者在连接后选择数据库。例如：

```java
Connection connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/?useUnicode=true&characterEncoding=UTF-8&useSSL=false&allowMultiQueries=true", "username", "password");

// 选择数据库
Statement statement = connection.createStatement();
statement.execute("USE sakila");

// 执行查询
ResultSet resultSet = statement.executeQuery("SELECT * FROM sakila.film");
```

或者你可以在每个查询中显式指定数据库名称：

```java
ResultSet resultSet = statement.executeQuery("SELECT * FROM sakila.film");
```

这样，你的连接将不再限制在一个特定的数据库中，你可以在代码中灵活地选择和切换数据库。

### 语义解析是什么？

指的是LLM模块中，用于生成的增强问题代码，会根据之前所说的语义建模中的标签信息，加上表单中解析出来的内容Schema等进行说明。例如添加了”部门“指标：代码解析出了HR在表单中属于这个类，则会在问题增强中对大模型进行说明（“HR”是一个“部门”），这样可以让大模型更好的理解问题的结构和内容，达到增强问题的目的。

### 一致性投票是如何进行的？

[需要代码解析](https://www.notion.so/cae82e2fe6a24c49931c385191cfbf66?pvs=21)：`ResponseHelper.selfConsistencyVote`

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2040.png)

使用场景：generate函数 分析：

1. **召回示例（exemplars）**
    
    ```java
    List<List<SqlExemplar>> exemplarsList = promptHelper.getFewShotExemplars(llmReq);
    ```
    
    这一步从 `promptHelper` 中获取示例列表，每个列表包含多个 `SqlExemplar`。这些示例是用于生成SQL查询的参考示例。
    
2. **为每个自一致性推断生成SQL生成提示**
    
    ```java
    Map<Prompt, List<SqlExemplar>> prompt2Exemplar = new HashMap<>();
    for (List<SqlExemplar> exemplars : exemplarsList) {
        Prompt prompt = generatePrompt(llmReq, exemplars);
        prompt2Exemplar.put(prompt, exemplars);
    }
    ```
    
    为每个示例生成一个 `Prompt` 对象，并将其与示例关联起来。`Prompt` 对象是用于生成SQL查询的提示信息。
    
3. **并行执行多个自一致性推断**
    
    ```java
    Map<Prompt, String> prompt2Output = new ConcurrentHashMap<>();
    prompt2Exemplar.keySet().parallelStream().forEach(prompt -> {
        keyPipelineLog.info("OnePassSCSqlGenStrategy reqPrompt:\n{}", prompt.toUserMessage());
        ChatLanguageModel chatLanguageModel = getChatLanguageModel(llmReq.getLlmConfig());
        Response<AiMessage> response = chatLanguageModel.generate(prompt.toUserMessage());
        String result = response.content().text();
        prompt2Output.put(prompt, result);
        keyPipelineLog.info("OnePassSCSqlGenStrategy modelResp:\n{}", result);
    });
    ```
    
    并行执行多个自一致性推断，即并行调用大模型生成SQL查询，并将每个 `Prompt` 生成的SQL查询存储在 `prompt2Output` 中。
    
4. **记录 `prompt2Output` 的内容**
    
    ```java
    prompt2Output.forEach((prompt, result) -> {
        keyPipelineLog.info("Prompt: {}\nResult: {}", prompt, result);
    });
    ```
    
    这一步用于记录每个 `Prompt` 及其生成的结果，方便调试和分析。
    
5. **格式化响应**
    
    ```java
    Pair<String, Map<String, Double>> sqlMapPair = ResponseHelper.selfConsistencyVote(Lists.newArrayList(prompt2Output.values()));
    LLMResp llmResp = new LLMResp();
    llmResp.setQuery(promptHelper.buildAugmentedQuestion(llmReq));
    llmResp.setDbSchema(promptHelper.buildSchemaStr(llmReq));
    llmResp.setSqlOutput(sqlMapPair.getLeft());
    llmResp.setSqlRespMap(ResponseHelper.buildSqlRespMap(exemplarsList.get(0), sqlMapPair.getRight()));
    ```
    
    这一步包括以下内容：
    
    - 调用 `ResponseHelper.selfConsistencyVote` 方法进行投票，选择最有可能正确的SQL查询。
    - 使用 `promptHelper` 构建增强问题和数据库架构字符串。
    - 将投票选出的SQL查询设置为响应的 `sqlOutput`。
    - 构建SQL响应映射，并设置为响应的 `sqlRespMap`。

**自一致性投票机制的具体实现**

1. **从 `prompt2Output` 中获取所有生成的SQL查询**
    
    ```java
    Pair<String, Map<String, Double>> sqlMapPair = ResponseHelper.selfConsistencyVote(Lists.newArrayList(prompt2Output.values()));
    ```
    
    这一步调用 `ResponseHelper.selfConsistencyVote` 方法，对所有生成的SQL查询进行投票。传入的参数是 `prompt2Output` 中所有的SQL查询。
    
2. **统计每个SQL查询的出现次数**
    
    ```java
    Map<String, Integer> inputCounts = new HashMap<>();
    for (String input : outputList) {
        inputCounts.put(input, inputCounts.getOrDefault(input, 0) + 1);
    }
    ```
    
    在 `selfConsistencyVote` 方法中，首先统计每个SQL查询的出现次数。使用一个 `HashMap` 来存储每个SQL查询的出现次数。
    
3. **确定出现次数最多的SQL查询**
    
    ```java
    String inputMax = null;
    int maxCount = 0;
    int inputSize = outputList.size();
    Map<String, Double> votePercentage = new HashMap<>();
    for (Map.Entry<String, Integer> entry : inputCounts.entrySet()) {
        String input = entry.getKey();
        int count = entry.getValue();
        if (count > maxCount) {
            inputMax = input;
            maxCount = count;
        }
        double percentage = (double) count / inputSize;
        votePercentage.put(input, percentage);
    }
    ```
    
    遍历 `inputCounts`，找出出现次数最多的SQL查询（`inputMax`），并计算每个SQL查询的出现次数占总数的百分比（`votePercentage`）。
    
4. **返回结果**
    
    ```java
    return Pair.of(inputMax, votePercentage);
    ```
    
    最后返回出现次数最多的SQL查询及每个SQL查询的投票百分比。
    

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2041.png)

这个方法用于对多个SQL查询候选进行投票，选择出现次数最多的SQL查询作为最终结果。具体步骤如下：

- **计数每个SQL查询的出现次数**：使用一个 `Map<String, Integer>` 来存储每个SQL查询的出现次数。
- **确定出现次数最多的SQL查询**：遍历 `inputCounts`，找出出现次数最多的SQL查询（`inputMax`）。
- **计算每个SQL查询的投票百分比**：计算每个SQL查询的出现次数占总数的百分比，并存储在 `votePercentage` 中。
- **返回结果**：返回出现次数最多的SQL查询及每个SQL查询的投票百分比。

**投票机制的实现**

- **投票的对象**：多个由大模型生成的SQL查询候选。
- **投票的过程**：通过统计每个SQL查询在候选列表中的出现次数，来确定最常出现的SQL查询。这个过程在 `selfConsistencyVote` 方法中实现。
- **投票的标准**：标准是SQL查询的出现次数，出现次数最多的SQL查询被认为是最可能正确的查询。

总结而言：就是简单粗暴选择出现最多的那个SQL查询语句

## 8.2 故障排查

### 编译bug修正

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2042.png)

impl改大写：`package com.tencent.supersonic.auth.authentication.persistence.repository.Impl;`

### 数据库连接bug修正

![Untitled](SuperSonic%20%E5%88%86%E6%9E%90%E6%96%87%E6%A1%A3%204c6b9ed87a8146b78a51419e54e7b612/Untitled%2043.png)

由于 MySQL 的连接配置中，`Public Key Retrieval is not allowed` 造成。该问题通常与 MySQL 8.0+ 版本中的新安全功能有关，需要进行以下配置调整：

解决方法：

1. **修改 JDBC URL**：
在 JDBC URL 中添加 `allowPublicKeyRetrieval=true` 参数。例如：
    
    ```yaml
    jdbc:mysql://localhost:3306/supersonic?useUnicode=true&characterEncoding=UTF-8&useSSL=false&allowMultiQueries=true&allowPublicKeyRetrieval=true
    
    ```
    
2. **修改 MySQL 配置**：
如果你有权限修改 MySQL 服务器配置，可以在 MySQL 配置文件（通常是 `my.cnf` 或 `my.ini`）中添加以下内容：
    
    ```
    caching_sha2_password=off
    ```
    

### 无影响-JWT报错

系统在尝试验证 JWT (JSON Web Token) 时遇到了令牌过期的问题。具体错误信息是 `io.jsonwebtoken.ExpiredJwtException: JWT expired`，这意味着当前时间已经超过了令牌的有效期。

**解决方法：**

1. **刷新令牌**：确保令牌在有效期内，可以通过刷新令牌来延长其有效期。
2. **增加时钟偏差**：在验证 JWT 时增加一个允许的时钟偏差 (clock skew)，这样可以允许一些时间偏差。如下是一个示例：
    
    ```java
    Jwts.parser()
        .setAllowedClockSkewSeconds(60)  // 允许60秒的时钟偏差
        .setSigningKey(secretKey)
        .parseClaimsJws(token);
    
    ```
    
3. **检查服务器时间**：确保服务器的系统时间是正确且同步的，避免因为服务器时间不准确导致的 JWT 过期错误。
4. **处理令牌过期的逻辑**：在应用中增加对令牌过期的处理逻辑，例如引导用户重新登录或者自动刷新令牌。

```java
try {
    Claims claims = Jwts.parser()
                        .setAllowedClockSkewSeconds(60)  // 允许60秒的时钟偏差
                        .setSigningKey(secretKey)
                        .parseClaimsJws(token)
                        .getBody();
    // 处理成功解析的令牌
} catch (ExpiredJwtException e) {
    // 处理令牌过期的情况，例如引导用户重新登录
    throw new CustomException("Token has expired", e);
}
```