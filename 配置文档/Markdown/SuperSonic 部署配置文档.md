# SuperSonic 部署配置文档

作者：罗天成 

日期：2024.08.15

# 1. 文档概述

## 1.1 目的

项目本身含有官方说明文档，其中包含在线体验、docker启动、本地配置启动等说明档案。但由于项目还在完善开发中，存在说明不够细致以及各种安装指引不明确等问题，因此撰写这份作为补充说明，便于后续开发安装配置。

## 1.2 官方文档

### 在线体验

[http://117.72.46.148:9080/](http://117.72.46.148:9080/)

### 配置安装

[快速体验](https://supersonicbi.github.io/docs/快速体验/)

# 2. 环境要求

## 2.1 硬件要求

任意windows和linux系统电脑均可，分别具有相应的配置脚本。

## 2.2 软件要求

### 相关库及语言

Java 8（验证可用） / 11

maven ≥ 3.8.0

node j's

npm

pnpm

### 其他配套

Docker ≥ 26.0.0

任意Java开发IDE（IDEA、VScode等）

任意数据库（Mysql 8.0/8.4等）

# 3. 安装步骤

以windows系统为例

## 3.1 docker启动

### 部署前提

下载安装Docker和Docker Compose，并启动docker

Docker版本：26.0.0+

Docker Compose：v2.26.1+

### 启动流程

1. 下载项目：`git clone [https://github.com/tencentmusic/supersonic.git](https://github.com/tencentmusic/supersonic.git)`
2. 启动服务：`docker-compose up -d`

> 注意：支持按照版本启动，不指定版本默认是：latest
> 
> 
> `SUPERSONIC_VERSION=0.9.2-SNAPSHOT docker-compose up -d`
> 
1. 查看容器：`docker-compose ps`
2. 等待启动完成直接浏览器进入：[http://localhost:9080](http://localhost:9080/) 
3. 查看进程日志信息：`docker exec -it supersonic_standalone bash`
4. 关闭服务：`docker-compose down`

## 3.2 本地IDE启动

### 修正错误（可能新版本已修复）

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled.png)

impl改大写：`package com.tencent.supersonic.auth.authentication.persistence.repository.Impl;`

### 启动流程

1. 下载项目：`git clone [https://github.com/tencentmusic/supersonic.git](https://github.com/tencentmusic/supersonic.git)`
2. 配置jdk以及maven必须：**`java1.8 + maven ≥ 3.8.0`**，参考IDE：IntelliJ IDEA （官方：后端编译需要JDK，推荐安装版本11）
3. 确保npm，nodejs保持最新即可，安装pnpm：`npm install -g pnpm` （官方：前端编译需要Node，推荐安装版本v20.16.0）
4. IDEA打开maven项目目录为根目录，等待识别project完成
5. `mvn clean install`  确保完成构建，大约2分钟
6. Windows：`.\assembly\bin\supersonic-build.bat webapp` 
    
    Linux：`sh assembly/bin/supersonic-build.sh webapp`
    
7. 检查是否构建完成 `.\assembly\build\supersonic-webapp.tar.gz`
8. **~~解压并移动生成的文件**：~~
    - ~~检查生成的 `supersonic-webapp.tar.gz` 文件：~~
        
        `~~ls assembly/build/supersonic-webapp.tar.gz~~`
        
    - ~~解压并移动文件到 `standalone/target/classes/` 目录下：~~
        
        `~~cd assembly/build
        tar xvf supersonic-webapp.tar.gz
        mv supersonic-webapp ../launchers/standalone/target/classes/~~`
        
    - ~~确认 `supersonic-webapp` 目录存在于 `standalone/target/classes/` 目录下：~~
        
        `~~ls ../launchers/standalone/target/classes/supersonic-webapp~~`
        
    - ~~也可以全程手动移动和检查，默认会在`standalone/target/classes/` 目录下创建webapp文件夹，内容基本一致但是无法后续启动~~
9. **运行 `StandaloneLauncher` 类**：
    
    IDE进入目录：
    
    `.\launchers\standalone\src\main\java\com\tencent\supersonic\StandaloneLauncher.java`
    
    - 在文件顶部，点击绿色的三角形按钮（`Run`）
    - 或者右键点击`StandaloneLauncher`类，然后选择`Run 'StandaloneLauncher.main()'`

10. 成功运行

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%201.png)

存在大模型接口设置问题，需要自行设置api，否则报错到达token上限（使用默认demo api仅1000 token长度限制）

1. 等待启动完成直接浏览器进入：[http://localhost:9080](http://localhost:9080/) 可以看到如下界面：

![image.png](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/image.png)

## 3.3 源代码编译包启动（未验证）

1. 下载相应版本[source code](https://github.com/tencentmusic/supersonic)
2. 执行编译脚本：`sh assembly/bin/supersonic-build.sh` 注：前端编译需要Node，推荐安装版本v20.16.0；后端编译需要JDK，推荐安装版本11
3. 编译完成后从`assembly/build`目录获取release包
4. 解压release包，`unzip supersonic-standalone-{revision}.zip`
5. 进行release目录，执行启动脚本`sh bin/supersonic-daemon.sh start`
6. 访问浏览器：[http://localhost:9080/](http://localhost:9080/)

# 4. 配置说明

## 4.1 数据库配置

项目默认使用H2内存数据库 ，直接启动即可，但是无法保存信息，重新启动记录消失，如需要保存前序操作内容，需要自行配置相关数据库保存数据。

### 官方说明

[配置DB](https://supersonicbi.github.io/docs/系统部署/配置db/)

### SQL脚本分析

[SQL脚本分析](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/SQL%E8%84%9A%E6%9C%AC%E5%88%86%E6%9E%90%20a71f321f83ba4dd3b1e1f2d3b112b2e4.md)

### 配置流程

以MySQL数据库为例：8.4LTS版本—8.0/5.7更优

1. 启动本地Mysql并链接
    - 链接数据库：`mysql -h 127.0.0.1 -uroot -proot`
    - 查看所有数据库：`show databases;`
    - 查看该数据库下的表：`show tables;`
2. `CREATE DATABASE supersonic CHARACTER SET utf8 COLLATE utf8_unicode_ci;`
3. `USE supersonic;`
4. `SOURCE your_path\supersonic\launchers\standalone\src\main\resources\db\schema-mysql.sql;`

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%202.png)

1. `SOURCE your_path\supersonic\launchers\standalone\src\main\resources\db\data-mysql.sql;`

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%203.png)

（存在部分数据导入问题，问题应为列长度不足，不影响整体数据暂保持不处理）

1. 配置YAML文件：将conf下`application-local.yaml`文件（`supersonic\launchers\standalone\src\main\resources\application-local.yaml`）默认的DB - H2配置, 替换为本地MySQL或其他在线数据库

```yaml
spring:
  datasource:
    driver-class-name: com.mysql.cj.jdbc.Driver
    url: jdbc:mysql://localhost:3306/supersonic?useUnicode=true&characterEncoding=UTF-8&useSSL=false&allowMultiQueries=true
    username: root
    password: root
  h2:
    console:
      path: /h2-console/semantic
      enabled: false
  config:
    import:
      - classpath:langchain4j-local.yaml
```

1. 进入网页设置Mysql服务器版本：

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%204.png)

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%205.png)

- 检查数据库配置是否正确并更改数据库版本为8.0：

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%206.png)

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%207.png)

### Mysql数据库链接成功：

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%208.png)

## 4.2 大模型配置

### 官方文档

非openai设置参考：https://supersonicbi.github.io/docs/系统部署/配置llm/

### 有哪些国内的大模型服务对接？

A: 当前我们验证过一些主流大模型服务，其申请链接如下表所示：

| 提供商 | API申请链接 | 推荐模型 |
| --- | --- | --- |
| 智谱AI | https://open.bigmodel.cn/api/paas/v4 | glm-4 |
| 阿里云 | https://dashscope.aliyuncs.com/compatible-mode/v1 | qwen-max |
| 幻方 | https://api.deepseek.com/ | deepseek-chat |
| 月之暗面 | https://api.moonshot.cn/v1 | moonshot-v1-8k |

### OpenAI模型配置参考

1. 创建OpenAI的api端口获取密钥：

[OpenAI Platform](https://platform.openai.com/api-keys)

1. 测试链接：`curl [https://api.openai.com/v1/models](https://api.openai.com/v1/models) -H "Authorization: Bearer your_api_key"`
2. 测试api返回：

```python
import openai

openai.api_key = "your_api_key"

response = openai.ChatCompletion.create(
  model="gpt-3.5-turbo",
  messages=[
      {"role": "system", "content": "You are a helpful assistant."},
      {"role": "user", "content": "Say this is a test"}
  ]
)

print(response.choices[0].message['content'])
```

1. 进入路径：`your_path\supersonic\launchers\standalone\src\main\resources\langchain4j-local.yaml`
2. 设置`langchain4j-local.yaml`

```yaml
langchain4j:
  # Replace `open_ai` with ollama/zhipu/azure/dashscope as needed.
  # Note:
  # 1. `open_ai` is commonly used to connect to cloud-based models;
  # 2. `ollama` is commonly used to connect to local models.
  open-ai:
    chat-model:
      # It is recommended to replace with your API key in production.
      # Note: The default API key `demo` is provided by langchain4j community
      #       which limits 1000 tokens per request.
#      base-url: ${OPENAI_API_BASE:https://api.openai.com/v1}
#      api-key: ${OPENAI_API_KEY:demo}
#      model-name: ${OPENAI_MODEL_NAME:gpt-3.5-turbo}
#      temperature: ${OPENAI_TEMPERATURE:0.0}
#      timeout: ${OPENAI_TIMEOUT:PT60S}

      base-url: ${OPENAI_API_BASE:https://api.openai.com/v1}
      api-key: ${OPENAI_API_KEY:your_api_key}
      model-name: ${OPENAI_MODEL_NAME:gpt-3.5-turbo}
      temperature: ${OPENAI_TEMPERATURE:0.0}
      timeout: ${OPENAI_TIMEOUT:PT60S}
```

1. 保存并启动supersonic，启动方式见前
2. 登录并按照如下顺序配置：

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%209.png)

## 4.3 数据集配置

系统自带默认数据集Supersonic/超音速，自行数据集配置参考官方文档

[SuperSonic](https://supersonicbi.github.io/docs/headless-bi/组装数据集/)

![image.png](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/image%201.png)

## 4.4 日志输出设置

默认使用INFO级别输出，会缺少大量中间信息输出，需要手动调整

### log4j日志设置

目录：`\supersonic\launchers\standalone\src\main\resources\logback-spring.xml`

`logback-spring.xml`是Logback配置文件的一种形式。如果您的项目使用的是Spring框架并且配置文件被命名为`logback-spring.xml`，那么它将由Spring Boot自动加载。

要增加日志的详细程度，将日志级别设置为`DEBUG`，可以按以下步骤进行：

### 修改 `logback-spring.xml` 文件

1. 将 `<root>` 元素中的 `level` 属性修改为 `DEBUG`。
2. 确保您感兴趣的 `logger` 元素也设置为 `DEBUG`。

以下是修改后的 `logback-spring.xml` 示例：

```xml
<?xml version="1.0" encoding="UTF-8"?>
<configuration scan="true">
    <contextName>logback</contextName>
    <!--    <property name="LOG_PATH" value="${logback.logdir:-logs}"/>-->
    <property name="LOG_PATH" value="${LOG_PATH:-logs}"/>
    <property name="LOG_APPNAME" value="chat"/>
    <!--输出到控制台-->
    <appender name="consoleLog" class="ch.qos.logback.core.ConsoleAppender">
        <encoder>
            <pattern>%d{HH:mm:ss} [%thread] %-5level %logger{36} %line - %msg%n</pattern>
        </encoder>
    </appender>

    <appender name="fileInfoLog" class="ch.qos.logback.core.rolling.RollingFileAppender">
        <File>${LOG_PATH}/info.${LOG_APPNAME}.log</File>
        <rollingPolicy class="ch.qos.logback.core.rolling.TimeBasedRollingPolicy">
            <FileNamePattern>${LOG_PATH}/info.${LOG_APPNAME}.%d{yyyy-MM-dd}.log.gz</FileNamePattern>
            <maxHistory>30</maxHistory>
        </rollingPolicy>
        <encoder>
            <charset>UTF-8</charset>
            <pattern>%d [%thread] %-5level [%X{traceId}] %logger{36} %line - %msg%n</pattern>
        </encoder>
    </appender>

    <appender name="fileErrorLog" class="ch.qos.logback.core.rolling.RollingFileAppender">
        <filter class="ch.qos.logback.classic.filter.ThresholdFilter">
            <level>ERROR</level>
        </filter>
        <File>${LOG_PATH}/error.${LOG_APPNAME}.log</File>
        <rollingPolicy class="ch.qos.logback.core.rolling.TimeBasedRollingPolicy">
            <FileNamePattern>${LOG_PATH}/error.${LOG_APPNAME}.%d{yyyy-MM-dd}.log.gz</FileNamePattern>
            <maxHistory>90</maxHistory>
        </rollingPolicy>
        <encoder>
            <charset>UTF-8</charset>
            <pattern>%d [%thread] %-5level [%X{traceId}] %logger{36} %line - %msg%n</pattern>
        </encoder>
    </appender>

    <appender name="serviceLog" class="ch.qos.logback.core.rolling.RollingFileAppender">
        <File>${LOG_PATH}/serviceinfo.${LOG_APPNAME}.log</File>
        <rollingPolicy class="ch.qos.logback.core.rolling.TimeBasedRollingPolicy">
            <FileNamePattern>${LOG_PATH}/serviceinfo.${LOG_APPNAME}.%d{yyyy-MM-dd}.log.gz</FileNamePattern>
            <maxHistory>30</maxHistory>
        </rollingPolicy>
        <encoder>
            <charset>UTF-8</charset>
            <pattern>%d [%thread] %-5level [%X{traceId}] %logger{36} %line - %msg%n</pattern>
        </encoder>
    </appender>

    <logger name="com.tencent.supersonic" level="DEBUG" additivity="true">
        <appender-ref ref="serviceLog"/>
    </logger>

    <!-- 业务日志输出 -->
    <appender name="keyPipelineAppender" class="ch.qos.logback.core.rolling.RollingFileAppender">
        <File>${LOG_PATH}/keyPipeline.log</File>
        <rollingPolicy class="ch.qos.logback.core.rolling.TimeBasedRollingPolicy">
            <fileNamePattern>${LOG_PATH}/keyPipeline.%d{yyyy-MM-dd}.log</fileNamePattern>
            <maxHistory>30</maxHistory>
            <cleanHistoryOnStart>true</cleanHistoryOnStart>
        </rollingPolicy>
        <encoder>
            <charset>UTF-8</charset>
            <pattern>%d [%thread] %-5level [%X{traceId}] %logger{36} %line - %msg%n</pattern>
        </encoder>
         <!--<filter class="ch.qos.logback.classic.filter.LevelFilter">-->
             <!--<level>DEBUG</level>-->
         <!--</filter>-->
    </appender>
    <!--keyPipeline相关日志-->
    <logger name="keyPipeline" level="DEBUG" additivity="false">
        <appender-ref ref="keyPipelineAppender"/>
    </logger>

    <root level="DEBUG">
        <appender-ref ref="fileInfoLog"/>
        <appender-ref ref="fileErrorLog"/>
        <appender-ref ref="consoleLog"/>
    </root>
</configuration>
```

### 解释

全部更改为DEBUG级别

### 重新启动项目

完成配置修改后，重新编译并启动您的项目，查看控制台输出和日志文件，确认日志级别设置已生效。

### 验证日志输出

确认您在控制台和日志文件中可以看到 `DEBUG` 级别的日志消息，包括之前无法看到的`"before handleNoMetric, sql:{}"`和`"after handleNoMetric, sql:{}"`日志输出。

# 5. 验证与测试

## 5.1 数据库测试

入网页设置Mysql服务器版本：

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%204.png)

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%205.png)

- 检查数据库配置是否正确并更改数据库版本为8.0：

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%206.png)

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%207.png)

以及直接控制台代码测试数据库内容

- 链接数据库：`mysql -h 127.0.0.1 -uroot -proot`
- 查看所有数据库：`show databases;`
- 查看该数据库下的表：`show tables;` 等

## 5.2 大模型测试

控制台测试/新调试创建接口：

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%2010.png)

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%2011.png)

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%2012.png)

测试代码及结果：

```python
import openai

openai.api_key = "YOUR_API_KEY"

response = openai.ChatCompletion.create(
  model="gpt-3.5-turbo",
  messages=[
    {"role": "system", "content": "You are a helpful assistant."},
    {"role": "user", "content": "Say this is a test"}
  ]
)

print(response.choices[0].message['content'])

# response = openai.Model.list()
# print(response)
```

![Untitled](SuperSonic%20%E9%83%A8%E7%BD%B2%E9%85%8D%E7%BD%AE%E6%96%87%E6%A1%A3%205afa1b32eefc42a997a00a5c93c2ff39/Untitled%2013.png)

LLM配置使用说明：

[SuperSonic](https://supersonicbi.github.io/docs/chat-bi/配置助理/)

最终直接进行“来闲聊”模块对话即可验证是否连接成功。

# 6. 相关资料

[Docker部署](https://supersonicbi.github.io/docs/系统部署/docker部署/)

[https://github.com/tencentmusic/supersonic/blob/master/README_CN.md](https://github.com/tencentmusic/supersonic/blob/master/README_CN.md)

[](https://www.jianshu.com/p/c51d92a9f91d)

[windows安装npm教程_npm 安装-CSDN博客](https://blog.csdn.net/zhouyan8603/article/details/109039732)

[下载 | Node.js 中文网](https://nodejs.cn/download/)

[pnpm 基本详细使用教程（安装、卸载、使用、可能遇到的问题及解决办法）-CSDN博客](https://blog.csdn.net/m0_56416743/article/details/136122153)