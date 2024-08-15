---
title: SuperSonic API文档
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
code_clipboard: true
highlight_theme: darkula
headingLevel: 2
generator: "@tarslib/widdershins v4.0.23"

---

# SuperSonic API文档
# 罗天成 2024.08.15

Base URLs:

# Authentication

# agent-controller

<a id="opIdupdateAgentUsingPUT"></a>

## PUT updateAgent

PUT /api/chat/agent

> Body 请求参数

```json
{
  "agentConfig": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "enableSearch": 0,
  "examples": [
    "string"
  ],
  "id": 0,
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "multiTurnConfig": {
    "enableMultiTurn": true
  },
  "name": "string",
  "status": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "visualConfig": {
    "enableSimpleMode": true,
    "showDebugInfo": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[AgentReq](#schemaagentreq)| 否 | AgentReq|none|

> 返回示例

> 200 Response

```json
{
  "agentConfig": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetIds": [
    0
  ],
  "description": "string",
  "enableSearch": 0,
  "examples": [
    "string"
  ],
  "id": 0,
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "multiTurnConfig": {
    "enableMultiTurn": true
  },
  "name": "string",
  "status": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "visualConfig": {
    "enableSimpleMode": true,
    "showDebugInfo": true
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[AgentRes](#schemaagentres)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdcreateAgentUsingPOST"></a>

## POST createAgent

POST /api/chat/agent

> Body 请求参数

```json
{
  "agentConfig": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "enableSearch": 0,
  "examples": [
    "string"
  ],
  "id": 0,
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "multiTurnConfig": {
    "enableMultiTurn": true
  },
  "name": "string",
  "status": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "visualConfig": {
    "enableSimpleMode": true,
    "showDebugInfo": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[AgentReq](#schemaagentreq)| 否 | AgentReq|none|

> 返回示例

> 200 Response

```json
{
  "agentConfig": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetIds": [
    0
  ],
  "description": "string",
  "enableSearch": 0,
  "examples": [
    "string"
  ],
  "id": 0,
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "multiTurnConfig": {
    "enableMultiTurn": true
  },
  "name": "string",
  "status": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "visualConfig": {
    "enableSimpleMode": true,
    "showDebugInfo": true
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[AgentRes](#schemaagentres)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetAgentListUsingGET"></a>

## GET getAgentList

GET /api/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetAgentListUsingPUT"></a>

## PUT getAgentList

PUT /api/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetAgentListUsingPOST"></a>

## POST getAgentList

POST /api/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetAgentListUsingDELETE"></a>

## DELETE getAgentList

DELETE /api/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetAgentListUsingOPTIONS"></a>

## OPTIONS getAgentList

OPTIONS /api/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetAgentListUsingHEAD"></a>

## HEAD getAgentList

HEAD /api/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetAgentListUsingPATCH"></a>

## PATCH getAgentList

PATCH /api/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetAgentListUsingTRACE"></a>

## TRACE getAgentList

TRACE /api/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetToolTypesUsingGET"></a>

## GET getToolTypes

GET /api/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdgetToolTypesUsingPUT"></a>

## PUT getToolTypes

PUT /api/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdgetToolTypesUsingPOST"></a>

## POST getToolTypes

POST /api/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdgetToolTypesUsingDELETE"></a>

## DELETE getToolTypes

DELETE /api/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdgetToolTypesUsingOPTIONS"></a>

## OPTIONS getToolTypes

OPTIONS /api/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdgetToolTypesUsingHEAD"></a>

## HEAD getToolTypes

HEAD /api/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdgetToolTypesUsingPATCH"></a>

## PATCH getToolTypes

PATCH /api/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdgetToolTypesUsingTRACE"></a>

## TRACE getToolTypes

TRACE /api/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdtestLLMConnUsingPOST"></a>

## POST testLLMConn

POST /api/chat/agent/testLLMConn

> Body 请求参数

```json
{
  "apiKey": "string",
  "baseUrl": "string",
  "modelName": "string",
  "provider": "string",
  "temperature": 0,
  "timeOut": 0
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[LLMConfig](#schemallmconfig)| 否 | LLMConfig|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteAgentUsingDELETE"></a>

## DELETE deleteAgent

DELETE /api/chat/agent/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int32)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdupdateAgentUsingPUT_1"></a>

## PUT updateAgent

PUT /openapi/chat/agent

> Body 请求参数

```json
{
  "agentConfig": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "enableSearch": 0,
  "examples": [
    "string"
  ],
  "id": 0,
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "multiTurnConfig": {
    "enableMultiTurn": true
  },
  "name": "string",
  "status": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "visualConfig": {
    "enableSimpleMode": true,
    "showDebugInfo": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[AgentReq](#schemaagentreq)| 否 | AgentReq|none|

> 返回示例

> 200 Response

```json
{
  "agentConfig": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetIds": [
    0
  ],
  "description": "string",
  "enableSearch": 0,
  "examples": [
    "string"
  ],
  "id": 0,
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "multiTurnConfig": {
    "enableMultiTurn": true
  },
  "name": "string",
  "status": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "visualConfig": {
    "enableSimpleMode": true,
    "showDebugInfo": true
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[AgentRes](#schemaagentres)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdcreateAgentUsingPOST_1"></a>

## POST createAgent

POST /openapi/chat/agent

> Body 请求参数

```json
{
  "agentConfig": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "enableSearch": 0,
  "examples": [
    "string"
  ],
  "id": 0,
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "multiTurnConfig": {
    "enableMultiTurn": true
  },
  "name": "string",
  "status": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "visualConfig": {
    "enableSimpleMode": true,
    "showDebugInfo": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[AgentReq](#schemaagentreq)| 否 | AgentReq|none|

> 返回示例

> 200 Response

```json
{
  "agentConfig": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetIds": [
    0
  ],
  "description": "string",
  "enableSearch": 0,
  "examples": [
    "string"
  ],
  "id": 0,
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "multiTurnConfig": {
    "enableMultiTurn": true
  },
  "name": "string",
  "status": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "visualConfig": {
    "enableSimpleMode": true,
    "showDebugInfo": true
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[AgentRes](#schemaagentres)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetAgentListUsingGET_1"></a>

## GET getAgentList

GET /openapi/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetAgentListUsingPUT_1"></a>

## PUT getAgentList

PUT /openapi/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetAgentListUsingPOST_1"></a>

## POST getAgentList

POST /openapi/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetAgentListUsingDELETE_1"></a>

## DELETE getAgentList

DELETE /openapi/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetAgentListUsingOPTIONS_1"></a>

## OPTIONS getAgentList

OPTIONS /openapi/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetAgentListUsingHEAD_1"></a>

## HEAD getAgentList

HEAD /openapi/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetAgentListUsingPATCH_1"></a>

## PATCH getAgentList

PATCH /openapi/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetAgentListUsingTRACE_1"></a>

## TRACE getAgentList

TRACE /openapi/chat/agent/getAgentList

> 返回示例

> 200 Response

```json
[
  {
    "agentConfig": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetIds": [
      0
    ],
    "description": "string",
    "enableSearch": 0,
    "examples": [
      "string"
    ],
    "id": 0,
    "llmConfig": {
      "apiKey": "string",
      "baseUrl": "string",
      "modelName": "string",
      "provider": "string",
      "temperature": 0,
      "timeOut": 0
    },
    "multiTurnConfig": {
      "enableMultiTurn": true
    },
    "name": "string",
    "status": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "visualConfig": {
      "enableSimpleMode": true,
      "showDebugInfo": true
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AgentRes](#schemaagentres)]|false|none||none|
|» AgentRes|[AgentRes](#schemaagentres)|false|none|AgentRes|none|
|»» agentConfig|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetIds|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» enableSearch|integer(int32)|false|none||none|
|»» examples|[string]|false|none||none|
|»» id|integer(int32)|false|none||none|
|»» llmConfig|[LLMConfig](#schemallmconfig)|false|none|LLMConfig|none|
|»»» apiKey|string|false|none||none|
|»»» baseUrl|string|false|none||none|
|»»» modelName|string|false|none||none|
|»»» provider|string|false|none||none|
|»»» temperature|number(double)|false|none||none|
|»»» timeOut|integer(int64)|false|none||none|
|»» multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none|MultiTurnConfig|none|
|»»» enableMultiTurn|boolean|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» visualConfig|[VisualConfig](#schemavisualconfig)|false|none|VisualConfig|none|
|»»» enableSimpleMode|boolean|false|none||none|
|»»» showDebugInfo|boolean|false|none||none|

<a id="opIdgetToolTypesUsingGET_1"></a>

## GET getToolTypes

GET /openapi/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdgetToolTypesUsingPUT_1"></a>

## PUT getToolTypes

PUT /openapi/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdgetToolTypesUsingPOST_1"></a>

## POST getToolTypes

POST /openapi/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdgetToolTypesUsingDELETE_1"></a>

## DELETE getToolTypes

DELETE /openapi/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdgetToolTypesUsingOPTIONS_1"></a>

## OPTIONS getToolTypes

OPTIONS /openapi/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdgetToolTypesUsingHEAD_1"></a>

## HEAD getToolTypes

HEAD /openapi/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdgetToolTypesUsingPATCH_1"></a>

## PATCH getToolTypes

PATCH /openapi/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdgetToolTypesUsingTRACE_1"></a>

## TRACE getToolTypes

TRACE /openapi/chat/agent/getToolTypes

> 返回示例

> 200 Response

```json
{
  "property1": "string",
  "property2": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|string|false|none||none|

<a id="opIdtestLLMConnUsingPOST_1"></a>

## POST testLLMConn

POST /openapi/chat/agent/testLLMConn

> Body 请求参数

```json
{
  "apiKey": "string",
  "baseUrl": "string",
  "modelName": "string",
  "provider": "string",
  "temperature": 0,
  "timeOut": 0
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[LLMConfig](#schemallmconfig)| 否 | LLMConfig|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteAgentUsingDELETE_1"></a>

## DELETE deleteAgent

DELETE /openapi/chat/agent/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int32)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

# app-controller

<a id="opIdupdateUsingPUT"></a>

## PUT update

PUT /api/semantic/app

> Body 请求参数

```json
{
  "config": {
    "items": [
      {
        "bizName": "string",
        "createdBy": "string",
        "id": 0,
        "name": "string",
        "relateItems": [
          {
            "bizName": null,
            "createdBy": null,
            "id": null,
            "name": null,
            "relateItems": null,
            "type": null
          }
        ],
        "type": "DIMENSION"
      }
    ]
  },
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "endDate": "2019-08-24T14:15:22Z",
  "id": 0,
  "name": "string",
  "owners": [
    "string"
  ],
  "qps": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[AppReq](#schemaappreq)| 否 | AppReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdsaveUsingPOST"></a>

## POST save

POST /api/semantic/app

> Body 请求参数

```json
{
  "config": {
    "items": [
      {
        "bizName": "string",
        "createdBy": "string",
        "id": 0,
        "name": "string",
        "relateItems": [
          {
            "bizName": null,
            "createdBy": null,
            "id": null,
            "name": null,
            "relateItems": null,
            "type": null
          }
        ],
        "type": "DIMENSION"
      }
    ]
  },
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "endDate": "2019-08-24T14:15:22Z",
  "id": 0,
  "name": "string",
  "owners": [
    "string"
  ],
  "qps": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[AppReq](#schemaappreq)| 否 | AppReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdofflineUsingPUT"></a>

## PUT offline

PUT /api/semantic/app/offline/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int32)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdonlineUsingPUT"></a>

## PUT online

PUT /api/semantic/app/online/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int32)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdpageAppUsingPOST"></a>

## POST pageApp

POST /api/semantic/app/page

> Body 请求参数

```json
{
  "appStatus": [
    "DELETED"
  ],
  "createdBy": "string",
  "current": 0,
  "name": "string",
  "orderCondition": "string",
  "pageSize": 0,
  "sort": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[AppQueryReq](#schemaappqueryreq)| 否 | AppQueryReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "appStatus": "DELETED",
      "config": {
        "items": [
          {
            "bizName": "string",
            "createdBy": "string",
            "id": 0,
            "name": "string",
            "relateItems": [
              {
                "bizName": "string",
                "createdBy": "string",
                "id": 0,
                "name": "string",
                "relateItems": [],
                "type": "DIMENSION",
                "value": "string"
              }
            ],
            "type": "DIMENSION",
            "value": "string"
          }
        ]
      },
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "description": "string",
      "endDate": "2019-08-24T14:15:22Z",
      "hasAdminRes": true,
      "id": 0,
      "name": "string",
      "owners": [
        "string"
      ],
      "qps": 0,
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetAppUsingGET"></a>

## GET getApp

GET /api/semantic/app/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int32)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "appSecret": "string",
  "appStatus": "DELETED",
  "config": {
    "items": [
      {
        "bizName": "string",
        "createdBy": "string",
        "id": 0,
        "name": "string",
        "relateItems": [
          {
            "bizName": null,
            "createdBy": null,
            "id": null,
            "name": null,
            "relateItems": null,
            "type": null,
            "value": null
          }
        ],
        "type": "DIMENSION",
        "value": "string"
      }
    ]
  },
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "endDate": "2019-08-24T14:15:22Z",
  "hasAdminRes": true,
  "id": 0,
  "name": "string",
  "owners": [
    "string"
  ],
  "qps": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[AppDetailResp](#schemaappdetailresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteUsingDELETE"></a>

## DELETE delete

DELETE /api/semantic/app/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int32)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

# auth-controller

<a id="opIdnewAuthGroupUsingPOST"></a>

## POST newAuthGroup

POST /api/auth/createGroup

> Body 请求参数

```json
{
  "authRules": [
    {
      "description": "string",
      "dimensions": [
        "string"
      ],
      "metrics": [
        "string"
      ],
      "name": "string"
    }
  ],
  "authorizedDepartmentIds": [
    "string"
  ],
  "authorizedUsers": [
    "string"
  ],
  "dimensionFilterDescription": "string",
  "dimensionFilters": [
    "string"
  ],
  "groupId": 0,
  "modelId": 0,
  "name": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[AuthGroup](#schemaauthgroup)| 否 | AuthGroup|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryAuthorizedResourcesUsingPOST"></a>

## POST queryAuthorizedResources

POST /api/auth/queryAuthorizedRes

> Body 请求参数

```json
{
  "departmentIds": [
    "string"
  ],
  "modelId": 0,
  "modelIds": [
    0
  ],
  "resources": [
    {
      "modelId": 0,
      "name": "string"
    }
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QueryAuthResReq](#schemaqueryauthresreq)| 否 | QueryAuthResReq|none|

> 返回示例

> 200 Response

```json
{
  "filters": [
    {
      "description": "string",
      "expressions": [
        "string"
      ]
    }
  ],
  "resources": [
    {
      "group": [
        {
          "modelId": 0,
          "name": "string"
        }
      ]
    }
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[AuthorizedResourceResp](#schemaauthorizedresourceresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryAuthGroupUsingGET"></a>

## GET queryAuthGroup

GET /api/auth/queryGroup

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|modelId|query|string| 是 ||modelId|
|groupId|query|integer(int32)| 否 ||groupId|

> 返回示例

> 200 Response

```json
[
  {
    "authRules": [
      {
        "description": "string",
        "dimensions": [
          "string"
        ],
        "metrics": [
          "string"
        ],
        "name": "string"
      }
    ],
    "authorizedDepartmentIds": [
      "string"
    ],
    "authorizedUsers": [
      "string"
    ],
    "dimensionFilterDescription": "string",
    "dimensionFilters": [
      "string"
    ],
    "groupId": 0,
    "modelId": 0,
    "name": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[AuthGroup](#schemaauthgroup)]|false|none||none|
|» AuthGroup|[AuthGroup](#schemaauthgroup)|false|none|AuthGroup|none|
|»» authRules|[[AuthRule](#schemaauthrule)]|false|none||none|
|»»» AuthRule|[AuthRule](#schemaauthrule)|false|none|AuthRule|none|
|»»»» description|string|false|none||none|
|»»»» dimensions|[string]|false|none||none|
|»»»» metrics|[string]|false|none||none|
|»»»» name|string|false|none||none|
|»» authorizedDepartmentIds|[string]|false|none||none|
|»» authorizedUsers|[string]|false|none||none|
|»» dimensionFilterDescription|string|false|none||none|
|»» dimensionFilters|[string]|false|none||none|
|»» groupId|integer(int32)|false|none||none|
|»» modelId|integer(int64)|false|none||none|
|»» name|string|false|none||none|

<a id="opIdremoveAuthGroupUsingPOST"></a>

## POST removeAuthGroup

POST /api/auth/removeGroup

> Body 请求参数

```json
{
  "authRules": [
    {
      "description": "string",
      "dimensions": [
        "string"
      ],
      "metrics": [
        "string"
      ],
      "name": "string"
    }
  ],
  "authorizedDepartmentIds": [
    "string"
  ],
  "authorizedUsers": [
    "string"
  ],
  "dimensionFilterDescription": "string",
  "dimensionFilters": [
    "string"
  ],
  "groupId": 0,
  "modelId": 0,
  "name": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[AuthGroup](#schemaauthgroup)| 否 | AuthGroup|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdupdateAuthGroupUsingPOST"></a>

## POST updateAuthGroup

POST /api/auth/updateGroup

> Body 请求参数

```json
{
  "authRules": [
    {
      "description": "string",
      "dimensions": [
        "string"
      ],
      "metrics": [
        "string"
      ],
      "name": "string"
    }
  ],
  "authorizedDepartmentIds": [
    "string"
  ],
  "authorizedUsers": [
    "string"
  ],
  "dimensionFilterDescription": "string",
  "dimensionFilters": [
    "string"
  ],
  "groupId": 0,
  "modelId": 0,
  "name": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[AuthGroup](#schemaauthgroup)| 否 | AuthGroup|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# canvas-controller

<a id="opIdcreateOrUpdateCanvasUsingPOST"></a>

## POST createOrUpdateCanvas

POST /api/semantic/viewInfo/createOrUpdateViewInfo

> Body 请求参数

```json
{
  "config": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "domainId": 0,
  "id": 0,
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[CanvasReq](#schemacanvasreq)| 否 | CanvasReq|none|

> 返回示例

> 200 Response

```json
{
  "config": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "domainId": 0,
  "id": 0,
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[CanvasDO](#schemacanvasdo)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteCanvasUsingDELETE"></a>

## DELETE deleteCanvas

DELETE /api/semantic/viewInfo/deleteViewInfo/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetDomainSchemaUsingGET"></a>

## GET getDomainSchema

GET /api/semantic/viewInfo/getDomainSchemaRela/{domainId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|path|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
[
  {
    "dimensions": [
      {
        "alias": "string",
        "bizName": "string",
        "createdAt": "2019-08-24T14:15:22Z",
        "createdBy": "string",
        "dataType": "ARRAY",
        "defaultValues": [
          "string"
        ],
        "description": "string",
        "dimValueMaps": [
          {
            "alias": [
              null
            ],
            "bizName": "string",
            "techName": "string"
          }
        ],
        "expr": "string",
        "ext": {},
        "id": 0,
        "isTag": 0,
        "modelBizName": "string",
        "modelFilterSql": "string",
        "modelId": 0,
        "modelName": "string",
        "name": "string",
        "semanticType": "string",
        "sensitiveLevel": 0,
        "status": 0,
        "type": "string",
        "typeEnum": "DATASET",
        "updatedAt": "2019-08-24T14:15:22Z",
        "updatedBy": "string"
      }
    ],
    "domainId": 0,
    "metrics": [
      {
        "alias": "string",
        "bizName": "string",
        "classifications": [
          "string"
        ],
        "createdAt": "2019-08-24T14:15:22Z",
        "createdBy": "string",
        "dataFormat": {
          "decimalPlaces": 0,
          "needMultiply100": true
        },
        "dataFormatType": "string",
        "defaultAgg": "string",
        "description": "string",
        "domainId": 0,
        "drillDownDimensions": [
          {
            "dimensionId": 0,
            "inheritedFromModel": true,
            "necessary": true
          }
        ],
        "expr": "string",
        "ext": {},
        "hasAdminRes": true,
        "id": 0,
        "isCollect": true,
        "isPublish": 0,
        "isTag": 0,
        "metricDefineByFieldParams": {
          "expr": "string",
          "fields": [
            {}
          ],
          "filterSql": "string"
        },
        "metricDefineByMeasureParams": {
          "expr": "string",
          "filterSql": "string",
          "measures": [
            {}
          ]
        },
        "metricDefineByMetricParams": {
          "expr": "string",
          "filterSql": "string",
          "metrics": [
            {}
          ]
        },
        "metricDefineType": "FIELD",
        "modelBizName": "string",
        "modelId": 0,
        "modelName": "string",
        "name": "string",
        "relaDimensionIdKey": "string",
        "relateDimension": {
          "drillDownDimensions": [
            {}
          ]
        },
        "sensitiveLevel": 0,
        "similarity": 0,
        "status": 0,
        "type": "string",
        "typeEnum": "DATASET",
        "updatedAt": "2019-08-24T14:15:22Z",
        "updatedBy": "string"
      }
    ],
    "model": {
      "adminOrgs": [
        "string"
      ],
      "admins": [
        "string"
      ],
      "alias": "string",
      "bizName": "string",
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "databaseId": 0,
      "depends": "string",
      "description": "string",
      "domainId": 0,
      "drillDownDimensions": [
        {
          "dimensionId": 0,
          "inheritedFromModel": true,
          "necessary": true
        }
      ],
      "ext": {},
      "fieldList": [
        "string"
      ],
      "filterSql": "string",
      "fullPath": "string",
      "id": 0,
      "isOpen": 0,
      "modelDetail": {
        "dimensions": [
          {
            "bizName": null,
            "dateFormat": null,
            "description": null,
            "expr": null,
            "fieldName": null,
            "isCreateDimension": null,
            "isTag": null,
            "name": null,
            "type": null,
            "typeParams": null
          }
        ],
        "fields": [
          {
            "dataType": null,
            "fieldName": null
          }
        ],
        "identifiers": [
          {
            "bizName": null,
            "entityNames": null,
            "fieldName": null,
            "isCreateDimension": null,
            "name": null,
            "type": null
          }
        ],
        "measures": [
          {
            "agg": null,
            "alias": null,
            "bizName": null,
            "constraint": null,
            "expr": null,
            "fieldName": null,
            "isCreateMetric": null,
            "name": null
          }
        ],
        "queryType": "string",
        "sqlQuery": "string",
        "sqlVariables": [
          {
            "defaultValues": null,
            "name": null,
            "valueType": null
          }
        ],
        "tableQuery": "string"
      },
      "name": "string",
      "primaryIdentify": {
        "bizName": "string",
        "entityNames": [
          "string"
        ],
        "fieldName": "string",
        "isCreateDimension": 0,
        "name": "string",
        "type": "string"
      },
      "sensitiveLevel": 0,
      "status": 0,
      "tagObjectId": 0,
      "timeDimension": [
        {
          "bizName": "string",
          "dateFormat": "string",
          "description": "string",
          "expr": "string",
          "fieldName": "string",
          "isCreateDimension": 0,
          "isTag": 0,
          "name": "string",
          "type": "string",
          "typeParams": {
            "isPrimary": null,
            "timeGranularity": null
          }
        }
      ],
      "typeEnum": "DATASET",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string",
      "viewOrgs": [
        "string"
      ],
      "viewers": [
        "string"
      ]
    }
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[CanvasSchemaResp](#schemacanvasschemaresp)]|false|none||none|
|» CanvasSchemaResp|[CanvasSchemaResp](#schemacanvasschemaresp)|false|none|CanvasSchemaResp|none|
|»» dimensions|[[DimensionResp](#schemadimensionresp)]|false|none||none|
|»»» DimensionResp|[DimensionResp](#schemadimensionresp)|false|none|DimensionResp|none|
|»»»» alias|string|false|none||none|
|»»»» bizName|string|false|none||none|
|»»»» createdAt|string(date-time)|false|none||none|
|»»»» createdBy|string|false|none||none|
|»»»» dataType|string|false|none||none|
|»»»» defaultValues|[string]|false|none||none|
|»»»» description|string|false|none||none|
|»»»» dimValueMaps|[[DimValueMap](#schemadimvaluemap)]|false|none||none|
|»»»»» DimValueMap|[DimValueMap](#schemadimvaluemap)|false|none|DimValueMap|none|
|»»»»»» alias|[string]|false|none||none|
|»»»»»» bizName|string|false|none||none|
|»»»»»» techName|string|false|none||none|
|»»»» expr|string|false|none||none|
|»»»» ext|object|false|none||none|
|»»»» id|integer(int64)|false|none||none|
|»»»» isTag|integer(int32)|false|none||none|
|»»»» modelBizName|string|false|none||none|
|»»»» modelFilterSql|string|false|none||none|
|»»»» modelId|integer(int64)|false|none||none|
|»»»» modelName|string|false|none||none|
|»»»» name|string|false|none||none|
|»»»» semanticType|string|false|none||none|
|»»»» sensitiveLevel|integer(int32)|false|none||none|
|»»»» status|integer(int32)|false|none||none|
|»»»» type|string|false|none||none|
|»»»» typeEnum|string|false|none||none|
|»»»» updatedAt|string(date-time)|false|none||none|
|»»»» updatedBy|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» metrics|[[MetricResp](#schemametricresp)]|false|none||none|
|»»» MetricResp|[MetricResp](#schemametricresp)|false|none|MetricResp|none|
|»»»» alias|string|false|none||none|
|»»»» bizName|string|false|none||none|
|»»»» classifications|[string]|false|none||none|
|»»»» createdAt|string(date-time)|false|none||none|
|»»»» createdBy|string|false|none||none|
|»»»» dataFormat|[DataFormat](#schemadataformat)|false|none|DataFormat|none|
|»»»»» decimalPlaces|integer(int32)|false|none||none|
|»»»»» needMultiply100|boolean|false|none||none|
|»»»» dataFormatType|string|false|none||none|
|»»»» defaultAgg|string|false|none||none|
|»»»» description|string|false|none||none|
|»»»» domainId|integer(int64)|false|none||none|
|»»»» drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|»»»»» DrillDownDimension|[DrillDownDimension](#schemadrilldowndimension)|false|none|DrillDownDimension|none|
|»»»»»» dimensionId|integer(int64)|false|none||none|
|»»»»»» inheritedFromModel|boolean|false|none||none|
|»»»»»» necessary|boolean|false|none||none|
|»»»» expr|string|false|none||none|
|»»»» ext|object|false|none||none|
|»»»» hasAdminRes|boolean|false|none||none|
|»»»» id|integer(int64)|false|none||none|
|»»»» isCollect|boolean|false|none||none|
|»»»» isPublish|integer(int32)|false|none||none|
|»»»» isTag|integer(int32)|false|none||none|
|»»»» metricDefineByFieldParams|[MetricDefineByFieldParams](#schemametricdefinebyfieldparams)|false|none|MetricDefineByFieldParams|none|
|»»»»» expr|string|false|none||none|
|»»»»» fields|[[FieldParam](#schemafieldparam)]|false|none||none|
|»»»»»» FieldParam|[FieldParam](#schemafieldparam)|false|none|FieldParam|none|
|»»»»»»» fieldName|string|false|none||none|
|»»»»» filterSql|string|false|none||none|
|»»»» metricDefineByMeasureParams|[MetricDefineByMeasureParams](#schemametricdefinebymeasureparams)|false|none|MetricDefineByMeasureParams|none|
|»»»»» expr|string|false|none||none|
|»»»»» filterSql|string|false|none||none|
|»»»»» measures|[[MeasureParam](#schemameasureparam)]|false|none||none|
|»»»»»» MeasureParam|[MeasureParam](#schemameasureparam)|false|none|MeasureParam|none|
|»»»»»»» agg|string|false|none||none|
|»»»»»»» bizName|string|false|none||none|
|»»»»»»» constraint|string|false|none||none|
|»»»» metricDefineByMetricParams|[MetricDefineByMetricParams](#schemametricdefinebymetricparams)|false|none|MetricDefineByMetricParams|none|
|»»»»» expr|string|false|none||none|
|»»»»» filterSql|string|false|none||none|
|»»»»» metrics|[[MetricParam](#schemametricparam)]|false|none||none|
|»»»»»» MetricParam|[MetricParam](#schemametricparam)|false|none|MetricParam|none|
|»»»»»»» bizName|string|false|none||none|
|»»»»»»» id|integer(int64)|false|none||none|
|»»»» metricDefineType|string|false|none||none|
|»»»» modelBizName|string|false|none||none|
|»»»» modelId|integer(int64)|false|none||none|
|»»»» modelName|string|false|none||none|
|»»»» name|string|false|none||none|
|»»»» relaDimensionIdKey|string|false|none||none|
|»»»» relateDimension|[RelateDimension](#schemarelatedimension)|false|none|RelateDimension|none|
|»»»»» drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|»»»»»» DrillDownDimension|[DrillDownDimension](#schemadrilldowndimension)|false|none|DrillDownDimension|none|
|»»»»»»» dimensionId|integer(int64)|false|none||none|
|»»»»»»» inheritedFromModel|boolean|false|none||none|
|»»»»»»» necessary|boolean|false|none||none|
|»»»» sensitiveLevel|integer(int32)|false|none||none|
|»»»» similarity|number(double)|false|none||none|
|»»»» status|integer(int32)|false|none||none|
|»»»» type|string|false|none||none|
|»»»» typeEnum|string|false|none||none|
|»»»» updatedAt|string(date-time)|false|none||none|
|»»»» updatedBy|string|false|none||none|
|»» model|[ModelResp](#schemamodelresp)|false|none|ModelResp|none|
|»»» adminOrgs|[string]|false|none||none|
|»»» admins|[string]|false|none||none|
|»»» alias|string|false|none||none|
|»»» bizName|string|false|none||none|
|»»» createdAt|string(date-time)|false|none||none|
|»»» createdBy|string|false|none||none|
|»»» databaseId|integer(int64)|false|none||none|
|»»» depends|string|false|none||none|
|»»» description|string|false|none||none|
|»»» domainId|integer(int64)|false|none||none|
|»»» drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|»»»» DrillDownDimension|[DrillDownDimension](#schemadrilldowndimension)|false|none|DrillDownDimension|none|
|»»»»» dimensionId|integer(int64)|false|none||none|
|»»»»» inheritedFromModel|boolean|false|none||none|
|»»»»» necessary|boolean|false|none||none|
|»»» ext|object|false|none||none|
|»»» fieldList|[string]|false|none||none|
|»»» filterSql|string|false|none||none|
|»»» fullPath|string|false|none||none|
|»»» id|integer(int64)|false|none||none|
|»»» isOpen|integer(int32)|false|none||none|
|»»» modelDetail|[ModelDetail](#schemamodeldetail)|false|none|ModelDetail|none|
|»»»» dimensions|[[Dim](#schemadim)]|false|none||none|
|»»»»» Dim|[Dim](#schemadim)|false|none|Dim|none|
|»»»»»» bizName|string|false|none||none|
|»»»»»» dateFormat|string|false|none||none|
|»»»»»» description|string|false|none||none|
|»»»»»» expr|string|false|none||none|
|»»»»»» fieldName|string|false|none||none|
|»»»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»»»» isTag|integer(int32)|false|none||none|
|»»»»»» name|string|false|none||none|
|»»»»»» type|string|false|none||none|
|»»»»»» typeParams|[DimensionTimeTypeParams](#schemadimensiontimetypeparams)|false|none|DimensionTimeTypeParams|none|
|»»»»»»» isPrimary|string|false|none||none|
|»»»»»»» timeGranularity|string|false|none||none|
|»»»» fields|[[Field](#schemafield)]|false|none||none|
|»»»»» Field|[Field](#schemafield)|false|none|Field|none|
|»»»»»» dataType|string|false|none||none|
|»»»»»» fieldName|string|false|none||none|
|»»»» identifiers|[[Identify](#schemaidentify)]|false|none||none|
|»»»»» Identify|[Identify](#schemaidentify)|false|none|Identify|none|
|»»»»»» bizName|string|false|none||none|
|»»»»»» entityNames|[string]|false|none||none|
|»»»»»» fieldName|string|false|none||none|
|»»»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»»»» name|string|false|none||none|
|»»»»»» type|string|false|none||none|
|»»»» measures|[[Measure](#schemameasure)]|false|none||none|
|»»»»» Measure|[Measure](#schemameasure)|false|none|Measure|none|
|»»»»»» agg|string|false|none||none|
|»»»»»» alias|string|false|none||none|
|»»»»»» bizName|string|false|none||none|
|»»»»»» constraint|string|false|none||none|
|»»»»»» expr|string|false|none||none|
|»»»»»» fieldName|string|false|none||none|
|»»»»»» isCreateMetric|integer(int32)|false|none||none|
|»»»»»» name|string|false|none||none|
|»»»» queryType|string|false|none||none|
|»»»» sqlQuery|string|false|none||none|
|»»»» sqlVariables|[[SqlVariable](#schemasqlvariable)]|false|none||none|
|»»»»» SqlVariable|[SqlVariable](#schemasqlvariable)|false|none|SqlVariable|none|
|»»»»»» defaultValues|[object]|false|none||none|
|»»»»»» name|string|false|none||none|
|»»»»»» valueType|string|false|none||none|
|»»»» tableQuery|string|false|none||none|
|»»» name|string|false|none||none|
|»»» primaryIdentify|[Identify](#schemaidentify)|false|none|Identify|none|
|»»»» bizName|string|false|none||none|
|»»»» entityNames|[string]|false|none||none|
|»»»» fieldName|string|false|none||none|
|»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»» name|string|false|none||none|
|»»»» type|string|false|none||none|
|»»» sensitiveLevel|integer(int32)|false|none||none|
|»»» status|integer(int32)|false|none||none|
|»»» tagObjectId|integer(int64)|false|none||none|
|»»» timeDimension|[[Dim](#schemadim)]|false|none||none|
|»»»» Dim|[Dim](#schemadim)|false|none|Dim|none|
|»»»»» bizName|string|false|none||none|
|»»»»» dateFormat|string|false|none||none|
|»»»»» description|string|false|none||none|
|»»»»» expr|string|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»»» isTag|integer(int32)|false|none||none|
|»»»»» name|string|false|none||none|
|»»»»» type|string|false|none||none|
|»»»»» typeParams|[DimensionTimeTypeParams](#schemadimensiontimetypeparams)|false|none|DimensionTimeTypeParams|none|
|»»» typeEnum|string|false|none||none|
|»»» updatedAt|string(date-time)|false|none||none|
|»»» updatedBy|string|false|none||none|
|»»» viewOrgs|[string]|false|none||none|
|»»» viewers|[string]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|dataType|ARRAY|
|dataType|BIGINT|
|dataType|DATE|
|dataType|DECIMAL|
|dataType|DOUBLE|
|dataType|FLOAT|
|dataType|INT|
|dataType|JSON|
|dataType|MAP|
|dataType|UNKNOWN|
|dataType|VARCHAR|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|
|metricDefineType|FIELD|
|metricDefineType|MEASURE|
|metricDefineType|METRIC|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|
|valueType|EXPR|
|valueType|NUMBER|
|valueType|STRING|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdgetCanvasListUsingGET"></a>

## GET getCanvasList

GET /api/semantic/viewInfo/getViewInfoList/{domainId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|path|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
[
  {
    "config": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "domainId": 0,
    "id": 0,
    "type": "string",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[CanvasDO](#schemacanvasdo)]|false|none||none|
|» CanvasDO|[CanvasDO](#schemacanvasdo)|false|none|CanvasDO|none|
|»» config|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» type|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

# chat-config-controller

<a id="opIdeditModelExtendUsingPUT"></a>

## PUT editModelExtend

PUT /api/chat/conf

> Body 请求参数

```json
{
  "id": 0,
  "llmExamples": "string",
  "modelId": 0,
  "recommendedQuestions": [
    {
      "question": "string"
    }
  ],
  "status": "DELETED"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatConfigEditReqReq](#schemachatconfigeditreqreq)| 否 | ChatConfigEditReqReq|none|

> 返回示例

> 200 Response

```json
0
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|integer|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdaddChatConfigUsingPOST"></a>

## POST addChatConfig

POST /api/chat/conf

> Body 请求参数

```json
{
  "llmExamples": "string",
  "modelId": 0,
  "recommendedQuestions": [
    {
      "question": "string"
    }
  ],
  "status": "DELETED"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatConfigBaseReq](#schemachatconfigbasereq)| 否 | ChatConfigBaseReq|none|

> 返回示例

> 200 Response

```json
0
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|integer|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetDataSetSchemaUsingGET"></a>

## GET getDataSetSchema

GET /api/chat/conf/getDataSetSchema/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "dataSet": {
    "alias": [
      "string"
    ],
    "bizName": "string",
    "dataFormatType": "string",
    "dataSet": 0,
    "dataSetName": "string",
    "defaultAgg": "string",
    "description": "string",
    "id": 0,
    "isTag": 0,
    "model": 0,
    "name": "string",
    "order": 0,
    "relatedSchemaElements": [
      {
        "dimensionId": 0,
        "necessary": true
      }
    ],
    "schemaValueMaps": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "techName": "string"
      }
    ],
    "type": "DATASET",
    "useCnt": 0
  },
  "dimensionValues": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "dimensions": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "entity": {
    "alias": [
      "string"
    ],
    "bizName": "string",
    "dataFormatType": "string",
    "dataSet": 0,
    "dataSetName": "string",
    "defaultAgg": "string",
    "description": "string",
    "id": 0,
    "isTag": 0,
    "model": 0,
    "name": "string",
    "order": 0,
    "relatedSchemaElements": [
      {
        "dimensionId": 0,
        "necessary": true
      }
    ],
    "schemaValueMaps": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "techName": "string"
      }
    ],
    "type": "DATASET",
    "useCnt": 0
  },
  "metricTypeTimeDefaultConfig": {
    "period": "string",
    "timeMode": "LAST",
    "unit": 0
  },
  "metrics": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "queryConfig": {
    "metricTypeDefaultConfig": {
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    },
    "tagTypeDefaultConfig": {
      "defaultDisplayInfo": {
        "dimensionIds": [
          0
        ],
        "metricIds": [
          0
        ]
      },
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    }
  },
  "tagDefaultDimensions": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "tagDefaultMetrics": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "tagTypeDefaultConfig": {
    "defaultDisplayInfo": {
      "dimensionIds": [
        0
      ],
      "metricIds": [
        0
      ]
    },
    "timeDefaultConfig": {
      "period": "string",
      "timeMode": "LAST",
      "unit": 0
    }
  },
  "tagTypeTimeDefaultConfig": {
    "period": "string",
    "timeMode": "LAST",
    "unit": 0
  },
  "tags": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "terms": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DataSetSchema](#schemadatasetschema)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetDomainDataSetTreeUsingGET"></a>

## GET getDomainDataSetTree

GET /api/chat/conf/getDomainDataSetTree

> 返回示例

> 200 Response

```json
[
  {
    "children": [
      {
        "children": [
          {
            "children": [
              null
            ],
            "id": 0,
            "name": "string",
            "parentId": 0,
            "root": true,
            "type": "["
          }
        ],
        "id": 0,
        "name": "string",
        "parentId": 0,
        "root": true,
        "type": "DATASET"
      }
    ],
    "id": 0,
    "name": "string",
    "parentId": 0,
    "root": true,
    "type": "DATASET"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ItemResp](#schemaitemresp)]|false|none||none|
|» ItemResp|[ItemResp](#schemaitemresp)|false|none|ItemResp|none|
|»» children|[[ItemResp](#schemaitemresp)]|false|none||none|
|»»» ItemResp|[ItemResp](#schemaitemresp)|false|none|ItemResp|none|
|»»»» children|[[ItemResp](#schemaitemresp)]|false|none||none|
|»»»» id|integer(int64)|false|none||none|
|»»»» name|string|false|none||none|
|»»»» parentId|integer(int64)|false|none||none|
|»»»» root|boolean|false|none||none|
|»»»» type|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» parentId|integer(int64)|false|none||none|
|»» root|boolean|false|none||none|
|»» type|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|

<a id="opIdgetAllChatRichConfigUsingGET"></a>

## GET getAllChatRichConfig

GET /api/chat/conf/richDesc/all

> 返回示例

> 200 Response

```json
[
  {
    "bizName": "string",
    "chatAggRichConfig": {
      "chatDefaultConfig": {
        "dimensions": [
          {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          }
        ],
        "metrics": [
          {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          }
        ],
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      },
      "globalKnowledgeConfig": {
        "blackList": [
          "string"
        ],
        "ruleList": [
          "string"
        ],
        "whiteList": [
          "string"
        ]
      },
      "knowledgeInfos": [
        {
          "bizName": "string",
          "itemId": 0,
          "knowledgeAdvancedConfig": {
            "blackList": null,
            "ruleList": null,
            "whiteList": null
          },
          "searchEnable": true,
          "type": "DATASET"
        }
      ],
      "visibility": {
        "blackDimIdList": [
          0
        ],
        "blackMetricIdList": [
          0
        ],
        "whiteDimIdList": [
          0
        ],
        "whiteMetricIdList": [
          0
        ]
      }
    },
    "chatDetailRichConfig": {
      "chatDefaultConfig": {
        "dimensions": [
          {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          }
        ],
        "metrics": [
          {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          }
        ],
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      },
      "globalKnowledgeConfig": {
        "blackList": [
          "string"
        ],
        "ruleList": [
          "string"
        ],
        "whiteList": [
          "string"
        ]
      },
      "knowledgeInfos": [
        {
          "bizName": "string",
          "itemId": 0,
          "knowledgeAdvancedConfig": {
            "blackList": null,
            "ruleList": null,
            "whiteList": null
          },
          "searchEnable": true,
          "type": "DATASET"
        }
      ],
      "visibility": {
        "blackDimIdList": [
          0
        ],
        "blackMetricIdList": [
          0
        ],
        "whiteDimIdList": [
          0
        ],
        "whiteMetricIdList": [
          0
        ]
      }
    },
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "id": 0,
    "modelId": 0,
    "modelName": "string",
    "recommendedQuestions": [
      {
        "question": "string"
      }
    ],
    "statusEnum": "DELETED",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatConfigRichResp](#schemachatconfigrichresp)]|false|none||none|
|» ChatConfigRichResp|[ChatConfigRichResp](#schemachatconfigrichresp)|false|none|ChatConfigRichResp|none|
|»» bizName|string|false|none||none|
|»» chatAggRichConfig|[ChatAggRichConfigResp](#schemachataggrichconfigresp)|false|none|ChatAggRichConfigResp|none|
|»»» chatDefaultConfig|[ChatDefaultRichConfigResp](#schemachatdefaultrichconfigresp)|false|none|ChatDefaultRichConfigResp|none|
|»»»» dimensions|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|»»»»» SchemaElement|[SchemaElement](#schemaschemaelement)|false|none|SchemaElement|none|
|»»»»»» alias|[string]|false|none||none|
|»»»»»» bizName|string|false|none||none|
|»»»»»» dataFormatType|string|false|none||none|
|»»»»»» dataSet|integer(int64)|false|none||none|
|»»»»»» dataSetName|string|false|none||none|
|»»»»»» defaultAgg|string|false|none||none|
|»»»»»» description|string|false|none||none|
|»»»»»» id|integer(int64)|false|none||none|
|»»»»»» isTag|integer(int32)|false|none||none|
|»»»»»» model|integer(int64)|false|none||none|
|»»»»»» name|string|false|none||none|
|»»»»»» order|number(double)|false|none||none|
|»»»»»» relatedSchemaElements|[[RelatedSchemaElement](#schemarelatedschemaelement)]|false|none||none|
|»»»»»»» RelatedSchemaElement|[RelatedSchemaElement](#schemarelatedschemaelement)|false|none|RelatedSchemaElement|none|
|»»»»»»»» dimensionId|integer(int64)|false|none||none|
|»»»»»»»» necessary|boolean|false|none||none|
|»»»»»» schemaValueMaps|[[SchemaValueMap](#schemaschemavaluemap)]|false|none||none|
|»»»»»»» SchemaValueMap|[SchemaValueMap](#schemaschemavaluemap)|false|none|SchemaValueMap|none|
|»»»»»»»» alias|[string]|false|none||none|
|»»»»»»»» bizName|string|false|none||none|
|»»»»»»»» techName|string|false|none||none|
|»»»»»» type|string|false|none||none|
|»»»»»» useCnt|integer(int64)|false|none||none|
|»»»» metrics|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|»»»»» SchemaElement|[SchemaElement](#schemaschemaelement)|false|none|SchemaElement|none|
|»»»»»» alias|[string]|false|none||none|
|»»»»»» bizName|string|false|none||none|
|»»»»»» dataFormatType|string|false|none||none|
|»»»»»» dataSet|integer(int64)|false|none||none|
|»»»»»» dataSetName|string|false|none||none|
|»»»»»» defaultAgg|string|false|none||none|
|»»»»»» description|string|false|none||none|
|»»»»»» id|integer(int64)|false|none||none|
|»»»»»» isTag|integer(int32)|false|none||none|
|»»»»»» model|integer(int64)|false|none||none|
|»»»»»» name|string|false|none||none|
|»»»»»» order|number(double)|false|none||none|
|»»»»»» relatedSchemaElements|[[RelatedSchemaElement](#schemarelatedschemaelement)]|false|none||none|
|»»»»»» schemaValueMaps|[[SchemaValueMap](#schemaschemavaluemap)]|false|none||none|
|»»»»»» type|string|false|none||none|
|»»»»»» useCnt|integer(int64)|false|none||none|
|»»»» period|string|false|none||none|
|»»»» timeMode|string|false|none||none|
|»»»» unit|integer(int32)|false|none||none|
|»»» globalKnowledgeConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»» blackList|[string]|false|none||none|
|»»»» ruleList|[string]|false|none||none|
|»»»» whiteList|[string]|false|none||none|
|»»» knowledgeInfos|[[KnowledgeInfoReq](#schemaknowledgeinforeq)]|false|none||none|
|»»»» KnowledgeInfoReq|[KnowledgeInfoReq](#schemaknowledgeinforeq)|false|none|KnowledgeInfoReq|none|
|»»»»» bizName|string|false|none||none|
|»»»»» itemId|integer(int64)|false|none||none|
|»»»»» knowledgeAdvancedConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»»»» blackList|[string]|false|none||none|
|»»»»»» ruleList|[string]|false|none||none|
|»»»»»» whiteList|[string]|false|none||none|
|»»»»» searchEnable|boolean|false|none||none|
|»»»»» type|string|true|none||none|
|»»» visibility|[ItemVisibilityInfo](#schemaitemvisibilityinfo)|false|none|ItemVisibilityInfo|none|
|»»»» blackDimIdList|[integer]|false|none||none|
|»»»» blackMetricIdList|[integer]|false|none||none|
|»»»» whiteDimIdList|[integer]|false|none||none|
|»»»» whiteMetricIdList|[integer]|false|none||none|
|»» chatDetailRichConfig|[ChatDetailRichConfigResp](#schemachatdetailrichconfigresp)|false|none|ChatDetailRichConfigResp|none|
|»»» chatDefaultConfig|[ChatDefaultRichConfigResp](#schemachatdefaultrichconfigresp)|false|none|ChatDefaultRichConfigResp|none|
|»»»» dimensions|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|»»»» metrics|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|»»»» period|string|false|none||none|
|»»»» timeMode|string|false|none||none|
|»»»» unit|integer(int32)|false|none||none|
|»»» globalKnowledgeConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»» blackList|[string]|false|none||none|
|»»»» ruleList|[string]|false|none||none|
|»»»» whiteList|[string]|false|none||none|
|»»» knowledgeInfos|[[KnowledgeInfoReq](#schemaknowledgeinforeq)]|false|none||none|
|»»»» KnowledgeInfoReq|[KnowledgeInfoReq](#schemaknowledgeinforeq)|false|none|KnowledgeInfoReq|none|
|»»»»» bizName|string|false|none||none|
|»»»»» itemId|integer(int64)|false|none||none|
|»»»»» knowledgeAdvancedConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»»» searchEnable|boolean|false|none||none|
|»»»»» type|string|true|none||none|
|»»» visibility|[ItemVisibilityInfo](#schemaitemvisibilityinfo)|false|none|ItemVisibilityInfo|none|
|»»»» blackDimIdList|[integer]|false|none||none|
|»»»» blackMetricIdList|[integer]|false|none||none|
|»»»» whiteDimIdList|[integer]|false|none||none|
|»»»» whiteMetricIdList|[integer]|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» modelId|integer(int64)|false|none||none|
|»» modelName|string|false|none||none|
|»» recommendedQuestions|[[RecommendedQuestionReq](#schemarecommendedquestionreq)]|false|none||none|
|»»» RecommendedQuestionReq|[RecommendedQuestionReq](#schemarecommendedquestionreq)|false|none|RecommendedQuestionReq|none|
|»»»» question|string|false|none||none|
|»» statusEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|DATASET|
|type|DATE|
|type|DIMENSION|
|type|ENTITY|
|type|ID|
|type|METRIC|
|type|TAG|
|type|TERM|
|type|VALUE|
|type|DATASET|
|type|DATE|
|type|DIMENSION|
|type|ENTITY|
|type|ID|
|type|METRIC|
|type|TAG|
|type|TERM|
|type|VALUE|
|timeMode|LAST|
|timeMode|RECENT|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|
|timeMode|LAST|
|timeMode|RECENT|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|
|statusEnum|DELETED|
|statusEnum|INITIALIZED|
|statusEnum|OFFLINE|
|statusEnum|ONLINE|
|statusEnum|UNAVAILABLE|
|statusEnum|UNKNOWN|

<a id="opIdgetModelExtendRichInfoUsingGET"></a>

## GET getModelExtendRichInfo

GET /api/chat/conf/richDesc/{modelId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|modelId|path|integer(int64)| 是 ||modelId|

> 返回示例

> 200 Response

```json
{
  "bizName": "string",
  "chatAggRichConfig": {
    "chatDefaultConfig": {
      "dimensions": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "metrics": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "period": "string",
      "timeMode": "LAST",
      "unit": 0
    },
    "globalKnowledgeConfig": {
      "blackList": [
        "string"
      ],
      "ruleList": [
        "string"
      ],
      "whiteList": [
        "string"
      ]
    },
    "knowledgeInfos": [
      {
        "bizName": "string",
        "itemId": 0,
        "knowledgeAdvancedConfig": {
          "blackList": [
            null
          ],
          "ruleList": [
            null
          ],
          "whiteList": [
            null
          ]
        },
        "searchEnable": true,
        "type": "DATASET"
      }
    ],
    "visibility": {
      "blackDimIdList": [
        0
      ],
      "blackMetricIdList": [
        0
      ],
      "whiteDimIdList": [
        0
      ],
      "whiteMetricIdList": [
        0
      ]
    }
  },
  "chatDetailRichConfig": {
    "chatDefaultConfig": {
      "dimensions": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "metrics": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "period": "string",
      "timeMode": "LAST",
      "unit": 0
    },
    "globalKnowledgeConfig": {
      "blackList": [
        "string"
      ],
      "ruleList": [
        "string"
      ],
      "whiteList": [
        "string"
      ]
    },
    "knowledgeInfos": [
      {
        "bizName": "string",
        "itemId": 0,
        "knowledgeAdvancedConfig": {
          "blackList": [
            null
          ],
          "ruleList": [
            null
          ],
          "whiteList": [
            null
          ]
        },
        "searchEnable": true,
        "type": "DATASET"
      }
    ],
    "visibility": {
      "blackDimIdList": [
        0
      ],
      "blackMetricIdList": [
        0
      ],
      "whiteDimIdList": [
        0
      ],
      "whiteMetricIdList": [
        0
      ]
    }
  },
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "id": 0,
  "modelId": 0,
  "modelName": "string",
  "recommendedQuestions": [
    {
      "question": "string"
    }
  ],
  "statusEnum": "DELETED",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ChatConfigRichResp](#schemachatconfigrichresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdsearchUsingPOST"></a>

## POST search

POST /api/chat/conf/search

> Body 请求参数

```json
{
  "id": 0,
  "modelId": 0,
  "status": "DELETED"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatConfigFilter](#schemachatconfigfilter)| 否 | ChatConfigFilter|none|

> 返回示例

> 200 Response

```json
[
  {
    "chatAggConfig": {
      "chatDefaultConfig": {
        "dimensionIds": [
          0
        ],
        "metricIds": [
          0
        ]
      },
      "globalKnowledgeConfig": {
        "blackList": [
          "string"
        ],
        "ruleList": [
          "string"
        ],
        "whiteList": [
          "string"
        ]
      },
      "knowledgeInfos": [
        {
          "bizName": "string",
          "itemId": 0,
          "knowledgeAdvancedConfig": {
            "blackList": null,
            "ruleList": null,
            "whiteList": null
          },
          "searchEnable": true,
          "type": "DATASET"
        }
      ],
      "visibility": {
        "blackDimIdList": [
          0
        ],
        "blackMetricIdList": [
          0
        ]
      }
    },
    "chatDetailConfig": {
      "chatDefaultConfig": {
        "dimensionIds": [
          0
        ],
        "metricIds": [
          0
        ]
      },
      "globalKnowledgeConfig": {
        "blackList": [
          "string"
        ],
        "ruleList": [
          "string"
        ],
        "whiteList": [
          "string"
        ]
      },
      "knowledgeInfos": [
        {
          "bizName": "string",
          "itemId": 0,
          "knowledgeAdvancedConfig": {
            "blackList": null,
            "ruleList": null,
            "whiteList": null
          },
          "searchEnable": true,
          "type": "DATASET"
        }
      ],
      "visibility": {
        "blackDimIdList": [
          0
        ],
        "blackMetricIdList": [
          0
        ]
      }
    },
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "id": 0,
    "llmExamples": "string",
    "modelId": 0,
    "recommendedQuestions": [
      {
        "question": "string"
      }
    ],
    "statusEnum": "DELETED",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatConfigResp](#schemachatconfigresp)]|false|none||none|
|» ChatConfigResp|[ChatConfigResp](#schemachatconfigresp)|false|none|ChatConfigResp|none|
|»» chatAggConfig|[ChatAggConfigReq](#schemachataggconfigreq)|false|none|ChatAggConfigReq|none|
|»»» chatDefaultConfig|[ChatDefaultConfigReq](#schemachatdefaultconfigreq)|false|none|ChatDefaultConfigReq|none|
|»»»» dimensionIds|[integer]|false|none||none|
|»»»» metricIds|[integer]|false|none||none|
|»»» globalKnowledgeConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»» blackList|[string]|false|none||none|
|»»»» ruleList|[string]|false|none||none|
|»»»» whiteList|[string]|false|none||none|
|»»» knowledgeInfos|[[KnowledgeInfoReq](#schemaknowledgeinforeq)]|false|none||none|
|»»»» KnowledgeInfoReq|[KnowledgeInfoReq](#schemaknowledgeinforeq)|false|none|KnowledgeInfoReq|none|
|»»»»» bizName|string|false|none||none|
|»»»»» itemId|integer(int64)|false|none||none|
|»»»»» knowledgeAdvancedConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»»»» blackList|[string]|false|none||none|
|»»»»»» ruleList|[string]|false|none||none|
|»»»»»» whiteList|[string]|false|none||none|
|»»»»» searchEnable|boolean|false|none||none|
|»»»»» type|string|true|none||none|
|»»» visibility|[ItemVisibility](#schemaitemvisibility)|false|none|ItemVisibility|none|
|»»»» blackDimIdList|[integer]|false|none||none|
|»»»» blackMetricIdList|[integer]|false|none||none|
|»» chatDetailConfig|[ChatDetailConfigReq](#schemachatdetailconfigreq)|false|none|ChatDetailConfigReq|none|
|»»» chatDefaultConfig|[ChatDefaultConfigReq](#schemachatdefaultconfigreq)|false|none|ChatDefaultConfigReq|none|
|»»»» dimensionIds|[integer]|false|none||none|
|»»»» metricIds|[integer]|false|none||none|
|»»» globalKnowledgeConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»» blackList|[string]|false|none||none|
|»»»» ruleList|[string]|false|none||none|
|»»»» whiteList|[string]|false|none||none|
|»»» knowledgeInfos|[[KnowledgeInfoReq](#schemaknowledgeinforeq)]|false|none||none|
|»»»» KnowledgeInfoReq|[KnowledgeInfoReq](#schemaknowledgeinforeq)|false|none|KnowledgeInfoReq|none|
|»»»»» bizName|string|false|none||none|
|»»»»» itemId|integer(int64)|false|none||none|
|»»»»» knowledgeAdvancedConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»»» searchEnable|boolean|false|none||none|
|»»»»» type|string|true|none||none|
|»»» visibility|[ItemVisibility](#schemaitemvisibility)|false|none|ItemVisibility|none|
|»»»» blackDimIdList|[integer]|false|none||none|
|»»»» blackMetricIdList|[integer]|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» llmExamples|string|false|none||none|
|»» modelId|integer(int64)|false|none||none|
|»» recommendedQuestions|[[RecommendedQuestionReq](#schemarecommendedquestionreq)]|false|none||none|
|»»» RecommendedQuestionReq|[RecommendedQuestionReq](#schemarecommendedquestionreq)|false|none|RecommendedQuestionReq|none|
|»»»» question|string|false|none||none|
|»» statusEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|
|statusEnum|DELETED|
|statusEnum|INITIALIZED|
|statusEnum|OFFLINE|
|statusEnum|ONLINE|
|statusEnum|UNAVAILABLE|
|statusEnum|UNKNOWN|

<a id="opIdeditModelExtendUsingPUT_1"></a>

## PUT editModelExtend

PUT /openapi/chat/conf

> Body 请求参数

```json
{
  "id": 0,
  "llmExamples": "string",
  "modelId": 0,
  "recommendedQuestions": [
    {
      "question": "string"
    }
  ],
  "status": "DELETED"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatConfigEditReqReq](#schemachatconfigeditreqreq)| 否 | ChatConfigEditReqReq|none|

> 返回示例

> 200 Response

```json
0
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|integer|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdaddChatConfigUsingPOST_1"></a>

## POST addChatConfig

POST /openapi/chat/conf

> Body 请求参数

```json
{
  "llmExamples": "string",
  "modelId": 0,
  "recommendedQuestions": [
    {
      "question": "string"
    }
  ],
  "status": "DELETED"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatConfigBaseReq](#schemachatconfigbasereq)| 否 | ChatConfigBaseReq|none|

> 返回示例

> 200 Response

```json
0
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|integer|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetDataSetSchemaUsingGET_1"></a>

## GET getDataSetSchema

GET /openapi/chat/conf/getDataSetSchema/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "dataSet": {
    "alias": [
      "string"
    ],
    "bizName": "string",
    "dataFormatType": "string",
    "dataSet": 0,
    "dataSetName": "string",
    "defaultAgg": "string",
    "description": "string",
    "id": 0,
    "isTag": 0,
    "model": 0,
    "name": "string",
    "order": 0,
    "relatedSchemaElements": [
      {
        "dimensionId": 0,
        "necessary": true
      }
    ],
    "schemaValueMaps": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "techName": "string"
      }
    ],
    "type": "DATASET",
    "useCnt": 0
  },
  "dimensionValues": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "dimensions": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "entity": {
    "alias": [
      "string"
    ],
    "bizName": "string",
    "dataFormatType": "string",
    "dataSet": 0,
    "dataSetName": "string",
    "defaultAgg": "string",
    "description": "string",
    "id": 0,
    "isTag": 0,
    "model": 0,
    "name": "string",
    "order": 0,
    "relatedSchemaElements": [
      {
        "dimensionId": 0,
        "necessary": true
      }
    ],
    "schemaValueMaps": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "techName": "string"
      }
    ],
    "type": "DATASET",
    "useCnt": 0
  },
  "metricTypeTimeDefaultConfig": {
    "period": "string",
    "timeMode": "LAST",
    "unit": 0
  },
  "metrics": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "queryConfig": {
    "metricTypeDefaultConfig": {
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    },
    "tagTypeDefaultConfig": {
      "defaultDisplayInfo": {
        "dimensionIds": [
          0
        ],
        "metricIds": [
          0
        ]
      },
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    }
  },
  "tagDefaultDimensions": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "tagDefaultMetrics": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "tagTypeDefaultConfig": {
    "defaultDisplayInfo": {
      "dimensionIds": [
        0
      ],
      "metricIds": [
        0
      ]
    },
    "timeDefaultConfig": {
      "period": "string",
      "timeMode": "LAST",
      "unit": 0
    }
  },
  "tagTypeTimeDefaultConfig": {
    "period": "string",
    "timeMode": "LAST",
    "unit": 0
  },
  "tags": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "terms": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DataSetSchema](#schemadatasetschema)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetDomainDataSetTreeUsingGET_1"></a>

## GET getDomainDataSetTree

GET /openapi/chat/conf/getDomainDataSetTree

> 返回示例

> 200 Response

```json
[
  {
    "children": [
      {
        "children": [
          {
            "children": [
              null
            ],
            "id": 0,
            "name": "string",
            "parentId": 0,
            "root": true,
            "type": "["
          }
        ],
        "id": 0,
        "name": "string",
        "parentId": 0,
        "root": true,
        "type": "DATASET"
      }
    ],
    "id": 0,
    "name": "string",
    "parentId": 0,
    "root": true,
    "type": "DATASET"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ItemResp](#schemaitemresp)]|false|none||none|
|» ItemResp|[ItemResp](#schemaitemresp)|false|none|ItemResp|none|
|»» children|[[ItemResp](#schemaitemresp)]|false|none||none|
|»»» ItemResp|[ItemResp](#schemaitemresp)|false|none|ItemResp|none|
|»»»» children|[[ItemResp](#schemaitemresp)]|false|none||none|
|»»»» id|integer(int64)|false|none||none|
|»»»» name|string|false|none||none|
|»»»» parentId|integer(int64)|false|none||none|
|»»»» root|boolean|false|none||none|
|»»»» type|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» parentId|integer(int64)|false|none||none|
|»» root|boolean|false|none||none|
|»» type|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|

<a id="opIdgetAllChatRichConfigUsingGET_1"></a>

## GET getAllChatRichConfig

GET /openapi/chat/conf/richDesc/all

> 返回示例

> 200 Response

```json
[
  {
    "bizName": "string",
    "chatAggRichConfig": {
      "chatDefaultConfig": {
        "dimensions": [
          {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          }
        ],
        "metrics": [
          {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          }
        ],
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      },
      "globalKnowledgeConfig": {
        "blackList": [
          "string"
        ],
        "ruleList": [
          "string"
        ],
        "whiteList": [
          "string"
        ]
      },
      "knowledgeInfos": [
        {
          "bizName": "string",
          "itemId": 0,
          "knowledgeAdvancedConfig": {
            "blackList": null,
            "ruleList": null,
            "whiteList": null
          },
          "searchEnable": true,
          "type": "DATASET"
        }
      ],
      "visibility": {
        "blackDimIdList": [
          0
        ],
        "blackMetricIdList": [
          0
        ],
        "whiteDimIdList": [
          0
        ],
        "whiteMetricIdList": [
          0
        ]
      }
    },
    "chatDetailRichConfig": {
      "chatDefaultConfig": {
        "dimensions": [
          {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          }
        ],
        "metrics": [
          {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          }
        ],
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      },
      "globalKnowledgeConfig": {
        "blackList": [
          "string"
        ],
        "ruleList": [
          "string"
        ],
        "whiteList": [
          "string"
        ]
      },
      "knowledgeInfos": [
        {
          "bizName": "string",
          "itemId": 0,
          "knowledgeAdvancedConfig": {
            "blackList": null,
            "ruleList": null,
            "whiteList": null
          },
          "searchEnable": true,
          "type": "DATASET"
        }
      ],
      "visibility": {
        "blackDimIdList": [
          0
        ],
        "blackMetricIdList": [
          0
        ],
        "whiteDimIdList": [
          0
        ],
        "whiteMetricIdList": [
          0
        ]
      }
    },
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "id": 0,
    "modelId": 0,
    "modelName": "string",
    "recommendedQuestions": [
      {
        "question": "string"
      }
    ],
    "statusEnum": "DELETED",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatConfigRichResp](#schemachatconfigrichresp)]|false|none||none|
|» ChatConfigRichResp|[ChatConfigRichResp](#schemachatconfigrichresp)|false|none|ChatConfigRichResp|none|
|»» bizName|string|false|none||none|
|»» chatAggRichConfig|[ChatAggRichConfigResp](#schemachataggrichconfigresp)|false|none|ChatAggRichConfigResp|none|
|»»» chatDefaultConfig|[ChatDefaultRichConfigResp](#schemachatdefaultrichconfigresp)|false|none|ChatDefaultRichConfigResp|none|
|»»»» dimensions|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|»»»»» SchemaElement|[SchemaElement](#schemaschemaelement)|false|none|SchemaElement|none|
|»»»»»» alias|[string]|false|none||none|
|»»»»»» bizName|string|false|none||none|
|»»»»»» dataFormatType|string|false|none||none|
|»»»»»» dataSet|integer(int64)|false|none||none|
|»»»»»» dataSetName|string|false|none||none|
|»»»»»» defaultAgg|string|false|none||none|
|»»»»»» description|string|false|none||none|
|»»»»»» id|integer(int64)|false|none||none|
|»»»»»» isTag|integer(int32)|false|none||none|
|»»»»»» model|integer(int64)|false|none||none|
|»»»»»» name|string|false|none||none|
|»»»»»» order|number(double)|false|none||none|
|»»»»»» relatedSchemaElements|[[RelatedSchemaElement](#schemarelatedschemaelement)]|false|none||none|
|»»»»»»» RelatedSchemaElement|[RelatedSchemaElement](#schemarelatedschemaelement)|false|none|RelatedSchemaElement|none|
|»»»»»»»» dimensionId|integer(int64)|false|none||none|
|»»»»»»»» necessary|boolean|false|none||none|
|»»»»»» schemaValueMaps|[[SchemaValueMap](#schemaschemavaluemap)]|false|none||none|
|»»»»»»» SchemaValueMap|[SchemaValueMap](#schemaschemavaluemap)|false|none|SchemaValueMap|none|
|»»»»»»»» alias|[string]|false|none||none|
|»»»»»»»» bizName|string|false|none||none|
|»»»»»»»» techName|string|false|none||none|
|»»»»»» type|string|false|none||none|
|»»»»»» useCnt|integer(int64)|false|none||none|
|»»»» metrics|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|»»»»» SchemaElement|[SchemaElement](#schemaschemaelement)|false|none|SchemaElement|none|
|»»»»»» alias|[string]|false|none||none|
|»»»»»» bizName|string|false|none||none|
|»»»»»» dataFormatType|string|false|none||none|
|»»»»»» dataSet|integer(int64)|false|none||none|
|»»»»»» dataSetName|string|false|none||none|
|»»»»»» defaultAgg|string|false|none||none|
|»»»»»» description|string|false|none||none|
|»»»»»» id|integer(int64)|false|none||none|
|»»»»»» isTag|integer(int32)|false|none||none|
|»»»»»» model|integer(int64)|false|none||none|
|»»»»»» name|string|false|none||none|
|»»»»»» order|number(double)|false|none||none|
|»»»»»» relatedSchemaElements|[[RelatedSchemaElement](#schemarelatedschemaelement)]|false|none||none|
|»»»»»» schemaValueMaps|[[SchemaValueMap](#schemaschemavaluemap)]|false|none||none|
|»»»»»» type|string|false|none||none|
|»»»»»» useCnt|integer(int64)|false|none||none|
|»»»» period|string|false|none||none|
|»»»» timeMode|string|false|none||none|
|»»»» unit|integer(int32)|false|none||none|
|»»» globalKnowledgeConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»» blackList|[string]|false|none||none|
|»»»» ruleList|[string]|false|none||none|
|»»»» whiteList|[string]|false|none||none|
|»»» knowledgeInfos|[[KnowledgeInfoReq](#schemaknowledgeinforeq)]|false|none||none|
|»»»» KnowledgeInfoReq|[KnowledgeInfoReq](#schemaknowledgeinforeq)|false|none|KnowledgeInfoReq|none|
|»»»»» bizName|string|false|none||none|
|»»»»» itemId|integer(int64)|false|none||none|
|»»»»» knowledgeAdvancedConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»»»» blackList|[string]|false|none||none|
|»»»»»» ruleList|[string]|false|none||none|
|»»»»»» whiteList|[string]|false|none||none|
|»»»»» searchEnable|boolean|false|none||none|
|»»»»» type|string|true|none||none|
|»»» visibility|[ItemVisibilityInfo](#schemaitemvisibilityinfo)|false|none|ItemVisibilityInfo|none|
|»»»» blackDimIdList|[integer]|false|none||none|
|»»»» blackMetricIdList|[integer]|false|none||none|
|»»»» whiteDimIdList|[integer]|false|none||none|
|»»»» whiteMetricIdList|[integer]|false|none||none|
|»» chatDetailRichConfig|[ChatDetailRichConfigResp](#schemachatdetailrichconfigresp)|false|none|ChatDetailRichConfigResp|none|
|»»» chatDefaultConfig|[ChatDefaultRichConfigResp](#schemachatdefaultrichconfigresp)|false|none|ChatDefaultRichConfigResp|none|
|»»»» dimensions|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|»»»» metrics|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|»»»» period|string|false|none||none|
|»»»» timeMode|string|false|none||none|
|»»»» unit|integer(int32)|false|none||none|
|»»» globalKnowledgeConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»» blackList|[string]|false|none||none|
|»»»» ruleList|[string]|false|none||none|
|»»»» whiteList|[string]|false|none||none|
|»»» knowledgeInfos|[[KnowledgeInfoReq](#schemaknowledgeinforeq)]|false|none||none|
|»»»» KnowledgeInfoReq|[KnowledgeInfoReq](#schemaknowledgeinforeq)|false|none|KnowledgeInfoReq|none|
|»»»»» bizName|string|false|none||none|
|»»»»» itemId|integer(int64)|false|none||none|
|»»»»» knowledgeAdvancedConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»»» searchEnable|boolean|false|none||none|
|»»»»» type|string|true|none||none|
|»»» visibility|[ItemVisibilityInfo](#schemaitemvisibilityinfo)|false|none|ItemVisibilityInfo|none|
|»»»» blackDimIdList|[integer]|false|none||none|
|»»»» blackMetricIdList|[integer]|false|none||none|
|»»»» whiteDimIdList|[integer]|false|none||none|
|»»»» whiteMetricIdList|[integer]|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» modelId|integer(int64)|false|none||none|
|»» modelName|string|false|none||none|
|»» recommendedQuestions|[[RecommendedQuestionReq](#schemarecommendedquestionreq)]|false|none||none|
|»»» RecommendedQuestionReq|[RecommendedQuestionReq](#schemarecommendedquestionreq)|false|none|RecommendedQuestionReq|none|
|»»»» question|string|false|none||none|
|»» statusEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|DATASET|
|type|DATE|
|type|DIMENSION|
|type|ENTITY|
|type|ID|
|type|METRIC|
|type|TAG|
|type|TERM|
|type|VALUE|
|type|DATASET|
|type|DATE|
|type|DIMENSION|
|type|ENTITY|
|type|ID|
|type|METRIC|
|type|TAG|
|type|TERM|
|type|VALUE|
|timeMode|LAST|
|timeMode|RECENT|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|
|timeMode|LAST|
|timeMode|RECENT|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|
|statusEnum|DELETED|
|statusEnum|INITIALIZED|
|statusEnum|OFFLINE|
|statusEnum|ONLINE|
|statusEnum|UNAVAILABLE|
|statusEnum|UNKNOWN|

<a id="opIdgetModelExtendRichInfoUsingGET_1"></a>

## GET getModelExtendRichInfo

GET /openapi/chat/conf/richDesc/{modelId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|modelId|path|integer(int64)| 是 ||modelId|

> 返回示例

> 200 Response

```json
{
  "bizName": "string",
  "chatAggRichConfig": {
    "chatDefaultConfig": {
      "dimensions": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "metrics": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "period": "string",
      "timeMode": "LAST",
      "unit": 0
    },
    "globalKnowledgeConfig": {
      "blackList": [
        "string"
      ],
      "ruleList": [
        "string"
      ],
      "whiteList": [
        "string"
      ]
    },
    "knowledgeInfos": [
      {
        "bizName": "string",
        "itemId": 0,
        "knowledgeAdvancedConfig": {
          "blackList": [
            null
          ],
          "ruleList": [
            null
          ],
          "whiteList": [
            null
          ]
        },
        "searchEnable": true,
        "type": "DATASET"
      }
    ],
    "visibility": {
      "blackDimIdList": [
        0
      ],
      "blackMetricIdList": [
        0
      ],
      "whiteDimIdList": [
        0
      ],
      "whiteMetricIdList": [
        0
      ]
    }
  },
  "chatDetailRichConfig": {
    "chatDefaultConfig": {
      "dimensions": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "metrics": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "period": "string",
      "timeMode": "LAST",
      "unit": 0
    },
    "globalKnowledgeConfig": {
      "blackList": [
        "string"
      ],
      "ruleList": [
        "string"
      ],
      "whiteList": [
        "string"
      ]
    },
    "knowledgeInfos": [
      {
        "bizName": "string",
        "itemId": 0,
        "knowledgeAdvancedConfig": {
          "blackList": [
            null
          ],
          "ruleList": [
            null
          ],
          "whiteList": [
            null
          ]
        },
        "searchEnable": true,
        "type": "DATASET"
      }
    ],
    "visibility": {
      "blackDimIdList": [
        0
      ],
      "blackMetricIdList": [
        0
      ],
      "whiteDimIdList": [
        0
      ],
      "whiteMetricIdList": [
        0
      ]
    }
  },
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "id": 0,
  "modelId": 0,
  "modelName": "string",
  "recommendedQuestions": [
    {
      "question": "string"
    }
  ],
  "statusEnum": "DELETED",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ChatConfigRichResp](#schemachatconfigrichresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdsearchUsingPOST_1"></a>

## POST search

POST /openapi/chat/conf/search

> Body 请求参数

```json
{
  "id": 0,
  "modelId": 0,
  "status": "DELETED"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatConfigFilter](#schemachatconfigfilter)| 否 | ChatConfigFilter|none|

> 返回示例

> 200 Response

```json
[
  {
    "chatAggConfig": {
      "chatDefaultConfig": {
        "dimensionIds": [
          0
        ],
        "metricIds": [
          0
        ]
      },
      "globalKnowledgeConfig": {
        "blackList": [
          "string"
        ],
        "ruleList": [
          "string"
        ],
        "whiteList": [
          "string"
        ]
      },
      "knowledgeInfos": [
        {
          "bizName": "string",
          "itemId": 0,
          "knowledgeAdvancedConfig": {
            "blackList": null,
            "ruleList": null,
            "whiteList": null
          },
          "searchEnable": true,
          "type": "DATASET"
        }
      ],
      "visibility": {
        "blackDimIdList": [
          0
        ],
        "blackMetricIdList": [
          0
        ]
      }
    },
    "chatDetailConfig": {
      "chatDefaultConfig": {
        "dimensionIds": [
          0
        ],
        "metricIds": [
          0
        ]
      },
      "globalKnowledgeConfig": {
        "blackList": [
          "string"
        ],
        "ruleList": [
          "string"
        ],
        "whiteList": [
          "string"
        ]
      },
      "knowledgeInfos": [
        {
          "bizName": "string",
          "itemId": 0,
          "knowledgeAdvancedConfig": {
            "blackList": null,
            "ruleList": null,
            "whiteList": null
          },
          "searchEnable": true,
          "type": "DATASET"
        }
      ],
      "visibility": {
        "blackDimIdList": [
          0
        ],
        "blackMetricIdList": [
          0
        ]
      }
    },
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "id": 0,
    "llmExamples": "string",
    "modelId": 0,
    "recommendedQuestions": [
      {
        "question": "string"
      }
    ],
    "statusEnum": "DELETED",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatConfigResp](#schemachatconfigresp)]|false|none||none|
|» ChatConfigResp|[ChatConfigResp](#schemachatconfigresp)|false|none|ChatConfigResp|none|
|»» chatAggConfig|[ChatAggConfigReq](#schemachataggconfigreq)|false|none|ChatAggConfigReq|none|
|»»» chatDefaultConfig|[ChatDefaultConfigReq](#schemachatdefaultconfigreq)|false|none|ChatDefaultConfigReq|none|
|»»»» dimensionIds|[integer]|false|none||none|
|»»»» metricIds|[integer]|false|none||none|
|»»» globalKnowledgeConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»» blackList|[string]|false|none||none|
|»»»» ruleList|[string]|false|none||none|
|»»»» whiteList|[string]|false|none||none|
|»»» knowledgeInfos|[[KnowledgeInfoReq](#schemaknowledgeinforeq)]|false|none||none|
|»»»» KnowledgeInfoReq|[KnowledgeInfoReq](#schemaknowledgeinforeq)|false|none|KnowledgeInfoReq|none|
|»»»»» bizName|string|false|none||none|
|»»»»» itemId|integer(int64)|false|none||none|
|»»»»» knowledgeAdvancedConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»»»» blackList|[string]|false|none||none|
|»»»»»» ruleList|[string]|false|none||none|
|»»»»»» whiteList|[string]|false|none||none|
|»»»»» searchEnable|boolean|false|none||none|
|»»»»» type|string|true|none||none|
|»»» visibility|[ItemVisibility](#schemaitemvisibility)|false|none|ItemVisibility|none|
|»»»» blackDimIdList|[integer]|false|none||none|
|»»»» blackMetricIdList|[integer]|false|none||none|
|»» chatDetailConfig|[ChatDetailConfigReq](#schemachatdetailconfigreq)|false|none|ChatDetailConfigReq|none|
|»»» chatDefaultConfig|[ChatDefaultConfigReq](#schemachatdefaultconfigreq)|false|none|ChatDefaultConfigReq|none|
|»»»» dimensionIds|[integer]|false|none||none|
|»»»» metricIds|[integer]|false|none||none|
|»»» globalKnowledgeConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»» blackList|[string]|false|none||none|
|»»»» ruleList|[string]|false|none||none|
|»»»» whiteList|[string]|false|none||none|
|»»» knowledgeInfos|[[KnowledgeInfoReq](#schemaknowledgeinforeq)]|false|none||none|
|»»»» KnowledgeInfoReq|[KnowledgeInfoReq](#schemaknowledgeinforeq)|false|none|KnowledgeInfoReq|none|
|»»»»» bizName|string|false|none||none|
|»»»»» itemId|integer(int64)|false|none||none|
|»»»»» knowledgeAdvancedConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none|KnowledgeAdvancedConfig|none|
|»»»»» searchEnable|boolean|false|none||none|
|»»»»» type|string|true|none||none|
|»»» visibility|[ItemVisibility](#schemaitemvisibility)|false|none|ItemVisibility|none|
|»»»» blackDimIdList|[integer]|false|none||none|
|»»»» blackMetricIdList|[integer]|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» llmExamples|string|false|none||none|
|»» modelId|integer(int64)|false|none||none|
|»» recommendedQuestions|[[RecommendedQuestionReq](#schemarecommendedquestionreq)]|false|none||none|
|»»» RecommendedQuestionReq|[RecommendedQuestionReq](#schemarecommendedquestionreq)|false|none|RecommendedQuestionReq|none|
|»»»» question|string|false|none||none|
|»» statusEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|
|statusEnum|DELETED|
|statusEnum|INITIALIZED|
|statusEnum|OFFLINE|
|statusEnum|ONLINE|
|statusEnum|UNAVAILABLE|
|statusEnum|UNKNOWN|

# chat-controller

<a id="opIddeleteConversionUsingPOST"></a>

## POST deleteConversion

POST /api/chat/manage/delete

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|chatId|query|integer(int64)| 是 ||chatId|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetAllConversionsUsingGET"></a>

## GET getAllConversions

GET /api/chat/manage/getAll

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|agentId|query|integer(int32)| 否 ||agentId|

> 返回示例

> 200 Response

```json
[
  {
    "agentId": 0,
    "chatId": 0,
    "chatName": "string",
    "createTime": "string",
    "creator": "string",
    "isDelete": 0,
    "isTop": 0,
    "lastQuestion": "string",
    "lastTime": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatDO](#schemachatdo)]|false|none||none|
|» ChatDO|[ChatDO](#schemachatdo)|false|none|ChatDO|none|
|»» agentId|integer(int32)|false|none||none|
|»» chatId|integer(int64)|false|none||none|
|»» chatName|string|false|none||none|
|»» createTime|string|false|none||none|
|»» creator|string|false|none||none|
|»» isDelete|integer(int32)|false|none||none|
|»» isTop|integer(int32)|false|none||none|
|»» lastQuestion|string|false|none||none|
|»» lastTime|string|false|none||none|

<a id="opIdgetChatQueryUsingGET"></a>

## GET getChatQuery

GET /api/chat/manage/getChatQuery/{queryId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|queryId|path|integer(int64)| 是 ||queryId|

> 返回示例

> 200 Response

```json
{
  "chatId": 0,
  "createTime": "2019-08-24T14:15:22Z",
  "feedback": "string",
  "parseInfos": [
    {
      "aggType": "AVG",
      "dataSet": {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      },
      "dateInfo": {
        "dateList": [
          "string"
        ],
        "dateMode": "ALL",
        "detectWord": "string",
        "endDate": "string",
        "groupByDate": true,
        "inherited": true,
        "period": "string",
        "startDate": "string",
        "unit": 0
      },
      "dimensionFilters": [
        {
          "bizName": "string",
          "elementID": 0,
          "function": "string",
          "name": "string",
          "operator": "!=",
          "value": {}
        }
      ],
      "dimensions": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            {}
          ],
          "schemaValueMaps": [
            {}
          ],
          "type": "DATASET",
          "useCnt": 0
        }
      ],
      "elementMatches": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "entity": {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      },
      "entityInfo": {
        "dataSetInfo": {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "primaryKey": "string",
          "value": "string",
          "words": [
            null
          ]
        },
        "dimensions": [
          {
            "bizName": null,
            "itemId": null,
            "name": null,
            "value": null
          }
        ],
        "entityId": "string",
        "metrics": [
          {
            "bizName": null,
            "itemId": null,
            "name": null,
            "value": null
          }
        ]
      },
      "filterType": "AND",
      "id": 0,
      "limit": 0,
      "metricFilters": [
        {
          "bizName": "string",
          "elementID": 0,
          "function": "string",
          "name": "string",
          "operator": "!=",
          "value": {}
        }
      ],
      "metrics": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            {}
          ],
          "schemaValueMaps": [
            {}
          ],
          "type": "DATASET",
          "useCnt": 0
        }
      ],
      "orders": [
        {
          "column": "string",
          "direction": "string"
        }
      ],
      "properties": {},
      "queryMode": "string",
      "queryType": "DETAIL",
      "score": 0,
      "sqlEvaluation": {
        "isValidated": true,
        "validateMsg": "string"
      },
      "sqlInfo": {
        "correctS2SQL": "string",
        "querySQL": "string",
        "s2SQL": "string",
        "sourceId": "string"
      },
      "textInfo": "string"
    }
  ],
  "parseTimeCost": {
    "parseStartTime": 0,
    "parseTime": 0,
    "sqlTime": 0
  },
  "queryResult": {
    "aggregateInfo": {
      "metricInfos": [
        {
          "date": "string",
          "dimension": "string",
          "name": "string",
          "statistics": {},
          "value": "string"
        }
      ]
    },
    "chatContext": {
      "aggType": "AVG",
      "dataSet": {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {}
        ],
        "schemaValueMaps": [
          {}
        ],
        "type": "DATASET",
        "useCnt": 0
      },
      "dateInfo": {
        "dateList": [
          "string"
        ],
        "dateMode": "ALL",
        "detectWord": "string",
        "endDate": "string",
        "groupByDate": true,
        "inherited": true,
        "period": "string",
        "startDate": "string",
        "unit": 0
      },
      "dimensionFilters": [
        {
          "bizName": "string",
          "elementID": 0,
          "function": "string",
          "name": "string",
          "operator": "[",
          "value": {}
        }
      ],
      "dimensions": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "elementMatches": [
        {
          "detectWord": "string",
          "element": {},
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "entity": {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {}
        ],
        "schemaValueMaps": [
          {}
        ],
        "type": "DATASET",
        "useCnt": 0
      },
      "entityInfo": {
        "dataSetInfo": {
          "bizName": null,
          "itemId": null,
          "name": null,
          "primaryKey": null,
          "value": null,
          "words": null
        },
        "dimensions": [
          {}
        ],
        "entityId": "string",
        "metrics": [
          {}
        ]
      },
      "filterType": "AND",
      "id": 0,
      "limit": 0,
      "metricFilters": [
        {
          "bizName": "string",
          "elementID": 0,
          "function": "string",
          "name": "string",
          "operator": "[",
          "value": {}
        }
      ],
      "metrics": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "orders": [
        {
          "column": "string",
          "direction": "string"
        }
      ],
      "properties": {},
      "queryMode": "string",
      "queryType": "DETAIL",
      "score": 0,
      "sqlEvaluation": {
        "isValidated": true,
        "validateMsg": "string"
      },
      "sqlInfo": {
        "correctS2SQL": "string",
        "querySQL": "string",
        "s2SQL": "string",
        "sourceId": "string"
      },
      "textInfo": "string"
    },
    "entityInfo": {
      "dataSetInfo": {
        "bizName": "string",
        "itemId": 0,
        "name": "string",
        "primaryKey": "string",
        "value": "string",
        "words": [
          "string"
        ]
      },
      "dimensions": [
        {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "value": "string"
        }
      ],
      "entityId": "string",
      "metrics": [
        {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "value": "string"
        }
      ]
    },
    "queryAuthorization": {
      "dimensionFilters": [
        "string"
      ],
      "dimensionFiltersDesc": [
        "string"
      ],
      "domainName": "string",
      "message": "string"
    },
    "queryColumns": [
      {
        "authorized": true,
        "comment": "string",
        "dataFormat": {
          "decimalPlaces": 0,
          "needMultiply100": true
        },
        "dataFormatType": "string",
        "name": "string",
        "nameEn": "string",
        "showType": "string",
        "type": "string"
      }
    ],
    "queryId": 0,
    "queryMode": "string",
    "queryResults": [
      {
        "property1": {},
        "property2": {}
      }
    ],
    "querySql": "string",
    "queryState": "EMPTY",
    "queryTimeCost": 0,
    "recommendedDimensions": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      }
    ],
    "response": {},
    "textResult": "string"
  },
  "queryText": "string",
  "questionId": 0,
  "score": 0,
  "similarQueries": [
    {
      "queryId": 0,
      "queryText": "string"
    }
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[QueryResp](#schemaqueryresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdpageQueryInfoUsingPOST"></a>

## POST pageQueryInfo

POST /api/chat/manage/pageQueryInfo

> Body 请求参数

```json
{
  "current": 0,
  "ids": [
    0
  ],
  "pageSize": 0,
  "userName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|chatId|query|integer(int64)| 是 ||chatId|
|body|body|[PageQueryInfoReq](#schemapagequeryinforeq)| 否 | PageQueryInfoReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "chatId": 0,
      "createTime": "2019-08-24T14:15:22Z",
      "feedback": "string",
      "parseInfos": [
        {
          "aggType": "AVG",
          "dataSet": {
            "alias": [
              "string"
            ],
            "bizName": "string",
            "dataFormatType": "string",
            "dataSet": 0,
            "dataSetName": "string",
            "defaultAgg": "string",
            "description": "string",
            "id": 0,
            "isTag": 0,
            "model": 0,
            "name": "string",
            "order": 0,
            "relatedSchemaElements": [
              {
                "dimensionId": 0,
                "necessary": true
              }
            ],
            "schemaValueMaps": [
              {
                "alias": [
                  "string"
                ],
                "bizName": "string",
                "techName": "string"
              }
            ],
            "type": "DATASET",
            "useCnt": 0
          },
          "dateInfo": {
            "dateList": [
              "string"
            ],
            "dateMode": "ALL",
            "detectWord": "string",
            "endDate": "string",
            "groupByDate": true,
            "inherited": true,
            "period": "string",
            "startDate": "string",
            "unit": 0
          },
          "dimensionFilters": [
            {
              "bizName": "string",
              "elementID": 0,
              "function": "string",
              "name": "string",
              "operator": "!=",
              "value": {}
            }
          ],
          "dimensions": [
            {
              "alias": [
                "string"
              ],
              "bizName": "string",
              "dataFormatType": "string",
              "dataSet": 0,
              "dataSetName": "string",
              "defaultAgg": "string",
              "description": "string",
              "id": 0,
              "isTag": 0,
              "model": 0,
              "name": "string",
              "order": 0,
              "relatedSchemaElements": [
                {
                  "dimensionId": 0,
                  "necessary": true
                }
              ],
              "schemaValueMaps": [
                {
                  "alias": [
                    "string"
                  ],
                  "bizName": "string",
                  "techName": "string"
                }
              ],
              "type": "DATASET",
              "useCnt": 0
            }
          ],
          "elementMatches": [
            {
              "detectWord": "string",
              "element": {
                "alias": [
                  "string"
                ],
                "bizName": "string",
                "dataFormatType": "string",
                "dataSet": 0,
                "dataSetName": "string",
                "defaultAgg": "string",
                "description": "string",
                "id": 0,
                "isTag": 0,
                "model": 0,
                "name": "string",
                "order": 0,
                "relatedSchemaElements": [
                  {
                    "dimensionId": 0,
                    "necessary": true
                  }
                ],
                "schemaValueMaps": [
                  {
                    "alias": "[Object]",
                    "bizName": "string",
                    "techName": "string"
                  }
                ],
                "type": "DATASET",
                "useCnt": 0
              },
              "frequency": 0,
              "inherited": true,
              "similarity": 0,
              "word": "string"
            }
          ],
          "entity": {
            "alias": [
              "string"
            ],
            "bizName": "string",
            "dataFormatType": "string",
            "dataSet": 0,
            "dataSetName": "string",
            "defaultAgg": "string",
            "description": "string",
            "id": 0,
            "isTag": 0,
            "model": 0,
            "name": "string",
            "order": 0,
            "relatedSchemaElements": [
              {
                "dimensionId": 0,
                "necessary": true
              }
            ],
            "schemaValueMaps": [
              {
                "alias": [
                  "string"
                ],
                "bizName": "string",
                "techName": "string"
              }
            ],
            "type": "DATASET",
            "useCnt": 0
          },
          "entityInfo": {
            "dataSetInfo": {
              "bizName": "string",
              "itemId": 0,
              "name": "string",
              "primaryKey": "string",
              "value": "string",
              "words": [
                "string"
              ]
            },
            "dimensions": [
              {
                "bizName": "string",
                "itemId": 0,
                "name": "string",
                "value": "string"
              }
            ],
            "entityId": "string",
            "metrics": [
              {
                "bizName": "string",
                "itemId": 0,
                "name": "string",
                "value": "string"
              }
            ]
          },
          "filterType": "AND",
          "id": 0,
          "limit": 0,
          "metricFilters": [
            {
              "bizName": "string",
              "elementID": 0,
              "function": "string",
              "name": "string",
              "operator": "!=",
              "value": {}
            }
          ],
          "metrics": [
            {
              "alias": [
                "string"
              ],
              "bizName": "string",
              "dataFormatType": "string",
              "dataSet": 0,
              "dataSetName": "string",
              "defaultAgg": "string",
              "description": "string",
              "id": 0,
              "isTag": 0,
              "model": 0,
              "name": "string",
              "order": 0,
              "relatedSchemaElements": [
                {
                  "dimensionId": 0,
                  "necessary": true
                }
              ],
              "schemaValueMaps": [
                {
                  "alias": [
                    "string"
                  ],
                  "bizName": "string",
                  "techName": "string"
                }
              ],
              "type": "DATASET",
              "useCnt": 0
            }
          ],
          "orders": [
            {
              "column": "string",
              "direction": "string"
            }
          ],
          "properties": {},
          "queryMode": "string",
          "queryType": "DETAIL",
          "score": 0,
          "sqlEvaluation": {
            "isValidated": true,
            "validateMsg": "string"
          },
          "sqlInfo": {
            "correctS2SQL": "string",
            "querySQL": "string",
            "s2SQL": "string",
            "sourceId": "string"
          },
          "textInfo": "string"
        }
      ],
      "parseTimeCost": {
        "parseStartTime": 0,
        "parseTime": 0,
        "sqlTime": 0
      },
      "queryResult": {
        "aggregateInfo": {
          "metricInfos": [
            {
              "date": "string",
              "dimension": "string",
              "name": "string",
              "statistics": {
                "property1": "string",
                "property2": "string"
              },
              "value": "string"
            }
          ]
        },
        "chatContext": {
          "aggType": "AVG",
          "dataSet": {
            "alias": [
              "string"
            ],
            "bizName": "string",
            "dataFormatType": "string",
            "dataSet": 0,
            "dataSetName": "string",
            "defaultAgg": "string",
            "description": "string",
            "id": 0,
            "isTag": 0,
            "model": 0,
            "name": "string",
            "order": 0,
            "relatedSchemaElements": [
              {
                "dimensionId": 0,
                "necessary": true
              }
            ],
            "schemaValueMaps": [
              {
                "alias": [
                  "string"
                ],
                "bizName": "string",
                "techName": "string"
              }
            ],
            "type": "DATASET",
            "useCnt": 0
          },
          "dateInfo": {
            "dateList": [
              "string"
            ],
            "dateMode": "ALL",
            "detectWord": "string",
            "endDate": "string",
            "groupByDate": true,
            "inherited": true,
            "period": "string",
            "startDate": "string",
            "unit": 0
          },
          "dimensionFilters": [
            {
              "bizName": "string",
              "elementID": 0,
              "function": "string",
              "name": "string",
              "operator": "!=",
              "value": {}
            }
          ],
          "dimensions": [
            {
              "alias": [
                "string"
              ],
              "bizName": "string",
              "dataFormatType": "string",
              "dataSet": 0,
              "dataSetName": "string",
              "defaultAgg": "string",
              "description": "string",
              "id": 0,
              "isTag": 0,
              "model": 0,
              "name": "string",
              "order": 0,
              "relatedSchemaElements": [
                {
                  "dimensionId": 0,
                  "necessary": true
                }
              ],
              "schemaValueMaps": [
                {
                  "alias": [
                    "string"
                  ],
                  "bizName": "string",
                  "techName": "string"
                }
              ],
              "type": "DATASET",
              "useCnt": 0
            }
          ],
          "elementMatches": [
            {
              "detectWord": "string",
              "element": {
                "alias": [
                  "string"
                ],
                "bizName": "string",
                "dataFormatType": "string",
                "dataSet": 0,
                "dataSetName": "string",
                "defaultAgg": "string",
                "description": "string",
                "id": 0,
                "isTag": 0,
                "model": 0,
                "name": "string",
                "order": 0,
                "relatedSchemaElements": [
                  {
                    "dimensionId": 0,
                    "necessary": true
                  }
                ],
                "schemaValueMaps": [
                  {
                    "alias": "[Object]",
                    "bizName": "string",
                    "techName": "string"
                  }
                ],
                "type": "DATASET",
                "useCnt": 0
              },
              "frequency": 0,
              "inherited": true,
              "similarity": 0,
              "word": "string"
            }
          ],
          "entity": {
            "alias": [
              "string"
            ],
            "bizName": "string",
            "dataFormatType": "string",
            "dataSet": 0,
            "dataSetName": "string",
            "defaultAgg": "string",
            "description": "string",
            "id": 0,
            "isTag": 0,
            "model": 0,
            "name": "string",
            "order": 0,
            "relatedSchemaElements": [
              {
                "dimensionId": 0,
                "necessary": true
              }
            ],
            "schemaValueMaps": [
              {
                "alias": [
                  "string"
                ],
                "bizName": "string",
                "techName": "string"
              }
            ],
            "type": "DATASET",
            "useCnt": 0
          },
          "entityInfo": {
            "dataSetInfo": {
              "bizName": "string",
              "itemId": 0,
              "name": "string",
              "primaryKey": "string",
              "value": "string",
              "words": [
                "string"
              ]
            },
            "dimensions": [
              {
                "bizName": "string",
                "itemId": 0,
                "name": "string",
                "value": "string"
              }
            ],
            "entityId": "string",
            "metrics": [
              {
                "bizName": "string",
                "itemId": 0,
                "name": "string",
                "value": "string"
              }
            ]
          },
          "filterType": "AND",
          "id": 0,
          "limit": 0,
          "metricFilters": [
            {
              "bizName": "string",
              "elementID": 0,
              "function": "string",
              "name": "string",
              "operator": "!=",
              "value": {}
            }
          ],
          "metrics": [
            {
              "alias": [
                "string"
              ],
              "bizName": "string",
              "dataFormatType": "string",
              "dataSet": 0,
              "dataSetName": "string",
              "defaultAgg": "string",
              "description": "string",
              "id": 0,
              "isTag": 0,
              "model": 0,
              "name": "string",
              "order": 0,
              "relatedSchemaElements": [
                {
                  "dimensionId": 0,
                  "necessary": true
                }
              ],
              "schemaValueMaps": [
                {
                  "alias": [
                    "string"
                  ],
                  "bizName": "string",
                  "techName": "string"
                }
              ],
              "type": "DATASET",
              "useCnt": 0
            }
          ],
          "orders": [
            {
              "column": "string",
              "direction": "string"
            }
          ],
          "properties": {},
          "queryMode": "string",
          "queryType": "DETAIL",
          "score": 0,
          "sqlEvaluation": {
            "isValidated": true,
            "validateMsg": "string"
          },
          "sqlInfo": {
            "correctS2SQL": "string",
            "querySQL": "string",
            "s2SQL": "string",
            "sourceId": "string"
          },
          "textInfo": "string"
        },
        "entityInfo": {
          "dataSetInfo": {
            "bizName": "string",
            "itemId": 0,
            "name": "string",
            "primaryKey": "string",
            "value": "string",
            "words": [
              "string"
            ]
          },
          "dimensions": [
            {
              "bizName": "string",
              "itemId": 0,
              "name": "string",
              "value": "string"
            }
          ],
          "entityId": "string",
          "metrics": [
            {
              "bizName": "string",
              "itemId": 0,
              "name": "string",
              "value": "string"
            }
          ]
        },
        "queryAuthorization": {
          "dimensionFilters": [
            "string"
          ],
          "dimensionFiltersDesc": [
            "string"
          ],
          "domainName": "string",
          "message": "string"
        },
        "queryColumns": [
          {
            "authorized": true,
            "comment": "string",
            "dataFormat": {
              "decimalPlaces": 0,
              "needMultiply100": true
            },
            "dataFormatType": "string",
            "name": "string",
            "nameEn": "string",
            "showType": "string",
            "type": "string"
          }
        ],
        "queryId": 0,
        "queryMode": "string",
        "queryResults": [
          {
            "property1": {},
            "property2": {}
          }
        ],
        "querySql": "string",
        "queryState": "EMPTY",
        "queryTimeCost": 0,
        "recommendedDimensions": [
          {
            "alias": [
              "string"
            ],
            "bizName": "string",
            "dataFormatType": "string",
            "dataSet": 0,
            "dataSetName": "string",
            "defaultAgg": "string",
            "description": "string",
            "id": 0,
            "isTag": 0,
            "model": 0,
            "name": "string",
            "order": 0,
            "relatedSchemaElements": [
              {
                "dimensionId": 0,
                "necessary": true
              }
            ],
            "schemaValueMaps": [
              {
                "alias": [
                  "string"
                ],
                "bizName": "string",
                "techName": "string"
              }
            ],
            "type": "DATASET",
            "useCnt": 0
          }
        ],
        "response": {},
        "textResult": "string"
      },
      "queryText": "string",
      "questionId": 0,
      "score": 0,
      "similarQueries": [
        {
          "queryId": 0,
          "queryText": "string"
        }
      ]
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryShowCaseUsingPOST"></a>

## POST queryShowCase

POST /api/chat/manage/queryShowCase

> Body 请求参数

```json
{
  "current": 0,
  "ids": [
    0
  ],
  "pageSize": 0,
  "userName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|agentId|query|integer(int32)| 是 ||agentId|
|body|body|[PageQueryInfoReq](#schemapagequeryinforeq)| 否 | PageQueryInfoReq|none|

> 返回示例

> 200 Response

```json
{
  "current": 0,
  "pageSize": 0,
  "showCaseMap": {
    "property1": [
      {
        "chatId": 0,
        "createTime": "2019-08-24T14:15:22Z",
        "feedback": "string",
        "parseInfos": [
          {
            "aggType": "[",
            "dataSet": {},
            "dateInfo": {},
            "dimensionFilters": [
              null
            ],
            "dimensions": [
              null
            ],
            "elementMatches": [
              null
            ],
            "entity": {},
            "entityInfo": {},
            "filterType": "[",
            "id": 0,
            "limit": 0,
            "metricFilters": [
              null
            ],
            "metrics": [
              null
            ],
            "orders": [
              null
            ],
            "properties": {},
            "queryMode": "string",
            "queryType": "[",
            "score": 0,
            "sqlEvaluation": {},
            "sqlInfo": {},
            "textInfo": "string"
          }
        ],
        "parseTimeCost": {
          "parseStartTime": 0,
          "parseTime": 0,
          "sqlTime": 0
        },
        "queryResult": {
          "aggregateInfo": {
            "metricInfos": null
          },
          "chatContext": {
            "aggType": null,
            "dataSet": null,
            "dateInfo": null,
            "dimensionFilters": null,
            "dimensions": null,
            "elementMatches": null,
            "entity": null,
            "entityInfo": null,
            "filterType": null,
            "id": null,
            "limit": null,
            "metricFilters": null,
            "metrics": null,
            "orders": null,
            "properties": null,
            "queryMode": null,
            "queryType": null,
            "score": null,
            "sqlEvaluation": null,
            "sqlInfo": null,
            "textInfo": null
          },
          "entityInfo": {
            "dataSetInfo": null,
            "dimensions": null,
            "entityId": null,
            "metrics": null
          },
          "queryAuthorization": {
            "dimensionFilters": null,
            "dimensionFiltersDesc": null,
            "domainName": null,
            "message": null
          },
          "queryColumns": [
            {}
          ],
          "queryId": 0,
          "queryMode": "string",
          "queryResults": [
            {}
          ],
          "querySql": "string",
          "queryState": "EMPTY",
          "queryTimeCost": 0,
          "recommendedDimensions": [
            {}
          ],
          "response": {},
          "textResult": "string"
        },
        "queryText": "string",
        "questionId": 0,
        "score": 0,
        "similarQueries": [
          {
            "queryId": 0,
            "queryText": "string"
          }
        ]
      }
    ],
    "property2": [
      {
        "chatId": 0,
        "createTime": "2019-08-24T14:15:22Z",
        "feedback": "string",
        "parseInfos": [
          {
            "aggType": "[",
            "dataSet": {},
            "dateInfo": {},
            "dimensionFilters": [
              null
            ],
            "dimensions": [
              null
            ],
            "elementMatches": [
              null
            ],
            "entity": {},
            "entityInfo": {},
            "filterType": "[",
            "id": 0,
            "limit": 0,
            "metricFilters": [
              null
            ],
            "metrics": [
              null
            ],
            "orders": [
              null
            ],
            "properties": {},
            "queryMode": "string",
            "queryType": "[",
            "score": 0,
            "sqlEvaluation": {},
            "sqlInfo": {},
            "textInfo": "string"
          }
        ],
        "parseTimeCost": {
          "parseStartTime": 0,
          "parseTime": 0,
          "sqlTime": 0
        },
        "queryResult": {
          "aggregateInfo": {
            "metricInfos": null
          },
          "chatContext": {
            "aggType": null,
            "dataSet": null,
            "dateInfo": null,
            "dimensionFilters": null,
            "dimensions": null,
            "elementMatches": null,
            "entity": null,
            "entityInfo": null,
            "filterType": null,
            "id": null,
            "limit": null,
            "metricFilters": null,
            "metrics": null,
            "orders": null,
            "properties": null,
            "queryMode": null,
            "queryType": null,
            "score": null,
            "sqlEvaluation": null,
            "sqlInfo": null,
            "textInfo": null
          },
          "entityInfo": {
            "dataSetInfo": null,
            "dimensions": null,
            "entityId": null,
            "metrics": null
          },
          "queryAuthorization": {
            "dimensionFilters": null,
            "dimensionFiltersDesc": null,
            "domainName": null,
            "message": null
          },
          "queryColumns": [
            {}
          ],
          "queryId": 0,
          "queryMode": "string",
          "queryResults": [
            {}
          ],
          "querySql": "string",
          "queryState": "EMPTY",
          "queryTimeCost": 0,
          "recommendedDimensions": [
            {}
          ],
          "response": {},
          "textResult": "string"
        },
        "queryText": "string",
        "questionId": 0,
        "score": 0,
        "similarQueries": [
          {
            "queryId": 0,
            "queryText": "string"
          }
        ]
      }
    ]
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ShowCaseResp](#schemashowcaseresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdsaveUsingPOST_1"></a>

## POST save

POST /api/chat/manage/save

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|chatName|query|string| 是 ||chatName|
|agentId|query|integer(int32)| 否 ||agentId|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdupdateConversionIsTopUsingPOST"></a>

## POST updateConversionIsTop

POST /api/chat/manage/updateChatIsTop

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|chatId|query|integer(int64)| 是 ||chatId|
|isTop|query|integer(int32)| 是 ||isTop|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdupdateConversionNameUsingPOST"></a>

## POST updateConversionName

POST /api/chat/manage/updateChatName

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|chatId|query|integer(int64)| 是 ||chatId|
|chatName|query|string| 是 ||chatName|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdupdateQAFeedbackUsingPOST"></a>

## POST updateQAFeedback

POST /api/chat/manage/updateQAFeedback

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|query|integer(int32)| 是 ||id|
|score|query|integer(int32)| 是 ||score|
|feedback|query|string| 否 ||feedback|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteConversionUsingPOST_1"></a>

## POST deleteConversion

POST /openapi/chat/manage/delete

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|chatId|query|integer(int64)| 是 ||chatId|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetAllConversionsUsingGET_1"></a>

## GET getAllConversions

GET /openapi/chat/manage/getAll

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|agentId|query|integer(int32)| 否 ||agentId|

> 返回示例

> 200 Response

```json
[
  {
    "agentId": 0,
    "chatId": 0,
    "chatName": "string",
    "createTime": "string",
    "creator": "string",
    "isDelete": 0,
    "isTop": 0,
    "lastQuestion": "string",
    "lastTime": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatDO](#schemachatdo)]|false|none||none|
|» ChatDO|[ChatDO](#schemachatdo)|false|none|ChatDO|none|
|»» agentId|integer(int32)|false|none||none|
|»» chatId|integer(int64)|false|none||none|
|»» chatName|string|false|none||none|
|»» createTime|string|false|none||none|
|»» creator|string|false|none||none|
|»» isDelete|integer(int32)|false|none||none|
|»» isTop|integer(int32)|false|none||none|
|»» lastQuestion|string|false|none||none|
|»» lastTime|string|false|none||none|

<a id="opIdgetChatQueryUsingGET_1"></a>

## GET getChatQuery

GET /openapi/chat/manage/getChatQuery/{queryId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|queryId|path|integer(int64)| 是 ||queryId|

> 返回示例

> 200 Response

```json
{
  "chatId": 0,
  "createTime": "2019-08-24T14:15:22Z",
  "feedback": "string",
  "parseInfos": [
    {
      "aggType": "AVG",
      "dataSet": {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      },
      "dateInfo": {
        "dateList": [
          "string"
        ],
        "dateMode": "ALL",
        "detectWord": "string",
        "endDate": "string",
        "groupByDate": true,
        "inherited": true,
        "period": "string",
        "startDate": "string",
        "unit": 0
      },
      "dimensionFilters": [
        {
          "bizName": "string",
          "elementID": 0,
          "function": "string",
          "name": "string",
          "operator": "!=",
          "value": {}
        }
      ],
      "dimensions": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            {}
          ],
          "schemaValueMaps": [
            {}
          ],
          "type": "DATASET",
          "useCnt": 0
        }
      ],
      "elementMatches": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "entity": {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      },
      "entityInfo": {
        "dataSetInfo": {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "primaryKey": "string",
          "value": "string",
          "words": [
            null
          ]
        },
        "dimensions": [
          {
            "bizName": null,
            "itemId": null,
            "name": null,
            "value": null
          }
        ],
        "entityId": "string",
        "metrics": [
          {
            "bizName": null,
            "itemId": null,
            "name": null,
            "value": null
          }
        ]
      },
      "filterType": "AND",
      "id": 0,
      "limit": 0,
      "metricFilters": [
        {
          "bizName": "string",
          "elementID": 0,
          "function": "string",
          "name": "string",
          "operator": "!=",
          "value": {}
        }
      ],
      "metrics": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            {}
          ],
          "schemaValueMaps": [
            {}
          ],
          "type": "DATASET",
          "useCnt": 0
        }
      ],
      "orders": [
        {
          "column": "string",
          "direction": "string"
        }
      ],
      "properties": {},
      "queryMode": "string",
      "queryType": "DETAIL",
      "score": 0,
      "sqlEvaluation": {
        "isValidated": true,
        "validateMsg": "string"
      },
      "sqlInfo": {
        "correctS2SQL": "string",
        "querySQL": "string",
        "s2SQL": "string",
        "sourceId": "string"
      },
      "textInfo": "string"
    }
  ],
  "parseTimeCost": {
    "parseStartTime": 0,
    "parseTime": 0,
    "sqlTime": 0
  },
  "queryResult": {
    "aggregateInfo": {
      "metricInfos": [
        {
          "date": "string",
          "dimension": "string",
          "name": "string",
          "statistics": {},
          "value": "string"
        }
      ]
    },
    "chatContext": {
      "aggType": "AVG",
      "dataSet": {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {}
        ],
        "schemaValueMaps": [
          {}
        ],
        "type": "DATASET",
        "useCnt": 0
      },
      "dateInfo": {
        "dateList": [
          "string"
        ],
        "dateMode": "ALL",
        "detectWord": "string",
        "endDate": "string",
        "groupByDate": true,
        "inherited": true,
        "period": "string",
        "startDate": "string",
        "unit": 0
      },
      "dimensionFilters": [
        {
          "bizName": "string",
          "elementID": 0,
          "function": "string",
          "name": "string",
          "operator": "[",
          "value": {}
        }
      ],
      "dimensions": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "elementMatches": [
        {
          "detectWord": "string",
          "element": {},
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "entity": {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {}
        ],
        "schemaValueMaps": [
          {}
        ],
        "type": "DATASET",
        "useCnt": 0
      },
      "entityInfo": {
        "dataSetInfo": {
          "bizName": null,
          "itemId": null,
          "name": null,
          "primaryKey": null,
          "value": null,
          "words": null
        },
        "dimensions": [
          {}
        ],
        "entityId": "string",
        "metrics": [
          {}
        ]
      },
      "filterType": "AND",
      "id": 0,
      "limit": 0,
      "metricFilters": [
        {
          "bizName": "string",
          "elementID": 0,
          "function": "string",
          "name": "string",
          "operator": "[",
          "value": {}
        }
      ],
      "metrics": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "orders": [
        {
          "column": "string",
          "direction": "string"
        }
      ],
      "properties": {},
      "queryMode": "string",
      "queryType": "DETAIL",
      "score": 0,
      "sqlEvaluation": {
        "isValidated": true,
        "validateMsg": "string"
      },
      "sqlInfo": {
        "correctS2SQL": "string",
        "querySQL": "string",
        "s2SQL": "string",
        "sourceId": "string"
      },
      "textInfo": "string"
    },
    "entityInfo": {
      "dataSetInfo": {
        "bizName": "string",
        "itemId": 0,
        "name": "string",
        "primaryKey": "string",
        "value": "string",
        "words": [
          "string"
        ]
      },
      "dimensions": [
        {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "value": "string"
        }
      ],
      "entityId": "string",
      "metrics": [
        {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "value": "string"
        }
      ]
    },
    "queryAuthorization": {
      "dimensionFilters": [
        "string"
      ],
      "dimensionFiltersDesc": [
        "string"
      ],
      "domainName": "string",
      "message": "string"
    },
    "queryColumns": [
      {
        "authorized": true,
        "comment": "string",
        "dataFormat": {
          "decimalPlaces": 0,
          "needMultiply100": true
        },
        "dataFormatType": "string",
        "name": "string",
        "nameEn": "string",
        "showType": "string",
        "type": "string"
      }
    ],
    "queryId": 0,
    "queryMode": "string",
    "queryResults": [
      {
        "property1": {},
        "property2": {}
      }
    ],
    "querySql": "string",
    "queryState": "EMPTY",
    "queryTimeCost": 0,
    "recommendedDimensions": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      }
    ],
    "response": {},
    "textResult": "string"
  },
  "queryText": "string",
  "questionId": 0,
  "score": 0,
  "similarQueries": [
    {
      "queryId": 0,
      "queryText": "string"
    }
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[QueryResp](#schemaqueryresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdpageQueryInfoUsingPOST_1"></a>

## POST pageQueryInfo

POST /openapi/chat/manage/pageQueryInfo

> Body 请求参数

```json
{
  "current": 0,
  "ids": [
    0
  ],
  "pageSize": 0,
  "userName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|chatId|query|integer(int64)| 是 ||chatId|
|body|body|[PageQueryInfoReq](#schemapagequeryinforeq)| 否 | PageQueryInfoReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "chatId": 0,
      "createTime": "2019-08-24T14:15:22Z",
      "feedback": "string",
      "parseInfos": [
        {
          "aggType": "AVG",
          "dataSet": {
            "alias": [
              "string"
            ],
            "bizName": "string",
            "dataFormatType": "string",
            "dataSet": 0,
            "dataSetName": "string",
            "defaultAgg": "string",
            "description": "string",
            "id": 0,
            "isTag": 0,
            "model": 0,
            "name": "string",
            "order": 0,
            "relatedSchemaElements": [
              {
                "dimensionId": 0,
                "necessary": true
              }
            ],
            "schemaValueMaps": [
              {
                "alias": [
                  "string"
                ],
                "bizName": "string",
                "techName": "string"
              }
            ],
            "type": "DATASET",
            "useCnt": 0
          },
          "dateInfo": {
            "dateList": [
              "string"
            ],
            "dateMode": "ALL",
            "detectWord": "string",
            "endDate": "string",
            "groupByDate": true,
            "inherited": true,
            "period": "string",
            "startDate": "string",
            "unit": 0
          },
          "dimensionFilters": [
            {
              "bizName": "string",
              "elementID": 0,
              "function": "string",
              "name": "string",
              "operator": "!=",
              "value": {}
            }
          ],
          "dimensions": [
            {
              "alias": [
                "string"
              ],
              "bizName": "string",
              "dataFormatType": "string",
              "dataSet": 0,
              "dataSetName": "string",
              "defaultAgg": "string",
              "description": "string",
              "id": 0,
              "isTag": 0,
              "model": 0,
              "name": "string",
              "order": 0,
              "relatedSchemaElements": [
                {
                  "dimensionId": 0,
                  "necessary": true
                }
              ],
              "schemaValueMaps": [
                {
                  "alias": [
                    "string"
                  ],
                  "bizName": "string",
                  "techName": "string"
                }
              ],
              "type": "DATASET",
              "useCnt": 0
            }
          ],
          "elementMatches": [
            {
              "detectWord": "string",
              "element": {
                "alias": [
                  "string"
                ],
                "bizName": "string",
                "dataFormatType": "string",
                "dataSet": 0,
                "dataSetName": "string",
                "defaultAgg": "string",
                "description": "string",
                "id": 0,
                "isTag": 0,
                "model": 0,
                "name": "string",
                "order": 0,
                "relatedSchemaElements": [
                  {
                    "dimensionId": 0,
                    "necessary": true
                  }
                ],
                "schemaValueMaps": [
                  {
                    "alias": "[Object]",
                    "bizName": "string",
                    "techName": "string"
                  }
                ],
                "type": "DATASET",
                "useCnt": 0
              },
              "frequency": 0,
              "inherited": true,
              "similarity": 0,
              "word": "string"
            }
          ],
          "entity": {
            "alias": [
              "string"
            ],
            "bizName": "string",
            "dataFormatType": "string",
            "dataSet": 0,
            "dataSetName": "string",
            "defaultAgg": "string",
            "description": "string",
            "id": 0,
            "isTag": 0,
            "model": 0,
            "name": "string",
            "order": 0,
            "relatedSchemaElements": [
              {
                "dimensionId": 0,
                "necessary": true
              }
            ],
            "schemaValueMaps": [
              {
                "alias": [
                  "string"
                ],
                "bizName": "string",
                "techName": "string"
              }
            ],
            "type": "DATASET",
            "useCnt": 0
          },
          "entityInfo": {
            "dataSetInfo": {
              "bizName": "string",
              "itemId": 0,
              "name": "string",
              "primaryKey": "string",
              "value": "string",
              "words": [
                "string"
              ]
            },
            "dimensions": [
              {
                "bizName": "string",
                "itemId": 0,
                "name": "string",
                "value": "string"
              }
            ],
            "entityId": "string",
            "metrics": [
              {
                "bizName": "string",
                "itemId": 0,
                "name": "string",
                "value": "string"
              }
            ]
          },
          "filterType": "AND",
          "id": 0,
          "limit": 0,
          "metricFilters": [
            {
              "bizName": "string",
              "elementID": 0,
              "function": "string",
              "name": "string",
              "operator": "!=",
              "value": {}
            }
          ],
          "metrics": [
            {
              "alias": [
                "string"
              ],
              "bizName": "string",
              "dataFormatType": "string",
              "dataSet": 0,
              "dataSetName": "string",
              "defaultAgg": "string",
              "description": "string",
              "id": 0,
              "isTag": 0,
              "model": 0,
              "name": "string",
              "order": 0,
              "relatedSchemaElements": [
                {
                  "dimensionId": 0,
                  "necessary": true
                }
              ],
              "schemaValueMaps": [
                {
                  "alias": [
                    "string"
                  ],
                  "bizName": "string",
                  "techName": "string"
                }
              ],
              "type": "DATASET",
              "useCnt": 0
            }
          ],
          "orders": [
            {
              "column": "string",
              "direction": "string"
            }
          ],
          "properties": {},
          "queryMode": "string",
          "queryType": "DETAIL",
          "score": 0,
          "sqlEvaluation": {
            "isValidated": true,
            "validateMsg": "string"
          },
          "sqlInfo": {
            "correctS2SQL": "string",
            "querySQL": "string",
            "s2SQL": "string",
            "sourceId": "string"
          },
          "textInfo": "string"
        }
      ],
      "parseTimeCost": {
        "parseStartTime": 0,
        "parseTime": 0,
        "sqlTime": 0
      },
      "queryResult": {
        "aggregateInfo": {
          "metricInfos": [
            {
              "date": "string",
              "dimension": "string",
              "name": "string",
              "statistics": {
                "property1": "string",
                "property2": "string"
              },
              "value": "string"
            }
          ]
        },
        "chatContext": {
          "aggType": "AVG",
          "dataSet": {
            "alias": [
              "string"
            ],
            "bizName": "string",
            "dataFormatType": "string",
            "dataSet": 0,
            "dataSetName": "string",
            "defaultAgg": "string",
            "description": "string",
            "id": 0,
            "isTag": 0,
            "model": 0,
            "name": "string",
            "order": 0,
            "relatedSchemaElements": [
              {
                "dimensionId": 0,
                "necessary": true
              }
            ],
            "schemaValueMaps": [
              {
                "alias": [
                  "string"
                ],
                "bizName": "string",
                "techName": "string"
              }
            ],
            "type": "DATASET",
            "useCnt": 0
          },
          "dateInfo": {
            "dateList": [
              "string"
            ],
            "dateMode": "ALL",
            "detectWord": "string",
            "endDate": "string",
            "groupByDate": true,
            "inherited": true,
            "period": "string",
            "startDate": "string",
            "unit": 0
          },
          "dimensionFilters": [
            {
              "bizName": "string",
              "elementID": 0,
              "function": "string",
              "name": "string",
              "operator": "!=",
              "value": {}
            }
          ],
          "dimensions": [
            {
              "alias": [
                "string"
              ],
              "bizName": "string",
              "dataFormatType": "string",
              "dataSet": 0,
              "dataSetName": "string",
              "defaultAgg": "string",
              "description": "string",
              "id": 0,
              "isTag": 0,
              "model": 0,
              "name": "string",
              "order": 0,
              "relatedSchemaElements": [
                {
                  "dimensionId": 0,
                  "necessary": true
                }
              ],
              "schemaValueMaps": [
                {
                  "alias": [
                    "string"
                  ],
                  "bizName": "string",
                  "techName": "string"
                }
              ],
              "type": "DATASET",
              "useCnt": 0
            }
          ],
          "elementMatches": [
            {
              "detectWord": "string",
              "element": {
                "alias": [
                  "string"
                ],
                "bizName": "string",
                "dataFormatType": "string",
                "dataSet": 0,
                "dataSetName": "string",
                "defaultAgg": "string",
                "description": "string",
                "id": 0,
                "isTag": 0,
                "model": 0,
                "name": "string",
                "order": 0,
                "relatedSchemaElements": [
                  {
                    "dimensionId": 0,
                    "necessary": true
                  }
                ],
                "schemaValueMaps": [
                  {
                    "alias": "[Object]",
                    "bizName": "string",
                    "techName": "string"
                  }
                ],
                "type": "DATASET",
                "useCnt": 0
              },
              "frequency": 0,
              "inherited": true,
              "similarity": 0,
              "word": "string"
            }
          ],
          "entity": {
            "alias": [
              "string"
            ],
            "bizName": "string",
            "dataFormatType": "string",
            "dataSet": 0,
            "dataSetName": "string",
            "defaultAgg": "string",
            "description": "string",
            "id": 0,
            "isTag": 0,
            "model": 0,
            "name": "string",
            "order": 0,
            "relatedSchemaElements": [
              {
                "dimensionId": 0,
                "necessary": true
              }
            ],
            "schemaValueMaps": [
              {
                "alias": [
                  "string"
                ],
                "bizName": "string",
                "techName": "string"
              }
            ],
            "type": "DATASET",
            "useCnt": 0
          },
          "entityInfo": {
            "dataSetInfo": {
              "bizName": "string",
              "itemId": 0,
              "name": "string",
              "primaryKey": "string",
              "value": "string",
              "words": [
                "string"
              ]
            },
            "dimensions": [
              {
                "bizName": "string",
                "itemId": 0,
                "name": "string",
                "value": "string"
              }
            ],
            "entityId": "string",
            "metrics": [
              {
                "bizName": "string",
                "itemId": 0,
                "name": "string",
                "value": "string"
              }
            ]
          },
          "filterType": "AND",
          "id": 0,
          "limit": 0,
          "metricFilters": [
            {
              "bizName": "string",
              "elementID": 0,
              "function": "string",
              "name": "string",
              "operator": "!=",
              "value": {}
            }
          ],
          "metrics": [
            {
              "alias": [
                "string"
              ],
              "bizName": "string",
              "dataFormatType": "string",
              "dataSet": 0,
              "dataSetName": "string",
              "defaultAgg": "string",
              "description": "string",
              "id": 0,
              "isTag": 0,
              "model": 0,
              "name": "string",
              "order": 0,
              "relatedSchemaElements": [
                {
                  "dimensionId": 0,
                  "necessary": true
                }
              ],
              "schemaValueMaps": [
                {
                  "alias": [
                    "string"
                  ],
                  "bizName": "string",
                  "techName": "string"
                }
              ],
              "type": "DATASET",
              "useCnt": 0
            }
          ],
          "orders": [
            {
              "column": "string",
              "direction": "string"
            }
          ],
          "properties": {},
          "queryMode": "string",
          "queryType": "DETAIL",
          "score": 0,
          "sqlEvaluation": {
            "isValidated": true,
            "validateMsg": "string"
          },
          "sqlInfo": {
            "correctS2SQL": "string",
            "querySQL": "string",
            "s2SQL": "string",
            "sourceId": "string"
          },
          "textInfo": "string"
        },
        "entityInfo": {
          "dataSetInfo": {
            "bizName": "string",
            "itemId": 0,
            "name": "string",
            "primaryKey": "string",
            "value": "string",
            "words": [
              "string"
            ]
          },
          "dimensions": [
            {
              "bizName": "string",
              "itemId": 0,
              "name": "string",
              "value": "string"
            }
          ],
          "entityId": "string",
          "metrics": [
            {
              "bizName": "string",
              "itemId": 0,
              "name": "string",
              "value": "string"
            }
          ]
        },
        "queryAuthorization": {
          "dimensionFilters": [
            "string"
          ],
          "dimensionFiltersDesc": [
            "string"
          ],
          "domainName": "string",
          "message": "string"
        },
        "queryColumns": [
          {
            "authorized": true,
            "comment": "string",
            "dataFormat": {
              "decimalPlaces": 0,
              "needMultiply100": true
            },
            "dataFormatType": "string",
            "name": "string",
            "nameEn": "string",
            "showType": "string",
            "type": "string"
          }
        ],
        "queryId": 0,
        "queryMode": "string",
        "queryResults": [
          {
            "property1": {},
            "property2": {}
          }
        ],
        "querySql": "string",
        "queryState": "EMPTY",
        "queryTimeCost": 0,
        "recommendedDimensions": [
          {
            "alias": [
              "string"
            ],
            "bizName": "string",
            "dataFormatType": "string",
            "dataSet": 0,
            "dataSetName": "string",
            "defaultAgg": "string",
            "description": "string",
            "id": 0,
            "isTag": 0,
            "model": 0,
            "name": "string",
            "order": 0,
            "relatedSchemaElements": [
              {
                "dimensionId": 0,
                "necessary": true
              }
            ],
            "schemaValueMaps": [
              {
                "alias": [
                  "string"
                ],
                "bizName": "string",
                "techName": "string"
              }
            ],
            "type": "DATASET",
            "useCnt": 0
          }
        ],
        "response": {},
        "textResult": "string"
      },
      "queryText": "string",
      "questionId": 0,
      "score": 0,
      "similarQueries": [
        {
          "queryId": 0,
          "queryText": "string"
        }
      ]
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryShowCaseUsingPOST_1"></a>

## POST queryShowCase

POST /openapi/chat/manage/queryShowCase

> Body 请求参数

```json
{
  "current": 0,
  "ids": [
    0
  ],
  "pageSize": 0,
  "userName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|agentId|query|integer(int32)| 是 ||agentId|
|body|body|[PageQueryInfoReq](#schemapagequeryinforeq)| 否 | PageQueryInfoReq|none|

> 返回示例

> 200 Response

```json
{
  "current": 0,
  "pageSize": 0,
  "showCaseMap": {
    "property1": [
      {
        "chatId": 0,
        "createTime": "2019-08-24T14:15:22Z",
        "feedback": "string",
        "parseInfos": [
          {
            "aggType": "[",
            "dataSet": {},
            "dateInfo": {},
            "dimensionFilters": [
              null
            ],
            "dimensions": [
              null
            ],
            "elementMatches": [
              null
            ],
            "entity": {},
            "entityInfo": {},
            "filterType": "[",
            "id": 0,
            "limit": 0,
            "metricFilters": [
              null
            ],
            "metrics": [
              null
            ],
            "orders": [
              null
            ],
            "properties": {},
            "queryMode": "string",
            "queryType": "[",
            "score": 0,
            "sqlEvaluation": {},
            "sqlInfo": {},
            "textInfo": "string"
          }
        ],
        "parseTimeCost": {
          "parseStartTime": 0,
          "parseTime": 0,
          "sqlTime": 0
        },
        "queryResult": {
          "aggregateInfo": {
            "metricInfos": null
          },
          "chatContext": {
            "aggType": null,
            "dataSet": null,
            "dateInfo": null,
            "dimensionFilters": null,
            "dimensions": null,
            "elementMatches": null,
            "entity": null,
            "entityInfo": null,
            "filterType": null,
            "id": null,
            "limit": null,
            "metricFilters": null,
            "metrics": null,
            "orders": null,
            "properties": null,
            "queryMode": null,
            "queryType": null,
            "score": null,
            "sqlEvaluation": null,
            "sqlInfo": null,
            "textInfo": null
          },
          "entityInfo": {
            "dataSetInfo": null,
            "dimensions": null,
            "entityId": null,
            "metrics": null
          },
          "queryAuthorization": {
            "dimensionFilters": null,
            "dimensionFiltersDesc": null,
            "domainName": null,
            "message": null
          },
          "queryColumns": [
            {}
          ],
          "queryId": 0,
          "queryMode": "string",
          "queryResults": [
            {}
          ],
          "querySql": "string",
          "queryState": "EMPTY",
          "queryTimeCost": 0,
          "recommendedDimensions": [
            {}
          ],
          "response": {},
          "textResult": "string"
        },
        "queryText": "string",
        "questionId": 0,
        "score": 0,
        "similarQueries": [
          {
            "queryId": 0,
            "queryText": "string"
          }
        ]
      }
    ],
    "property2": [
      {
        "chatId": 0,
        "createTime": "2019-08-24T14:15:22Z",
        "feedback": "string",
        "parseInfos": [
          {
            "aggType": "[",
            "dataSet": {},
            "dateInfo": {},
            "dimensionFilters": [
              null
            ],
            "dimensions": [
              null
            ],
            "elementMatches": [
              null
            ],
            "entity": {},
            "entityInfo": {},
            "filterType": "[",
            "id": 0,
            "limit": 0,
            "metricFilters": [
              null
            ],
            "metrics": [
              null
            ],
            "orders": [
              null
            ],
            "properties": {},
            "queryMode": "string",
            "queryType": "[",
            "score": 0,
            "sqlEvaluation": {},
            "sqlInfo": {},
            "textInfo": "string"
          }
        ],
        "parseTimeCost": {
          "parseStartTime": 0,
          "parseTime": 0,
          "sqlTime": 0
        },
        "queryResult": {
          "aggregateInfo": {
            "metricInfos": null
          },
          "chatContext": {
            "aggType": null,
            "dataSet": null,
            "dateInfo": null,
            "dimensionFilters": null,
            "dimensions": null,
            "elementMatches": null,
            "entity": null,
            "entityInfo": null,
            "filterType": null,
            "id": null,
            "limit": null,
            "metricFilters": null,
            "metrics": null,
            "orders": null,
            "properties": null,
            "queryMode": null,
            "queryType": null,
            "score": null,
            "sqlEvaluation": null,
            "sqlInfo": null,
            "textInfo": null
          },
          "entityInfo": {
            "dataSetInfo": null,
            "dimensions": null,
            "entityId": null,
            "metrics": null
          },
          "queryAuthorization": {
            "dimensionFilters": null,
            "dimensionFiltersDesc": null,
            "domainName": null,
            "message": null
          },
          "queryColumns": [
            {}
          ],
          "queryId": 0,
          "queryMode": "string",
          "queryResults": [
            {}
          ],
          "querySql": "string",
          "queryState": "EMPTY",
          "queryTimeCost": 0,
          "recommendedDimensions": [
            {}
          ],
          "response": {},
          "textResult": "string"
        },
        "queryText": "string",
        "questionId": 0,
        "score": 0,
        "similarQueries": [
          {
            "queryId": 0,
            "queryText": "string"
          }
        ]
      }
    ]
  }
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ShowCaseResp](#schemashowcaseresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdsaveUsingPOST_2"></a>

## POST save

POST /openapi/chat/manage/save

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|chatName|query|string| 是 ||chatName|
|agentId|query|integer(int32)| 否 ||agentId|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdupdateConversionIsTopUsingPOST_1"></a>

## POST updateConversionIsTop

POST /openapi/chat/manage/updateChatIsTop

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|chatId|query|integer(int64)| 是 ||chatId|
|isTop|query|integer(int32)| 是 ||isTop|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdupdateConversionNameUsingPOST_1"></a>

## POST updateConversionName

POST /openapi/chat/manage/updateChatName

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|chatId|query|integer(int64)| 是 ||chatId|
|chatName|query|string| 是 ||chatName|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdupdateQAFeedbackUsingPOST_1"></a>

## POST updateQAFeedback

POST /openapi/chat/manage/updateQAFeedback

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|query|integer(int32)| 是 ||id|
|score|query|integer(int32)| 是 ||score|
|feedback|query|string| 否 ||feedback|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# chat-query-api-controller

<a id="opIdexecuteUsingPOST"></a>

## POST execute

POST /api/semantic/query/chat/execute

> Body 请求参数

```json
{
  "chatId": 0,
  "parseInfo": {
    "aggType": "AVG",
    "dataSet": {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    },
    "dateInfo": {
      "dateList": [
        "string"
      ],
      "dateMode": "ALL",
      "detectWord": "string",
      "endDate": "string",
      "groupByDate": true,
      "inherited": true,
      "period": "string",
      "startDate": "string",
      "unit": 0
    },
    "dimensionFilters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "dimensions": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      }
    ],
    "elementMatches": [
      {
        "detectWord": "string",
        "element": {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        },
        "frequency": 0,
        "inherited": true,
        "similarity": 0,
        "word": "string"
      }
    ],
    "entity": {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    },
    "entityInfo": {
      "dataSetInfo": {
        "bizName": "string",
        "itemId": 0,
        "name": "string",
        "primaryKey": "string",
        "value": "string",
        "words": [
          "string"
        ]
      },
      "dimensions": [
        {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "value": "string"
        }
      ],
      "entityId": "string",
      "metrics": [
        {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "value": "string"
        }
      ]
    },
    "filterType": "AND",
    "id": 0,
    "limit": 0,
    "metricFilters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "metrics": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      }
    ],
    "orders": [
      {
        "column": "string",
        "direction": "string"
      }
    ],
    "properties": {},
    "queryMode": "string",
    "queryType": "DETAIL",
    "score": 0,
    "sqlEvaluation": {
      "isValidated": true,
      "validateMsg": "string"
    },
    "sqlInfo": {
      "correctS2SQL": "string",
      "querySQL": "string",
      "s2SQL": "string",
      "sourceId": "string"
    },
    "textInfo": "string"
  },
  "queryId": 0,
  "queryText": "string",
  "saveAnswer": true,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ExecuteQueryReq](#schemaexecutequeryreq)| 否 | ExecuteQueryReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdmapUsingPOST"></a>

## POST map

POST /api/semantic/query/chat/map

> Body 请求参数

```json
{
  "chatId": 0,
  "dataSetIds": [
    0
  ],
  "exemplars": [
    {
      "dbSchema": "string",
      "question": "string",
      "sql": "string"
    }
  ],
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    }
  },
  "mapModeEnum": "LOOSE",
  "queryDataType": "ALL",
  "queryFilters": {
    "filters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "params": {}
  },
  "queryText": "string",
  "saveAnswer": true,
  "text2SQLType": "ONLY_LLM",
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QueryReq](#schemaqueryreq)| 否 | QueryReq|none|

> 返回示例

> 200 Response

```json
{
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    },
    "matchedDataSetInfos": [
      0
    ]
  },
  "queryText": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MapResp](#schemamapresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdparseUsingPOST"></a>

## POST parse

POST /api/semantic/query/chat/parse

> Body 请求参数

```json
{
  "chatId": 0,
  "dataSetIds": [
    0
  ],
  "exemplars": [
    {
      "dbSchema": "string",
      "question": "string",
      "sql": "string"
    }
  ],
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    }
  },
  "mapModeEnum": "LOOSE",
  "queryDataType": "ALL",
  "queryFilters": {
    "filters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "params": {}
  },
  "queryText": "string",
  "saveAnswer": true,
  "text2SQLType": "ONLY_LLM",
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QueryReq](#schemaqueryreq)| 否 | QueryReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdsearchUsingPOST_2"></a>

## POST search

POST /api/semantic/query/chat/search

> Body 请求参数

```json
{
  "chatId": 0,
  "dataSetIds": [
    0
  ],
  "exemplars": [
    {
      "dbSchema": "string",
      "question": "string",
      "sql": "string"
    }
  ],
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    }
  },
  "mapModeEnum": "LOOSE",
  "queryDataType": "ALL",
  "queryFilters": {
    "filters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "params": {}
  },
  "queryText": "string",
  "saveAnswer": true,
  "text2SQLType": "ONLY_LLM",
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QueryReq](#schemaqueryreq)| 否 | QueryReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# chat-query-controller

<a id="opIdqueryUsingPOST"></a>

## POST query

POST /api/chat/query/

> Body 请求参数

```json
{
  "agentId": 0,
  "chatId": 0,
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    }
  },
  "queryFilters": {
    "filters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "params": {}
  },
  "queryText": "string",
  "saveAnswer": true,
  "topN": 0,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatParseReq](#schemachatparsereq)| 否 | ChatParseReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdexecuteUsingPOST_1"></a>

## POST execute

POST /api/chat/query/execute

> Body 请求参数

```json
{
  "agentId": 0,
  "chatId": 0,
  "parseId": 0,
  "queryId": 0,
  "queryText": "string",
  "saveAnswer": true,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatExecuteReq](#schemachatexecutereq)| 否 | ChatExecuteReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdparseUsingPOST_1"></a>

## POST parse

POST /api/chat/query/parse

> Body 请求参数

```json
{
  "agentId": 0,
  "chatId": 0,
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    }
  },
  "queryFilters": {
    "filters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "params": {}
  },
  "queryText": "string",
  "saveAnswer": true,
  "topN": 0,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatParseReq](#schemachatparsereq)| 否 | ChatParseReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryContextUsingPOST"></a>

## POST queryContext

POST /api/chat/query/queryContext

> Body 请求参数

```json
{
  "chatId": 0,
  "dataSetIds": [
    0
  ],
  "exemplars": [
    {
      "dbSchema": "string",
      "question": "string",
      "sql": "string"
    }
  ],
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    }
  },
  "mapModeEnum": "LOOSE",
  "queryDataType": "ALL",
  "queryFilters": {
    "filters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "params": {}
  },
  "queryText": "string",
  "saveAnswer": true,
  "text2SQLType": "ONLY_LLM",
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QueryReq](#schemaqueryreq)| 否 | QueryReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryDataUsingPOST"></a>

## POST queryData

POST /api/chat/query/queryData

> Body 请求参数

```json
{
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "dimensionFilters": [
    {
      "bizName": "string",
      "elementID": 0,
      "function": "string",
      "name": "string",
      "operator": "!=",
      "value": {}
    }
  ],
  "dimensions": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "metricFilters": [
    {
      "bizName": "string",
      "elementID": 0,
      "function": "string",
      "name": "string",
      "operator": "!=",
      "value": {}
    }
  ],
  "metrics": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "parseId": 0,
  "queryId": 0,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatQueryDataReq](#schemachatquerydatareq)| 否 | ChatQueryDataReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryDimensionValueUsingPOST"></a>

## POST queryDimensionValue

POST /api/chat/query/queryDimensionValue

> Body 请求参数

```json
{
  "agentId": 0,
  "bizName": "string",
  "dataSetIds": [
    0
  ],
  "elementID": 0,
  "modelId": 0,
  "value": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DimensionValueReq](#schemadimensionvaluereq)| 否 | DimensionValueReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdsearchUsingPOST_3"></a>

## POST search

POST /api/chat/query/search

> Body 请求参数

```json
{
  "agentId": 0,
  "chatId": 0,
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    }
  },
  "queryFilters": {
    "filters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "params": {}
  },
  "queryText": "string",
  "saveAnswer": true,
  "topN": 0,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatParseReq](#schemachatparsereq)| 否 | ChatParseReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryUsingPOST_1"></a>

## POST query

POST /openapi/chat/query/

> Body 请求参数

```json
{
  "agentId": 0,
  "chatId": 0,
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    }
  },
  "queryFilters": {
    "filters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "params": {}
  },
  "queryText": "string",
  "saveAnswer": true,
  "topN": 0,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatParseReq](#schemachatparsereq)| 否 | ChatParseReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdexecuteUsingPOST_2"></a>

## POST execute

POST /openapi/chat/query/execute

> Body 请求参数

```json
{
  "agentId": 0,
  "chatId": 0,
  "parseId": 0,
  "queryId": 0,
  "queryText": "string",
  "saveAnswer": true,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatExecuteReq](#schemachatexecutereq)| 否 | ChatExecuteReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdparseUsingPOST_2"></a>

## POST parse

POST /openapi/chat/query/parse

> Body 请求参数

```json
{
  "agentId": 0,
  "chatId": 0,
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    }
  },
  "queryFilters": {
    "filters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "params": {}
  },
  "queryText": "string",
  "saveAnswer": true,
  "topN": 0,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatParseReq](#schemachatparsereq)| 否 | ChatParseReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryContextUsingPOST_1"></a>

## POST queryContext

POST /openapi/chat/query/queryContext

> Body 请求参数

```json
{
  "chatId": 0,
  "dataSetIds": [
    0
  ],
  "exemplars": [
    {
      "dbSchema": "string",
      "question": "string",
      "sql": "string"
    }
  ],
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    }
  },
  "mapModeEnum": "LOOSE",
  "queryDataType": "ALL",
  "queryFilters": {
    "filters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "params": {}
  },
  "queryText": "string",
  "saveAnswer": true,
  "text2SQLType": "ONLY_LLM",
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QueryReq](#schemaqueryreq)| 否 | QueryReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryDataUsingPOST_1"></a>

## POST queryData

POST /openapi/chat/query/queryData

> Body 请求参数

```json
{
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "dimensionFilters": [
    {
      "bizName": "string",
      "elementID": 0,
      "function": "string",
      "name": "string",
      "operator": "!=",
      "value": {}
    }
  ],
  "dimensions": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "metricFilters": [
    {
      "bizName": "string",
      "elementID": 0,
      "function": "string",
      "name": "string",
      "operator": "!=",
      "value": {}
    }
  ],
  "metrics": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "parseId": 0,
  "queryId": 0,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatQueryDataReq](#schemachatquerydatareq)| 否 | ChatQueryDataReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryDimensionValueUsingPOST_1"></a>

## POST queryDimensionValue

POST /openapi/chat/query/queryDimensionValue

> Body 请求参数

```json
{
  "agentId": 0,
  "bizName": "string",
  "dataSetIds": [
    0
  ],
  "elementID": 0,
  "modelId": 0,
  "value": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DimensionValueReq](#schemadimensionvaluereq)| 否 | DimensionValueReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdsearchUsingPOST_4"></a>

## POST search

POST /openapi/chat/query/search

> Body 请求参数

```json
{
  "agentId": 0,
  "chatId": 0,
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    }
  },
  "queryFilters": {
    "filters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "params": {}
  },
  "queryText": "string",
  "saveAnswer": true,
  "topN": 0,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatParseReq](#schemachatparsereq)| 否 | ChatParseReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# class-controller

<a id="opIdcreateUsingPOST"></a>

## POST create

POST /api/semantic/class/create

> Body 请求参数

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "id": 0,
  "itemIds": [
    0
  ],
  "name": "string",
  "parentId": 0,
  "sensitiveLevel": 0,
  "status": 0,
  "tagObjectId": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ClassReq](#schemaclassreq)| 否 | ClassReq|none|

> 返回示例

> 200 Response

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetId": 0,
  "description": "string",
  "domainId": 0,
  "domainName": "string",
  "fullPath": "string",
  "id": 0,
  "itemIds": [
    0
  ],
  "name": "string",
  "status": 0,
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ClassResp](#schemaclassresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetUsingGET"></a>

## GET get

GET /api/semantic/class/delete/{id}/{force}

> Body 请求参数

```json
{
  "bizName": "string",
  "classId": 0,
  "createdBy": "string",
  "dataSetId": 0,
  "domainId": 0,
  "fieldsDepend": [
    "string"
  ],
  "id": "string",
  "ids": [
    0
  ],
  "isTag": 0,
  "key": "string",
  "modelIds": [
    0
  ],
  "name": "string",
  "names": [
    "string"
  ],
  "sensitiveLevel": 0,
  "status": 0,
  "type": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|string| 是 ||none|
|force|path|string| 是 ||none|
|body|body|[ClassFilter](#schemaclassfilter)| 否 | ClassFilter|none|

> 返回示例

> 200 Response

```json
[
  {
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetId": 0,
    "description": "string",
    "domainId": 0,
    "domainName": "string",
    "fullPath": "string",
    "id": 0,
    "itemIds": [
      0
    ],
    "name": "string",
    "status": 0,
    "type": "string",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ClassResp](#schemaclassresp)]|false|none||none|
|» ClassResp|[ClassResp](#schemaclassresp)|false|none|ClassResp|none|
|»» bizName|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetId|integer(int64)|false|none||none|
|»» description|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» domainName|string|false|none||none|
|»» fullPath|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» itemIds|[integer]|false|none||none|
|»» name|string|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» type|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

<a id="opIddeleteUsingDELETE_1"></a>

## DELETE delete

DELETE /api/semantic/class/delete/{id}/{force}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|force|path|boolean| 是 ||force|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdupdateUsingPUT_1"></a>

## PUT update

PUT /api/semantic/class/update

> Body 请求参数

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "id": 0,
  "itemIds": [
    0
  ],
  "name": "string",
  "parentId": 0,
  "sensitiveLevel": 0,
  "status": 0,
  "tagObjectId": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ClassReq](#schemaclassreq)| 否 | ClassReq|none|

> 返回示例

> 200 Response

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetId": 0,
  "description": "string",
  "domainId": 0,
  "domainName": "string",
  "fullPath": "string",
  "id": 0,
  "itemIds": [
    0
  ],
  "name": "string",
  "status": 0,
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ClassResp](#schemaclassresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# collect-controller

<a id="opIdcreateCollectionIndicatorsUsingPOST"></a>

## POST createCollectionIndicators

POST /api/semantic/collect/createCollectionIndicators

> Body 请求参数

```json
{
  "collectId": 0,
  "createTime": "2019-08-24T14:15:22Z",
  "id": 0,
  "type": "string",
  "updateTime": "2019-08-24T14:15:22Z",
  "username": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[CollectDO](#schemacollectdo)| 否 | CollectDO|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteCollectionIndicatorsUsingPOST"></a>

## POST deleteCollectionIndicators

POST /api/semantic/collect/deleteCollectionIndicators

> Body 请求参数

```json
{
  "collectId": 0,
  "createTime": "2019-08-24T14:15:22Z",
  "id": 0,
  "type": "string",
  "updateTime": "2019-08-24T14:15:22Z",
  "username": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[CollectDO](#schemacollectdo)| 否 | CollectDO|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteCollectionIndicatorsUsingDELETE"></a>

## DELETE deleteCollectionIndicators

DELETE /api/semantic/collect/deleteCollectionIndicators/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

# data-set-controller

<a id="opIdupdateUsingPUT_2"></a>

## PUT update

PUT /api/semantic/dataSet

> Body 请求参数

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetDetail": {
    "dataSetModelConfigs": [
      {
        "dimensions": [
          0
        ],
        "id": 0,
        "includesAll": true,
        "metrics": [
          0
        ]
      }
    ]
  },
  "description": "string",
  "domainId": 0,
  "id": 0,
  "name": "string",
  "queryConfig": {
    "metricTypeDefaultConfig": {
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    },
    "tagTypeDefaultConfig": {
      "defaultDisplayInfo": {
        "dimensionIds": [
          0
        ],
        "metricIds": [
          0
        ]
      },
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    }
  },
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DataSetReq](#schemadatasetreq)| 否 | DataSetReq|none|

> 返回示例

> 200 Response

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "alias": "string",
  "allDimensions": [
    {
      "isTag": 0,
      "itemId": 0
    }
  ],
  "allIncludeAllModels": [
    0
  ],
  "allMetrics": [
    {
      "isTag": 0,
      "itemId": 0
    }
  ],
  "allModels": [
    0
  ],
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetDetail": {
    "dataSetModelConfigs": [
      {
        "dimensions": [
          0
        ],
        "id": 0,
        "includesAll": true,
        "metrics": [
          0
        ]
      }
    ]
  },
  "description": "string",
  "domainId": 0,
  "filterSql": "string",
  "id": 0,
  "name": "string",
  "queryConfig": {
    "metricTypeDefaultConfig": {
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    },
    "tagTypeDefaultConfig": {
      "defaultDisplayInfo": {
        "dimensionIds": [
          0
        ],
        "metricIds": [
          0
        ]
      },
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    }
  },
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DataSetResp](#schemadatasetresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdsaveUsingPOST_3"></a>

## POST save

POST /api/semantic/dataSet

> Body 请求参数

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetDetail": {
    "dataSetModelConfigs": [
      {
        "dimensions": [
          0
        ],
        "id": 0,
        "includesAll": true,
        "metrics": [
          0
        ]
      }
    ]
  },
  "description": "string",
  "domainId": 0,
  "id": 0,
  "name": "string",
  "queryConfig": {
    "metricTypeDefaultConfig": {
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    },
    "tagTypeDefaultConfig": {
      "defaultDisplayInfo": {
        "dimensionIds": [
          0
        ],
        "metricIds": [
          0
        ]
      },
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    }
  },
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DataSetReq](#schemadatasetreq)| 否 | DataSetReq|none|

> 返回示例

> 200 Response

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "alias": "string",
  "allDimensions": [
    {
      "isTag": 0,
      "itemId": 0
    }
  ],
  "allIncludeAllModels": [
    0
  ],
  "allMetrics": [
    {
      "isTag": 0,
      "itemId": 0
    }
  ],
  "allModels": [
    0
  ],
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetDetail": {
    "dataSetModelConfigs": [
      {
        "dimensions": [
          0
        ],
        "id": 0,
        "includesAll": true,
        "metrics": [
          0
        ]
      }
    ]
  },
  "description": "string",
  "domainId": 0,
  "filterSql": "string",
  "id": 0,
  "name": "string",
  "queryConfig": {
    "metricTypeDefaultConfig": {
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    },
    "tagTypeDefaultConfig": {
      "defaultDisplayInfo": {
        "dimensionIds": [
          0
        ],
        "metricIds": [
          0
        ]
      },
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    }
  },
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DataSetResp](#schemadatasetresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetDataSetListUsingGET"></a>

## GET getDataSetList

GET /api/semantic/dataSet/getDataSetList

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|query|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
[
  {
    "adminOrgs": [
      "string"
    ],
    "admins": [
      "string"
    ],
    "alias": "string",
    "allDimensions": [
      {
        "isTag": 0,
        "itemId": 0
      }
    ],
    "allIncludeAllModels": [
      0
    ],
    "allMetrics": [
      {
        "isTag": 0,
        "itemId": 0
      }
    ],
    "allModels": [
      0
    ],
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetDetail": {
      "dataSetModelConfigs": [
        {
          "dimensions": [
            0
          ],
          "id": 0,
          "includesAll": true,
          "metrics": [
            0
          ]
        }
      ]
    },
    "description": "string",
    "domainId": 0,
    "filterSql": "string",
    "id": 0,
    "name": "string",
    "queryConfig": {
      "metricTypeDefaultConfig": {
        "timeDefaultConfig": {
          "period": "string",
          "timeMode": "[",
          "unit": 0
        }
      },
      "tagTypeDefaultConfig": {
        "defaultDisplayInfo": {
          "dimensionIds": [
            null
          ],
          "metricIds": [
            null
          ]
        },
        "timeDefaultConfig": {
          "period": "string",
          "timeMode": "[",
          "unit": 0
        }
      }
    },
    "sensitiveLevel": 0,
    "status": 0,
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[DataSetResp](#schemadatasetresp)]|false|none||none|
|» DataSetResp|[DataSetResp](#schemadatasetresp)|false|none|DataSetResp|none|
|»» adminOrgs|[string]|false|none||none|
|»» admins|[string]|false|none||none|
|»» alias|string|false|none||none|
|»» allDimensions|[[TagItem](#schematagitem)]|false|none||none|
|»»» TagItem|[TagItem](#schematagitem)|false|none|TagItem|none|
|»»»» isTag|integer(int32)|false|none||none|
|»»»» itemId|integer(int64)|false|none||none|
|»» allIncludeAllModels|[integer]|false|none||none|
|»» allMetrics|[[TagItem](#schematagitem)]|false|none||none|
|»»» TagItem|[TagItem](#schematagitem)|false|none|TagItem|none|
|»»»» isTag|integer(int32)|false|none||none|
|»»»» itemId|integer(int64)|false|none||none|
|»» allModels|[integer]|false|none||none|
|»» bizName|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetDetail|[DataSetDetail](#schemadatasetdetail)|false|none|DataSetDetail|none|
|»»» dataSetModelConfigs|[[DataSetModelConfig](#schemadatasetmodelconfig)]|false|none||none|
|»»»» DataSetModelConfig|[DataSetModelConfig](#schemadatasetmodelconfig)|false|none|DataSetModelConfig|none|
|»»»»» dimensions|[integer]|false|none||none|
|»»»»» id|integer(int64)|false|none||none|
|»»»»» includesAll|boolean|false|none||none|
|»»»»» metrics|[integer]|false|none||none|
|»» description|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» filterSql|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» queryConfig|[QueryConfig](#schemaqueryconfig)|false|none|QueryConfig|none|
|»»» metricTypeDefaultConfig|[MetricTypeDefaultConfig](#schemametrictypedefaultconfig)|false|none|MetricTypeDefaultConfig|none|
|»»»» timeDefaultConfig|[TimeDefaultConfig](#schematimedefaultconfig)|false|none|TimeDefaultConfig|none|
|»»»»» period|string|false|none||none|
|»»»»» timeMode|string|false|none||none|
|»»»»» unit|integer(int32)|false|none||none|
|»»» tagTypeDefaultConfig|[TagTypeDefaultConfig](#schematagtypedefaultconfig)|false|none|TagTypeDefaultConfig|none|
|»»»» defaultDisplayInfo|[DefaultDisplayInfo](#schemadefaultdisplayinfo)|false|none|DefaultDisplayInfo|none|
|»»»»» dimensionIds|[integer]|false|none||none|
|»»»»» metricIds|[integer]|false|none||none|
|»»»» timeDefaultConfig|[TimeDefaultConfig](#schematimedefaultconfig)|false|none|TimeDefaultConfig|none|
|»»»»» period|string|false|none||none|
|»»»»» timeMode|string|false|none||none|
|»»»»» unit|integer(int32)|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|timeMode|LAST|
|timeMode|RECENT|
|timeMode|LAST|
|timeMode|RECENT|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdgetDataSetUsingGET"></a>

## GET getDataSet

GET /api/semantic/dataSet/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "alias": "string",
  "allDimensions": [
    {
      "isTag": 0,
      "itemId": 0
    }
  ],
  "allIncludeAllModels": [
    0
  ],
  "allMetrics": [
    {
      "isTag": 0,
      "itemId": 0
    }
  ],
  "allModels": [
    0
  ],
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetDetail": {
    "dataSetModelConfigs": [
      {
        "dimensions": [
          0
        ],
        "id": 0,
        "includesAll": true,
        "metrics": [
          0
        ]
      }
    ]
  },
  "description": "string",
  "domainId": 0,
  "filterSql": "string",
  "id": 0,
  "name": "string",
  "queryConfig": {
    "metricTypeDefaultConfig": {
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    },
    "tagTypeDefaultConfig": {
      "defaultDisplayInfo": {
        "dimensionIds": [
          0
        ],
        "metricIds": [
          0
        ]
      },
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    }
  },
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DataSetResp](#schemadatasetresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteUsingDELETE_2"></a>

## DELETE delete

DELETE /api/semantic/dataSet/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

# data-set-query-api-controller

<a id="opIdqueryByDataSetUsingPOST"></a>

## POST queryByDataSet

POST /api/semantic/query/dataSet

> Body 请求参数

```json
{
  "aggregators": [
    {
      "alias": "string",
      "args": [
        "string"
      ],
      "column": "string",
      "func": "AVG",
      "nameCh": "string"
    }
  ],
  "cacheInfo": {
    "cache": true
  },
  "dataSetId": 0,
  "dataSetName": "string",
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "dimensionFilters": [
    {
      "bizName": "string",
      "children": [
        {
          "bizName": "string",
          "children": [
            {}
          ],
          "id": 0,
          "name": "string",
          "operator": "!=",
          "relation": "AND",
          "value": {}
        }
      ],
      "id": 0,
      "name": "string",
      "operator": "!=",
      "relation": "AND",
      "value": {}
    }
  ],
  "groups": [
    "string"
  ],
  "innerLayerNative": true,
  "limit": 0,
  "metricFilters": [
    {
      "bizName": "string",
      "children": [
        {
          "bizName": "string",
          "children": [
            {}
          ],
          "id": 0,
          "name": "string",
          "operator": "!=",
          "relation": "AND",
          "value": {}
        }
      ],
      "id": 0,
      "name": "string",
      "operator": "!=",
      "relation": "AND",
      "value": {}
    }
  ],
  "needAuth": true,
  "orders": [
    {
      "column": "string",
      "direction": "string"
    }
  ],
  "params": [
    {
      "name": "string",
      "value": "string"
    }
  ],
  "queryType": "DETAIL",
  "sql": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QueryDataSetReq](#schemaquerydatasetreq)| 否 | QueryDataSetReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# database-controller

<a id="opIdcreateOrUpdateDatabaseUsingPOST"></a>

## POST createOrUpdateDatabase

POST /api/semantic/database/createOrUpdateDatabase

> Body 请求参数

```json
{
  "admins": [
    "string"
  ],
  "database": "string",
  "description": "string",
  "host": "string",
  "id": 0,
  "name": "string",
  "password": "string",
  "port": "string",
  "schema": "string",
  "type": "string",
  "url": "string",
  "username": "string",
  "version": "string",
  "viewers": [
    "string"
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DatabaseReq](#schemadatabasereq)| 否 | DatabaseReq|none|

> 返回示例

> 200 Response

```json
{
  "admins": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "database": "string",
  "description": "string",
  "hasEditPermission": true,
  "hasPermission": true,
  "hasUsePermission": true,
  "host": "string",
  "id": 0,
  "name": "string",
  "password": "string",
  "port": "string",
  "schema": "string",
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "url": "string",
  "username": "string",
  "version": "string",
  "viewers": [
    "string"
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DatabaseResp](#schemadatabaseresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdexecuteSqlUsingPOST"></a>

## POST executeSql

POST /api/semantic/database/executeSql

> Body 请求参数

```json
{
  "id": 0,
  "limit": 0,
  "sql": "string",
  "sqlVariables": [
    {
      "defaultValues": [
        {}
      ],
      "name": "string",
      "valueType": "EXPR"
    }
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[SqlExecuteReq](#schemasqlexecutereq)| 否 | SqlExecuteReq|none|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetColumnsUsingGET"></a>

## GET getColumns

GET /api/semantic/database/getColumns/{id}/{db}/{table}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|
|table|path|string| 是 ||table|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetColumnsUsingPUT"></a>

## PUT getColumns

PUT /api/semantic/database/getColumns/{id}/{db}/{table}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|
|table|path|string| 是 ||table|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetColumnsUsingPOST"></a>

## POST getColumns

POST /api/semantic/database/getColumns/{id}/{db}/{table}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|
|table|path|string| 是 ||table|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetColumnsUsingDELETE"></a>

## DELETE getColumns

DELETE /api/semantic/database/getColumns/{id}/{db}/{table}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|
|table|path|string| 是 ||table|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetColumnsUsingOPTIONS"></a>

## OPTIONS getColumns

OPTIONS /api/semantic/database/getColumns/{id}/{db}/{table}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|
|table|path|string| 是 ||table|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetColumnsUsingHEAD"></a>

## HEAD getColumns

HEAD /api/semantic/database/getColumns/{id}/{db}/{table}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|
|table|path|string| 是 ||table|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetColumnsUsingPATCH"></a>

## PATCH getColumns

PATCH /api/semantic/database/getColumns/{id}/{db}/{table}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|
|table|path|string| 是 ||table|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetColumnsUsingTRACE"></a>

## TRACE getColumns

TRACE /api/semantic/database/getColumns/{id}/{db}/{table}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|
|table|path|string| 是 ||table|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetDatabaseListUsingGET"></a>

## GET getDatabaseList

GET /api/semantic/database/getDatabaseList

> 返回示例

> 200 Response

```json
[
  {
    "admins": [
      "string"
    ],
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "database": "string",
    "description": "string",
    "hasEditPermission": true,
    "hasPermission": true,
    "hasUsePermission": true,
    "host": "string",
    "id": 0,
    "name": "string",
    "password": "string",
    "port": "string",
    "schema": "string",
    "type": "string",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "url": "string",
    "username": "string",
    "version": "string",
    "viewers": [
      "string"
    ]
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[DatabaseResp](#schemadatabaseresp)]|false|none||none|
|» DatabaseResp|[DatabaseResp](#schemadatabaseresp)|false|none|DatabaseResp|none|
|»» admins|[string]|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» database|string|false|none||none|
|»» description|string|false|none||none|
|»» hasEditPermission|boolean|false|none||none|
|»» hasPermission|boolean|false|none||none|
|»» hasUsePermission|boolean|false|none||none|
|»» host|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» password|string|false|none||none|
|»» port|string|false|none||none|
|»» schema|string|false|none||none|
|»» type|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» url|string|false|none||none|
|»» username|string|false|none||none|
|»» version|string|false|none||none|
|»» viewers|[string]|false|none||none|

<a id="opIdgetDatabaseParametersUsingGET"></a>

## GET getDatabaseParameters

GET /api/semantic/database/getDatabaseParameters

> 返回示例

> 200 Response

```json
{
  "property1": [
    {
      "candidateValues": [
        {}
      ],
      "comment": "string",
      "dataType": "string",
      "name": "string",
      "placeholder": "string",
      "require": true,
      "value": "string"
    }
  ],
  "property2": [
    {
      "candidateValues": [
        {}
      ],
      "comment": "string",
      "dataType": "string",
      "name": "string",
      "placeholder": "string",
      "require": true,
      "value": "string"
    }
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|» **additionalProperties**|[[DatabaseParameter](#schemadatabaseparameter)]|false|none||none|
|»» DatabaseParameter|[DatabaseParameter](#schemadatabaseparameter)|false|none|DatabaseParameter|none|
|»»» candidateValues|[object]|false|none||none|
|»»» comment|string|false|none||none|
|»»» dataType|string|false|none||none|
|»»» name|string|false|none||none|
|»»» placeholder|string|false|none||none|
|»»» require|boolean|false|none||none|
|»»» value|string|false|none||none|

<a id="opIdgetDbNamesUsingGET"></a>

## GET getDbNames

GET /api/semantic/database/getDbNames/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetDbNamesUsingPUT"></a>

## PUT getDbNames

PUT /api/semantic/database/getDbNames/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetDbNamesUsingPOST"></a>

## POST getDbNames

POST /api/semantic/database/getDbNames/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetDbNamesUsingDELETE"></a>

## DELETE getDbNames

DELETE /api/semantic/database/getDbNames/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetDbNamesUsingOPTIONS"></a>

## OPTIONS getDbNames

OPTIONS /api/semantic/database/getDbNames/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetDbNamesUsingHEAD"></a>

## HEAD getDbNames

HEAD /api/semantic/database/getDbNames/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetDbNamesUsingPATCH"></a>

## PATCH getDbNames

PATCH /api/semantic/database/getDbNames/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetDbNamesUsingTRACE"></a>

## TRACE getDbNames

TRACE /api/semantic/database/getDbNames/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetTablesUsingGET"></a>

## GET getTables

GET /api/semantic/database/getTables/{id}/{db}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetTablesUsingPUT"></a>

## PUT getTables

PUT /api/semantic/database/getTables/{id}/{db}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetTablesUsingPOST"></a>

## POST getTables

POST /api/semantic/database/getTables/{id}/{db}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetTablesUsingDELETE"></a>

## DELETE getTables

DELETE /api/semantic/database/getTables/{id}/{db}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetTablesUsingOPTIONS"></a>

## OPTIONS getTables

OPTIONS /api/semantic/database/getTables/{id}/{db}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetTablesUsingHEAD"></a>

## HEAD getTables

HEAD /api/semantic/database/getTables/{id}/{db}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetTablesUsingPATCH"></a>

## PATCH getTables

PATCH /api/semantic/database/getTables/{id}/{db}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetTablesUsingTRACE"></a>

## TRACE getTables

TRACE /api/semantic/database/getTables/{id}/{db}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|
|db|path|string| 是 ||db|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdtestConnectUsingPOST"></a>

## POST testConnect

POST /api/semantic/database/testConnect

> Body 请求参数

```json
{
  "admins": [
    "string"
  ],
  "database": "string",
  "description": "string",
  "host": "string",
  "id": 0,
  "name": "string",
  "password": "string",
  "port": "string",
  "schema": "string",
  "type": "string",
  "url": "string",
  "username": "string",
  "version": "string",
  "viewers": [
    "string"
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DatabaseReq](#schemadatabasereq)| 否 | DatabaseReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetDatabaseUsingGET"></a>

## GET getDatabase

GET /api/semantic/database/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "admins": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "database": "string",
  "description": "string",
  "hasEditPermission": true,
  "hasPermission": true,
  "hasUsePermission": true,
  "host": "string",
  "id": 0,
  "name": "string",
  "password": "string",
  "port": "string",
  "schema": "string",
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "url": "string",
  "username": "string",
  "version": "string",
  "viewers": [
    "string"
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DatabaseResp](#schemadatabaseresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteDatabaseUsingDELETE"></a>

## DELETE deleteDatabase

DELETE /api/semantic/database/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

# dimension-controller

<a id="opIdbatchUpdateSensitiveLevelUsingPOST"></a>

## POST batchUpdateSensitiveLevel

POST /api/semantic/dimension/batchUpdateSensitiveLevel

> Body 请求参数

```json
{
  "bizNames": [
    "string"
  ],
  "classifications": [
    "string"
  ],
  "ids": [
    0
  ],
  "modelIds": [
    0
  ],
  "sensitiveLevel": 0,
  "status": 0,
  "type": "ADD"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[MetaBatchReq](#schemametabatchreq)| 否 | MetaBatchReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdbatchUpdateStatusUsingPOST"></a>

## POST batchUpdateStatus

POST /api/semantic/dimension/batchUpdateStatus

> Body 请求参数

```json
{
  "bizNames": [
    "string"
  ],
  "classifications": [
    "string"
  ],
  "ids": [
    0
  ],
  "modelIds": [
    0
  ],
  "sensitiveLevel": 0,
  "status": 0,
  "type": "ADD"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[MetaBatchReq](#schemametabatchreq)| 否 | MetaBatchReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdcreateDimensionUsingPOST"></a>

## POST createDimension

POST /api/semantic/dimension/createDimension

> Body 请求参数

```json
{
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataType": "ARRAY",
  "defaultValues": [
    "string"
  ],
  "description": "string",
  "dimValueMaps": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "techName": "string"
    }
  ],
  "expr": "string",
  "ext": {},
  "id": 0,
  "isTag": 0,
  "modelId": 0,
  "name": "string",
  "semanticType": "string",
  "sensitiveLevel": 0,
  "status": 0,
  "type": "string",
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DimensionReq](#schemadimensionreq)| 否 | DimensionReq|none|

> 返回示例

> 200 Response

```json
{
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataType": "ARRAY",
  "defaultValues": [
    "string"
  ],
  "description": "string",
  "dimValueMaps": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "techName": "string"
    }
  ],
  "expr": "string",
  "ext": {},
  "id": 0,
  "isTag": 0,
  "modelBizName": "string",
  "modelFilterSql": "string",
  "modelId": 0,
  "modelName": "string",
  "name": "string",
  "semanticType": "string",
  "sensitiveLevel": 0,
  "status": 0,
  "type": "string",
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DimensionResp](#schemadimensionresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteDimensionUsingDELETE"></a>

## DELETE deleteDimension

DELETE /api/semantic/dimension/deleteDimension/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetAllHighSensitiveDimensionUsingGET"></a>

## GET getAllHighSensitiveDimension

GET /api/semantic/dimension/getAllHighSensitiveDimension

> 返回示例

> 200 Response

```json
[
  {
    "alias": "string",
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataType": "ARRAY",
    "defaultValues": [
      "string"
    ],
    "description": "string",
    "dimValueMaps": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "techName": "string"
      }
    ],
    "expr": "string",
    "ext": {},
    "id": 0,
    "isTag": 0,
    "modelBizName": "string",
    "modelFilterSql": "string",
    "modelId": 0,
    "modelName": "string",
    "name": "string",
    "semanticType": "string",
    "sensitiveLevel": 0,
    "status": 0,
    "type": "string",
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[DimensionResp](#schemadimensionresp)]|false|none||none|
|» DimensionResp|[DimensionResp](#schemadimensionresp)|false|none|DimensionResp|none|
|»» alias|string|false|none||none|
|»» bizName|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataType|string|false|none||none|
|»» defaultValues|[string]|false|none||none|
|»» description|string|false|none||none|
|»» dimValueMaps|[[DimValueMap](#schemadimvaluemap)]|false|none||none|
|»»» DimValueMap|[DimValueMap](#schemadimvaluemap)|false|none|DimValueMap|none|
|»»»» alias|[string]|false|none||none|
|»»»» bizName|string|false|none||none|
|»»»» techName|string|false|none||none|
|»» expr|string|false|none||none|
|»» ext|object|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isTag|integer(int32)|false|none||none|
|»» modelBizName|string|false|none||none|
|»» modelFilterSql|string|false|none||none|
|»» modelId|integer(int64)|false|none||none|
|»» modelName|string|false|none||none|
|»» name|string|false|none||none|
|»» semanticType|string|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» type|string|false|none||none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|dataType|ARRAY|
|dataType|BIGINT|
|dataType|DATE|
|dataType|DECIMAL|
|dataType|DOUBLE|
|dataType|FLOAT|
|dataType|INT|
|dataType|JSON|
|dataType|MAP|
|dataType|UNKNOWN|
|dataType|VARCHAR|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdgetDimensionInModelClusterUsingGET"></a>

## GET getDimensionInModelCluster

GET /api/semantic/dimension/getDimensionInModelCluster/{modelId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|modelId|path|integer(int64)| 是 ||modelId|

> 返回示例

> 200 Response

```json
[
  {
    "alias": "string",
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataType": "ARRAY",
    "defaultValues": [
      "string"
    ],
    "description": "string",
    "dimValueMaps": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "techName": "string"
      }
    ],
    "expr": "string",
    "ext": {},
    "id": 0,
    "isTag": 0,
    "modelBizName": "string",
    "modelFilterSql": "string",
    "modelId": 0,
    "modelName": "string",
    "name": "string",
    "semanticType": "string",
    "sensitiveLevel": 0,
    "status": 0,
    "type": "string",
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[DimensionResp](#schemadimensionresp)]|false|none||none|
|» DimensionResp|[DimensionResp](#schemadimensionresp)|false|none|DimensionResp|none|
|»» alias|string|false|none||none|
|»» bizName|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataType|string|false|none||none|
|»» defaultValues|[string]|false|none||none|
|»» description|string|false|none||none|
|»» dimValueMaps|[[DimValueMap](#schemadimvaluemap)]|false|none||none|
|»»» DimValueMap|[DimValueMap](#schemadimvaluemap)|false|none|DimValueMap|none|
|»»»» alias|[string]|false|none||none|
|»»»» bizName|string|false|none||none|
|»»»» techName|string|false|none||none|
|»» expr|string|false|none||none|
|»» ext|object|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isTag|integer(int32)|false|none||none|
|»» modelBizName|string|false|none||none|
|»» modelFilterSql|string|false|none||none|
|»» modelId|integer(int64)|false|none||none|
|»» modelName|string|false|none||none|
|»» name|string|false|none||none|
|»» semanticType|string|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» type|string|false|none||none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|dataType|ARRAY|
|dataType|BIGINT|
|dataType|DATE|
|dataType|DECIMAL|
|dataType|DOUBLE|
|dataType|FLOAT|
|dataType|INT|
|dataType|JSON|
|dataType|MAP|
|dataType|UNKNOWN|
|dataType|VARCHAR|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdgetDimensionUsingGET"></a>

## GET getDimension

GET /api/semantic/dimension/getDimensionList/{modelId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|modelId|path|integer(int64)| 是 ||modelId|

> 返回示例

> 200 Response

```json
[
  {
    "alias": "string",
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataType": "ARRAY",
    "defaultValues": [
      "string"
    ],
    "description": "string",
    "dimValueMaps": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "techName": "string"
      }
    ],
    "expr": "string",
    "ext": {},
    "id": 0,
    "isTag": 0,
    "modelBizName": "string",
    "modelFilterSql": "string",
    "modelId": 0,
    "modelName": "string",
    "name": "string",
    "semanticType": "string",
    "sensitiveLevel": 0,
    "status": 0,
    "type": "string",
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[DimensionResp](#schemadimensionresp)]|false|none||none|
|» DimensionResp|[DimensionResp](#schemadimensionresp)|false|none|DimensionResp|none|
|»» alias|string|false|none||none|
|»» bizName|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataType|string|false|none||none|
|»» defaultValues|[string]|false|none||none|
|»» description|string|false|none||none|
|»» dimValueMaps|[[DimValueMap](#schemadimvaluemap)]|false|none||none|
|»»» DimValueMap|[DimValueMap](#schemadimvaluemap)|false|none|DimValueMap|none|
|»»»» alias|[string]|false|none||none|
|»»»» bizName|string|false|none||none|
|»»»» techName|string|false|none||none|
|»» expr|string|false|none||none|
|»» ext|object|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isTag|integer(int32)|false|none||none|
|»» modelBizName|string|false|none||none|
|»» modelFilterSql|string|false|none||none|
|»» modelId|integer(int64)|false|none||none|
|»» modelName|string|false|none||none|
|»» name|string|false|none||none|
|»» semanticType|string|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» type|string|false|none||none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|dataType|ARRAY|
|dataType|BIGINT|
|dataType|DATE|
|dataType|DECIMAL|
|dataType|DOUBLE|
|dataType|FLOAT|
|dataType|INT|
|dataType|JSON|
|dataType|MAP|
|dataType|UNKNOWN|
|dataType|VARCHAR|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdmockMetricAliasUsingPOST"></a>

## POST mockMetricAlias

POST /api/semantic/dimension/mockDimensionAlias

> Body 请求参数

```json
{
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataType": "ARRAY",
  "defaultValues": [
    "string"
  ],
  "description": "string",
  "dimValueMaps": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "techName": "string"
    }
  ],
  "expr": "string",
  "ext": {},
  "id": 0,
  "isTag": 0,
  "modelId": 0,
  "name": "string",
  "semanticType": "string",
  "sensitiveLevel": 0,
  "status": 0,
  "type": "string",
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DimensionReq](#schemadimensionreq)| 否 | DimensionReq|none|

> 返回示例

> 200 Response

```json
[
  "string"
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdmockDimensionValuesAliasUsingPOST"></a>

## POST mockDimensionValuesAlias

POST /api/semantic/dimension/mockDimensionValuesAlias

> Body 请求参数

```json
{
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataType": "ARRAY",
  "defaultValues": [
    "string"
  ],
  "description": "string",
  "dimValueMaps": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "techName": "string"
    }
  ],
  "expr": "string",
  "ext": {},
  "id": 0,
  "isTag": 0,
  "modelId": 0,
  "name": "string",
  "semanticType": "string",
  "sensitiveLevel": 0,
  "status": 0,
  "type": "string",
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DimensionReq](#schemadimensionreq)| 否 | DimensionReq|none|

> 返回示例

> 200 Response

```json
[
  {
    "alias": [
      "string"
    ],
    "bizName": "string",
    "techName": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[DimValueMap](#schemadimvaluemap)]|false|none||none|
|» DimValueMap|[DimValueMap](#schemadimvaluemap)|false|none|DimValueMap|none|
|»» alias|[string]|false|none||none|
|»» bizName|string|false|none||none|
|»» techName|string|false|none||none|

<a id="opIdqueryDimValueUsingPOST"></a>

## POST queryDimValue

POST /api/semantic/dimension/queryDimValue

> Body 请求参数

```json
{
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "dimensionBizName": "string",
  "modelId": 0,
  "value": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QueryDimValueReq](#schemaquerydimvaluereq)| 否 | QueryDimValueReq|none|

> 返回示例

> 200 Response

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SemanticQueryResp](#schemasemanticqueryresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryDimensionUsingPOST"></a>

## POST queryDimension

POST /api/semantic/dimension/queryDimension

> Body 请求参数

```json
{
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdBy": "string",
  "current": 0,
  "domainIds": [
    0
  ],
  "hasCollect": true,
  "id": "string",
  "ids": [
    0
  ],
  "isTag": 0,
  "key": "string",
  "modelIds": [
    0
  ],
  "name": "string",
  "orderCondition": "string",
  "pageSize": 0,
  "sensitiveLevel": 0,
  "sort": "string",
  "status": 0
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[PageDimensionReq](#schemapagedimensionreq)| 否 | PageDimensionReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "alias": "string",
      "bizName": "string",
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dataType": "ARRAY",
      "defaultValues": [
        "string"
      ],
      "description": "string",
      "dimValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "expr": "string",
      "ext": {},
      "id": 0,
      "isTag": 0,
      "modelBizName": "string",
      "modelFilterSql": "string",
      "modelId": 0,
      "modelName": "string",
      "name": "string",
      "semanticType": "string",
      "sensitiveLevel": 0,
      "status": 0,
      "type": "string",
      "typeEnum": "DATASET",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdupdateDimensionUsingPOST"></a>

## POST updateDimension

POST /api/semantic/dimension/updateDimension

> Body 请求参数

```json
{
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataType": "ARRAY",
  "defaultValues": [
    "string"
  ],
  "description": "string",
  "dimValueMaps": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "techName": "string"
    }
  ],
  "expr": "string",
  "ext": {},
  "id": 0,
  "isTag": 0,
  "modelId": 0,
  "name": "string",
  "semanticType": "string",
  "sensitiveLevel": 0,
  "status": 0,
  "type": "string",
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DimensionReq](#schemadimensionreq)| 否 | DimensionReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetDimensionDescByNameAndIdUsingGET"></a>

## GET getDimensionDescByNameAndId

GET /api/semantic/dimension/{modelId}/{dimensionName}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|modelId|path|integer(int64)| 是 ||modelId|
|dimensionName|path|string| 是 ||dimensionName|

> 返回示例

> 200 Response

```json
{
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataType": "ARRAY",
  "defaultValues": [
    "string"
  ],
  "description": "string",
  "dimValueMaps": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "techName": "string"
    }
  ],
  "expr": "string",
  "ext": {},
  "id": 0,
  "isTag": 0,
  "modelBizName": "string",
  "modelFilterSql": "string",
  "modelId": 0,
  "modelName": "string",
  "name": "string",
  "semanticType": "string",
  "sensitiveLevel": 0,
  "status": 0,
  "type": "string",
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DimensionResp](#schemadimensionresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# domain-controller

<a id="opIdcreateDomainUsingPOST"></a>

## POST createDomain

POST /api/semantic/domain/createDomain

> Body 请求参数

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "id": 0,
  "isOpen": 0,
  "name": "string",
  "parentId": 0,
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "viewOrgs": [
    "string"
  ],
  "viewers": [
    "string"
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DomainReq](#schemadomainreq)| 否 | DomainReq|none|

> 返回示例

> 200 Response

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "fullPath": "string",
  "hasEditPermission": true,
  "hasModel": true,
  "id": 0,
  "isOpen": 0,
  "name": "string",
  "parentId": 0,
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "viewOrgs": [
    "string"
  ],
  "viewers": [
    "string"
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DomainResp](#schemadomainresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteDomainUsingDELETE"></a>

## DELETE deleteDomain

DELETE /api/semantic/domain/deleteDomain/{domainId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|path|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetDomainUsingGET"></a>

## GET getDomain

GET /api/semantic/domain/getDomain/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "fullPath": "string",
  "hasEditPermission": true,
  "hasModel": true,
  "id": 0,
  "isOpen": 0,
  "name": "string",
  "parentId": 0,
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "viewOrgs": [
    "string"
  ],
  "viewers": [
    "string"
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DomainResp](#schemadomainresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetDomainListUsingGET"></a>

## GET getDomainList

GET /api/semantic/domain/getDomainList

> 返回示例

> 200 Response

```json
[
  {
    "adminOrgs": [
      "string"
    ],
    "admins": [
      "string"
    ],
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "description": "string",
    "fullPath": "string",
    "hasEditPermission": true,
    "hasModel": true,
    "id": 0,
    "isOpen": 0,
    "name": "string",
    "parentId": 0,
    "sensitiveLevel": 0,
    "status": 0,
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "viewOrgs": [
      "string"
    ],
    "viewers": [
      "string"
    ]
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[DomainResp](#schemadomainresp)]|false|none||none|
|» DomainResp|[DomainResp](#schemadomainresp)|false|none|DomainResp|none|
|»» adminOrgs|[string]|false|none||none|
|»» admins|[string]|false|none||none|
|»» bizName|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» description|string|false|none||none|
|»» fullPath|string|false|none||none|
|»» hasEditPermission|boolean|false|none||none|
|»» hasModel|boolean|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isOpen|integer(int32)|false|none||none|
|»» name|string|false|none||none|
|»» parentId|integer(int64)|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» viewOrgs|[string]|false|none||none|
|»» viewers|[string]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdgetDomainListByIdsUsingGET"></a>

## GET getDomainListByIds

GET /api/semantic/domain/getDomainListByIds/{domainIds}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainIds|path|string| 是 ||domainIds|

> 返回示例

> 200 Response

```json
[
  {
    "adminOrgs": [
      "string"
    ],
    "admins": [
      "string"
    ],
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "description": "string",
    "fullPath": "string",
    "hasEditPermission": true,
    "hasModel": true,
    "id": 0,
    "isOpen": 0,
    "name": "string",
    "parentId": 0,
    "sensitiveLevel": 0,
    "status": 0,
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "viewOrgs": [
      "string"
    ],
    "viewers": [
      "string"
    ]
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[DomainResp](#schemadomainresp)]|false|none||none|
|» DomainResp|[DomainResp](#schemadomainresp)|false|none|DomainResp|none|
|»» adminOrgs|[string]|false|none||none|
|»» admins|[string]|false|none||none|
|»» bizName|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» description|string|false|none||none|
|»» fullPath|string|false|none||none|
|»» hasEditPermission|boolean|false|none||none|
|»» hasModel|boolean|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isOpen|integer(int32)|false|none||none|
|»» name|string|false|none||none|
|»» parentId|integer(int64)|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» viewOrgs|[string]|false|none||none|
|»» viewers|[string]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdupdateDomainUsingPOST"></a>

## POST updateDomain

POST /api/semantic/domain/updateDomain

> Body 请求参数

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "id": 0,
  "isOpen": 0,
  "name": "string",
  "parentId": 0,
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "viewOrgs": [
    "string"
  ],
  "viewers": [
    "string"
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DomainUpdateReq](#schemadomainupdatereq)| 否 | DomainUpdateReq|none|

> 返回示例

> 200 Response

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "fullPath": "string",
  "hasEditPermission": true,
  "hasModel": true,
  "id": 0,
  "isOpen": 0,
  "name": "string",
  "parentId": 0,
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "viewOrgs": [
    "string"
  ],
  "viewers": [
    "string"
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DomainResp](#schemadomainresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# knowledge-controller

<a id="opIdeditDictConfUsingPUT"></a>

## PUT editDictConf

PUT /api/semantic/knowledge/conf

> Body 请求参数

```json
{
  "config": {
    "blackList": [
      "string"
    ],
    "dateConf": {
      "dateList": [
        "string"
      ],
      "dateMode": "ALL",
      "detectWord": "string",
      "endDate": "string",
      "groupByDate": true,
      "inherited": true,
      "period": "string",
      "startDate": "string",
      "unit": 0
    },
    "limit": 0,
    "metricId": 0,
    "ruleList": [
      "string"
    ],
    "whiteList": [
      "string"
    ]
  },
  "id": 0,
  "itemId": 0,
  "status": "DELETED",
  "type": "DATASET"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DictItemReq](#schemadictitemreq)| 否 | DictItemReq|none|

> 返回示例

> 200 Response

```json
{
  "bizName": "string",
  "config": {
    "blackList": [
      "string"
    ],
    "dateConf": {
      "dateList": [
        "string"
      ],
      "dateMode": "ALL",
      "detectWord": "string",
      "endDate": "string",
      "groupByDate": true,
      "groupByTimeDimension": "string",
      "inherited": true,
      "period": "string",
      "startDate": "string",
      "unit": 0
    },
    "limit": 0,
    "metricId": 0,
    "ruleList": [
      "string"
    ],
    "whiteList": [
      "string"
    ]
  },
  "id": 0,
  "itemId": 0,
  "modelId": 0,
  "nature": "string",
  "status": "DELETED",
  "type": "DATASET"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DictItemResp](#schemadictitemresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdaddDictConfUsingPOST"></a>

## POST addDictConf

POST /api/semantic/knowledge/conf

> Body 请求参数

```json
{
  "config": {
    "blackList": [
      "string"
    ],
    "dateConf": {
      "dateList": [
        "string"
      ],
      "dateMode": "ALL",
      "detectWord": "string",
      "endDate": "string",
      "groupByDate": true,
      "inherited": true,
      "period": "string",
      "startDate": "string",
      "unit": 0
    },
    "limit": 0,
    "metricId": 0,
    "ruleList": [
      "string"
    ],
    "whiteList": [
      "string"
    ]
  },
  "id": 0,
  "itemId": 0,
  "status": "DELETED",
  "type": "DATASET"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DictItemReq](#schemadictitemreq)| 否 | DictItemReq|none|

> 返回示例

> 200 Response

```json
{
  "bizName": "string",
  "config": {
    "blackList": [
      "string"
    ],
    "dateConf": {
      "dateList": [
        "string"
      ],
      "dateMode": "ALL",
      "detectWord": "string",
      "endDate": "string",
      "groupByDate": true,
      "groupByTimeDimension": "string",
      "inherited": true,
      "period": "string",
      "startDate": "string",
      "unit": 0
    },
    "limit": 0,
    "metricId": 0,
    "ruleList": [
      "string"
    ],
    "whiteList": [
      "string"
    ]
  },
  "id": 0,
  "itemId": 0,
  "modelId": 0,
  "nature": "string",
  "status": "DELETED",
  "type": "DATASET"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DictItemResp](#schemadictitemresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryDictConfUsingPOST"></a>

## POST queryDictConf

POST /api/semantic/knowledge/conf/query

> Body 请求参数

```json
{
  "id": 0,
  "itemId": 0,
  "status": "DELETED",
  "type": "DATASET"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DictItemFilter](#schemadictitemfilter)| 否 | DictItemFilter|none|

> 返回示例

> 200 Response

```json
[
  {
    "bizName": "string",
    "config": {
      "blackList": [
        "string"
      ],
      "dateConf": {
        "dateList": [
          "string"
        ],
        "dateMode": "ALL",
        "detectWord": "string",
        "endDate": "string",
        "groupByDate": true,
        "groupByTimeDimension": "string",
        "inherited": true,
        "period": "string",
        "startDate": "string",
        "unit": 0
      },
      "limit": 0,
      "metricId": 0,
      "ruleList": [
        "string"
      ],
      "whiteList": [
        "string"
      ]
    },
    "id": 0,
    "itemId": 0,
    "modelId": 0,
    "nature": "string",
    "status": "DELETED",
    "type": "DATASET"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[DictItemResp](#schemadictitemresp)]|false|none||none|
|» DictItemResp|[DictItemResp](#schemadictitemresp)|false|none|DictItemResp|none|
|»» bizName|string|false|none||none|
|»» config|[ItemValueConfigRes](#schemaitemvalueconfigres)|false|none|ItemValueConfigRes|none|
|»»» blackList|[string]|false|none||none|
|»»» dateConf|[DateConfRes](#schemadateconfres)|false|none|DateConfRes|none|
|»»»» dateList|[string]|false|none||none|
|»»»» dateMode|string|false|none||none|
|»»»» detectWord|string|false|none||none|
|»»»» endDate|string|false|none||none|
|»»»» groupByDate|boolean|false|none||none|
|»»»» groupByTimeDimension|string|false|none||none|
|»»»» inherited|boolean|false|none||none|
|»»»» period|string|false|none||none|
|»»»» startDate|string|false|none||none|
|»»»» unit|integer(int32)|false|none||none|
|»»» limit|integer(int64)|false|none||none|
|»»» metricId|integer(int64)|false|none||none|
|»»» ruleList|[string]|false|none||none|
|»»» whiteList|[string]|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» itemId|integer(int64)|true|none||none|
|»» modelId|integer(int64)|false|none||none|
|»» nature|string|false|none||none|
|»» status|string|true|none||none|
|»» type|string|true|none||none|

#### 枚举值

|属性|值|
|---|---|
|dateMode|ALL|
|dateMode|AVAILABLE|
|dateMode|BETWEEN|
|dateMode|LIST|
|dateMode|RECENT|
|status|DELETED|
|status|INITIALIZED|
|status|OFFLINE|
|status|ONLINE|
|status|UNAVAILABLE|
|status|UNKNOWN|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|

<a id="opIdqueryDictValueUsingPOST"></a>

## POST queryDictValue

POST /api/semantic/knowledge/dict/data

> Body 请求参数

```json
{
  "current": 0,
  "itemId": 0,
  "modelId": 0,
  "orderCondition": "string",
  "pageSize": 0,
  "sort": "string",
  "type": "DATASET"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DictValueReq](#schemadictvaluereq)| 否 | DictValueReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "frequency": 0,
      "nature": "string",
      "value": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryDictFilePathUsingPOST"></a>

## POST queryDictFilePath

POST /api/semantic/knowledge/dict/file

> Body 请求参数

```json
{
  "current": 0,
  "itemId": 0,
  "modelId": 0,
  "orderCondition": "string",
  "pageSize": 0,
  "sort": "string",
  "type": "DATASET"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DictValueReq](#schemadictvaluereq)| 否 | DictValueReq|none|

> 返回示例

> 200 Response

```json
"string"
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdexecutePersistFileTaskUsingGET"></a>

## GET executePersistFileTask

GET /api/semantic/knowledge/embedding/persistFile

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdreloadMetaEmbeddingUsingGET"></a>

## GET reloadMetaEmbedding

GET /api/semantic/knowledge/meta/embedding/reload

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdaddDictTaskUsingPOST"></a>

## POST addDictTask

POST /api/semantic/knowledge/task

> Body 请求参数

```json
{
  "itemId": 0,
  "type": "DATASET"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DictSingleTaskReq](#schemadictsingletaskreq)| 否 | DictSingleTaskReq|none|

> 返回示例

> 200 Response

```json
0
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|integer|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddailyDictTaskUsingPUT"></a>

## PUT dailyDictTask

PUT /api/semantic/knowledge/task/all

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteDictTaskUsingPUT"></a>

## PUT deleteDictTask

PUT /api/semantic/knowledge/task/delete

> Body 请求参数

```json
{
  "itemId": 0,
  "type": "DATASET"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DictSingleTaskReq](#schemadictsingletaskreq)| 否 | DictSingleTaskReq|none|

> 返回示例

> 200 Response

```json
0
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|integer|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryLatestDictTaskUsingPOST"></a>

## POST queryLatestDictTask

POST /api/semantic/knowledge/task/search

> Body 请求参数

```json
{
  "itemId": 0,
  "type": "DATASET"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DictSingleTaskReq](#schemadictsingletaskreq)| 否 | DictSingleTaskReq|none|

> 返回示例

> 200 Response

```json
{
  "bizName": "string",
  "config": {
    "blackList": [
      "string"
    ],
    "dateConf": {
      "dateList": [
        "string"
      ],
      "dateMode": "ALL",
      "detectWord": "string",
      "endDate": "string",
      "groupByDate": true,
      "groupByTimeDimension": "string",
      "inherited": true,
      "period": "string",
      "startDate": "string",
      "unit": 0
    },
    "limit": 0,
    "metricId": 0,
    "ruleList": [
      "string"
    ],
    "whiteList": [
      "string"
    ]
  },
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "elapsedMs": 0,
  "id": 0,
  "itemId": 0,
  "modelId": 0,
  "name": "string",
  "nature": "string",
  "status": "DELETED",
  "taskStatus": "string",
  "type": "DATASET"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DictTaskResp](#schemadicttaskresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# memory-controller

<a id="opIdpageMemoriesUsingGET"></a>

## GET pageMemories

GET /api/chat/memory/pageMemories

> Body 请求参数

```json
{
  "chatMemoryFilter": {
    "agentId": 0,
    "humanReviewRet": "NEGATIVE",
    "llmReviewRet": "NEGATIVE",
    "question": "string",
    "questions": [
      "string"
    ],
    "status": "DISABLED"
  },
  "current": 0,
  "orderCondition": "string",
  "pageSize": 0,
  "sort": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[PageMemoryReq](#schemapagememoryreq)| 否 | PageMemoryReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "agentId": 0,
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dbSchema": "string",
      "humanReviewCmt": "string",
      "humanReviewRet": "NEGATIVE",
      "id": 0,
      "llmReviewCmt": "string",
      "llmReviewRet": "NEGATIVE",
      "question": "string",
      "s2sql": "string",
      "status": "DISABLED",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdpageMemoriesUsingPUT"></a>

## PUT pageMemories

PUT /api/chat/memory/pageMemories

> Body 请求参数

```json
{
  "chatMemoryFilter": {
    "agentId": 0,
    "humanReviewRet": "NEGATIVE",
    "llmReviewRet": "NEGATIVE",
    "question": "string",
    "questions": [
      "string"
    ],
    "status": "DISABLED"
  },
  "current": 0,
  "orderCondition": "string",
  "pageSize": 0,
  "sort": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[PageMemoryReq](#schemapagememoryreq)| 否 | PageMemoryReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "agentId": 0,
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dbSchema": "string",
      "humanReviewCmt": "string",
      "humanReviewRet": "NEGATIVE",
      "id": 0,
      "llmReviewCmt": "string",
      "llmReviewRet": "NEGATIVE",
      "question": "string",
      "s2sql": "string",
      "status": "DISABLED",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdpageMemoriesUsingPOST"></a>

## POST pageMemories

POST /api/chat/memory/pageMemories

> Body 请求参数

```json
{
  "chatMemoryFilter": {
    "agentId": 0,
    "humanReviewRet": "NEGATIVE",
    "llmReviewRet": "NEGATIVE",
    "question": "string",
    "questions": [
      "string"
    ],
    "status": "DISABLED"
  },
  "current": 0,
  "orderCondition": "string",
  "pageSize": 0,
  "sort": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[PageMemoryReq](#schemapagememoryreq)| 否 | PageMemoryReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "agentId": 0,
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dbSchema": "string",
      "humanReviewCmt": "string",
      "humanReviewRet": "NEGATIVE",
      "id": 0,
      "llmReviewCmt": "string",
      "llmReviewRet": "NEGATIVE",
      "question": "string",
      "s2sql": "string",
      "status": "DISABLED",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdpageMemoriesUsingDELETE"></a>

## DELETE pageMemories

DELETE /api/chat/memory/pageMemories

> Body 请求参数

```json
{
  "chatMemoryFilter": {
    "agentId": 0,
    "humanReviewRet": "NEGATIVE",
    "llmReviewRet": "NEGATIVE",
    "question": "string",
    "questions": [
      "string"
    ],
    "status": "DISABLED"
  },
  "current": 0,
  "orderCondition": "string",
  "pageSize": 0,
  "sort": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[PageMemoryReq](#schemapagememoryreq)| 否 | PageMemoryReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "agentId": 0,
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dbSchema": "string",
      "humanReviewCmt": "string",
      "humanReviewRet": "NEGATIVE",
      "id": 0,
      "llmReviewCmt": "string",
      "llmReviewRet": "NEGATIVE",
      "question": "string",
      "s2sql": "string",
      "status": "DISABLED",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdpageMemoriesUsingOPTIONS"></a>

## OPTIONS pageMemories

OPTIONS /api/chat/memory/pageMemories

> Body 请求参数

```json
{
  "chatMemoryFilter": {
    "agentId": 0,
    "humanReviewRet": "NEGATIVE",
    "llmReviewRet": "NEGATIVE",
    "question": "string",
    "questions": [
      "string"
    ],
    "status": "DISABLED"
  },
  "current": 0,
  "orderCondition": "string",
  "pageSize": 0,
  "sort": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[PageMemoryReq](#schemapagememoryreq)| 否 | PageMemoryReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "agentId": 0,
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dbSchema": "string",
      "humanReviewCmt": "string",
      "humanReviewRet": "NEGATIVE",
      "id": 0,
      "llmReviewCmt": "string",
      "llmReviewRet": "NEGATIVE",
      "question": "string",
      "s2sql": "string",
      "status": "DISABLED",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdpageMemoriesUsingHEAD"></a>

## HEAD pageMemories

HEAD /api/chat/memory/pageMemories

> Body 请求参数

```json
{
  "chatMemoryFilter": {
    "agentId": 0,
    "humanReviewRet": "NEGATIVE",
    "llmReviewRet": "NEGATIVE",
    "question": "string",
    "questions": [
      "string"
    ],
    "status": "DISABLED"
  },
  "current": 0,
  "orderCondition": "string",
  "pageSize": 0,
  "sort": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[PageMemoryReq](#schemapagememoryreq)| 否 | PageMemoryReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "agentId": 0,
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dbSchema": "string",
      "humanReviewCmt": "string",
      "humanReviewRet": "NEGATIVE",
      "id": 0,
      "llmReviewCmt": "string",
      "llmReviewRet": "NEGATIVE",
      "question": "string",
      "s2sql": "string",
      "status": "DISABLED",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdpageMemoriesUsingPATCH"></a>

## PATCH pageMemories

PATCH /api/chat/memory/pageMemories

> Body 请求参数

```json
{
  "chatMemoryFilter": {
    "agentId": 0,
    "humanReviewRet": "NEGATIVE",
    "llmReviewRet": "NEGATIVE",
    "question": "string",
    "questions": [
      "string"
    ],
    "status": "DISABLED"
  },
  "current": 0,
  "orderCondition": "string",
  "pageSize": 0,
  "sort": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[PageMemoryReq](#schemapagememoryreq)| 否 | PageMemoryReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "agentId": 0,
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dbSchema": "string",
      "humanReviewCmt": "string",
      "humanReviewRet": "NEGATIVE",
      "id": 0,
      "llmReviewCmt": "string",
      "llmReviewRet": "NEGATIVE",
      "question": "string",
      "s2sql": "string",
      "status": "DISABLED",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdpageMemoriesUsingTRACE"></a>

## TRACE pageMemories

TRACE /api/chat/memory/pageMemories

> Body 请求参数

```json
{
  "chatMemoryFilter": {
    "agentId": 0,
    "humanReviewRet": "NEGATIVE",
    "llmReviewRet": "NEGATIVE",
    "question": "string",
    "questions": [
      "string"
    ],
    "status": "DISABLED"
  },
  "current": 0,
  "orderCondition": "string",
  "pageSize": 0,
  "sort": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[PageMemoryReq](#schemapagememoryreq)| 否 | PageMemoryReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "agentId": 0,
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dbSchema": "string",
      "humanReviewCmt": "string",
      "humanReviewRet": "NEGATIVE",
      "id": 0,
      "llmReviewCmt": "string",
      "llmReviewRet": "NEGATIVE",
      "question": "string",
      "s2sql": "string",
      "status": "DISABLED",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdupdateMemoryUsingPOST"></a>

## POST updateMemory

POST /api/chat/memory/updateMemory

> Body 请求参数

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dbSchema": "string",
  "humanReviewCmt": "string",
  "humanReviewRet": "NEGATIVE",
  "id": 0,
  "s2sql": "string",
  "status": "DISABLED",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatMemoryUpdateReq](#schemachatmemoryupdatereq)| 否 | ChatMemoryUpdateReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# meta-discovery-api-controller

<a id="opIdmapUsingPOST_1"></a>

## POST map

POST /api/semantic/meta/map

> Body 请求参数

```json
{
  "dataSetNames": [
    "string"
  ],
  "mapModeEnum": "LOOSE",
  "queryDataType": "ALL",
  "queryText": "string",
  "topN": 0,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QueryMapReq](#schemaquerymapreq)| 否 | QueryMapReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# metric-controller

<a id="opIdbatchPublishUsingPOST"></a>

## POST batchPublish

POST /api/semantic/metric/batchPublish

> Body 请求参数

```json
{
  "bizNames": [
    "string"
  ],
  "classifications": [
    "string"
  ],
  "ids": [
    0
  ],
  "modelIds": [
    0
  ],
  "sensitiveLevel": 0,
  "status": 0,
  "type": "ADD"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[MetaBatchReq](#schemametabatchreq)| 否 | MetaBatchReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdbatchUnPublishUsingPOST"></a>

## POST batchUnPublish

POST /api/semantic/metric/batchUnPublish

> Body 请求参数

```json
{
  "bizNames": [
    "string"
  ],
  "classifications": [
    "string"
  ],
  "ids": [
    0
  ],
  "modelIds": [
    0
  ],
  "sensitiveLevel": 0,
  "status": 0,
  "type": "ADD"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[MetaBatchReq](#schemametabatchreq)| 否 | MetaBatchReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdbatchUpdateClassificationsUsingPOST"></a>

## POST batchUpdateClassifications

POST /api/semantic/metric/batchUpdateClassifications

> Body 请求参数

```json
{
  "bizNames": [
    "string"
  ],
  "classifications": [
    "string"
  ],
  "ids": [
    0
  ],
  "modelIds": [
    0
  ],
  "sensitiveLevel": 0,
  "status": 0,
  "type": "ADD"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[MetaBatchReq](#schemametabatchreq)| 否 | MetaBatchReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdbatchUpdateSensitiveLevelUsingPOST_1"></a>

## POST batchUpdateSensitiveLevel

POST /api/semantic/metric/batchUpdateSensitiveLevel

> Body 请求参数

```json
{
  "bizNames": [
    "string"
  ],
  "classifications": [
    "string"
  ],
  "ids": [
    0
  ],
  "modelIds": [
    0
  ],
  "sensitiveLevel": 0,
  "status": 0,
  "type": "ADD"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[MetaBatchReq](#schemametabatchreq)| 否 | MetaBatchReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdbatchUpdateStatusUsingPOST_1"></a>

## POST batchUpdateStatus

POST /api/semantic/metric/batchUpdateStatus

> Body 请求参数

```json
{
  "bizNames": [
    "string"
  ],
  "classifications": [
    "string"
  ],
  "ids": [
    0
  ],
  "modelIds": [
    0
  ],
  "sensitiveLevel": 0,
  "status": 0,
  "type": "ADD"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[MetaBatchReq](#schemametabatchreq)| 否 | MetaBatchReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdcreateMetricUsingPOST"></a>

## POST createMetric

POST /api/semantic/metric/createMetric

> Body 请求参数

```json
{
  "alias": "string",
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataFormat": {
    "decimalPlaces": 0,
    "needMultiply100": true
  },
  "dataFormatType": "string",
  "description": "string",
  "ext": {},
  "id": 0,
  "isTag": 0,
  "metricDefineByFieldParams": {
    "expr": "string",
    "fields": [
      {
        "fieldName": "string"
      }
    ],
    "filterSql": "string"
  },
  "metricDefineByMeasureParams": {
    "expr": "string",
    "filterSql": "string",
    "measures": [
      {
        "agg": "string",
        "bizName": "string",
        "constraint": "string"
      }
    ]
  },
  "metricDefineByMetricParams": {
    "expr": "string",
    "filterSql": "string",
    "metrics": [
      {
        "bizName": "string",
        "id": 0
      }
    ]
  },
  "metricDefineType": "FIELD",
  "modelId": 0,
  "name": "string",
  "relateDimension": {
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ]
  },
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[MetricReq](#schemametricreq)| 否 | MetricReq|none|

> 返回示例

> 200 Response

```json
{
  "alias": "string",
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataFormat": {
    "decimalPlaces": 0,
    "needMultiply100": true
  },
  "dataFormatType": "string",
  "defaultAgg": "string",
  "description": "string",
  "domainId": 0,
  "drillDownDimensions": [
    {
      "dimensionId": 0,
      "inheritedFromModel": true,
      "necessary": true
    }
  ],
  "expr": "string",
  "ext": {},
  "hasAdminRes": true,
  "id": 0,
  "isCollect": true,
  "isPublish": 0,
  "isTag": 0,
  "metricDefineByFieldParams": {
    "expr": "string",
    "fields": [
      {
        "fieldName": "string"
      }
    ],
    "filterSql": "string"
  },
  "metricDefineByMeasureParams": {
    "expr": "string",
    "filterSql": "string",
    "measures": [
      {
        "agg": "string",
        "bizName": "string",
        "constraint": "string"
      }
    ]
  },
  "metricDefineByMetricParams": {
    "expr": "string",
    "filterSql": "string",
    "metrics": [
      {
        "bizName": "string",
        "id": 0
      }
    ]
  },
  "metricDefineType": "FIELD",
  "modelBizName": "string",
  "modelId": 0,
  "modelName": "string",
  "name": "string",
  "relaDimensionIdKey": "string",
  "relateDimension": {
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ]
  },
  "sensitiveLevel": 0,
  "similarity": 0,
  "status": 0,
  "type": "string",
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MetricResp](#schemametricresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteMetricUsingDELETE"></a>

## DELETE deleteMetric

DELETE /api/semantic/metric/deleteMetric/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetAllHighSensitiveMetricUsingGET"></a>

## GET getAllHighSensitiveMetric

GET /api/semantic/metric/getAllHighSensitiveMetric

> 返回示例

> 200 Response

```json
[
  {
    "alias": "string",
    "bizName": "string",
    "classifications": [
      "string"
    ],
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataFormat": {
      "decimalPlaces": 0,
      "needMultiply100": true
    },
    "dataFormatType": "string",
    "defaultAgg": "string",
    "description": "string",
    "domainId": 0,
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ],
    "expr": "string",
    "ext": {},
    "hasAdminRes": true,
    "id": 0,
    "isCollect": true,
    "isPublish": 0,
    "isTag": 0,
    "metricDefineByFieldParams": {
      "expr": "string",
      "fields": [
        {
          "fieldName": "string"
        }
      ],
      "filterSql": "string"
    },
    "metricDefineByMeasureParams": {
      "expr": "string",
      "filterSql": "string",
      "measures": [
        {
          "agg": "string",
          "bizName": "string",
          "constraint": "string"
        }
      ]
    },
    "metricDefineByMetricParams": {
      "expr": "string",
      "filterSql": "string",
      "metrics": [
        {
          "bizName": "string",
          "id": 0
        }
      ]
    },
    "metricDefineType": "FIELD",
    "modelBizName": "string",
    "modelId": 0,
    "modelName": "string",
    "name": "string",
    "relaDimensionIdKey": "string",
    "relateDimension": {
      "drillDownDimensions": [
        {
          "dimensionId": 0,
          "inheritedFromModel": true,
          "necessary": true
        }
      ]
    },
    "sensitiveLevel": 0,
    "similarity": 0,
    "status": 0,
    "type": "string",
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[MetricResp](#schemametricresp)]|false|none||none|
|» MetricResp|[MetricResp](#schemametricresp)|false|none|MetricResp|none|
|»» alias|string|false|none||none|
|»» bizName|string|false|none||none|
|»» classifications|[string]|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataFormat|[DataFormat](#schemadataformat)|false|none|DataFormat|none|
|»»» decimalPlaces|integer(int32)|false|none||none|
|»»» needMultiply100|boolean|false|none||none|
|»» dataFormatType|string|false|none||none|
|»» defaultAgg|string|false|none||none|
|»» description|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|»»» DrillDownDimension|[DrillDownDimension](#schemadrilldowndimension)|false|none|DrillDownDimension|none|
|»»»» dimensionId|integer(int64)|false|none||none|
|»»»» inheritedFromModel|boolean|false|none||none|
|»»»» necessary|boolean|false|none||none|
|»» expr|string|false|none||none|
|»» ext|object|false|none||none|
|»» hasAdminRes|boolean|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isCollect|boolean|false|none||none|
|»» isPublish|integer(int32)|false|none||none|
|»» isTag|integer(int32)|false|none||none|
|»» metricDefineByFieldParams|[MetricDefineByFieldParams](#schemametricdefinebyfieldparams)|false|none|MetricDefineByFieldParams|none|
|»»» expr|string|false|none||none|
|»»» fields|[[FieldParam](#schemafieldparam)]|false|none||none|
|»»»» FieldParam|[FieldParam](#schemafieldparam)|false|none|FieldParam|none|
|»»»»» fieldName|string|false|none||none|
|»»» filterSql|string|false|none||none|
|»» metricDefineByMeasureParams|[MetricDefineByMeasureParams](#schemametricdefinebymeasureparams)|false|none|MetricDefineByMeasureParams|none|
|»»» expr|string|false|none||none|
|»»» filterSql|string|false|none||none|
|»»» measures|[[MeasureParam](#schemameasureparam)]|false|none||none|
|»»»» MeasureParam|[MeasureParam](#schemameasureparam)|false|none|MeasureParam|none|
|»»»»» agg|string|false|none||none|
|»»»»» bizName|string|false|none||none|
|»»»»» constraint|string|false|none||none|
|»» metricDefineByMetricParams|[MetricDefineByMetricParams](#schemametricdefinebymetricparams)|false|none|MetricDefineByMetricParams|none|
|»»» expr|string|false|none||none|
|»»» filterSql|string|false|none||none|
|»»» metrics|[[MetricParam](#schemametricparam)]|false|none||none|
|»»»» MetricParam|[MetricParam](#schemametricparam)|false|none|MetricParam|none|
|»»»»» bizName|string|false|none||none|
|»»»»» id|integer(int64)|false|none||none|
|»» metricDefineType|string|false|none||none|
|»» modelBizName|string|false|none||none|
|»» modelId|integer(int64)|false|none||none|
|»» modelName|string|false|none||none|
|»» name|string|false|none||none|
|»» relaDimensionIdKey|string|false|none||none|
|»» relateDimension|[RelateDimension](#schemarelatedimension)|false|none|RelateDimension|none|
|»»» drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|»»»» DrillDownDimension|[DrillDownDimension](#schemadrilldowndimension)|false|none|DrillDownDimension|none|
|»»»»» dimensionId|integer(int64)|false|none||none|
|»»»»» inheritedFromModel|boolean|false|none||none|
|»»»»» necessary|boolean|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» similarity|number(double)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» type|string|false|none||none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|metricDefineType|FIELD|
|metricDefineType|MEASURE|
|metricDefineType|METRIC|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdgetDrillDownDimensionUsingGET"></a>

## GET getDrillDownDimension

GET /api/semantic/metric/getDrillDownDimension

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|metricId|query|integer(int64)| 否 ||metricId|

> 返回示例

> 200 Response

```json
[
  {
    "dimensionId": 0,
    "inheritedFromModel": true,
    "necessary": true
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|» DrillDownDimension|[DrillDownDimension](#schemadrilldowndimension)|false|none|DrillDownDimension|none|
|»» dimensionId|integer(int64)|false|none||none|
|»» inheritedFromModel|boolean|false|none||none|
|»» necessary|boolean|false|none||none|

<a id="opIdgetMetricUsingGET_1"></a>

## GET getMetric

GET /api/semantic/metric/getMetric/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "alias": "string",
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataFormat": {
    "decimalPlaces": 0,
    "needMultiply100": true
  },
  "dataFormatType": "string",
  "defaultAgg": "string",
  "description": "string",
  "domainId": 0,
  "drillDownDimensions": [
    {
      "dimensionId": 0,
      "inheritedFromModel": true,
      "necessary": true
    }
  ],
  "expr": "string",
  "ext": {},
  "hasAdminRes": true,
  "id": 0,
  "isCollect": true,
  "isPublish": 0,
  "isTag": 0,
  "metricDefineByFieldParams": {
    "expr": "string",
    "fields": [
      {
        "fieldName": "string"
      }
    ],
    "filterSql": "string"
  },
  "metricDefineByMeasureParams": {
    "expr": "string",
    "filterSql": "string",
    "measures": [
      {
        "agg": "string",
        "bizName": "string",
        "constraint": "string"
      }
    ]
  },
  "metricDefineByMetricParams": {
    "expr": "string",
    "filterSql": "string",
    "metrics": [
      {
        "bizName": "string",
        "id": 0
      }
    ]
  },
  "metricDefineType": "FIELD",
  "modelBizName": "string",
  "modelId": 0,
  "modelName": "string",
  "name": "string",
  "relaDimensionIdKey": "string",
  "relateDimension": {
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ]
  },
  "sensitiveLevel": 0,
  "similarity": 0,
  "status": 0,
  "type": "string",
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MetricResp](#schemametricresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetMetricUsingGET"></a>

## GET getMetric

GET /api/semantic/metric/getMetric/{modelId}/{bizName}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|modelId|path|integer(int64)| 是 ||modelId|
|bizName|path|string| 是 ||bizName|

> 返回示例

> 200 Response

```json
{
  "alias": "string",
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataFormat": {
    "decimalPlaces": 0,
    "needMultiply100": true
  },
  "dataFormatType": "string",
  "defaultAgg": "string",
  "description": "string",
  "domainId": 0,
  "drillDownDimensions": [
    {
      "dimensionId": 0,
      "inheritedFromModel": true,
      "necessary": true
    }
  ],
  "expr": "string",
  "ext": {},
  "hasAdminRes": true,
  "id": 0,
  "isCollect": true,
  "isPublish": 0,
  "isTag": 0,
  "metricDefineByFieldParams": {
    "expr": "string",
    "fields": [
      {
        "fieldName": "string"
      }
    ],
    "filterSql": "string"
  },
  "metricDefineByMeasureParams": {
    "expr": "string",
    "filterSql": "string",
    "measures": [
      {
        "agg": "string",
        "bizName": "string",
        "constraint": "string"
      }
    ]
  },
  "metricDefineByMetricParams": {
    "expr": "string",
    "filterSql": "string",
    "metrics": [
      {
        "bizName": "string",
        "id": 0
      }
    ]
  },
  "metricDefineType": "FIELD",
  "modelBizName": "string",
  "modelId": 0,
  "modelName": "string",
  "name": "string",
  "relaDimensionIdKey": "string",
  "relateDimension": {
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ]
  },
  "sensitiveLevel": 0,
  "similarity": 0,
  "status": 0,
  "type": "string",
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MetricResp](#schemametricresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetMetricClassificationsUsingGET"></a>

## GET getMetricClassifications

GET /api/semantic/metric/getMetricClassifications

> 返回示例

> 200 Response

```json
[
  "string"
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetMetricListUsingGET"></a>

## GET getMetricList

GET /api/semantic/metric/getMetricList/{modelId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|modelId|path|integer(int64)| 是 ||modelId|

> 返回示例

> 200 Response

```json
[
  {
    "alias": "string",
    "bizName": "string",
    "classifications": [
      "string"
    ],
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataFormat": {
      "decimalPlaces": 0,
      "needMultiply100": true
    },
    "dataFormatType": "string",
    "defaultAgg": "string",
    "description": "string",
    "domainId": 0,
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ],
    "expr": "string",
    "ext": {},
    "hasAdminRes": true,
    "id": 0,
    "isCollect": true,
    "isPublish": 0,
    "isTag": 0,
    "metricDefineByFieldParams": {
      "expr": "string",
      "fields": [
        {
          "fieldName": "string"
        }
      ],
      "filterSql": "string"
    },
    "metricDefineByMeasureParams": {
      "expr": "string",
      "filterSql": "string",
      "measures": [
        {
          "agg": "string",
          "bizName": "string",
          "constraint": "string"
        }
      ]
    },
    "metricDefineByMetricParams": {
      "expr": "string",
      "filterSql": "string",
      "metrics": [
        {
          "bizName": "string",
          "id": 0
        }
      ]
    },
    "metricDefineType": "FIELD",
    "modelBizName": "string",
    "modelId": 0,
    "modelName": "string",
    "name": "string",
    "relaDimensionIdKey": "string",
    "relateDimension": {
      "drillDownDimensions": [
        {
          "dimensionId": 0,
          "inheritedFromModel": true,
          "necessary": true
        }
      ]
    },
    "sensitiveLevel": 0,
    "similarity": 0,
    "status": 0,
    "type": "string",
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[MetricResp](#schemametricresp)]|false|none||none|
|» MetricResp|[MetricResp](#schemametricresp)|false|none|MetricResp|none|
|»» alias|string|false|none||none|
|»» bizName|string|false|none||none|
|»» classifications|[string]|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataFormat|[DataFormat](#schemadataformat)|false|none|DataFormat|none|
|»»» decimalPlaces|integer(int32)|false|none||none|
|»»» needMultiply100|boolean|false|none||none|
|»» dataFormatType|string|false|none||none|
|»» defaultAgg|string|false|none||none|
|»» description|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|»»» DrillDownDimension|[DrillDownDimension](#schemadrilldowndimension)|false|none|DrillDownDimension|none|
|»»»» dimensionId|integer(int64)|false|none||none|
|»»»» inheritedFromModel|boolean|false|none||none|
|»»»» necessary|boolean|false|none||none|
|»» expr|string|false|none||none|
|»» ext|object|false|none||none|
|»» hasAdminRes|boolean|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isCollect|boolean|false|none||none|
|»» isPublish|integer(int32)|false|none||none|
|»» isTag|integer(int32)|false|none||none|
|»» metricDefineByFieldParams|[MetricDefineByFieldParams](#schemametricdefinebyfieldparams)|false|none|MetricDefineByFieldParams|none|
|»»» expr|string|false|none||none|
|»»» fields|[[FieldParam](#schemafieldparam)]|false|none||none|
|»»»» FieldParam|[FieldParam](#schemafieldparam)|false|none|FieldParam|none|
|»»»»» fieldName|string|false|none||none|
|»»» filterSql|string|false|none||none|
|»» metricDefineByMeasureParams|[MetricDefineByMeasureParams](#schemametricdefinebymeasureparams)|false|none|MetricDefineByMeasureParams|none|
|»»» expr|string|false|none||none|
|»»» filterSql|string|false|none||none|
|»»» measures|[[MeasureParam](#schemameasureparam)]|false|none||none|
|»»»» MeasureParam|[MeasureParam](#schemameasureparam)|false|none|MeasureParam|none|
|»»»»» agg|string|false|none||none|
|»»»»» bizName|string|false|none||none|
|»»»»» constraint|string|false|none||none|
|»» metricDefineByMetricParams|[MetricDefineByMetricParams](#schemametricdefinebymetricparams)|false|none|MetricDefineByMetricParams|none|
|»»» expr|string|false|none||none|
|»»» filterSql|string|false|none||none|
|»»» metrics|[[MetricParam](#schemametricparam)]|false|none||none|
|»»»» MetricParam|[MetricParam](#schemametricparam)|false|none|MetricParam|none|
|»»»»» bizName|string|false|none||none|
|»»»»» id|integer(int64)|false|none||none|
|»» metricDefineType|string|false|none||none|
|»» modelBizName|string|false|none||none|
|»» modelId|integer(int64)|false|none||none|
|»» modelName|string|false|none||none|
|»» name|string|false|none||none|
|»» relaDimensionIdKey|string|false|none||none|
|»» relateDimension|[RelateDimension](#schemarelatedimension)|false|none|RelateDimension|none|
|»»» drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|»»»» DrillDownDimension|[DrillDownDimension](#schemadrilldowndimension)|false|none|DrillDownDimension|none|
|»»»»» dimensionId|integer(int64)|false|none||none|
|»»»»» inheritedFromModel|boolean|false|none||none|
|»»»»» necessary|boolean|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» similarity|number(double)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» type|string|false|none||none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|metricDefineType|FIELD|
|metricDefineType|MEASURE|
|metricDefineType|METRIC|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdgetMetricQueryDefaultConfigUsingGET"></a>

## GET getMetricQueryDefaultConfig

GET /api/semantic/metric/getMetricQueryDefaultConfig/{metricId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|metricId|path|integer(int64)| 是 ||metricId|

> 返回示例

> 200 Response

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "defaultConfig": "string",
  "id": 0,
  "metricId": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "userName": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MetricQueryDefaultConfig](#schemametricquerydefaultconfig)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetMetricQueryDefaultConfigUsingPUT"></a>

## PUT getMetricQueryDefaultConfig

PUT /api/semantic/metric/getMetricQueryDefaultConfig/{metricId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|metricId|path|integer(int64)| 是 ||metricId|

> 返回示例

> 200 Response

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "defaultConfig": "string",
  "id": 0,
  "metricId": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "userName": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MetricQueryDefaultConfig](#schemametricquerydefaultconfig)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetMetricQueryDefaultConfigUsingPOST"></a>

## POST getMetricQueryDefaultConfig

POST /api/semantic/metric/getMetricQueryDefaultConfig/{metricId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|metricId|path|integer(int64)| 是 ||metricId|

> 返回示例

> 200 Response

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "defaultConfig": "string",
  "id": 0,
  "metricId": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "userName": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MetricQueryDefaultConfig](#schemametricquerydefaultconfig)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetMetricQueryDefaultConfigUsingDELETE"></a>

## DELETE getMetricQueryDefaultConfig

DELETE /api/semantic/metric/getMetricQueryDefaultConfig/{metricId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|metricId|path|integer(int64)| 是 ||metricId|

> 返回示例

> 200 Response

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "defaultConfig": "string",
  "id": 0,
  "metricId": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "userName": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MetricQueryDefaultConfig](#schemametricquerydefaultconfig)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetMetricQueryDefaultConfigUsingOPTIONS"></a>

## OPTIONS getMetricQueryDefaultConfig

OPTIONS /api/semantic/metric/getMetricQueryDefaultConfig/{metricId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|metricId|path|integer(int64)| 是 ||metricId|

> 返回示例

> 200 Response

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "defaultConfig": "string",
  "id": 0,
  "metricId": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "userName": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MetricQueryDefaultConfig](#schemametricquerydefaultconfig)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetMetricQueryDefaultConfigUsingHEAD"></a>

## HEAD getMetricQueryDefaultConfig

HEAD /api/semantic/metric/getMetricQueryDefaultConfig/{metricId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|metricId|path|integer(int64)| 是 ||metricId|

> 返回示例

> 200 Response

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "defaultConfig": "string",
  "id": 0,
  "metricId": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "userName": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MetricQueryDefaultConfig](#schemametricquerydefaultconfig)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetMetricQueryDefaultConfigUsingPATCH"></a>

## PATCH getMetricQueryDefaultConfig

PATCH /api/semantic/metric/getMetricQueryDefaultConfig/{metricId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|metricId|path|integer(int64)| 是 ||metricId|

> 返回示例

> 200 Response

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "defaultConfig": "string",
  "id": 0,
  "metricId": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "userName": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MetricQueryDefaultConfig](#schemametricquerydefaultconfig)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetMetricQueryDefaultConfigUsingTRACE"></a>

## TRACE getMetricQueryDefaultConfig

TRACE /api/semantic/metric/getMetricQueryDefaultConfig/{metricId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|metricId|path|integer(int64)| 是 ||metricId|

> 返回示例

> 200 Response

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "defaultConfig": "string",
  "id": 0,
  "metricId": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "userName": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MetricQueryDefaultConfig](#schemametricquerydefaultconfig)|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetMetricTagsUsingGET"></a>

## GET getMetricTags

GET /api/semantic/metric/getMetricTags

> 返回示例

> 200 Response

```json
[
  "string"
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetMetricsToCreateNewMetricUsingGET"></a>

## GET getMetricsToCreateNewMetric

GET /api/semantic/metric/getMetricsToCreateNewMetric/{modelId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|modelId|path|integer(int64)| 是 ||modelId|

> 返回示例

> 200 Response

```json
[
  {
    "alias": "string",
    "bizName": "string",
    "classifications": [
      "string"
    ],
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataFormat": {
      "decimalPlaces": 0,
      "needMultiply100": true
    },
    "dataFormatType": "string",
    "defaultAgg": "string",
    "description": "string",
    "domainId": 0,
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ],
    "expr": "string",
    "ext": {},
    "hasAdminRes": true,
    "id": 0,
    "isCollect": true,
    "isPublish": 0,
    "isTag": 0,
    "metricDefineByFieldParams": {
      "expr": "string",
      "fields": [
        {
          "fieldName": "string"
        }
      ],
      "filterSql": "string"
    },
    "metricDefineByMeasureParams": {
      "expr": "string",
      "filterSql": "string",
      "measures": [
        {
          "agg": "string",
          "bizName": "string",
          "constraint": "string"
        }
      ]
    },
    "metricDefineByMetricParams": {
      "expr": "string",
      "filterSql": "string",
      "metrics": [
        {
          "bizName": "string",
          "id": 0
        }
      ]
    },
    "metricDefineType": "FIELD",
    "modelBizName": "string",
    "modelId": 0,
    "modelName": "string",
    "name": "string",
    "relaDimensionIdKey": "string",
    "relateDimension": {
      "drillDownDimensions": [
        {
          "dimensionId": 0,
          "inheritedFromModel": true,
          "necessary": true
        }
      ]
    },
    "sensitiveLevel": 0,
    "similarity": 0,
    "status": 0,
    "type": "string",
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[MetricResp](#schemametricresp)]|false|none||none|
|» MetricResp|[MetricResp](#schemametricresp)|false|none|MetricResp|none|
|»» alias|string|false|none||none|
|»» bizName|string|false|none||none|
|»» classifications|[string]|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataFormat|[DataFormat](#schemadataformat)|false|none|DataFormat|none|
|»»» decimalPlaces|integer(int32)|false|none||none|
|»»» needMultiply100|boolean|false|none||none|
|»» dataFormatType|string|false|none||none|
|»» defaultAgg|string|false|none||none|
|»» description|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|»»» DrillDownDimension|[DrillDownDimension](#schemadrilldowndimension)|false|none|DrillDownDimension|none|
|»»»» dimensionId|integer(int64)|false|none||none|
|»»»» inheritedFromModel|boolean|false|none||none|
|»»»» necessary|boolean|false|none||none|
|»» expr|string|false|none||none|
|»» ext|object|false|none||none|
|»» hasAdminRes|boolean|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isCollect|boolean|false|none||none|
|»» isPublish|integer(int32)|false|none||none|
|»» isTag|integer(int32)|false|none||none|
|»» metricDefineByFieldParams|[MetricDefineByFieldParams](#schemametricdefinebyfieldparams)|false|none|MetricDefineByFieldParams|none|
|»»» expr|string|false|none||none|
|»»» fields|[[FieldParam](#schemafieldparam)]|false|none||none|
|»»»» FieldParam|[FieldParam](#schemafieldparam)|false|none|FieldParam|none|
|»»»»» fieldName|string|false|none||none|
|»»» filterSql|string|false|none||none|
|»» metricDefineByMeasureParams|[MetricDefineByMeasureParams](#schemametricdefinebymeasureparams)|false|none|MetricDefineByMeasureParams|none|
|»»» expr|string|false|none||none|
|»»» filterSql|string|false|none||none|
|»»» measures|[[MeasureParam](#schemameasureparam)]|false|none||none|
|»»»» MeasureParam|[MeasureParam](#schemameasureparam)|false|none|MeasureParam|none|
|»»»»» agg|string|false|none||none|
|»»»»» bizName|string|false|none||none|
|»»»»» constraint|string|false|none||none|
|»» metricDefineByMetricParams|[MetricDefineByMetricParams](#schemametricdefinebymetricparams)|false|none|MetricDefineByMetricParams|none|
|»»» expr|string|false|none||none|
|»»» filterSql|string|false|none||none|
|»»» metrics|[[MetricParam](#schemametricparam)]|false|none||none|
|»»»» MetricParam|[MetricParam](#schemametricparam)|false|none|MetricParam|none|
|»»»»» bizName|string|false|none||none|
|»»»»» id|integer(int64)|false|none||none|
|»» metricDefineType|string|false|none||none|
|»» modelBizName|string|false|none||none|
|»» modelId|integer(int64)|false|none||none|
|»» modelName|string|false|none||none|
|»» name|string|false|none||none|
|»» relaDimensionIdKey|string|false|none||none|
|»» relateDimension|[RelateDimension](#schemarelatedimension)|false|none|RelateDimension|none|
|»»» drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|»»»» DrillDownDimension|[DrillDownDimension](#schemadrilldowndimension)|false|none|DrillDownDimension|none|
|»»»»» dimensionId|integer(int64)|false|none||none|
|»»»»» inheritedFromModel|boolean|false|none||none|
|»»»»» necessary|boolean|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» similarity|number(double)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» type|string|false|none||none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|metricDefineType|FIELD|
|metricDefineType|MEASURE|
|metricDefineType|METRIC|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdmockMetricAliasUsingPOST_1"></a>

## POST mockMetricAlias

POST /api/semantic/metric/mockMetricAlias

> Body 请求参数

```json
{
  "alias": "string",
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataFormat": {
    "decimalPlaces": 0,
    "needMultiply100": true
  },
  "dataFormatType": "string",
  "description": "string",
  "ext": {},
  "id": 0,
  "isTag": 0,
  "modelId": 0,
  "name": "string",
  "relateDimension": {
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ]
  },
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[MetricBaseReq](#schemametricbasereq)| 否 | MetricBaseReq|none|

> 返回示例

> 200 Response

```json
[
  "string"
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryMetricUsingPOST"></a>

## POST queryMetric

POST /api/semantic/metric/queryMetric

> Body 请求参数

```json
{
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdBy": "string",
  "current": 0,
  "domainIds": [
    0
  ],
  "hasCollect": true,
  "id": "string",
  "ids": [
    0
  ],
  "isPublish": 0,
  "isTag": 0,
  "key": "string",
  "modelIds": [
    0
  ],
  "name": "string",
  "orderCondition": "string",
  "pageSize": 0,
  "sensitiveLevel": 0,
  "sort": "string",
  "status": 0,
  "type": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[PageMetricReq](#schemapagemetricreq)| 否 | PageMetricReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "alias": "string",
      "bizName": "string",
      "classifications": [
        "string"
      ],
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "defaultAgg": "string",
      "description": "string",
      "domainId": 0,
      "drillDownDimensions": [
        {
          "dimensionId": 0,
          "inheritedFromModel": true,
          "necessary": true
        }
      ],
      "expr": "string",
      "ext": {},
      "hasAdminRes": true,
      "id": 0,
      "isCollect": true,
      "isPublish": 0,
      "isTag": 0,
      "metricDefineByFieldParams": {
        "expr": "string",
        "fields": [
          {
            "fieldName": "string"
          }
        ],
        "filterSql": "string"
      },
      "metricDefineByMeasureParams": {
        "expr": "string",
        "filterSql": "string",
        "measures": [
          {
            "agg": "string",
            "bizName": "string",
            "constraint": "string"
          }
        ]
      },
      "metricDefineByMetricParams": {
        "expr": "string",
        "filterSql": "string",
        "metrics": [
          {
            "bizName": "string",
            "id": 0
          }
        ]
      },
      "metricDefineType": "FIELD",
      "modelBizName": "string",
      "modelId": 0,
      "modelName": "string",
      "name": "string",
      "relaDimensionIdKey": "string",
      "relateDimension": {
        "drillDownDimensions": [
          {
            "dimensionId": 0,
            "inheritedFromModel": true,
            "necessary": true
          }
        ]
      },
      "sensitiveLevel": 0,
      "similarity": 0,
      "status": 0,
      "type": "string",
      "typeEnum": "DATASET",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdsaveMetricQueryDefaultConfigUsingPOST"></a>

## POST saveMetricQueryDefaultConfig

POST /api/semantic/metric/saveMetricQueryDefaultConfig

> Body 请求参数

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "defaultConfig": "string",
  "id": 0,
  "metricId": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "userName": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[MetricQueryDefaultConfig](#schemametricquerydefaultconfig)| 否 | MetricQueryDefaultConfig|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdupdateMetricUsingPOST"></a>

## POST updateMetric

POST /api/semantic/metric/updateMetric

> Body 请求参数

```json
{
  "alias": "string",
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataFormat": {
    "decimalPlaces": 0,
    "needMultiply100": true
  },
  "dataFormatType": "string",
  "description": "string",
  "ext": {},
  "id": 0,
  "isTag": 0,
  "metricDefineByFieldParams": {
    "expr": "string",
    "fields": [
      {
        "fieldName": "string"
      }
    ],
    "filterSql": "string"
  },
  "metricDefineByMeasureParams": {
    "expr": "string",
    "filterSql": "string",
    "measures": [
      {
        "agg": "string",
        "bizName": "string",
        "constraint": "string"
      }
    ]
  },
  "metricDefineByMetricParams": {
    "expr": "string",
    "filterSql": "string",
    "metrics": [
      {
        "bizName": "string",
        "id": 0
      }
    ]
  },
  "metricDefineType": "FIELD",
  "modelId": 0,
  "name": "string",
  "relateDimension": {
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ]
  },
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[MetricReq](#schemametricreq)| 否 | MetricReq|none|

> 返回示例

> 200 Response

```json
{
  "alias": "string",
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataFormat": {
    "decimalPlaces": 0,
    "needMultiply100": true
  },
  "dataFormatType": "string",
  "defaultAgg": "string",
  "description": "string",
  "domainId": 0,
  "drillDownDimensions": [
    {
      "dimensionId": 0,
      "inheritedFromModel": true,
      "necessary": true
    }
  ],
  "expr": "string",
  "ext": {},
  "hasAdminRes": true,
  "id": 0,
  "isCollect": true,
  "isPublish": 0,
  "isTag": 0,
  "metricDefineByFieldParams": {
    "expr": "string",
    "fields": [
      {
        "fieldName": "string"
      }
    ],
    "filterSql": "string"
  },
  "metricDefineByMeasureParams": {
    "expr": "string",
    "filterSql": "string",
    "measures": [
      {
        "agg": "string",
        "bizName": "string",
        "constraint": "string"
      }
    ]
  },
  "metricDefineByMetricParams": {
    "expr": "string",
    "filterSql": "string",
    "metrics": [
      {
        "bizName": "string",
        "id": 0
      }
    ]
  },
  "metricDefineType": "FIELD",
  "modelBizName": "string",
  "modelId": 0,
  "modelName": "string",
  "name": "string",
  "relaDimensionIdKey": "string",
  "relateDimension": {
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ]
  },
  "sensitiveLevel": 0,
  "similarity": 0,
  "status": 0,
  "type": "string",
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[MetricResp](#schemametricresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# metric-query-api-controller

<a id="opIddownloadMetricUsingPOST"></a>

## POST downloadMetric

POST /api/semantic/query/download/metric

> Body 请求参数

```json
{
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "dimensionIds": [
    0
  ],
  "dimensionNames": [
    "string"
  ],
  "domainId": 0,
  "filters": [
    {
      "bizName": "string",
      "children": [
        {
          "bizName": "string",
          "children": [
            {}
          ],
          "id": 0,
          "name": "string",
          "operator": "!=",
          "relation": "AND",
          "value": {}
        }
      ],
      "id": 0,
      "name": "string",
      "operator": "!=",
      "relation": "AND",
      "value": {}
    }
  ],
  "innerLayerNative": true,
  "isTransform": true,
  "limit": 0,
  "metricIds": [
    0
  ],
  "metricNames": [
    "string"
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[DownloadMetricReq](#schemadownloadmetricreq)| 否 | DownloadMetricReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddownloadBatchUsingPOST"></a>

## POST downloadBatch

POST /api/semantic/query/downloadBatch/metric

> Body 请求参数

```json
{
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "metricIds": [
    0
  ],
  "transform": true
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[BatchDownloadReq](#schemabatchdownloadreq)| 否 | BatchDownloadReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryByMetricUsingPOST"></a>

## POST queryByMetric

POST /api/semantic/query/metric

> Body 请求参数

```json
{
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "dimensionIds": [
    0
  ],
  "dimensionNames": [
    "string"
  ],
  "domainId": 0,
  "filters": [
    {
      "bizName": "string",
      "children": [
        {
          "bizName": "string",
          "children": [
            {}
          ],
          "id": 0,
          "name": "string",
          "operator": "!=",
          "relation": "AND",
          "value": {}
        }
      ],
      "id": 0,
      "name": "string",
      "operator": "!=",
      "relation": "AND",
      "value": {}
    }
  ],
  "innerLayerNative": true,
  "limit": 0,
  "metricIds": [
    0
  ],
  "metricNames": [
    "string"
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QueryMetricReq](#schemaquerymetricreq)| 否 | QueryMetricReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# model-controller

<a id="opIdbatchUpdateStatusUsingPOST_2"></a>

## POST batchUpdateStatus

POST /api/semantic/model/batchUpdateStatus

> Body 请求参数

```json
{
  "bizNames": [
    "string"
  ],
  "classifications": [
    "string"
  ],
  "ids": [
    0
  ],
  "modelIds": [
    0
  ],
  "sensitiveLevel": 0,
  "status": 0,
  "type": "ADD"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[MetaBatchReq](#schemametabatchreq)| 否 | MetaBatchReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdcreateModelUsingPOST"></a>

## POST createModel

POST /api/semantic/model/createModel

> Body 请求参数

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "databaseId": 0,
  "description": "string",
  "domainId": 0,
  "drillDownDimensions": [
    {
      "dimensionId": 0,
      "inheritedFromModel": true,
      "necessary": true
    }
  ],
  "ext": {},
  "filterSql": "string",
  "id": 0,
  "isOpen": 0,
  "modelDetail": {
    "dimensions": [
      {
        "bizName": "string",
        "dateFormat": "string",
        "description": "string",
        "expr": "string",
        "isCreateDimension": 0,
        "isTag": 0,
        "name": "string",
        "type": "string",
        "typeParams": {
          "isPrimary": "string",
          "timeGranularity": "string"
        }
      }
    ],
    "fields": [
      {
        "dataType": "string",
        "fieldName": "string"
      }
    ],
    "identifiers": [
      {
        "bizName": "string",
        "entityNames": [
          "string"
        ],
        "isCreateDimension": 0,
        "name": "string",
        "type": "string"
      }
    ],
    "measures": [
      {
        "agg": "string",
        "alias": "string",
        "bizName": "string",
        "constraint": "string",
        "expr": "string",
        "isCreateMetric": 0,
        "name": "string"
      }
    ],
    "queryType": "string",
    "sqlQuery": "string",
    "sqlVariables": [
      {
        "defaultValues": [
          {}
        ],
        "name": "string",
        "valueType": "EXPR"
      }
    ],
    "tableQuery": "string"
  },
  "name": "string",
  "sensitiveLevel": 0,
  "sourceType": "string",
  "status": 0,
  "tagObjectId": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "viewOrgs": [
    "string"
  ],
  "viewers": [
    "string"
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ModelReq](#schemamodelreq)| 否 | ModelReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteModelUsingDELETE"></a>

## DELETE deleteModel

DELETE /api/semantic/model/deleteModel/{modelId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|modelId|path|integer(int64)| 是 ||modelId|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetAllModelByDomainIdUsingGET"></a>

## GET getAllModelByDomainId

GET /api/semantic/model/getAllModelByDomainId

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|query|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
[
  {
    "adminOrgs": [
      "string"
    ],
    "admins": [
      "string"
    ],
    "alias": "string",
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "databaseId": 0,
    "depends": "string",
    "description": "string",
    "domainId": 0,
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ],
    "ext": {},
    "fieldList": [
      "string"
    ],
    "filterSql": "string",
    "fullPath": "string",
    "id": 0,
    "isOpen": 0,
    "modelDetail": {
      "dimensions": [
        {
          "bizName": "string",
          "dateFormat": "string",
          "description": "string",
          "expr": "string",
          "fieldName": "string",
          "isCreateDimension": 0,
          "isTag": 0,
          "name": "string",
          "type": "string",
          "typeParams": {
            "isPrimary": null,
            "timeGranularity": null
          }
        }
      ],
      "fields": [
        {
          "dataType": "string",
          "fieldName": "string"
        }
      ],
      "identifiers": [
        {
          "bizName": "string",
          "entityNames": [
            "string"
          ],
          "fieldName": "string",
          "isCreateDimension": 0,
          "name": "string",
          "type": "string"
        }
      ],
      "measures": [
        {
          "agg": "string",
          "alias": "string",
          "bizName": "string",
          "constraint": "string",
          "expr": "string",
          "fieldName": "string",
          "isCreateMetric": 0,
          "name": "string"
        }
      ],
      "queryType": "string",
      "sqlQuery": "string",
      "sqlVariables": [
        {
          "defaultValues": [
            {}
          ],
          "name": "string",
          "valueType": "EXPR"
        }
      ],
      "tableQuery": "string"
    },
    "name": "string",
    "primaryIdentify": {
      "bizName": "string",
      "entityNames": [
        "string"
      ],
      "fieldName": "string",
      "isCreateDimension": 0,
      "name": "string",
      "type": "string"
    },
    "sensitiveLevel": 0,
    "status": 0,
    "tagObjectId": 0,
    "timeDimension": [
      {
        "bizName": "string",
        "dateFormat": "string",
        "description": "string",
        "expr": "string",
        "fieldName": "string",
        "isCreateDimension": 0,
        "isTag": 0,
        "name": "string",
        "type": "string",
        "typeParams": {
          "isPrimary": "string",
          "timeGranularity": "string"
        }
      }
    ],
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "viewOrgs": [
      "string"
    ],
    "viewers": [
      "string"
    ]
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ModelResp](#schemamodelresp)]|false|none||none|
|» ModelResp|[ModelResp](#schemamodelresp)|false|none|ModelResp|none|
|»» adminOrgs|[string]|false|none||none|
|»» admins|[string]|false|none||none|
|»» alias|string|false|none||none|
|»» bizName|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» databaseId|integer(int64)|false|none||none|
|»» depends|string|false|none||none|
|»» description|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|»»» DrillDownDimension|[DrillDownDimension](#schemadrilldowndimension)|false|none|DrillDownDimension|none|
|»»»» dimensionId|integer(int64)|false|none||none|
|»»»» inheritedFromModel|boolean|false|none||none|
|»»»» necessary|boolean|false|none||none|
|»» ext|object|false|none||none|
|»» fieldList|[string]|false|none||none|
|»» filterSql|string|false|none||none|
|»» fullPath|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isOpen|integer(int32)|false|none||none|
|»» modelDetail|[ModelDetail](#schemamodeldetail)|false|none|ModelDetail|none|
|»»» dimensions|[[Dim](#schemadim)]|false|none||none|
|»»»» Dim|[Dim](#schemadim)|false|none|Dim|none|
|»»»»» bizName|string|false|none||none|
|»»»»» dateFormat|string|false|none||none|
|»»»»» description|string|false|none||none|
|»»»»» expr|string|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»»» isTag|integer(int32)|false|none||none|
|»»»»» name|string|false|none||none|
|»»»»» type|string|false|none||none|
|»»»»» typeParams|[DimensionTimeTypeParams](#schemadimensiontimetypeparams)|false|none|DimensionTimeTypeParams|none|
|»»»»»» isPrimary|string|false|none||none|
|»»»»»» timeGranularity|string|false|none||none|
|»»» fields|[[Field](#schemafield)]|false|none||none|
|»»»» Field|[Field](#schemafield)|false|none|Field|none|
|»»»»» dataType|string|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»» identifiers|[[Identify](#schemaidentify)]|false|none||none|
|»»»» Identify|[Identify](#schemaidentify)|false|none|Identify|none|
|»»»»» bizName|string|false|none||none|
|»»»»» entityNames|[string]|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»»» name|string|false|none||none|
|»»»»» type|string|false|none||none|
|»»» measures|[[Measure](#schemameasure)]|false|none||none|
|»»»» Measure|[Measure](#schemameasure)|false|none|Measure|none|
|»»»»» agg|string|false|none||none|
|»»»»» alias|string|false|none||none|
|»»»»» bizName|string|false|none||none|
|»»»»» constraint|string|false|none||none|
|»»»»» expr|string|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»»»» isCreateMetric|integer(int32)|false|none||none|
|»»»»» name|string|false|none||none|
|»»» queryType|string|false|none||none|
|»»» sqlQuery|string|false|none||none|
|»»» sqlVariables|[[SqlVariable](#schemasqlvariable)]|false|none||none|
|»»»» SqlVariable|[SqlVariable](#schemasqlvariable)|false|none|SqlVariable|none|
|»»»»» defaultValues|[object]|false|none||none|
|»»»»» name|string|false|none||none|
|»»»»» valueType|string|false|none||none|
|»»» tableQuery|string|false|none||none|
|»» name|string|false|none||none|
|»» primaryIdentify|[Identify](#schemaidentify)|false|none|Identify|none|
|»»» bizName|string|false|none||none|
|»»» entityNames|[string]|false|none||none|
|»»» fieldName|string|false|none||none|
|»»» isCreateDimension|integer(int32)|false|none||none|
|»»» name|string|false|none||none|
|»»» type|string|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» tagObjectId|integer(int64)|false|none||none|
|»» timeDimension|[[Dim](#schemadim)]|false|none||none|
|»»» Dim|[Dim](#schemadim)|false|none|Dim|none|
|»»»» bizName|string|false|none||none|
|»»»» dateFormat|string|false|none||none|
|»»»» description|string|false|none||none|
|»»»» expr|string|false|none||none|
|»»»» fieldName|string|false|none||none|
|»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»» isTag|integer(int32)|false|none||none|
|»»»» name|string|false|none||none|
|»»»» type|string|false|none||none|
|»»»» typeParams|[DimensionTimeTypeParams](#schemadimensiontimetypeparams)|false|none|DimensionTimeTypeParams|none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» viewOrgs|[string]|false|none||none|
|»» viewers|[string]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|valueType|EXPR|
|valueType|NUMBER|
|valueType|STRING|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdgetModelUsingGET"></a>

## GET getModel

GET /api/semantic/model/getModel/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "databaseId": 0,
  "depends": "string",
  "description": "string",
  "domainId": 0,
  "drillDownDimensions": [
    {
      "dimensionId": 0,
      "inheritedFromModel": true,
      "necessary": true
    }
  ],
  "ext": {},
  "fieldList": [
    "string"
  ],
  "filterSql": "string",
  "fullPath": "string",
  "id": 0,
  "isOpen": 0,
  "modelDetail": {
    "dimensions": [
      {
        "bizName": "string",
        "dateFormat": "string",
        "description": "string",
        "expr": "string",
        "fieldName": "string",
        "isCreateDimension": 0,
        "isTag": 0,
        "name": "string",
        "type": "string",
        "typeParams": {
          "isPrimary": "string",
          "timeGranularity": "string"
        }
      }
    ],
    "fields": [
      {
        "dataType": "string",
        "fieldName": "string"
      }
    ],
    "identifiers": [
      {
        "bizName": "string",
        "entityNames": [
          "string"
        ],
        "fieldName": "string",
        "isCreateDimension": 0,
        "name": "string",
        "type": "string"
      }
    ],
    "measures": [
      {
        "agg": "string",
        "alias": "string",
        "bizName": "string",
        "constraint": "string",
        "expr": "string",
        "fieldName": "string",
        "isCreateMetric": 0,
        "name": "string"
      }
    ],
    "queryType": "string",
    "sqlQuery": "string",
    "sqlVariables": [
      {
        "defaultValues": [
          {}
        ],
        "name": "string",
        "valueType": "EXPR"
      }
    ],
    "tableQuery": "string"
  },
  "name": "string",
  "primaryIdentify": {
    "bizName": "string",
    "entityNames": [
      "string"
    ],
    "fieldName": "string",
    "isCreateDimension": 0,
    "name": "string",
    "type": "string"
  },
  "sensitiveLevel": 0,
  "status": 0,
  "tagObjectId": 0,
  "timeDimension": [
    {
      "bizName": "string",
      "dateFormat": "string",
      "description": "string",
      "expr": "string",
      "fieldName": "string",
      "isCreateDimension": 0,
      "isTag": 0,
      "name": "string",
      "type": "string",
      "typeParams": {
        "isPrimary": "string",
        "timeGranularity": "string"
      }
    }
  ],
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "viewOrgs": [
    "string"
  ],
  "viewers": [
    "string"
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ModelResp](#schemamodelresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetModelDatabaseUsingGET"></a>

## GET getModelDatabase

GET /api/semantic/model/getModelDatabase/{modelId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|modelId|path|integer(int64)| 是 ||modelId|

> 返回示例

> 200 Response

```json
{
  "admins": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "database": "string",
  "description": "string",
  "hasEditPermission": true,
  "hasPermission": true,
  "hasUsePermission": true,
  "host": "string",
  "id": 0,
  "name": "string",
  "password": "string",
  "port": "string",
  "schema": "string",
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "url": "string",
  "username": "string",
  "version": "string",
  "viewers": [
    "string"
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[DatabaseResp](#schemadatabaseresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetModelListUsingGET"></a>

## GET getModelList

GET /api/semantic/model/getModelList/{domainId}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|path|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
[
  {
    "adminOrgs": [
      "string"
    ],
    "admins": [
      "string"
    ],
    "alias": "string",
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "databaseId": 0,
    "depends": "string",
    "description": "string",
    "domainId": 0,
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ],
    "ext": {},
    "fieldList": [
      "string"
    ],
    "filterSql": "string",
    "fullPath": "string",
    "id": 0,
    "isOpen": 0,
    "modelDetail": {
      "dimensions": [
        {
          "bizName": "string",
          "dateFormat": "string",
          "description": "string",
          "expr": "string",
          "fieldName": "string",
          "isCreateDimension": 0,
          "isTag": 0,
          "name": "string",
          "type": "string",
          "typeParams": {
            "isPrimary": null,
            "timeGranularity": null
          }
        }
      ],
      "fields": [
        {
          "dataType": "string",
          "fieldName": "string"
        }
      ],
      "identifiers": [
        {
          "bizName": "string",
          "entityNames": [
            "string"
          ],
          "fieldName": "string",
          "isCreateDimension": 0,
          "name": "string",
          "type": "string"
        }
      ],
      "measures": [
        {
          "agg": "string",
          "alias": "string",
          "bizName": "string",
          "constraint": "string",
          "expr": "string",
          "fieldName": "string",
          "isCreateMetric": 0,
          "name": "string"
        }
      ],
      "queryType": "string",
      "sqlQuery": "string",
      "sqlVariables": [
        {
          "defaultValues": [
            {}
          ],
          "name": "string",
          "valueType": "EXPR"
        }
      ],
      "tableQuery": "string"
    },
    "name": "string",
    "primaryIdentify": {
      "bizName": "string",
      "entityNames": [
        "string"
      ],
      "fieldName": "string",
      "isCreateDimension": 0,
      "name": "string",
      "type": "string"
    },
    "sensitiveLevel": 0,
    "status": 0,
    "tagObjectId": 0,
    "timeDimension": [
      {
        "bizName": "string",
        "dateFormat": "string",
        "description": "string",
        "expr": "string",
        "fieldName": "string",
        "isCreateDimension": 0,
        "isTag": 0,
        "name": "string",
        "type": "string",
        "typeParams": {
          "isPrimary": "string",
          "timeGranularity": "string"
        }
      }
    ],
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "viewOrgs": [
      "string"
    ],
    "viewers": [
      "string"
    ]
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ModelResp](#schemamodelresp)]|false|none||none|
|» ModelResp|[ModelResp](#schemamodelresp)|false|none|ModelResp|none|
|»» adminOrgs|[string]|false|none||none|
|»» admins|[string]|false|none||none|
|»» alias|string|false|none||none|
|»» bizName|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» databaseId|integer(int64)|false|none||none|
|»» depends|string|false|none||none|
|»» description|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|»»» DrillDownDimension|[DrillDownDimension](#schemadrilldowndimension)|false|none|DrillDownDimension|none|
|»»»» dimensionId|integer(int64)|false|none||none|
|»»»» inheritedFromModel|boolean|false|none||none|
|»»»» necessary|boolean|false|none||none|
|»» ext|object|false|none||none|
|»» fieldList|[string]|false|none||none|
|»» filterSql|string|false|none||none|
|»» fullPath|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isOpen|integer(int32)|false|none||none|
|»» modelDetail|[ModelDetail](#schemamodeldetail)|false|none|ModelDetail|none|
|»»» dimensions|[[Dim](#schemadim)]|false|none||none|
|»»»» Dim|[Dim](#schemadim)|false|none|Dim|none|
|»»»»» bizName|string|false|none||none|
|»»»»» dateFormat|string|false|none||none|
|»»»»» description|string|false|none||none|
|»»»»» expr|string|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»»» isTag|integer(int32)|false|none||none|
|»»»»» name|string|false|none||none|
|»»»»» type|string|false|none||none|
|»»»»» typeParams|[DimensionTimeTypeParams](#schemadimensiontimetypeparams)|false|none|DimensionTimeTypeParams|none|
|»»»»»» isPrimary|string|false|none||none|
|»»»»»» timeGranularity|string|false|none||none|
|»»» fields|[[Field](#schemafield)]|false|none||none|
|»»»» Field|[Field](#schemafield)|false|none|Field|none|
|»»»»» dataType|string|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»» identifiers|[[Identify](#schemaidentify)]|false|none||none|
|»»»» Identify|[Identify](#schemaidentify)|false|none|Identify|none|
|»»»»» bizName|string|false|none||none|
|»»»»» entityNames|[string]|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»»» name|string|false|none||none|
|»»»»» type|string|false|none||none|
|»»» measures|[[Measure](#schemameasure)]|false|none||none|
|»»»» Measure|[Measure](#schemameasure)|false|none|Measure|none|
|»»»»» agg|string|false|none||none|
|»»»»» alias|string|false|none||none|
|»»»»» bizName|string|false|none||none|
|»»»»» constraint|string|false|none||none|
|»»»»» expr|string|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»»»» isCreateMetric|integer(int32)|false|none||none|
|»»»»» name|string|false|none||none|
|»»» queryType|string|false|none||none|
|»»» sqlQuery|string|false|none||none|
|»»» sqlVariables|[[SqlVariable](#schemasqlvariable)]|false|none||none|
|»»»» SqlVariable|[SqlVariable](#schemasqlvariable)|false|none|SqlVariable|none|
|»»»»» defaultValues|[object]|false|none||none|
|»»»»» name|string|false|none||none|
|»»»»» valueType|string|false|none||none|
|»»» tableQuery|string|false|none||none|
|»» name|string|false|none||none|
|»» primaryIdentify|[Identify](#schemaidentify)|false|none|Identify|none|
|»»» bizName|string|false|none||none|
|»»» entityNames|[string]|false|none||none|
|»»» fieldName|string|false|none||none|
|»»» isCreateDimension|integer(int32)|false|none||none|
|»»» name|string|false|none||none|
|»»» type|string|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» tagObjectId|integer(int64)|false|none||none|
|»» timeDimension|[[Dim](#schemadim)]|false|none||none|
|»»» Dim|[Dim](#schemadim)|false|none|Dim|none|
|»»»» bizName|string|false|none||none|
|»»»» dateFormat|string|false|none||none|
|»»»» description|string|false|none||none|
|»»»» expr|string|false|none||none|
|»»»» fieldName|string|false|none||none|
|»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»» isTag|integer(int32)|false|none||none|
|»»»» name|string|false|none||none|
|»»»» type|string|false|none||none|
|»»»» typeParams|[DimensionTimeTypeParams](#schemadimensiontimetypeparams)|false|none|DimensionTimeTypeParams|none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» viewOrgs|[string]|false|none||none|
|»» viewers|[string]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|valueType|EXPR|
|valueType|NUMBER|
|valueType|STRING|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdgetModelListByIdsUsingGET"></a>

## GET getModelListByIds

GET /api/semantic/model/getModelListByIds/{modelIds}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|modelIds|path|string| 是 ||modelIds|

> 返回示例

> 200 Response

```json
[
  {
    "adminOrgs": [
      "string"
    ],
    "admins": [
      "string"
    ],
    "alias": "string",
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "databaseId": 0,
    "depends": "string",
    "description": "string",
    "domainId": 0,
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ],
    "ext": {},
    "fieldList": [
      "string"
    ],
    "filterSql": "string",
    "fullPath": "string",
    "id": 0,
    "isOpen": 0,
    "modelDetail": {
      "dimensions": [
        {
          "bizName": "string",
          "dateFormat": "string",
          "description": "string",
          "expr": "string",
          "fieldName": "string",
          "isCreateDimension": 0,
          "isTag": 0,
          "name": "string",
          "type": "string",
          "typeParams": {
            "isPrimary": null,
            "timeGranularity": null
          }
        }
      ],
      "fields": [
        {
          "dataType": "string",
          "fieldName": "string"
        }
      ],
      "identifiers": [
        {
          "bizName": "string",
          "entityNames": [
            "string"
          ],
          "fieldName": "string",
          "isCreateDimension": 0,
          "name": "string",
          "type": "string"
        }
      ],
      "measures": [
        {
          "agg": "string",
          "alias": "string",
          "bizName": "string",
          "constraint": "string",
          "expr": "string",
          "fieldName": "string",
          "isCreateMetric": 0,
          "name": "string"
        }
      ],
      "queryType": "string",
      "sqlQuery": "string",
      "sqlVariables": [
        {
          "defaultValues": [
            {}
          ],
          "name": "string",
          "valueType": "EXPR"
        }
      ],
      "tableQuery": "string"
    },
    "name": "string",
    "primaryIdentify": {
      "bizName": "string",
      "entityNames": [
        "string"
      ],
      "fieldName": "string",
      "isCreateDimension": 0,
      "name": "string",
      "type": "string"
    },
    "sensitiveLevel": 0,
    "status": 0,
    "tagObjectId": 0,
    "timeDimension": [
      {
        "bizName": "string",
        "dateFormat": "string",
        "description": "string",
        "expr": "string",
        "fieldName": "string",
        "isCreateDimension": 0,
        "isTag": 0,
        "name": "string",
        "type": "string",
        "typeParams": {
          "isPrimary": "string",
          "timeGranularity": "string"
        }
      }
    ],
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "viewOrgs": [
      "string"
    ],
    "viewers": [
      "string"
    ]
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ModelResp](#schemamodelresp)]|false|none||none|
|» ModelResp|[ModelResp](#schemamodelresp)|false|none|ModelResp|none|
|»» adminOrgs|[string]|false|none||none|
|»» admins|[string]|false|none||none|
|»» alias|string|false|none||none|
|»» bizName|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» databaseId|integer(int64)|false|none||none|
|»» depends|string|false|none||none|
|»» description|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|»»» DrillDownDimension|[DrillDownDimension](#schemadrilldowndimension)|false|none|DrillDownDimension|none|
|»»»» dimensionId|integer(int64)|false|none||none|
|»»»» inheritedFromModel|boolean|false|none||none|
|»»»» necessary|boolean|false|none||none|
|»» ext|object|false|none||none|
|»» fieldList|[string]|false|none||none|
|»» filterSql|string|false|none||none|
|»» fullPath|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isOpen|integer(int32)|false|none||none|
|»» modelDetail|[ModelDetail](#schemamodeldetail)|false|none|ModelDetail|none|
|»»» dimensions|[[Dim](#schemadim)]|false|none||none|
|»»»» Dim|[Dim](#schemadim)|false|none|Dim|none|
|»»»»» bizName|string|false|none||none|
|»»»»» dateFormat|string|false|none||none|
|»»»»» description|string|false|none||none|
|»»»»» expr|string|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»»» isTag|integer(int32)|false|none||none|
|»»»»» name|string|false|none||none|
|»»»»» type|string|false|none||none|
|»»»»» typeParams|[DimensionTimeTypeParams](#schemadimensiontimetypeparams)|false|none|DimensionTimeTypeParams|none|
|»»»»»» isPrimary|string|false|none||none|
|»»»»»» timeGranularity|string|false|none||none|
|»»» fields|[[Field](#schemafield)]|false|none||none|
|»»»» Field|[Field](#schemafield)|false|none|Field|none|
|»»»»» dataType|string|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»» identifiers|[[Identify](#schemaidentify)]|false|none||none|
|»»»» Identify|[Identify](#schemaidentify)|false|none|Identify|none|
|»»»»» bizName|string|false|none||none|
|»»»»» entityNames|[string]|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»»» name|string|false|none||none|
|»»»»» type|string|false|none||none|
|»»» measures|[[Measure](#schemameasure)]|false|none||none|
|»»»» Measure|[Measure](#schemameasure)|false|none|Measure|none|
|»»»»» agg|string|false|none||none|
|»»»»» alias|string|false|none||none|
|»»»»» bizName|string|false|none||none|
|»»»»» constraint|string|false|none||none|
|»»»»» expr|string|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»»»» isCreateMetric|integer(int32)|false|none||none|
|»»»»» name|string|false|none||none|
|»»» queryType|string|false|none||none|
|»»» sqlQuery|string|false|none||none|
|»»» sqlVariables|[[SqlVariable](#schemasqlvariable)]|false|none||none|
|»»»» SqlVariable|[SqlVariable](#schemasqlvariable)|false|none|SqlVariable|none|
|»»»»» defaultValues|[object]|false|none||none|
|»»»»» name|string|false|none||none|
|»»»»» valueType|string|false|none||none|
|»»» tableQuery|string|false|none||none|
|»» name|string|false|none||none|
|»» primaryIdentify|[Identify](#schemaidentify)|false|none|Identify|none|
|»»» bizName|string|false|none||none|
|»»» entityNames|[string]|false|none||none|
|»»» fieldName|string|false|none||none|
|»»» isCreateDimension|integer(int32)|false|none||none|
|»»» name|string|false|none||none|
|»»» type|string|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» tagObjectId|integer(int64)|false|none||none|
|»» timeDimension|[[Dim](#schemadim)]|false|none||none|
|»»» Dim|[Dim](#schemadim)|false|none|Dim|none|
|»»»» bizName|string|false|none||none|
|»»»» dateFormat|string|false|none||none|
|»»»» description|string|false|none||none|
|»»»» expr|string|false|none||none|
|»»»» fieldName|string|false|none||none|
|»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»» isTag|integer(int32)|false|none||none|
|»»»» name|string|false|none||none|
|»»»» type|string|false|none||none|
|»»»» typeParams|[DimensionTimeTypeParams](#schemadimensiontimetypeparams)|false|none|DimensionTimeTypeParams|none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» viewOrgs|[string]|false|none||none|
|»» viewers|[string]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|valueType|EXPR|
|valueType|NUMBER|
|valueType|STRING|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdgetUnAvailableItemUsingPOST"></a>

## POST getUnAvailableItem

POST /api/semantic/model/getUnAvailableItem

> Body 请求参数

```json
{
  "fields": [
    "string"
  ],
  "modelId": 0
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[FieldRemovedReq](#schemafieldremovedreq)| 否 | FieldRemovedReq|none|

> 返回示例

> 200 Response

```json
{
  "dimensionResps": [
    {
      "alias": "string",
      "bizName": "string",
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dataType": "ARRAY",
      "defaultValues": [
        "string"
      ],
      "description": "string",
      "dimValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "expr": "string",
      "ext": {},
      "id": 0,
      "isTag": 0,
      "modelBizName": "string",
      "modelFilterSql": "string",
      "modelId": 0,
      "modelName": "string",
      "name": "string",
      "semanticType": "string",
      "sensitiveLevel": 0,
      "status": 0,
      "type": "string",
      "typeEnum": "DATASET",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "metricResps": [
    {
      "alias": "string",
      "bizName": "string",
      "classifications": [
        "string"
      ],
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "defaultAgg": "string",
      "description": "string",
      "domainId": 0,
      "drillDownDimensions": [
        {
          "dimensionId": 0,
          "inheritedFromModel": true,
          "necessary": true
        }
      ],
      "expr": "string",
      "ext": {},
      "hasAdminRes": true,
      "id": 0,
      "isCollect": true,
      "isPublish": 0,
      "isTag": 0,
      "metricDefineByFieldParams": {
        "expr": "string",
        "fields": [
          {
            "fieldName": null
          }
        ],
        "filterSql": "string"
      },
      "metricDefineByMeasureParams": {
        "expr": "string",
        "filterSql": "string",
        "measures": [
          {
            "agg": null,
            "bizName": null,
            "constraint": null
          }
        ]
      },
      "metricDefineByMetricParams": {
        "expr": "string",
        "filterSql": "string",
        "metrics": [
          {
            "bizName": null,
            "id": null
          }
        ]
      },
      "metricDefineType": "FIELD",
      "modelBizName": "string",
      "modelId": 0,
      "modelName": "string",
      "name": "string",
      "relaDimensionIdKey": "string",
      "relateDimension": {
        "drillDownDimensions": [
          {
            "dimensionId": null,
            "inheritedFromModel": null,
            "necessary": null
          }
        ]
      },
      "sensitiveLevel": 0,
      "similarity": 0,
      "status": 0,
      "type": "string",
      "typeEnum": "DATASET",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[UnAvailableItemResp](#schemaunavailableitemresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdupdateModelUsingPOST"></a>

## POST updateModel

POST /api/semantic/model/updateModel

> Body 请求参数

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "databaseId": 0,
  "description": "string",
  "domainId": 0,
  "drillDownDimensions": [
    {
      "dimensionId": 0,
      "inheritedFromModel": true,
      "necessary": true
    }
  ],
  "ext": {},
  "filterSql": "string",
  "id": 0,
  "isOpen": 0,
  "modelDetail": {
    "dimensions": [
      {
        "bizName": "string",
        "dateFormat": "string",
        "description": "string",
        "expr": "string",
        "isCreateDimension": 0,
        "isTag": 0,
        "name": "string",
        "type": "string",
        "typeParams": {
          "isPrimary": "string",
          "timeGranularity": "string"
        }
      }
    ],
    "fields": [
      {
        "dataType": "string",
        "fieldName": "string"
      }
    ],
    "identifiers": [
      {
        "bizName": "string",
        "entityNames": [
          "string"
        ],
        "isCreateDimension": 0,
        "name": "string",
        "type": "string"
      }
    ],
    "measures": [
      {
        "agg": "string",
        "alias": "string",
        "bizName": "string",
        "constraint": "string",
        "expr": "string",
        "isCreateMetric": 0,
        "name": "string"
      }
    ],
    "queryType": "string",
    "sqlQuery": "string",
    "sqlVariables": [
      {
        "defaultValues": [
          {}
        ],
        "name": "string",
        "valueType": "EXPR"
      }
    ],
    "tableQuery": "string"
  },
  "name": "string",
  "sensitiveLevel": 0,
  "sourceType": "string",
  "status": 0,
  "tagObjectId": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "viewOrgs": [
    "string"
  ],
  "viewers": [
    "string"
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ModelReq](#schemamodelreq)| 否 | ModelReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# model-rela-controller

<a id="opIdupdateUsingPUT_3"></a>

## PUT update

PUT /api/semantic/modelRela

> Body 请求参数

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "domainId": 0,
  "fromModelId": 0,
  "id": 0,
  "joinConditions": [
    {
      "leftField": "string",
      "operator": "!=",
      "rightField": "string"
    }
  ],
  "joinType": "string",
  "toModelId": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|displayName|query|string| 否 ||none|
|email|query|string| 否 ||none|
|id|query|integer(int64)| 否 ||none|
|isAdmin|query|integer(int32)| 否 ||none|
|name|query|string| 否 ||none|
|superAdmin|query|boolean| 否 ||none|
|body|body|[ModelRela](#schemamodelrela)| 否 | ModelRela|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdsaveUsingPOST_4"></a>

## POST save

POST /api/semantic/modelRela

> Body 请求参数

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "domainId": 0,
  "fromModelId": 0,
  "id": 0,
  "joinConditions": [
    {
      "leftField": "string",
      "operator": "!=",
      "rightField": "string"
    }
  ],
  "joinType": "string",
  "toModelId": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|displayName|query|string| 否 ||none|
|email|query|string| 否 ||none|
|id|query|integer(int64)| 否 ||none|
|isAdmin|query|integer(int32)| 否 ||none|
|name|query|string| 否 ||none|
|superAdmin|query|boolean| 否 ||none|
|body|body|[ModelRela](#schemamodelrela)| 否 | ModelRela|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetModelRelaListUsingGET"></a>

## GET getModelRelaList

GET /api/semantic/modelRela/list

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|query|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
[
  {
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "domainId": 0,
    "fromModelId": 0,
    "id": 0,
    "joinConditions": [
      {
        "leftField": "string",
        "operator": "!=",
        "rightField": "string"
      }
    ],
    "joinType": "string",
    "toModelId": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ModelRela](#schemamodelrela)]|false|none||none|
|» ModelRela|[ModelRela](#schemamodelrela)|false|none|ModelRela|none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» fromModelId|integer(int64)|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» joinConditions|[[JoinCondition](#schemajoincondition)]|false|none||none|
|»»» JoinCondition|[JoinCondition](#schemajoincondition)|false|none|JoinCondition|none|
|»»»» leftField|string|false|none||none|
|»»»» operator|string|false|none||none|
|»»»» rightField|string|false|none||none|
|»» joinType|string|false|none||none|
|»» toModelId|integer(int64)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|operator|!=|
|operator|<|
|operator|<=|
|operator|=|
|operator|>|
|operator|>=|
|operator|BETWEEN|
|operator|EXISTS|
|operator|IN|
|operator|IS_NOT_NULL|
|operator|IS_NULL|
|operator|LIKE|
|operator|NOT_IN|
|operator|SQL_PART|

<a id="opIdgetModelRelaListUsingPUT"></a>

## PUT getModelRelaList

PUT /api/semantic/modelRela/list

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|query|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
[
  {
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "domainId": 0,
    "fromModelId": 0,
    "id": 0,
    "joinConditions": [
      {
        "leftField": "string",
        "operator": "!=",
        "rightField": "string"
      }
    ],
    "joinType": "string",
    "toModelId": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ModelRela](#schemamodelrela)]|false|none||none|
|» ModelRela|[ModelRela](#schemamodelrela)|false|none|ModelRela|none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» fromModelId|integer(int64)|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» joinConditions|[[JoinCondition](#schemajoincondition)]|false|none||none|
|»»» JoinCondition|[JoinCondition](#schemajoincondition)|false|none|JoinCondition|none|
|»»»» leftField|string|false|none||none|
|»»»» operator|string|false|none||none|
|»»»» rightField|string|false|none||none|
|»» joinType|string|false|none||none|
|»» toModelId|integer(int64)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|operator|!=|
|operator|<|
|operator|<=|
|operator|=|
|operator|>|
|operator|>=|
|operator|BETWEEN|
|operator|EXISTS|
|operator|IN|
|operator|IS_NOT_NULL|
|operator|IS_NULL|
|operator|LIKE|
|operator|NOT_IN|
|operator|SQL_PART|

<a id="opIdgetModelRelaListUsingPOST"></a>

## POST getModelRelaList

POST /api/semantic/modelRela/list

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|query|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
[
  {
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "domainId": 0,
    "fromModelId": 0,
    "id": 0,
    "joinConditions": [
      {
        "leftField": "string",
        "operator": "!=",
        "rightField": "string"
      }
    ],
    "joinType": "string",
    "toModelId": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ModelRela](#schemamodelrela)]|false|none||none|
|» ModelRela|[ModelRela](#schemamodelrela)|false|none|ModelRela|none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» fromModelId|integer(int64)|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» joinConditions|[[JoinCondition](#schemajoincondition)]|false|none||none|
|»»» JoinCondition|[JoinCondition](#schemajoincondition)|false|none|JoinCondition|none|
|»»»» leftField|string|false|none||none|
|»»»» operator|string|false|none||none|
|»»»» rightField|string|false|none||none|
|»» joinType|string|false|none||none|
|»» toModelId|integer(int64)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|operator|!=|
|operator|<|
|operator|<=|
|operator|=|
|operator|>|
|operator|>=|
|operator|BETWEEN|
|operator|EXISTS|
|operator|IN|
|operator|IS_NOT_NULL|
|operator|IS_NULL|
|operator|LIKE|
|operator|NOT_IN|
|operator|SQL_PART|

<a id="opIdgetModelRelaListUsingDELETE"></a>

## DELETE getModelRelaList

DELETE /api/semantic/modelRela/list

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|query|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
[
  {
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "domainId": 0,
    "fromModelId": 0,
    "id": 0,
    "joinConditions": [
      {
        "leftField": "string",
        "operator": "!=",
        "rightField": "string"
      }
    ],
    "joinType": "string",
    "toModelId": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ModelRela](#schemamodelrela)]|false|none||none|
|» ModelRela|[ModelRela](#schemamodelrela)|false|none|ModelRela|none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» fromModelId|integer(int64)|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» joinConditions|[[JoinCondition](#schemajoincondition)]|false|none||none|
|»»» JoinCondition|[JoinCondition](#schemajoincondition)|false|none|JoinCondition|none|
|»»»» leftField|string|false|none||none|
|»»»» operator|string|false|none||none|
|»»»» rightField|string|false|none||none|
|»» joinType|string|false|none||none|
|»» toModelId|integer(int64)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|operator|!=|
|operator|<|
|operator|<=|
|operator|=|
|operator|>|
|operator|>=|
|operator|BETWEEN|
|operator|EXISTS|
|operator|IN|
|operator|IS_NOT_NULL|
|operator|IS_NULL|
|operator|LIKE|
|operator|NOT_IN|
|operator|SQL_PART|

<a id="opIdgetModelRelaListUsingOPTIONS"></a>

## OPTIONS getModelRelaList

OPTIONS /api/semantic/modelRela/list

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|query|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
[
  {
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "domainId": 0,
    "fromModelId": 0,
    "id": 0,
    "joinConditions": [
      {
        "leftField": "string",
        "operator": "!=",
        "rightField": "string"
      }
    ],
    "joinType": "string",
    "toModelId": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ModelRela](#schemamodelrela)]|false|none||none|
|» ModelRela|[ModelRela](#schemamodelrela)|false|none|ModelRela|none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» fromModelId|integer(int64)|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» joinConditions|[[JoinCondition](#schemajoincondition)]|false|none||none|
|»»» JoinCondition|[JoinCondition](#schemajoincondition)|false|none|JoinCondition|none|
|»»»» leftField|string|false|none||none|
|»»»» operator|string|false|none||none|
|»»»» rightField|string|false|none||none|
|»» joinType|string|false|none||none|
|»» toModelId|integer(int64)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|operator|!=|
|operator|<|
|operator|<=|
|operator|=|
|operator|>|
|operator|>=|
|operator|BETWEEN|
|operator|EXISTS|
|operator|IN|
|operator|IS_NOT_NULL|
|operator|IS_NULL|
|operator|LIKE|
|operator|NOT_IN|
|operator|SQL_PART|

<a id="opIdgetModelRelaListUsingHEAD"></a>

## HEAD getModelRelaList

HEAD /api/semantic/modelRela/list

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|query|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
[
  {
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "domainId": 0,
    "fromModelId": 0,
    "id": 0,
    "joinConditions": [
      {
        "leftField": "string",
        "operator": "!=",
        "rightField": "string"
      }
    ],
    "joinType": "string",
    "toModelId": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ModelRela](#schemamodelrela)]|false|none||none|
|» ModelRela|[ModelRela](#schemamodelrela)|false|none|ModelRela|none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» fromModelId|integer(int64)|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» joinConditions|[[JoinCondition](#schemajoincondition)]|false|none||none|
|»»» JoinCondition|[JoinCondition](#schemajoincondition)|false|none|JoinCondition|none|
|»»»» leftField|string|false|none||none|
|»»»» operator|string|false|none||none|
|»»»» rightField|string|false|none||none|
|»» joinType|string|false|none||none|
|»» toModelId|integer(int64)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|operator|!=|
|operator|<|
|operator|<=|
|operator|=|
|operator|>|
|operator|>=|
|operator|BETWEEN|
|operator|EXISTS|
|operator|IN|
|operator|IS_NOT_NULL|
|operator|IS_NULL|
|operator|LIKE|
|operator|NOT_IN|
|operator|SQL_PART|

<a id="opIdgetModelRelaListUsingPATCH"></a>

## PATCH getModelRelaList

PATCH /api/semantic/modelRela/list

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|query|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
[
  {
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "domainId": 0,
    "fromModelId": 0,
    "id": 0,
    "joinConditions": [
      {
        "leftField": "string",
        "operator": "!=",
        "rightField": "string"
      }
    ],
    "joinType": "string",
    "toModelId": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ModelRela](#schemamodelrela)]|false|none||none|
|» ModelRela|[ModelRela](#schemamodelrela)|false|none|ModelRela|none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» fromModelId|integer(int64)|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» joinConditions|[[JoinCondition](#schemajoincondition)]|false|none||none|
|»»» JoinCondition|[JoinCondition](#schemajoincondition)|false|none|JoinCondition|none|
|»»»» leftField|string|false|none||none|
|»»»» operator|string|false|none||none|
|»»»» rightField|string|false|none||none|
|»» joinType|string|false|none||none|
|»» toModelId|integer(int64)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|operator|!=|
|operator|<|
|operator|<=|
|operator|=|
|operator|>|
|operator|>=|
|operator|BETWEEN|
|operator|EXISTS|
|operator|IN|
|operator|IS_NOT_NULL|
|operator|IS_NULL|
|operator|LIKE|
|operator|NOT_IN|
|operator|SQL_PART|

<a id="opIdgetModelRelaListUsingTRACE"></a>

## TRACE getModelRelaList

TRACE /api/semantic/modelRela/list

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|query|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
[
  {
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "domainId": 0,
    "fromModelId": 0,
    "id": 0,
    "joinConditions": [
      {
        "leftField": "string",
        "operator": "!=",
        "rightField": "string"
      }
    ],
    "joinType": "string",
    "toModelId": 0,
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ModelRela](#schemamodelrela)]|false|none||none|
|» ModelRela|[ModelRela](#schemamodelrela)|false|none|ModelRela|none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» fromModelId|integer(int64)|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» joinConditions|[[JoinCondition](#schemajoincondition)]|false|none||none|
|»»» JoinCondition|[JoinCondition](#schemajoincondition)|false|none|JoinCondition|none|
|»»»» leftField|string|false|none||none|
|»»»» operator|string|false|none||none|
|»»»» rightField|string|false|none||none|
|»» joinType|string|false|none||none|
|»» toModelId|integer(int64)|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|operator|!=|
|operator|<|
|operator|<=|
|operator|=|
|operator|>|
|operator|>=|
|operator|BETWEEN|
|operator|EXISTS|
|operator|IN|
|operator|IS_NOT_NULL|
|operator|IS_NULL|
|operator|LIKE|
|operator|NOT_IN|
|operator|SQL_PART|

<a id="opIddeleteUsingDELETE_3"></a>

## DELETE delete

DELETE /api/semantic/modelRela/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

# plugin-controller

<a id="opIdupdatePluginUsingPUT"></a>

## PUT updatePlugin

PUT /api/chat/plugin

> Body 请求参数

```json
{
  "comment": "string",
  "config": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetList": [
    0
  ],
  "id": 0,
  "name": "string",
  "parseMode": "EMBEDDING_RECALL",
  "parseModeConfig": "string",
  "pattern": "string",
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatPluginReq](#schemachatpluginreq)| 否 | ChatPluginReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdcreatePluginUsingPOST"></a>

## POST createPlugin

POST /api/chat/plugin

> Body 请求参数

```json
{
  "comment": "string",
  "config": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetList": [
    0
  ],
  "id": 0,
  "name": "string",
  "parseMode": "EMBEDDING_RECALL",
  "parseModeConfig": "string",
  "pattern": "string",
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ChatPluginReq](#schemachatpluginreq)| 否 | ChatPluginReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetPluginListUsingGET"></a>

## GET getPluginList

GET /api/chat/plugin/getPluginList

> 返回示例

> 200 Response

```json
[
  {
    "comment": "string",
    "config": "string",
    "containsAllDataSet": true,
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetList": [
      0
    ],
    "defaultMode": 0,
    "exampleQuestionList": [
      "string"
    ],
    "id": 0,
    "name": "string",
    "parseMode": "EMBEDDING_RECALL",
    "parseModeConfig": "string",
    "pattern": "string",
    "type": "string",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatPluginRes](#schemachatpluginres)]|false|none||none|
|» ChatPluginRes|[ChatPluginRes](#schemachatpluginres)|false|none|ChatPluginRes|none|
|»» comment|string|false|none||none|
|»» config|string|false|none||none|
|»» containsAllDataSet|boolean|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetList|[integer]|false|none||none|
|»» defaultMode|integer(int64)|false|none||none|
|»» exampleQuestionList|[string]|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» parseMode|string|false|none||none|
|»» parseModeConfig|string|false|none||none|
|»» pattern|string|false|none||none|
|»» type|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|parseMode|EMBEDDING_RECALL|
|parseMode|FUNCTION_CALL|

<a id="opIdgetPluginListUsingPUT"></a>

## PUT getPluginList

PUT /api/chat/plugin/getPluginList

> 返回示例

> 200 Response

```json
[
  {
    "comment": "string",
    "config": "string",
    "containsAllDataSet": true,
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetList": [
      0
    ],
    "defaultMode": 0,
    "exampleQuestionList": [
      "string"
    ],
    "id": 0,
    "name": "string",
    "parseMode": "EMBEDDING_RECALL",
    "parseModeConfig": "string",
    "pattern": "string",
    "type": "string",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatPluginRes](#schemachatpluginres)]|false|none||none|
|» ChatPluginRes|[ChatPluginRes](#schemachatpluginres)|false|none|ChatPluginRes|none|
|»» comment|string|false|none||none|
|»» config|string|false|none||none|
|»» containsAllDataSet|boolean|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetList|[integer]|false|none||none|
|»» defaultMode|integer(int64)|false|none||none|
|»» exampleQuestionList|[string]|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» parseMode|string|false|none||none|
|»» parseModeConfig|string|false|none||none|
|»» pattern|string|false|none||none|
|»» type|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|parseMode|EMBEDDING_RECALL|
|parseMode|FUNCTION_CALL|

<a id="opIdgetPluginListUsingPOST"></a>

## POST getPluginList

POST /api/chat/plugin/getPluginList

> 返回示例

> 200 Response

```json
[
  {
    "comment": "string",
    "config": "string",
    "containsAllDataSet": true,
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetList": [
      0
    ],
    "defaultMode": 0,
    "exampleQuestionList": [
      "string"
    ],
    "id": 0,
    "name": "string",
    "parseMode": "EMBEDDING_RECALL",
    "parseModeConfig": "string",
    "pattern": "string",
    "type": "string",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatPluginRes](#schemachatpluginres)]|false|none||none|
|» ChatPluginRes|[ChatPluginRes](#schemachatpluginres)|false|none|ChatPluginRes|none|
|»» comment|string|false|none||none|
|»» config|string|false|none||none|
|»» containsAllDataSet|boolean|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetList|[integer]|false|none||none|
|»» defaultMode|integer(int64)|false|none||none|
|»» exampleQuestionList|[string]|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» parseMode|string|false|none||none|
|»» parseModeConfig|string|false|none||none|
|»» pattern|string|false|none||none|
|»» type|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|parseMode|EMBEDDING_RECALL|
|parseMode|FUNCTION_CALL|

<a id="opIdgetPluginListUsingDELETE"></a>

## DELETE getPluginList

DELETE /api/chat/plugin/getPluginList

> 返回示例

> 200 Response

```json
[
  {
    "comment": "string",
    "config": "string",
    "containsAllDataSet": true,
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetList": [
      0
    ],
    "defaultMode": 0,
    "exampleQuestionList": [
      "string"
    ],
    "id": 0,
    "name": "string",
    "parseMode": "EMBEDDING_RECALL",
    "parseModeConfig": "string",
    "pattern": "string",
    "type": "string",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatPluginRes](#schemachatpluginres)]|false|none||none|
|» ChatPluginRes|[ChatPluginRes](#schemachatpluginres)|false|none|ChatPluginRes|none|
|»» comment|string|false|none||none|
|»» config|string|false|none||none|
|»» containsAllDataSet|boolean|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetList|[integer]|false|none||none|
|»» defaultMode|integer(int64)|false|none||none|
|»» exampleQuestionList|[string]|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» parseMode|string|false|none||none|
|»» parseModeConfig|string|false|none||none|
|»» pattern|string|false|none||none|
|»» type|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|parseMode|EMBEDDING_RECALL|
|parseMode|FUNCTION_CALL|

<a id="opIdgetPluginListUsingOPTIONS"></a>

## OPTIONS getPluginList

OPTIONS /api/chat/plugin/getPluginList

> 返回示例

> 200 Response

```json
[
  {
    "comment": "string",
    "config": "string",
    "containsAllDataSet": true,
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetList": [
      0
    ],
    "defaultMode": 0,
    "exampleQuestionList": [
      "string"
    ],
    "id": 0,
    "name": "string",
    "parseMode": "EMBEDDING_RECALL",
    "parseModeConfig": "string",
    "pattern": "string",
    "type": "string",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatPluginRes](#schemachatpluginres)]|false|none||none|
|» ChatPluginRes|[ChatPluginRes](#schemachatpluginres)|false|none|ChatPluginRes|none|
|»» comment|string|false|none||none|
|»» config|string|false|none||none|
|»» containsAllDataSet|boolean|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetList|[integer]|false|none||none|
|»» defaultMode|integer(int64)|false|none||none|
|»» exampleQuestionList|[string]|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» parseMode|string|false|none||none|
|»» parseModeConfig|string|false|none||none|
|»» pattern|string|false|none||none|
|»» type|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|parseMode|EMBEDDING_RECALL|
|parseMode|FUNCTION_CALL|

<a id="opIdgetPluginListUsingHEAD"></a>

## HEAD getPluginList

HEAD /api/chat/plugin/getPluginList

> 返回示例

> 200 Response

```json
[
  {
    "comment": "string",
    "config": "string",
    "containsAllDataSet": true,
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetList": [
      0
    ],
    "defaultMode": 0,
    "exampleQuestionList": [
      "string"
    ],
    "id": 0,
    "name": "string",
    "parseMode": "EMBEDDING_RECALL",
    "parseModeConfig": "string",
    "pattern": "string",
    "type": "string",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatPluginRes](#schemachatpluginres)]|false|none||none|
|» ChatPluginRes|[ChatPluginRes](#schemachatpluginres)|false|none|ChatPluginRes|none|
|»» comment|string|false|none||none|
|»» config|string|false|none||none|
|»» containsAllDataSet|boolean|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetList|[integer]|false|none||none|
|»» defaultMode|integer(int64)|false|none||none|
|»» exampleQuestionList|[string]|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» parseMode|string|false|none||none|
|»» parseModeConfig|string|false|none||none|
|»» pattern|string|false|none||none|
|»» type|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|parseMode|EMBEDDING_RECALL|
|parseMode|FUNCTION_CALL|

<a id="opIdgetPluginListUsingPATCH"></a>

## PATCH getPluginList

PATCH /api/chat/plugin/getPluginList

> 返回示例

> 200 Response

```json
[
  {
    "comment": "string",
    "config": "string",
    "containsAllDataSet": true,
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetList": [
      0
    ],
    "defaultMode": 0,
    "exampleQuestionList": [
      "string"
    ],
    "id": 0,
    "name": "string",
    "parseMode": "EMBEDDING_RECALL",
    "parseModeConfig": "string",
    "pattern": "string",
    "type": "string",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatPluginRes](#schemachatpluginres)]|false|none||none|
|» ChatPluginRes|[ChatPluginRes](#schemachatpluginres)|false|none|ChatPluginRes|none|
|»» comment|string|false|none||none|
|»» config|string|false|none||none|
|»» containsAllDataSet|boolean|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetList|[integer]|false|none||none|
|»» defaultMode|integer(int64)|false|none||none|
|»» exampleQuestionList|[string]|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» parseMode|string|false|none||none|
|»» parseModeConfig|string|false|none||none|
|»» pattern|string|false|none||none|
|»» type|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|parseMode|EMBEDDING_RECALL|
|parseMode|FUNCTION_CALL|

<a id="opIdgetPluginListUsingTRACE"></a>

## TRACE getPluginList

TRACE /api/chat/plugin/getPluginList

> 返回示例

> 200 Response

```json
[
  {
    "comment": "string",
    "config": "string",
    "containsAllDataSet": true,
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetList": [
      0
    ],
    "defaultMode": 0,
    "exampleQuestionList": [
      "string"
    ],
    "id": 0,
    "name": "string",
    "parseMode": "EMBEDDING_RECALL",
    "parseModeConfig": "string",
    "pattern": "string",
    "type": "string",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatPluginRes](#schemachatpluginres)]|false|none||none|
|» ChatPluginRes|[ChatPluginRes](#schemachatpluginres)|false|none|ChatPluginRes|none|
|»» comment|string|false|none||none|
|»» config|string|false|none||none|
|»» containsAllDataSet|boolean|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetList|[integer]|false|none||none|
|»» defaultMode|integer(int64)|false|none||none|
|»» exampleQuestionList|[string]|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» parseMode|string|false|none||none|
|»» parseModeConfig|string|false|none||none|
|»» pattern|string|false|none||none|
|»» type|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|parseMode|EMBEDDING_RECALL|
|parseMode|FUNCTION_CALL|

<a id="opIdpluginDemoUsingPOST"></a>

## POST pluginDemo

POST /api/chat/plugin/pluginDemo

> Body 请求参数

```json
{}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|queryText|query|string| 是 ||queryText|
|body|body|object| 否 ||none|

> 返回示例

> 200 Response

```json
"string"
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryUsingPOST_2"></a>

## POST query

POST /api/chat/plugin/query

> Body 请求参数

```json
{
  "createdBy": "string",
  "dataSet": "string",
  "name": "string",
  "parseMode": "string",
  "pattern": "string",
  "type": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[PluginQueryReq](#schemapluginqueryreq)| 否 | PluginQueryReq|none|

> 返回示例

> 200 Response

```json
[
  {
    "comment": "string",
    "config": "string",
    "containsAllDataSet": true,
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetList": [
      0
    ],
    "defaultMode": 0,
    "exampleQuestionList": [
      "string"
    ],
    "id": 0,
    "name": "string",
    "parseMode": "EMBEDDING_RECALL",
    "parseModeConfig": "string",
    "pattern": "string",
    "type": "string",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ChatPluginRes](#schemachatpluginres)]|false|none||none|
|» ChatPluginRes|[ChatPluginRes](#schemachatpluginres)|false|none|ChatPluginRes|none|
|»» comment|string|false|none||none|
|»» config|string|false|none||none|
|»» containsAllDataSet|boolean|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetList|[integer]|false|none||none|
|»» defaultMode|integer(int64)|false|none||none|
|»» exampleQuestionList|[string]|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» parseMode|string|false|none||none|
|»» parseModeConfig|string|false|none||none|
|»» pattern|string|false|none||none|
|»» type|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|parseMode|EMBEDDING_RECALL|
|parseMode|FUNCTION_CALL|

<a id="opIddeletePluginUsingDELETE"></a>

## DELETE deletePlugin

DELETE /api/chat/plugin/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

# query-rule-controller

<a id="opIdcreateUsingPOST_1"></a>

## POST create

POST /api/semantic/query/rule/create

> Body 请求参数

```json
{
  "action": {
    "out": [
      {}
    ]
  },
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetId": 0,
  "description": "string",
  "ext": {
    "property1": "string",
    "property2": "string"
  },
  "id": 0,
  "name": "string",
  "priority": 0,
  "rule": {
    "mode": "BEFORE",
    "parameters": [
      {}
    ]
  },
  "ruleType": "ADD_DATE",
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QueryRuleReq](#schemaqueryrulereq)| 否 | QueryRuleReq|none|

> 返回示例

> 200 Response

```json
{
  "action": {
    "out": [
      {}
    ]
  },
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetId": 0,
  "description": "string",
  "ext": {
    "property1": "string",
    "property2": "string"
  },
  "id": 0,
  "name": "string",
  "priority": 0,
  "rule": {
    "mode": "BEFORE",
    "parameters": [
      {}
    ]
  },
  "ruleType": "ADD_DATE",
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[QueryRuleResp](#schemaqueryruleresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteUsingDELETE_4"></a>

## DELETE delete

DELETE /api/semantic/query/rule/delete/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdqueryUsingPOST_3"></a>

## POST query

POST /api/semantic/query/rule/query

> Body 请求参数

```json
{
  "dataSetIds": [
    0
  ],
  "ruleIds": [
    0
  ],
  "statusList": [
    0
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QueryRuleFilter](#schemaqueryrulefilter)| 否 | QueryRuleFilter|none|

> 返回示例

> 200 Response

```json
[
  {
    "action": {
      "out": [
        {}
      ]
    },
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "dataSetId": 0,
    "description": "string",
    "ext": {
      "property1": "string",
      "property2": "string"
    },
    "id": 0,
    "name": "string",
    "priority": 0,
    "rule": {
      "mode": "BEFORE",
      "parameters": [
        {}
      ]
    },
    "ruleType": "ADD_DATE",
    "sensitiveLevel": 0,
    "status": 0,
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[QueryRuleResp](#schemaqueryruleresp)]|false|none||none|
|» QueryRuleResp|[QueryRuleResp](#schemaqueryruleresp)|false|none|QueryRuleResp|none|
|»» action|[ActionInfo](#schemaactioninfo)|false|none|ActionInfo|none|
|»»» out|[object]|false|none||none|
|»» bizName|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» dataSetId|integer(int64)|false|none||none|
|»» description|string|false|none||none|
|»» ext|object|false|none||none|
|»»» **additionalProperties**|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» priority|integer(int32)|false|none||none|
|»» rule|[RuleInfo](#schemaruleinfo)|true|none|RuleInfo|none|
|»»» mode|string|false|none||none|
|»»» parameters|[object]|false|none||none|
|»» ruleType|string|true|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|mode|BEFORE|
|mode|EXIST|
|mode|RECENT|
|ruleType|ADD_DATE|
|ruleType|ADD_SELECT|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdupdateUsingPOST"></a>

## POST update

POST /api/semantic/query/rule/update

> Body 请求参数

```json
{
  "action": {
    "out": [
      {}
    ]
  },
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetId": 0,
  "description": "string",
  "ext": {
    "property1": "string",
    "property2": "string"
  },
  "id": 0,
  "name": "string",
  "priority": 0,
  "rule": {
    "mode": "BEFORE",
    "parameters": [
      {}
    ]
  },
  "ruleType": "ADD_DATE",
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QueryRuleReq](#schemaqueryrulereq)| 否 | QueryRuleReq|none|

> 返回示例

> 200 Response

```json
{
  "action": {
    "out": [
      {}
    ]
  },
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetId": 0,
  "description": "string",
  "ext": {
    "property1": "string",
    "property2": "string"
  },
  "id": 0,
  "name": "string",
  "priority": 0,
  "rule": {
    "mode": "BEFORE",
    "parameters": [
      {}
    ]
  },
  "ruleType": "ADD_DATE",
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[QueryRuleResp](#schemaqueryruleresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# schema-controller

<a id="opIdgetDomainListUsingGET_1"></a>

## GET getDomainList

GET /api/semantic/schema/domain/list

> 返回示例

> 200 Response

```json
[
  {
    "adminOrgs": [
      "string"
    ],
    "admins": [
      "string"
    ],
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "description": "string",
    "fullPath": "string",
    "hasEditPermission": true,
    "hasModel": true,
    "id": 0,
    "isOpen": 0,
    "name": "string",
    "parentId": 0,
    "sensitiveLevel": 0,
    "status": 0,
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "viewOrgs": [
      "string"
    ],
    "viewers": [
      "string"
    ]
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[DomainResp](#schemadomainresp)]|false|none||none|
|» DomainResp|[DomainResp](#schemadomainresp)|false|none|DomainResp|none|
|»» adminOrgs|[string]|false|none||none|
|»» admins|[string]|false|none||none|
|»» bizName|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» description|string|false|none||none|
|»» fullPath|string|false|none||none|
|»» hasEditPermission|boolean|false|none||none|
|»» hasModel|boolean|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isOpen|integer(int32)|false|none||none|
|»» name|string|false|none||none|
|»» parentId|integer(int64)|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» viewOrgs|[string]|false|none||none|
|»» viewers|[string]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdgetModelListUsingGET_1"></a>

## GET getModelList

GET /api/semantic/schema/model/list

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|query|integer(int64)| 是 ||domainId|
|authType|query|string| 是 ||authType|

> 返回示例

> 200 Response

```json
[
  {
    "adminOrgs": [
      "string"
    ],
    "admins": [
      "string"
    ],
    "alias": "string",
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "databaseId": 0,
    "depends": "string",
    "description": "string",
    "domainId": 0,
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ],
    "ext": {},
    "fieldList": [
      "string"
    ],
    "filterSql": "string",
    "fullPath": "string",
    "id": 0,
    "isOpen": 0,
    "modelDetail": {
      "dimensions": [
        {
          "bizName": "string",
          "dateFormat": "string",
          "description": "string",
          "expr": "string",
          "fieldName": "string",
          "isCreateDimension": 0,
          "isTag": 0,
          "name": "string",
          "type": "string",
          "typeParams": {
            "isPrimary": null,
            "timeGranularity": null
          }
        }
      ],
      "fields": [
        {
          "dataType": "string",
          "fieldName": "string"
        }
      ],
      "identifiers": [
        {
          "bizName": "string",
          "entityNames": [
            "string"
          ],
          "fieldName": "string",
          "isCreateDimension": 0,
          "name": "string",
          "type": "string"
        }
      ],
      "measures": [
        {
          "agg": "string",
          "alias": "string",
          "bizName": "string",
          "constraint": "string",
          "expr": "string",
          "fieldName": "string",
          "isCreateMetric": 0,
          "name": "string"
        }
      ],
      "queryType": "string",
      "sqlQuery": "string",
      "sqlVariables": [
        {
          "defaultValues": [
            {}
          ],
          "name": "string",
          "valueType": "EXPR"
        }
      ],
      "tableQuery": "string"
    },
    "name": "string",
    "primaryIdentify": {
      "bizName": "string",
      "entityNames": [
        "string"
      ],
      "fieldName": "string",
      "isCreateDimension": 0,
      "name": "string",
      "type": "string"
    },
    "sensitiveLevel": 0,
    "status": 0,
    "tagObjectId": 0,
    "timeDimension": [
      {
        "bizName": "string",
        "dateFormat": "string",
        "description": "string",
        "expr": "string",
        "fieldName": "string",
        "isCreateDimension": 0,
        "isTag": 0,
        "name": "string",
        "type": "string",
        "typeParams": {
          "isPrimary": "string",
          "timeGranularity": "string"
        }
      }
    ],
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "viewOrgs": [
      "string"
    ],
    "viewers": [
      "string"
    ]
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[ModelResp](#schemamodelresp)]|false|none||none|
|» ModelResp|[ModelResp](#schemamodelresp)|false|none|ModelResp|none|
|»» adminOrgs|[string]|false|none||none|
|»» admins|[string]|false|none||none|
|»» alias|string|false|none||none|
|»» bizName|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» databaseId|integer(int64)|false|none||none|
|»» depends|string|false|none||none|
|»» description|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|»»» DrillDownDimension|[DrillDownDimension](#schemadrilldowndimension)|false|none|DrillDownDimension|none|
|»»»» dimensionId|integer(int64)|false|none||none|
|»»»» inheritedFromModel|boolean|false|none||none|
|»»»» necessary|boolean|false|none||none|
|»» ext|object|false|none||none|
|»» fieldList|[string]|false|none||none|
|»» filterSql|string|false|none||none|
|»» fullPath|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isOpen|integer(int32)|false|none||none|
|»» modelDetail|[ModelDetail](#schemamodeldetail)|false|none|ModelDetail|none|
|»»» dimensions|[[Dim](#schemadim)]|false|none||none|
|»»»» Dim|[Dim](#schemadim)|false|none|Dim|none|
|»»»»» bizName|string|false|none||none|
|»»»»» dateFormat|string|false|none||none|
|»»»»» description|string|false|none||none|
|»»»»» expr|string|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»»» isTag|integer(int32)|false|none||none|
|»»»»» name|string|false|none||none|
|»»»»» type|string|false|none||none|
|»»»»» typeParams|[DimensionTimeTypeParams](#schemadimensiontimetypeparams)|false|none|DimensionTimeTypeParams|none|
|»»»»»» isPrimary|string|false|none||none|
|»»»»»» timeGranularity|string|false|none||none|
|»»» fields|[[Field](#schemafield)]|false|none||none|
|»»»» Field|[Field](#schemafield)|false|none|Field|none|
|»»»»» dataType|string|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»» identifiers|[[Identify](#schemaidentify)]|false|none||none|
|»»»» Identify|[Identify](#schemaidentify)|false|none|Identify|none|
|»»»»» bizName|string|false|none||none|
|»»»»» entityNames|[string]|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»»» name|string|false|none||none|
|»»»»» type|string|false|none||none|
|»»» measures|[[Measure](#schemameasure)]|false|none||none|
|»»»» Measure|[Measure](#schemameasure)|false|none|Measure|none|
|»»»»» agg|string|false|none||none|
|»»»»» alias|string|false|none||none|
|»»»»» bizName|string|false|none||none|
|»»»»» constraint|string|false|none||none|
|»»»»» expr|string|false|none||none|
|»»»»» fieldName|string|false|none||none|
|»»»»» isCreateMetric|integer(int32)|false|none||none|
|»»»»» name|string|false|none||none|
|»»» queryType|string|false|none||none|
|»»» sqlQuery|string|false|none||none|
|»»» sqlVariables|[[SqlVariable](#schemasqlvariable)]|false|none||none|
|»»»» SqlVariable|[SqlVariable](#schemasqlvariable)|false|none|SqlVariable|none|
|»»»»» defaultValues|[object]|false|none||none|
|»»»»» name|string|false|none||none|
|»»»»» valueType|string|false|none||none|
|»»» tableQuery|string|false|none||none|
|»» name|string|false|none||none|
|»» primaryIdentify|[Identify](#schemaidentify)|false|none|Identify|none|
|»»» bizName|string|false|none||none|
|»»» entityNames|[string]|false|none||none|
|»»» fieldName|string|false|none||none|
|»»» isCreateDimension|integer(int32)|false|none||none|
|»»» name|string|false|none||none|
|»»» type|string|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» tagObjectId|integer(int64)|false|none||none|
|»» timeDimension|[[Dim](#schemadim)]|false|none||none|
|»»» Dim|[Dim](#schemadim)|false|none|Dim|none|
|»»»» bizName|string|false|none||none|
|»»»» dateFormat|string|false|none||none|
|»»»» description|string|false|none||none|
|»»»» expr|string|false|none||none|
|»»»» fieldName|string|false|none||none|
|»»»» isCreateDimension|integer(int32)|false|none||none|
|»»»» isTag|integer(int32)|false|none||none|
|»»»» name|string|false|none||none|
|»»»» type|string|false|none||none|
|»»»» typeParams|[DimensionTimeTypeParams](#schemadimensiontimetypeparams)|false|none|DimensionTimeTypeParams|none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|
|»» viewOrgs|[string]|false|none||none|
|»» viewers|[string]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|valueType|EXPR|
|valueType|NUMBER|
|valueType|STRING|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

# sql-query-api-controller

<a id="opIdqueryBySqlUsingPOST"></a>

## POST queryBySql

POST /api/semantic/query/sql

> Body 请求参数

```json
{
  "cacheInfo": {
    "cache": true
  },
  "dataSetId": 0,
  "dataSetName": "string",
  "innerLayerNative": true,
  "limit": 0,
  "modelIds": [
    0
  ],
  "needAuth": true,
  "params": [
    {
      "name": "string",
      "value": "string"
    }
  ],
  "sql": "string",
  "sqlInfo": {
    "correctS2SQL": "string",
    "querySQL": "string",
    "s2SQL": "string",
    "sourceId": "string"
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QuerySqlReq](#schemaquerysqlreq)| 否 | QuerySqlReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryBySqlsUsingPOST"></a>

## POST queryBySqls

POST /api/semantic/query/sqls

> Body 请求参数

```json
{
  "cacheInfo": {
    "cache": true
  },
  "dataSetId": 0,
  "dataSetName": "string",
  "innerLayerNative": true,
  "modelIds": [
    0
  ],
  "needAuth": true,
  "params": [
    {
      "name": "string",
      "value": "string"
    }
  ],
  "sqlInfo": {
    "correctS2SQL": "string",
    "querySQL": "string",
    "s2SQL": "string",
    "sourceId": "string"
  },
  "sqls": [
    "string"
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QuerySqlsReq](#schemaquerysqlsreq)| 否 | QuerySqlsReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryBySqlsWithExceptionUsingPOST"></a>

## POST queryBySqlsWithException

POST /api/semantic/query/sqlsWithException

> Body 请求参数

```json
{
  "cacheInfo": {
    "cache": true
  },
  "dataSetId": 0,
  "dataSetName": "string",
  "innerLayerNative": true,
  "modelIds": [
    0
  ],
  "needAuth": true,
  "params": [
    {
      "name": "string",
      "value": "string"
    }
  ],
  "sqlInfo": {
    "correctS2SQL": "string",
    "querySQL": "string",
    "s2SQL": "string",
    "sourceId": "string"
  },
  "sqls": [
    "string"
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QuerySqlsReq](#schemaquerysqlsreq)| 否 | QuerySqlsReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdvalidateUsingPOST"></a>

## POST validate

POST /api/semantic/query/validate

> Body 请求参数

```json
{
  "cacheInfo": {
    "cache": true
  },
  "dataSetId": 0,
  "dataSetName": "string",
  "innerLayerNative": true,
  "limit": 0,
  "modelIds": [
    0
  ],
  "needAuth": true,
  "params": [
    {
      "name": "string",
      "value": "string"
    }
  ],
  "sql": "string",
  "sqlInfo": {
    "correctS2SQL": "string",
    "querySQL": "string",
    "s2SQL": "string",
    "sourceId": "string"
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QuerySqlReq](#schemaquerysqlreq)| 否 | QuerySqlReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# system-config-controller

<a id="opIdgetUsingGET_1"></a>

## GET get

GET /api/semantic/parameter

> 返回示例

> 200 Response

```json
{
  "admin": "string",
  "admins": [
    "string"
  ],
  "id": 0,
  "parameters": [
    {
      "candidateValues": [
        {}
      ],
      "comment": "string",
      "dataType": "string",
      "defaultValue": "string",
      "description": "string",
      "module": "string",
      "name": "string",
      "value": "string"
    }
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[SystemConfigRes](#schemasystemconfigres)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdsaveUsingPOST_5"></a>

## POST save

POST /api/semantic/parameter

> Body 请求参数

```json
{
  "adminList": "string",
  "admins": [
    "string"
  ],
  "id": 0,
  "parameters": [
    {
      "candidateValues": [
        {}
      ],
      "comment": "string",
      "dataType": "string",
      "defaultValue": "string",
      "description": "string",
      "module": "string",
      "name": "string",
      "value": "string"
    }
  ]
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[SystemConfigReq](#schemasystemconfigreq)| 否 | SystemConfigReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# tag-controller

<a id="opIdcreateUsingPOST_2"></a>

## POST create

POST /api/semantic/tag/create

> Body 请求参数

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "id": 0,
  "itemId": 0,
  "tagDefineType": "DIMENSION",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[TagReq](#schematagreq)| 否 | TagReq|none|

> 返回示例

> 200 Response

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "domainName": "string",
  "ext": {},
  "hasAdminRes": true,
  "id": 0,
  "isCollect": true,
  "itemId": 0,
  "modelId": 0,
  "modelName": "string",
  "name": "string",
  "sensitiveLevel": 0,
  "tagDefineType": "string",
  "tagObjectId": 0,
  "tagObjectName": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[TagResp](#schematagresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdcreateBatchUsingPOST"></a>

## POST createBatch

POST /api/semantic/tag/create/batch

> Body 请求参数

```json
[
  {
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "id": 0,
    "itemId": 0,
    "tagDefineType": "DIMENSION",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[TagReq](#schematagreq)| 否 ||none|

> 返回示例

> 200 Response

```json
0
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|integer|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteBatchUsingPOST"></a>

## POST deleteBatch

POST /api/semantic/tag/delete/batch

> Body 请求参数

```json
[
  {
    "ids": [
      0
    ],
    "itemIds": [
      0
    ],
    "tagDefineType": "DIMENSION"
  }
]
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[TagDeleteReq](#schematagdeletereq)| 否 ||none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteUsingDELETE_5"></a>

## DELETE delete

DELETE /api/semantic/tag/delete/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdgetTagUsingGET"></a>

## GET getTag

GET /api/semantic/tag/getTag/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "domainName": "string",
  "ext": {},
  "hasAdminRes": true,
  "id": 0,
  "isCollect": true,
  "itemId": 0,
  "modelId": 0,
  "modelName": "string",
  "name": "string",
  "sensitiveLevel": 0,
  "tagDefineType": "string",
  "tagObjectId": 0,
  "tagObjectName": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[TagResp](#schematagresp)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryPageUsingPOST"></a>

## POST queryPage

POST /api/semantic/tag/queryTag

> Body 请求参数

```json
{
  "bizName": "string",
  "createdBy": "string",
  "dataSetId": 0,
  "domainId": 0,
  "fieldsDepend": [
    "string"
  ],
  "hasCollect": true,
  "id": "string",
  "ids": [
    0
  ],
  "isTag": 0,
  "itemIds": [
    0
  ],
  "key": "string",
  "modelIds": [
    0
  ],
  "name": "string",
  "names": [
    "string"
  ],
  "sensitiveLevel": 0,
  "status": 0,
  "tagDefineType": "DIMENSION"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[TagFilter](#schematagfilter)| 否 | TagFilter|none|

> 返回示例

> 200 Response

```json
[
  {
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "id": 0,
    "itemId": 0,
    "type": "string",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[TagDO](#schematagdo)]|false|none||none|
|» TagDO|[TagDO](#schematagdo)|false|none|TagDO|none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» itemId|integer(int64)|false|none||none|
|»» type|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

<a id="opIdqueryTagMarketPageUsingPOST"></a>

## POST queryTagMarketPage

POST /api/semantic/tag/queryTag/market

> Body 请求参数

```json
{
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdBy": "string",
  "current": 0,
  "domainIds": [
    0
  ],
  "hasCollect": true,
  "id": "string",
  "ids": [
    0
  ],
  "key": "string",
  "modelIds": [
    0
  ],
  "name": "string",
  "orderCondition": "string",
  "pageSize": 0,
  "sensitiveLevel": 0,
  "sort": "string",
  "status": 0,
  "tagDefineType": "DIMENSION",
  "tagObjectId": 0
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[TagFilterPageReq](#schematagfilterpagereq)| 否 | TagFilterPageReq|none|

> 返回示例

> 200 Response

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "bizName": "string",
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "description": "string",
      "domainId": 0,
      "domainName": "string",
      "ext": {},
      "hasAdminRes": true,
      "id": 0,
      "isCollect": true,
      "itemId": 0,
      "modelId": 0,
      "modelName": "string",
      "name": "string",
      "sensitiveLevel": 0,
      "tagDefineType": "string",
      "tagObjectId": 0,
      "tagObjectName": "string",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdqueryTagValueUsingPOST"></a>

## POST queryTagValue

POST /api/semantic/tag/value/distribution

> Body 请求参数

```json
{
  "dateConf": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "id": 0,
  "limit": 0
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[ItemValueReq](#schemaitemvaluereq)| 否 | ItemValueReq|none|

> 返回示例

> 200 Response

```json
{
  "bizName": "string",
  "itemId": 0,
  "name": "string",
  "type": "DATASET",
  "valueDistributionList": [
    {
      "ratio": 0,
      "totalCount": 0,
      "valueCount": 0,
      "valueMap": {}
    }
  ]
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ItemValueResp](#schemaitemvalueresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# tag-object-controller

<a id="opIdcreateUsingPOST_3"></a>

## POST create

POST /api/semantic/tagObject/create

> Body 请求参数

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "ext": {},
  "id": 0,
  "name": "string",
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[TagObjectReq](#schematagobjectreq)| 否 | TagObjectReq|none|

> 返回示例

> 200 Response

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "ext": {
    "property1": "string",
    "property2": "string"
  },
  "id": 0,
  "name": "string",
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[TagObjectResp](#schematagobjectresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteUsingDELETE_6"></a>

## DELETE delete

DELETE /api/semantic/tagObject/delete/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

<a id="opIdqueryTagObjectUsingPOST"></a>

## POST queryTagObject

POST /api/semantic/tagObject/query

> Body 请求参数

```json
{
  "bizName": "string",
  "createdBy": "string",
  "dataSetId": 0,
  "domainId": 0,
  "domainIds": [
    0
  ],
  "fieldsDepend": [
    "string"
  ],
  "id": "string",
  "ids": [
    0
  ],
  "isTag": 0,
  "key": "string",
  "modelIds": [
    0
  ],
  "name": "string",
  "names": [
    "string"
  ],
  "sensitiveLevel": 0,
  "status": 0
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[TagObjectFilter](#schematagobjectfilter)| 否 | TagObjectFilter|none|

> 返回示例

> 200 Response

```json
[
  {
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "description": "string",
    "domainId": 0,
    "ext": {
      "property1": "string",
      "property2": "string"
    },
    "id": 0,
    "name": "string",
    "sensitiveLevel": 0,
    "status": 0,
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[TagObjectResp](#schematagobjectresp)]|false|none||none|
|» TagObjectResp|[TagObjectResp](#schematagobjectresp)|false|none|TagObjectResp|none|
|»» bizName|string|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» description|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» ext|object|false|none||none|
|»»» **additionalProperties**|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» sensitiveLevel|integer(int32)|false|none||none|
|»» status|integer(int32)|false|none||none|
|»» typeEnum|string|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<a id="opIdupdateUsingPOST_1"></a>

## POST update

POST /api/semantic/tagObject/update

> Body 请求参数

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "ext": {},
  "id": 0,
  "name": "string",
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[TagObjectReq](#schematagobjectreq)| 否 | TagObjectReq|none|

> 返回示例

> 200 Response

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "ext": {
    "property1": "string",
    "property2": "string"
  },
  "id": 0,
  "name": "string",
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[TagObjectResp](#schematagobjectresp)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# tag-query-api-controller

<a id="opIdqueryByTagUsingPOST"></a>

## POST queryByTag

POST /api/semantic/query/tag

> Body 请求参数

```json
{
  "aggregators": [
    {
      "alias": "string",
      "args": [
        "string"
      ],
      "column": "string",
      "func": "AVG",
      "nameCh": "string"
    }
  ],
  "cacheInfo": {
    "cache": true
  },
  "convertToSql": true,
  "dataSetId": 0,
  "dataSetName": "string",
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "dimensionFilters": [
    {
      "bizName": "string",
      "children": [
        {
          "bizName": "string",
          "children": [
            {}
          ],
          "id": 0,
          "name": "string",
          "operator": "!=",
          "relation": "AND",
          "value": {}
        }
      ],
      "id": 0,
      "name": "string",
      "operator": "!=",
      "relation": "AND",
      "value": {}
    }
  ],
  "groups": [
    "string"
  ],
  "innerLayerNative": true,
  "limit": 0,
  "metricFilters": [
    {
      "bizName": "string",
      "children": [
        {
          "bizName": "string",
          "children": [
            {}
          ],
          "id": 0,
          "name": "string",
          "operator": "!=",
          "relation": "AND",
          "value": {}
        }
      ],
      "id": 0,
      "name": "string",
      "operator": "!=",
      "relation": "AND",
      "value": {}
    }
  ],
  "modelIds": [
    0
  ],
  "needAuth": true,
  "orders": [
    {
      "column": "string",
      "direction": "string"
    }
  ],
  "params": [
    {
      "name": "string",
      "value": "string"
    }
  ],
  "queryType": "DETAIL",
  "sqlInfo": {
    "correctS2SQL": "string",
    "querySQL": "string",
    "s2SQL": "string",
    "sourceId": "string"
  }
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[QueryStructReq](#schemaquerystructreq)| 否 | QueryStructReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# term-controller

<a id="opIdgetTermsUsingGET"></a>

## GET getTerms

GET /api/semantic/term

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|domainId|query|integer(int64)| 是 ||domainId|

> 返回示例

> 200 Response

```json
[
  {
    "alias": [
      "string"
    ],
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "description": "string",
    "domainId": 0,
    "id": 0,
    "name": "string",
    "relateDimensions": [
      0
    ],
    "relatedMetrics": [
      0
    ],
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string"
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[TermResp](#schematermresp)]|false|none||none|
|» TermResp|[TermResp](#schematermresp)|false|none|TermResp|none|
|»» alias|[string]|false|none||none|
|»» createdAt|string(date-time)|false|none||none|
|»» createdBy|string|false|none||none|
|»» description|string|false|none||none|
|»» domainId|integer(int64)|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» name|string|false|none||none|
|»» relateDimensions|[integer]|false|none||none|
|»» relatedMetrics|[integer]|false|none||none|
|»» updatedAt|string(date-time)|false|none||none|
|»» updatedBy|string|false|none||none|

<a id="opIdsaveOrUpdateUsingPOST"></a>

## POST saveOrUpdate

POST /api/semantic/term/saveOrUpdate

> Body 请求参数

```json
{
  "alias": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "id": 0,
  "name": "string",
  "relateDimensions": [
    0
  ],
  "relatedMetrics": [
    0
  ],
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[TermReq](#schematermreq)| 否 | TermReq|none|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIddeleteUsingDELETE_7"></a>

## DELETE delete

DELETE /api/semantic/term/{id}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|id|path|integer(int64)| 是 ||id|

> 返回示例

> 200 Response

```json
true
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|boolean|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|

### 返回数据结构

# user-controller

<a id="opIdgetCurrentUserUsingGET"></a>

## GET getCurrentUser

GET /api/auth/user/getCurrentUser

> 返回示例

> 200 Response

```json
{
  "displayName": "string",
  "email": "string",
  "id": 0,
  "isAdmin": 0,
  "name": "string",
  "superAdmin": true
}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[User](#schemauser)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetOrganizationTreeUsingGET"></a>

## GET getOrganizationTree

GET /api/auth/user/getOrganizationTree

> 返回示例

> 200 Response

```json
[
  {
    "fullName": "string",
    "id": "string",
    "name": "string",
    "parentId": "string",
    "root": true,
    "subOrganizations": [
      {
        "fullName": "string",
        "id": "string",
        "name": "string",
        "parentId": "string",
        "root": true,
        "subOrganizations": [
          {
            "fullName": "string",
            "id": "string",
            "name": "string",
            "parentId": "string",
            "root": true,
            "subOrganizations": [
              null
            ]
          }
        ]
      }
    ]
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[Organization](#schemaorganization)]|false|none||none|
|» Organization|[Organization](#schemaorganization)|false|none|Organization|none|
|»» fullName|string|false|none||none|
|»» id|string|false|none||none|
|»» name|string|false|none||none|
|»» parentId|string|false|none||none|
|»» root|boolean|false|none||none|
|»» subOrganizations|[[Organization](#schemaorganization)]|false|none||none|
|»»» Organization|[Organization](#schemaorganization)|false|none|Organization|none|
|»»»» fullName|string|false|none||none|
|»»»» id|string|false|none||none|
|»»»» name|string|false|none||none|
|»»»» parentId|string|false|none||none|
|»»»» root|boolean|false|none||none|
|»»»» subOrganizations|[[Organization](#schemaorganization)]|false|none||none|

<a id="opIdgetUserAllOrgIdUsingGET"></a>

## GET getUserAllOrgId

GET /api/auth/user/getUserAllOrgId/{userName}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|userName|path|string| 是 ||userName|

> 返回示例

> 200 Response

```json
[
  "string"
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdgetUserByOrgUsingGET"></a>

## GET getUserByOrg

GET /api/auth/user/getUserByOrg/{org}

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|org|path|string| 是 ||org|

> 返回示例

> 200 Response

```json
[
  {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[User](#schemauser)]|false|none||none|
|» User|[User](#schemauser)|false|none|User|none|
|»» displayName|string|false|none||none|
|»» email|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isAdmin|integer(int32)|false|none||none|
|»» name|string|false|none||none|
|»» superAdmin|boolean|false|none||none|

<a id="opIdgetUserListUsingGET"></a>

## GET getUserList

GET /api/auth/user/getUserList

> 返回示例

> 200 Response

```json
[
  {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

状态码 **200**

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|*anonymous*|[[User](#schemauser)]|false|none||none|
|» User|[User](#schemauser)|false|none|User|none|
|»» displayName|string|false|none||none|
|»» email|string|false|none||none|
|»» id|integer(int64)|false|none||none|
|»» isAdmin|integer(int32)|false|none||none|
|»» name|string|false|none||none|
|»» superAdmin|boolean|false|none||none|

<a id="opIdgetUserNamesUsingGET"></a>

## GET getUserNames

GET /api/auth/user/getUserNames

> 返回示例

> 200 Response

```json
[
  "string"
]
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdloginUsingPOST"></a>

## POST login

POST /api/auth/user/login

> Body 请求参数

```json
{
  "name": "string",
  "password": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[UserReq](#schemauserreq)| 否 | UserReq|none|

> 返回示例

> 200 Response

```json
"string"
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

<a id="opIdregisterUsingPOST"></a>

## POST register

POST /api/auth/user/register

> Body 请求参数

```json
{
  "name": "string",
  "password": "string"
}
```

### 请求参数

|名称|位置|类型|必选|中文名|说明|
|---|---|---|---|---|---|
|body|body|[UserReq](#schemauserreq)| 否 | UserReq|none|

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|Inline|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|Forbidden|Inline|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|Inline|

### 返回数据结构

# 数据模型

<h2 id="tocS_VisualConfig">VisualConfig</h2>

<a id="schemavisualconfig"></a>
<a id="schema_VisualConfig"></a>
<a id="tocSvisualconfig"></a>
<a id="tocsvisualconfig"></a>

```json
{
  "enableSimpleMode": true,
  "showDebugInfo": true
}

```

VisualConfig

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|enableSimpleMode|boolean|false|none||none|
|showDebugInfo|boolean|false|none||none|

<h2 id="tocS_ValueDistribution">ValueDistribution</h2>

<a id="schemavaluedistribution"></a>
<a id="schema_ValueDistribution"></a>
<a id="tocSvaluedistribution"></a>
<a id="tocsvaluedistribution"></a>

```json
{
  "ratio": 0,
  "totalCount": 0,
  "valueCount": 0,
  "valueMap": {}
}

```

ValueDistribution

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|ratio|number(double)|false|none||none|
|totalCount|integer(int64)|false|none||none|
|valueCount|integer(int64)|false|none||none|
|valueMap|object|false|none||none|

<h2 id="tocS_UserReq">UserReq</h2>

<a id="schemauserreq"></a>
<a id="schema_UserReq"></a>
<a id="tocSuserreq"></a>
<a id="tocsuserreq"></a>

```json
{
  "name": "string",
  "password": "string"
}

```

UserReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|name|string|true|none||none|
|password|string|true|none||none|

<h2 id="tocS_User">User</h2>

<a id="schemauser"></a>
<a id="schema_User"></a>
<a id="tocSuser"></a>
<a id="tocsuser"></a>

```json
{
  "displayName": "string",
  "email": "string",
  "id": 0,
  "isAdmin": 0,
  "name": "string",
  "superAdmin": true
}

```

User

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|displayName|string|false|none||none|
|email|string|false|none||none|
|id|integer(int64)|false|none||none|
|isAdmin|integer(int32)|false|none||none|
|name|string|false|none||none|
|superAdmin|boolean|false|none||none|

<h2 id="tocS_UnAvailableItemResp">UnAvailableItemResp</h2>

<a id="schemaunavailableitemresp"></a>
<a id="schema_UnAvailableItemResp"></a>
<a id="tocSunavailableitemresp"></a>
<a id="tocsunavailableitemresp"></a>

```json
{
  "dimensionResps": [
    {
      "alias": "string",
      "bizName": "string",
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dataType": "ARRAY",
      "defaultValues": [
        "string"
      ],
      "description": "string",
      "dimValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "expr": "string",
      "ext": {},
      "id": 0,
      "isTag": 0,
      "modelBizName": "string",
      "modelFilterSql": "string",
      "modelId": 0,
      "modelName": "string",
      "name": "string",
      "semanticType": "string",
      "sensitiveLevel": 0,
      "status": 0,
      "type": "string",
      "typeEnum": "DATASET",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "metricResps": [
    {
      "alias": "string",
      "bizName": "string",
      "classifications": [
        "string"
      ],
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "defaultAgg": "string",
      "description": "string",
      "domainId": 0,
      "drillDownDimensions": [
        {
          "dimensionId": 0,
          "inheritedFromModel": true,
          "necessary": true
        }
      ],
      "expr": "string",
      "ext": {},
      "hasAdminRes": true,
      "id": 0,
      "isCollect": true,
      "isPublish": 0,
      "isTag": 0,
      "metricDefineByFieldParams": {
        "expr": "string",
        "fields": [
          {
            "fieldName": null
          }
        ],
        "filterSql": "string"
      },
      "metricDefineByMeasureParams": {
        "expr": "string",
        "filterSql": "string",
        "measures": [
          {
            "agg": null,
            "bizName": null,
            "constraint": null
          }
        ]
      },
      "metricDefineByMetricParams": {
        "expr": "string",
        "filterSql": "string",
        "metrics": [
          {
            "bizName": null,
            "id": null
          }
        ]
      },
      "metricDefineType": "FIELD",
      "modelBizName": "string",
      "modelId": 0,
      "modelName": "string",
      "name": "string",
      "relaDimensionIdKey": "string",
      "relateDimension": {
        "drillDownDimensions": [
          {
            "dimensionId": null,
            "inheritedFromModel": null,
            "necessary": null
          }
        ]
      },
      "sensitiveLevel": 0,
      "similarity": 0,
      "status": 0,
      "type": "string",
      "typeEnum": "DATASET",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ]
}

```

UnAvailableItemResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dimensionResps|[[DimensionResp](#schemadimensionresp)]|false|none||none|
|metricResps|[[MetricResp](#schemametricresp)]|false|none||none|

<h2 id="tocS_TimeDefaultConfig">TimeDefaultConfig</h2>

<a id="schematimedefaultconfig"></a>
<a id="schema_TimeDefaultConfig"></a>
<a id="tocStimedefaultconfig"></a>
<a id="tocstimedefaultconfig"></a>

```json
{
  "period": "string",
  "timeMode": "LAST",
  "unit": 0
}

```

TimeDefaultConfig

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|period|string|false|none||none|
|timeMode|string|false|none||none|
|unit|integer(int32)|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|timeMode|LAST|
|timeMode|RECENT|

<h2 id="tocS_TermResp">TermResp</h2>

<a id="schematermresp"></a>
<a id="schema_TermResp"></a>
<a id="tocStermresp"></a>
<a id="tocstermresp"></a>

```json
{
  "alias": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "id": 0,
  "name": "string",
  "relateDimensions": [
    0
  ],
  "relatedMetrics": [
    0
  ],
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

TermResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|alias|[string]|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|description|string|false|none||none|
|domainId|integer(int64)|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|relateDimensions|[integer]|false|none||none|
|relatedMetrics|[integer]|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

<h2 id="tocS_TermReq">TermReq</h2>

<a id="schematermreq"></a>
<a id="schema_TermReq"></a>
<a id="tocStermreq"></a>
<a id="tocstermreq"></a>

```json
{
  "alias": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "id": 0,
  "name": "string",
  "relateDimensions": [
    0
  ],
  "relatedMetrics": [
    0
  ],
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

TermReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|alias|[string]|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|description|string|false|none||none|
|domainId|integer(int64)|true|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|relateDimensions|[integer]|false|none||none|
|relatedMetrics|[integer]|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

<h2 id="tocS_TagTypeDefaultConfig">TagTypeDefaultConfig</h2>

<a id="schematagtypedefaultconfig"></a>
<a id="schema_TagTypeDefaultConfig"></a>
<a id="tocStagtypedefaultconfig"></a>
<a id="tocstagtypedefaultconfig"></a>

```json
{
  "defaultDisplayInfo": {
    "dimensionIds": [
      0
    ],
    "metricIds": [
      0
    ]
  },
  "timeDefaultConfig": {
    "period": "string",
    "timeMode": "LAST",
    "unit": 0
  }
}

```

TagTypeDefaultConfig

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|defaultDisplayInfo|[DefaultDisplayInfo](#schemadefaultdisplayinfo)|false|none||none|
|timeDefaultConfig|[TimeDefaultConfig](#schematimedefaultconfig)|false|none||none|

<h2 id="tocS_TagResp">TagResp</h2>

<a id="schematagresp"></a>
<a id="schema_TagResp"></a>
<a id="tocStagresp"></a>
<a id="tocstagresp"></a>

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "domainName": "string",
  "ext": {},
  "hasAdminRes": true,
  "id": 0,
  "isCollect": true,
  "itemId": 0,
  "modelId": 0,
  "modelName": "string",
  "name": "string",
  "sensitiveLevel": 0,
  "tagDefineType": "string",
  "tagObjectId": 0,
  "tagObjectName": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

TagResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|description|string|false|none||none|
|domainId|integer(int64)|false|none||none|
|domainName|string|false|none||none|
|ext|object|false|none||none|
|hasAdminRes|boolean|false|none||none|
|id|integer(int64)|false|none||none|
|isCollect|boolean|false|none||none|
|itemId|integer(int64)|false|none||none|
|modelId|integer(int64)|false|none||none|
|modelName|string|false|none||none|
|name|string|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|tagDefineType|string|false|none||none|
|tagObjectId|integer(int64)|false|none||none|
|tagObjectName|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

<h2 id="tocS_TagReq">TagReq</h2>

<a id="schematagreq"></a>
<a id="schema_TagReq"></a>
<a id="tocStagreq"></a>
<a id="tocstagreq"></a>

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "id": 0,
  "itemId": 0,
  "tagDefineType": "DIMENSION",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

TagReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|id|integer(int64)|false|none||none|
|itemId|integer(int64)|true|none||none|
|tagDefineType|string|true|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|tagDefineType|DIMENSION|
|tagDefineType|FIELD|
|tagDefineType|METRIC|
|tagDefineType|TAG|

<h2 id="tocS_TagObjectResp">TagObjectResp</h2>

<a id="schematagobjectresp"></a>
<a id="schema_TagObjectResp"></a>
<a id="tocStagobjectresp"></a>
<a id="tocstagobjectresp"></a>

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "ext": {
    "property1": "string",
    "property2": "string"
  },
  "id": 0,
  "name": "string",
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

TagObjectResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|description|string|false|none||none|
|domainId|integer(int64)|false|none||none|
|ext|object|false|none||none|
|» **additionalProperties**|string|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_TagObjectReq">TagObjectReq</h2>

<a id="schematagobjectreq"></a>
<a id="schema_TagObjectReq"></a>
<a id="tocStagobjectreq"></a>
<a id="tocstagobjectreq"></a>

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "ext": {},
  "id": 0,
  "name": "string",
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

TagObjectReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|description|string|false|none||none|
|domainId|integer(int64)|true|none||none|
|ext|object|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_TagObjectFilter">TagObjectFilter</h2>

<a id="schematagobjectfilter"></a>
<a id="schema_TagObjectFilter"></a>
<a id="tocStagobjectfilter"></a>
<a id="tocstagobjectfilter"></a>

```json
{
  "bizName": "string",
  "createdBy": "string",
  "dataSetId": 0,
  "domainId": 0,
  "domainIds": [
    0
  ],
  "fieldsDepend": [
    "string"
  ],
  "id": "string",
  "ids": [
    0
  ],
  "isTag": 0,
  "key": "string",
  "modelIds": [
    0
  ],
  "name": "string",
  "names": [
    "string"
  ],
  "sensitiveLevel": 0,
  "status": 0
}

```

TagObjectFilter

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|createdBy|string|false|none||none|
|dataSetId|integer(int64)|false|none||none|
|domainId|integer(int64)|false|none||none|
|domainIds|[integer]|false|none||none|
|fieldsDepend|[string]|false|none||none|
|id|string|false|none||none|
|ids|[integer]|false|none||none|
|isTag|integer(int32)|false|none||none|
|key|string|false|none||none|
|modelIds|[integer]|false|none||none|
|name|string|false|none||none|
|names|[string]|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|

<h2 id="tocS_TagItem">TagItem</h2>

<a id="schematagitem"></a>
<a id="schema_TagItem"></a>
<a id="tocStagitem"></a>
<a id="tocstagitem"></a>

```json
{
  "isTag": 0,
  "itemId": 0
}

```

TagItem

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isTag|integer(int32)|false|none||none|
|itemId|integer(int64)|false|none||none|

<h2 id="tocS_TagFilterPageReq">TagFilterPageReq</h2>

<a id="schematagfilterpagereq"></a>
<a id="schema_TagFilterPageReq"></a>
<a id="tocStagfilterpagereq"></a>
<a id="tocstagfilterpagereq"></a>

```json
{
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdBy": "string",
  "current": 0,
  "domainIds": [
    0
  ],
  "hasCollect": true,
  "id": "string",
  "ids": [
    0
  ],
  "key": "string",
  "modelIds": [
    0
  ],
  "name": "string",
  "orderCondition": "string",
  "pageSize": 0,
  "sensitiveLevel": 0,
  "sort": "string",
  "status": 0,
  "tagDefineType": "DIMENSION",
  "tagObjectId": 0
}

```

TagFilterPageReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|classifications|[string]|false|none||none|
|createdBy|string|false|none||none|
|current|integer(int32)|false|none||none|
|domainIds|[integer]|false|none||none|
|hasCollect|boolean|false|none||none|
|id|string|false|none||none|
|ids|[integer]|false|none||none|
|key|string|false|none||none|
|modelIds|[integer]|false|none||none|
|name|string|false|none||none|
|orderCondition|string|false|none||none|
|pageSize|integer(int32)|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|sort|string|false|none||none|
|status|integer(int32)|false|none||none|
|tagDefineType|string|false|none||none|
|tagObjectId|integer(int64)|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|tagDefineType|DIMENSION|
|tagDefineType|FIELD|
|tagDefineType|METRIC|
|tagDefineType|TAG|

<h2 id="tocS_TagFilter">TagFilter</h2>

<a id="schematagfilter"></a>
<a id="schema_TagFilter"></a>
<a id="tocStagfilter"></a>
<a id="tocstagfilter"></a>

```json
{
  "bizName": "string",
  "createdBy": "string",
  "dataSetId": 0,
  "domainId": 0,
  "fieldsDepend": [
    "string"
  ],
  "hasCollect": true,
  "id": "string",
  "ids": [
    0
  ],
  "isTag": 0,
  "itemIds": [
    0
  ],
  "key": "string",
  "modelIds": [
    0
  ],
  "name": "string",
  "names": [
    "string"
  ],
  "sensitiveLevel": 0,
  "status": 0,
  "tagDefineType": "DIMENSION"
}

```

TagFilter

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|createdBy|string|false|none||none|
|dataSetId|integer(int64)|false|none||none|
|domainId|integer(int64)|false|none||none|
|fieldsDepend|[string]|false|none||none|
|hasCollect|boolean|false|none||none|
|id|string|false|none||none|
|ids|[integer]|false|none||none|
|isTag|integer(int32)|false|none||none|
|itemIds|[integer]|false|none||none|
|key|string|false|none||none|
|modelIds|[integer]|false|none||none|
|name|string|false|none||none|
|names|[string]|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|tagDefineType|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|tagDefineType|DIMENSION|
|tagDefineType|FIELD|
|tagDefineType|METRIC|
|tagDefineType|TAG|

<h2 id="tocS_TagDeleteReq">TagDeleteReq</h2>

<a id="schematagdeletereq"></a>
<a id="schema_TagDeleteReq"></a>
<a id="tocStagdeletereq"></a>
<a id="tocstagdeletereq"></a>

```json
{
  "ids": [
    0
  ],
  "itemIds": [
    0
  ],
  "tagDefineType": "DIMENSION"
}

```

TagDeleteReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|ids|[integer]|false|none||none|
|itemIds|[integer]|false|none||none|
|tagDefineType|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|tagDefineType|DIMENSION|
|tagDefineType|FIELD|
|tagDefineType|METRIC|
|tagDefineType|TAG|

<h2 id="tocS_TagDO">TagDO</h2>

<a id="schematagdo"></a>
<a id="schema_TagDO"></a>
<a id="tocStagdo"></a>
<a id="tocstagdo"></a>

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "id": 0,
  "itemId": 0,
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

TagDO

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|id|integer(int64)|false|none||none|
|itemId|integer(int64)|false|none||none|
|type|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

<h2 id="tocS_SystemConfigRes">SystemConfigRes</h2>

<a id="schemasystemconfigres"></a>
<a id="schema_SystemConfigRes"></a>
<a id="tocSsystemconfigres"></a>
<a id="tocssystemconfigres"></a>

```json
{
  "admin": "string",
  "admins": [
    "string"
  ],
  "id": 0,
  "parameters": [
    {
      "candidateValues": [
        {}
      ],
      "comment": "string",
      "dataType": "string",
      "defaultValue": "string",
      "description": "string",
      "module": "string",
      "name": "string",
      "value": "string"
    }
  ]
}

```

SystemConfigRes

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|admin|string|false|none||none|
|admins|[string]|false|none||none|
|id|integer(int32)|false|none||none|
|parameters|[[Parameter](#schemaparameter)]|false|none||none|

<h2 id="tocS_SystemConfigReq">SystemConfigReq</h2>

<a id="schemasystemconfigreq"></a>
<a id="schema_SystemConfigReq"></a>
<a id="tocSsystemconfigreq"></a>
<a id="tocssystemconfigreq"></a>

```json
{
  "adminList": "string",
  "admins": [
    "string"
  ],
  "id": 0,
  "parameters": [
    {
      "candidateValues": [
        {}
      ],
      "comment": "string",
      "dataType": "string",
      "defaultValue": "string",
      "description": "string",
      "module": "string",
      "name": "string",
      "value": "string"
    }
  ]
}

```

SystemConfigReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|adminList|string|false|none||none|
|admins|[string]|false|none||none|
|id|integer(int32)|false|none||none|
|parameters|[[Parameter](#schemaparameter)]|false|none||none|

<h2 id="tocS_SqlVariable">SqlVariable</h2>

<a id="schemasqlvariable"></a>
<a id="schema_SqlVariable"></a>
<a id="tocSsqlvariable"></a>
<a id="tocssqlvariable"></a>

```json
{
  "defaultValues": [
    {}
  ],
  "name": "string",
  "valueType": "EXPR"
}

```

SqlVariable

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|defaultValues|[object]|false|none||none|
|name|string|false|none||none|
|valueType|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|valueType|EXPR|
|valueType|NUMBER|
|valueType|STRING|

<h2 id="tocS_SqlInfo">SqlInfo</h2>

<a id="schemasqlinfo"></a>
<a id="schema_SqlInfo"></a>
<a id="tocSsqlinfo"></a>
<a id="tocssqlinfo"></a>

```json
{
  "correctS2SQL": "string",
  "querySQL": "string",
  "s2SQL": "string",
  "sourceId": "string"
}

```

SqlInfo

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|correctS2SQL|string|false|none||none|
|querySQL|string|false|none||none|
|s2SQL|string|false|none||none|
|sourceId|string|false|none||none|

<h2 id="tocS_SqlExemplar">SqlExemplar</h2>

<a id="schemasqlexemplar"></a>
<a id="schema_SqlExemplar"></a>
<a id="tocSsqlexemplar"></a>
<a id="tocssqlexemplar"></a>

```json
{
  "dbSchema": "string",
  "question": "string",
  "sql": "string"
}

```

SqlExemplar

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dbSchema|string|false|none||none|
|question|string|false|none||none|
|sql|string|false|none||none|

<h2 id="tocS_SqlExecuteReq">SqlExecuteReq</h2>

<a id="schemasqlexecutereq"></a>
<a id="schema_SqlExecuteReq"></a>
<a id="tocSsqlexecutereq"></a>
<a id="tocssqlexecutereq"></a>

```json
{
  "id": 0,
  "limit": 0,
  "sql": "string",
  "sqlVariables": [
    {
      "defaultValues": [
        {}
      ],
      "name": "string",
      "valueType": "EXPR"
    }
  ]
}

```

SqlExecuteReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|true|none||none|
|limit|integer(int32)|false|none||none|
|sql|string|true|none||none|
|sqlVariables|[[SqlVariable](#schemasqlvariable)]|false|none||none|

<h2 id="tocS_SqlEvaluation">SqlEvaluation</h2>

<a id="schemasqlevaluation"></a>
<a id="schema_SqlEvaluation"></a>
<a id="tocSsqlevaluation"></a>
<a id="tocssqlevaluation"></a>

```json
{
  "isValidated": true,
  "validateMsg": "string"
}

```

SqlEvaluation

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isValidated|boolean|false|none||none|
|validateMsg|string|false|none||none|

<h2 id="tocS_SimilarQueryRecallResp">SimilarQueryRecallResp</h2>

<a id="schemasimilarqueryrecallresp"></a>
<a id="schema_SimilarQueryRecallResp"></a>
<a id="tocSsimilarqueryrecallresp"></a>
<a id="tocssimilarqueryrecallresp"></a>

```json
{
  "queryId": 0,
  "queryText": "string"
}

```

SimilarQueryRecallResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|queryId|integer(int64)|false|none||none|
|queryText|string|false|none||none|

<h2 id="tocS_ShowCaseResp">ShowCaseResp</h2>

<a id="schemashowcaseresp"></a>
<a id="schema_ShowCaseResp"></a>
<a id="tocSshowcaseresp"></a>
<a id="tocsshowcaseresp"></a>

```json
{
  "current": 0,
  "pageSize": 0,
  "showCaseMap": {
    "property1": [
      {
        "chatId": 0,
        "createTime": "2019-08-24T14:15:22Z",
        "feedback": "string",
        "parseInfos": [
          {
            "aggType": "[",
            "dataSet": {},
            "dateInfo": {},
            "dimensionFilters": [
              null
            ],
            "dimensions": [
              null
            ],
            "elementMatches": [
              null
            ],
            "entity": {},
            "entityInfo": {},
            "filterType": "[",
            "id": 0,
            "limit": 0,
            "metricFilters": [
              null
            ],
            "metrics": [
              null
            ],
            "orders": [
              null
            ],
            "properties": {},
            "queryMode": "string",
            "queryType": "[",
            "score": 0,
            "sqlEvaluation": {},
            "sqlInfo": {},
            "textInfo": "string"
          }
        ],
        "parseTimeCost": {
          "parseStartTime": 0,
          "parseTime": 0,
          "sqlTime": 0
        },
        "queryResult": {
          "aggregateInfo": {
            "metricInfos": null
          },
          "chatContext": {
            "aggType": null,
            "dataSet": null,
            "dateInfo": null,
            "dimensionFilters": null,
            "dimensions": null,
            "elementMatches": null,
            "entity": null,
            "entityInfo": null,
            "filterType": null,
            "id": null,
            "limit": null,
            "metricFilters": null,
            "metrics": null,
            "orders": null,
            "properties": null,
            "queryMode": null,
            "queryType": null,
            "score": null,
            "sqlEvaluation": null,
            "sqlInfo": null,
            "textInfo": null
          },
          "entityInfo": {
            "dataSetInfo": null,
            "dimensions": null,
            "entityId": null,
            "metrics": null
          },
          "queryAuthorization": {
            "dimensionFilters": null,
            "dimensionFiltersDesc": null,
            "domainName": null,
            "message": null
          },
          "queryColumns": [
            {}
          ],
          "queryId": 0,
          "queryMode": "string",
          "queryResults": [
            {}
          ],
          "querySql": "string",
          "queryState": "EMPTY",
          "queryTimeCost": 0,
          "recommendedDimensions": [
            {}
          ],
          "response": {},
          "textResult": "string"
        },
        "queryText": "string",
        "questionId": 0,
        "score": 0,
        "similarQueries": [
          {
            "queryId": 0,
            "queryText": "string"
          }
        ]
      }
    ],
    "property2": [
      {
        "chatId": 0,
        "createTime": "2019-08-24T14:15:22Z",
        "feedback": "string",
        "parseInfos": [
          {
            "aggType": "[",
            "dataSet": {},
            "dateInfo": {},
            "dimensionFilters": [
              null
            ],
            "dimensions": [
              null
            ],
            "elementMatches": [
              null
            ],
            "entity": {},
            "entityInfo": {},
            "filterType": "[",
            "id": 0,
            "limit": 0,
            "metricFilters": [
              null
            ],
            "metrics": [
              null
            ],
            "orders": [
              null
            ],
            "properties": {},
            "queryMode": "string",
            "queryType": "[",
            "score": 0,
            "sqlEvaluation": {},
            "sqlInfo": {},
            "textInfo": "string"
          }
        ],
        "parseTimeCost": {
          "parseStartTime": 0,
          "parseTime": 0,
          "sqlTime": 0
        },
        "queryResult": {
          "aggregateInfo": {
            "metricInfos": null
          },
          "chatContext": {
            "aggType": null,
            "dataSet": null,
            "dateInfo": null,
            "dimensionFilters": null,
            "dimensions": null,
            "elementMatches": null,
            "entity": null,
            "entityInfo": null,
            "filterType": null,
            "id": null,
            "limit": null,
            "metricFilters": null,
            "metrics": null,
            "orders": null,
            "properties": null,
            "queryMode": null,
            "queryType": null,
            "score": null,
            "sqlEvaluation": null,
            "sqlInfo": null,
            "textInfo": null
          },
          "entityInfo": {
            "dataSetInfo": null,
            "dimensions": null,
            "entityId": null,
            "metrics": null
          },
          "queryAuthorization": {
            "dimensionFilters": null,
            "dimensionFiltersDesc": null,
            "domainName": null,
            "message": null
          },
          "queryColumns": [
            {}
          ],
          "queryId": 0,
          "queryMode": "string",
          "queryResults": [
            {}
          ],
          "querySql": "string",
          "queryState": "EMPTY",
          "queryTimeCost": 0,
          "recommendedDimensions": [
            {}
          ],
          "response": {},
          "textResult": "string"
        },
        "queryText": "string",
        "questionId": 0,
        "score": 0,
        "similarQueries": [
          {
            "queryId": 0,
            "queryText": "string"
          }
        ]
      }
    ]
  }
}

```

ShowCaseResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|current|integer(int32)|false|none||none|
|pageSize|integer(int32)|false|none||none|
|showCaseMap|object|false|none||none|
|» **additionalProperties**|[[QueryResp](#schemaqueryresp)]|false|none||none|

<h2 id="tocS_SemanticQueryResp">SemanticQueryResp</h2>

<a id="schemasemanticqueryresp"></a>
<a id="schema_SemanticQueryResp"></a>
<a id="tocSsemanticqueryresp"></a>
<a id="tocssemanticqueryresp"></a>

```json
{
  "columns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "dimensionColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "metricColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "pageNo": 0,
  "pageSize": 0,
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "resultList": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "sql": "string",
  "totalCount": 0,
  "useCache": true
}

```

SemanticQueryResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|columns|[[QueryColumn](#schemaquerycolumn)]|false|none||none|
|dimensionColumns|[[QueryColumn](#schemaquerycolumn)]|false|none||none|
|metricColumns|[[QueryColumn](#schemaquerycolumn)]|false|none||none|
|pageNo|integer(int32)|false|none||none|
|pageSize|integer(int32)|false|none||none|
|queryAuthorization|[QueryAuthorization](#schemaqueryauthorization)|false|none||none|
|resultList|[object]|false|none||none|
|» **additionalProperties**|object|false|none||none|
|sql|string|false|none||none|
|totalCount|integer(int64)|false|none||none|
|useCache|boolean|false|none||none|

<h2 id="tocS_SemanticParseInfo">SemanticParseInfo</h2>

<a id="schemasemanticparseinfo"></a>
<a id="schema_SemanticParseInfo"></a>
<a id="tocSsemanticparseinfo"></a>
<a id="tocssemanticparseinfo"></a>

```json
{
  "aggType": "AVG",
  "dataSet": {
    "alias": [
      "string"
    ],
    "bizName": "string",
    "dataFormatType": "string",
    "dataSet": 0,
    "dataSetName": "string",
    "defaultAgg": "string",
    "description": "string",
    "id": 0,
    "isTag": 0,
    "model": 0,
    "name": "string",
    "order": 0,
    "relatedSchemaElements": [
      {
        "dimensionId": 0,
        "necessary": true
      }
    ],
    "schemaValueMaps": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "techName": "string"
      }
    ],
    "type": "DATASET",
    "useCnt": 0
  },
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "dimensionFilters": [
    {
      "bizName": "string",
      "elementID": 0,
      "function": "string",
      "name": "string",
      "operator": "!=",
      "value": {}
    }
  ],
  "dimensions": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "elementMatches": [
    {
      "detectWord": "string",
      "element": {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      },
      "frequency": 0,
      "inherited": true,
      "similarity": 0,
      "word": "string"
    }
  ],
  "entity": {
    "alias": [
      "string"
    ],
    "bizName": "string",
    "dataFormatType": "string",
    "dataSet": 0,
    "dataSetName": "string",
    "defaultAgg": "string",
    "description": "string",
    "id": 0,
    "isTag": 0,
    "model": 0,
    "name": "string",
    "order": 0,
    "relatedSchemaElements": [
      {
        "dimensionId": 0,
        "necessary": true
      }
    ],
    "schemaValueMaps": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "techName": "string"
      }
    ],
    "type": "DATASET",
    "useCnt": 0
  },
  "entityInfo": {
    "dataSetInfo": {
      "bizName": "string",
      "itemId": 0,
      "name": "string",
      "primaryKey": "string",
      "value": "string",
      "words": [
        "string"
      ]
    },
    "dimensions": [
      {
        "bizName": "string",
        "itemId": 0,
        "name": "string",
        "value": "string"
      }
    ],
    "entityId": "string",
    "metrics": [
      {
        "bizName": "string",
        "itemId": 0,
        "name": "string",
        "value": "string"
      }
    ]
  },
  "filterType": "AND",
  "id": 0,
  "limit": 0,
  "metricFilters": [
    {
      "bizName": "string",
      "elementID": 0,
      "function": "string",
      "name": "string",
      "operator": "!=",
      "value": {}
    }
  ],
  "metrics": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "orders": [
    {
      "column": "string",
      "direction": "string"
    }
  ],
  "properties": {},
  "queryMode": "string",
  "queryType": "DETAIL",
  "score": 0,
  "sqlEvaluation": {
    "isValidated": true,
    "validateMsg": "string"
  },
  "sqlInfo": {
    "correctS2SQL": "string",
    "querySQL": "string",
    "s2SQL": "string",
    "sourceId": "string"
  },
  "textInfo": "string"
}

```

SemanticParseInfo

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|aggType|string|false|none||none|
|dataSet|[SchemaElement](#schemaschemaelement)|false|none||none|
|dateInfo|[DateConf](#schemadateconf)|false|none||none|
|dimensionFilters|[[QueryFilter](#schemaqueryfilter)]|false|none||none|
|dimensions|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|elementMatches|[[SchemaElementMatch](#schemaschemaelementmatch)]|false|none||none|
|entity|[SchemaElement](#schemaschemaelement)|false|none||none|
|entityInfo|[EntityInfo](#schemaentityinfo)|false|none||none|
|filterType|string|false|none||none|
|id|integer(int32)|false|none||none|
|limit|integer(int64)|false|none||none|
|metricFilters|[[QueryFilter](#schemaqueryfilter)]|false|none||none|
|metrics|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|orders|[[Order](#schemaorder)]|false|none||none|
|properties|object|false|none||none|
|queryMode|string|false|none||none|
|queryType|string|false|none||none|
|score|number(double)|false|none||none|
|sqlEvaluation|[SqlEvaluation](#schemasqlevaluation)|false|none||none|
|sqlInfo|[SqlInfo](#schemasqlinfo)|false|none||none|
|textInfo|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|aggType|AVG|
|aggType|COUNT|
|aggType|DISTINCT|
|aggType|MAX|
|aggType|MIN|
|aggType|NONE|
|aggType|SUM|
|aggType|TOPN|
|filterType|AND|
|filterType|UNION|
|queryType|DETAIL|
|queryType|ID|
|queryType|METRIC|

<h2 id="tocS_SchemaValueMap">SchemaValueMap</h2>

<a id="schemaschemavaluemap"></a>
<a id="schema_SchemaValueMap"></a>
<a id="tocSschemavaluemap"></a>
<a id="tocsschemavaluemap"></a>

```json
{
  "alias": [
    "string"
  ],
  "bizName": "string",
  "techName": "string"
}

```

SchemaValueMap

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|alias|[string]|false|none||none|
|bizName|string|false|none||none|
|techName|string|false|none||none|

<h2 id="tocS_SchemaMapInfoRes">SchemaMapInfoRes</h2>

<a id="schemaschemamapinfores"></a>
<a id="schema_SchemaMapInfoRes"></a>
<a id="tocSschemamapinfores"></a>
<a id="tocsschemamapinfores"></a>

```json
{
  "dataSetElementMatches": {
    "property1": [
      {
        "detectWord": "string",
        "element": {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            {}
          ],
          "schemaValueMaps": [
            {}
          ],
          "type": "DATASET",
          "useCnt": 0
        },
        "frequency": 0,
        "inherited": true,
        "similarity": 0,
        "word": "string"
      }
    ],
    "property2": [
      {
        "detectWord": "string",
        "element": {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            {}
          ],
          "schemaValueMaps": [
            {}
          ],
          "type": "DATASET",
          "useCnt": 0
        },
        "frequency": 0,
        "inherited": true,
        "similarity": 0,
        "word": "string"
      }
    ]
  },
  "matchedDataSetInfos": [
    0
  ]
}

```

SchemaMapInfoRes

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dataSetElementMatches|object|false|none||none|
|» **additionalProperties**|[[SchemaElementMatch](#schemaschemaelementmatch)]|false|none||none|
|matchedDataSetInfos|[integer]|false|none||none|

<h2 id="tocS_SchemaMapInfoReq">SchemaMapInfoReq</h2>

<a id="schemaschemamapinforeq"></a>
<a id="schema_SchemaMapInfoReq"></a>
<a id="tocSschemamapinforeq"></a>
<a id="tocsschemamapinforeq"></a>

```json
{
  "dataSetElementMatches": {
    "property1": [
      {
        "detectWord": "string",
        "element": {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            {}
          ],
          "schemaValueMaps": [
            {}
          ],
          "type": "DATASET",
          "useCnt": 0
        },
        "frequency": 0,
        "inherited": true,
        "similarity": 0,
        "word": "string"
      }
    ],
    "property2": [
      {
        "detectWord": "string",
        "element": {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            {}
          ],
          "schemaValueMaps": [
            {}
          ],
          "type": "DATASET",
          "useCnt": 0
        },
        "frequency": 0,
        "inherited": true,
        "similarity": 0,
        "word": "string"
      }
    ]
  }
}

```

SchemaMapInfoReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dataSetElementMatches|object|false|none||none|
|» **additionalProperties**|[[SchemaElementMatch](#schemaschemaelementmatch)]|false|none||none|

<h2 id="tocS_SchemaMapInfo">SchemaMapInfo</h2>

<a id="schemaschemamapinfo"></a>
<a id="schema_SchemaMapInfo"></a>
<a id="tocSschemamapinfo"></a>
<a id="tocsschemamapinfo"></a>

```json
{
  "dataSetElementMatches": {
    "property1": [
      {
        "detectWord": "string",
        "element": {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            {}
          ],
          "schemaValueMaps": [
            {}
          ],
          "type": "DATASET",
          "useCnt": 0
        },
        "frequency": 0,
        "inherited": true,
        "similarity": 0,
        "word": "string"
      }
    ],
    "property2": [
      {
        "detectWord": "string",
        "element": {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            {}
          ],
          "schemaValueMaps": [
            {}
          ],
          "type": "DATASET",
          "useCnt": 0
        },
        "frequency": 0,
        "inherited": true,
        "similarity": 0,
        "word": "string"
      }
    ]
  }
}

```

SchemaMapInfo

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dataSetElementMatches|object|false|none||none|
|» **additionalProperties**|[[SchemaElementMatch](#schemaschemaelementmatch)]|false|none||none|

<h2 id="tocS_SchemaElementMatch">SchemaElementMatch</h2>

<a id="schemaschemaelementmatch"></a>
<a id="schema_SchemaElementMatch"></a>
<a id="tocSschemaelementmatch"></a>
<a id="tocsschemaelementmatch"></a>

```json
{
  "detectWord": "string",
  "element": {
    "alias": [
      "string"
    ],
    "bizName": "string",
    "dataFormatType": "string",
    "dataSet": 0,
    "dataSetName": "string",
    "defaultAgg": "string",
    "description": "string",
    "id": 0,
    "isTag": 0,
    "model": 0,
    "name": "string",
    "order": 0,
    "relatedSchemaElements": [
      {
        "dimensionId": 0,
        "necessary": true
      }
    ],
    "schemaValueMaps": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "techName": "string"
      }
    ],
    "type": "DATASET",
    "useCnt": 0
  },
  "frequency": 0,
  "inherited": true,
  "similarity": 0,
  "word": "string"
}

```

SchemaElementMatch

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|detectWord|string|false|none||none|
|element|[SchemaElement](#schemaschemaelement)|false|none||none|
|frequency|integer(int64)|false|none||none|
|inherited|boolean|false|none||none|
|similarity|number(double)|false|none||none|
|word|string|false|none||none|

<h2 id="tocS_SchemaElement">SchemaElement</h2>

<a id="schemaschemaelement"></a>
<a id="schema_SchemaElement"></a>
<a id="tocSschemaelement"></a>
<a id="tocsschemaelement"></a>

```json
{
  "alias": [
    "string"
  ],
  "bizName": "string",
  "dataFormatType": "string",
  "dataSet": 0,
  "dataSetName": "string",
  "defaultAgg": "string",
  "description": "string",
  "id": 0,
  "isTag": 0,
  "model": 0,
  "name": "string",
  "order": 0,
  "relatedSchemaElements": [
    {
      "dimensionId": 0,
      "necessary": true
    }
  ],
  "schemaValueMaps": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "techName": "string"
    }
  ],
  "type": "DATASET",
  "useCnt": 0
}

```

SchemaElement

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|alias|[string]|false|none||none|
|bizName|string|false|none||none|
|dataFormatType|string|false|none||none|
|dataSet|integer(int64)|false|none||none|
|dataSetName|string|false|none||none|
|defaultAgg|string|false|none||none|
|description|string|false|none||none|
|id|integer(int64)|false|none||none|
|isTag|integer(int32)|false|none||none|
|model|integer(int64)|false|none||none|
|name|string|false|none||none|
|order|number(double)|false|none||none|
|relatedSchemaElements|[[RelatedSchemaElement](#schemarelatedschemaelement)]|false|none||none|
|schemaValueMaps|[[SchemaValueMap](#schemaschemavaluemap)]|false|none||none|
|type|string|false|none||none|
|useCnt|integer(int64)|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|DATASET|
|type|DATE|
|type|DIMENSION|
|type|ENTITY|
|type|ID|
|type|METRIC|
|type|TAG|
|type|TERM|
|type|VALUE|

<h2 id="tocS_RuleInfo">RuleInfo</h2>

<a id="schemaruleinfo"></a>
<a id="schema_RuleInfo"></a>
<a id="tocSruleinfo"></a>
<a id="tocsruleinfo"></a>

```json
{
  "mode": "BEFORE",
  "parameters": [
    {}
  ]
}

```

RuleInfo

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|mode|string|false|none||none|
|parameters|[object]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|mode|BEFORE|
|mode|EXIST|
|mode|RECENT|

<h2 id="tocS_RelatedSchemaElement">RelatedSchemaElement</h2>

<a id="schemarelatedschemaelement"></a>
<a id="schema_RelatedSchemaElement"></a>
<a id="tocSrelatedschemaelement"></a>
<a id="tocsrelatedschemaelement"></a>

```json
{
  "dimensionId": 0,
  "necessary": true
}

```

RelatedSchemaElement

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dimensionId|integer(int64)|false|none||none|
|necessary|boolean|false|none||none|

<h2 id="tocS_RelateDimension">RelateDimension</h2>

<a id="schemarelatedimension"></a>
<a id="schema_RelateDimension"></a>
<a id="tocSrelatedimension"></a>
<a id="tocsrelatedimension"></a>

```json
{
  "drillDownDimensions": [
    {
      "dimensionId": 0,
      "inheritedFromModel": true,
      "necessary": true
    }
  ]
}

```

RelateDimension

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|

<h2 id="tocS_RecommendedQuestionReq">RecommendedQuestionReq</h2>

<a id="schemarecommendedquestionreq"></a>
<a id="schema_RecommendedQuestionReq"></a>
<a id="tocSrecommendedquestionreq"></a>
<a id="tocsrecommendedquestionreq"></a>

```json
{
  "question": "string"
}

```

RecommendedQuestionReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|question|string|false|none||none|

<h2 id="tocS_QueryStructReq">QueryStructReq</h2>

<a id="schemaquerystructreq"></a>
<a id="schema_QueryStructReq"></a>
<a id="tocSquerystructreq"></a>
<a id="tocsquerystructreq"></a>

```json
{
  "aggregators": [
    {
      "alias": "string",
      "args": [
        "string"
      ],
      "column": "string",
      "func": "AVG",
      "nameCh": "string"
    }
  ],
  "cacheInfo": {
    "cache": true
  },
  "convertToSql": true,
  "dataSetId": 0,
  "dataSetName": "string",
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "dimensionFilters": [
    {
      "bizName": "string",
      "children": [
        {
          "bizName": "string",
          "children": [
            {}
          ],
          "id": 0,
          "name": "string",
          "operator": "!=",
          "relation": "AND",
          "value": {}
        }
      ],
      "id": 0,
      "name": "string",
      "operator": "!=",
      "relation": "AND",
      "value": {}
    }
  ],
  "groups": [
    "string"
  ],
  "innerLayerNative": true,
  "limit": 0,
  "metricFilters": [
    {
      "bizName": "string",
      "children": [
        {
          "bizName": "string",
          "children": [
            {}
          ],
          "id": 0,
          "name": "string",
          "operator": "!=",
          "relation": "AND",
          "value": {}
        }
      ],
      "id": 0,
      "name": "string",
      "operator": "!=",
      "relation": "AND",
      "value": {}
    }
  ],
  "modelIds": [
    0
  ],
  "needAuth": true,
  "orders": [
    {
      "column": "string",
      "direction": "string"
    }
  ],
  "params": [
    {
      "name": "string",
      "value": "string"
    }
  ],
  "queryType": "DETAIL",
  "sqlInfo": {
    "correctS2SQL": "string",
    "querySQL": "string",
    "s2SQL": "string",
    "sourceId": "string"
  }
}

```

QueryStructReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|aggregators|[[Aggregator](#schemaaggregator)]|false|none||none|
|cacheInfo|[Cache](#schemacache)|false|none||none|
|convertToSql|boolean|false|none||none|
|dataSetId|integer(int64)|false|none||none|
|dataSetName|string|false|none||none|
|dateInfo|[DateConf](#schemadateconf)|false|none||none|
|dimensionFilters|[[Filter](#schemafilter)]|false|none||none|
|groups|[string]|false|none||none|
|innerLayerNative|boolean|false|none||none|
|limit|integer(int64)|false|none||none|
|metricFilters|[[Filter](#schemafilter)]|false|none||none|
|modelIds|[integer]|false|none||none|
|needAuth|boolean|false|none||none|
|orders|[[Order](#schemaorder)]|false|none||none|
|params|[[Param](#schemaparam)]|false|none||none|
|queryType|string|false|none||none|
|sqlInfo|[SqlInfo](#schemasqlinfo)|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|queryType|DETAIL|
|queryType|ID|
|queryType|METRIC|

<h2 id="tocS_QuerySqlsReq">QuerySqlsReq</h2>

<a id="schemaquerysqlsreq"></a>
<a id="schema_QuerySqlsReq"></a>
<a id="tocSquerysqlsreq"></a>
<a id="tocsquerysqlsreq"></a>

```json
{
  "cacheInfo": {
    "cache": true
  },
  "dataSetId": 0,
  "dataSetName": "string",
  "innerLayerNative": true,
  "modelIds": [
    0
  ],
  "needAuth": true,
  "params": [
    {
      "name": "string",
      "value": "string"
    }
  ],
  "sqlInfo": {
    "correctS2SQL": "string",
    "querySQL": "string",
    "s2SQL": "string",
    "sourceId": "string"
  },
  "sqls": [
    "string"
  ]
}

```

QuerySqlsReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|cacheInfo|[Cache](#schemacache)|false|none||none|
|dataSetId|integer(int64)|false|none||none|
|dataSetName|string|false|none||none|
|innerLayerNative|boolean|false|none||none|
|modelIds|[integer]|false|none||none|
|needAuth|boolean|false|none||none|
|params|[[Param](#schemaparam)]|false|none||none|
|sqlInfo|[SqlInfo](#schemasqlinfo)|false|none||none|
|sqls|[string]|false|none||none|

<h2 id="tocS_QuerySqlReq">QuerySqlReq</h2>

<a id="schemaquerysqlreq"></a>
<a id="schema_QuerySqlReq"></a>
<a id="tocSquerysqlreq"></a>
<a id="tocsquerysqlreq"></a>

```json
{
  "cacheInfo": {
    "cache": true
  },
  "dataSetId": 0,
  "dataSetName": "string",
  "innerLayerNative": true,
  "limit": 0,
  "modelIds": [
    0
  ],
  "needAuth": true,
  "params": [
    {
      "name": "string",
      "value": "string"
    }
  ],
  "sql": "string",
  "sqlInfo": {
    "correctS2SQL": "string",
    "querySQL": "string",
    "s2SQL": "string",
    "sourceId": "string"
  }
}

```

QuerySqlReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|cacheInfo|[Cache](#schemacache)|false|none||none|
|dataSetId|integer(int64)|false|none||none|
|dataSetName|string|false|none||none|
|innerLayerNative|boolean|false|none||none|
|limit|integer(int32)|false|none||none|
|modelIds|[integer]|false|none||none|
|needAuth|boolean|false|none||none|
|params|[[Param](#schemaparam)]|false|none||none|
|sql|string|false|none||none|
|sqlInfo|[SqlInfo](#schemasqlinfo)|false|none||none|

<h2 id="tocS_QueryRuleResp">QueryRuleResp</h2>

<a id="schemaqueryruleresp"></a>
<a id="schema_QueryRuleResp"></a>
<a id="tocSqueryruleresp"></a>
<a id="tocsqueryruleresp"></a>

```json
{
  "action": {
    "out": [
      {}
    ]
  },
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetId": 0,
  "description": "string",
  "ext": {
    "property1": "string",
    "property2": "string"
  },
  "id": 0,
  "name": "string",
  "priority": 0,
  "rule": {
    "mode": "BEFORE",
    "parameters": [
      {}
    ]
  },
  "ruleType": "ADD_DATE",
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

QueryRuleResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|action|[ActionInfo](#schemaactioninfo)|false|none||none|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dataSetId|integer(int64)|false|none||none|
|description|string|false|none||none|
|ext|object|false|none||none|
|» **additionalProperties**|string|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|priority|integer(int32)|false|none||none|
|rule|[RuleInfo](#schemaruleinfo)|true|none||none|
|ruleType|string|true|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|ruleType|ADD_DATE|
|ruleType|ADD_SELECT|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_QueryRuleReq">QueryRuleReq</h2>

<a id="schemaqueryrulereq"></a>
<a id="schema_QueryRuleReq"></a>
<a id="tocSqueryrulereq"></a>
<a id="tocsqueryrulereq"></a>

```json
{
  "action": {
    "out": [
      {}
    ]
  },
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetId": 0,
  "description": "string",
  "ext": {
    "property1": "string",
    "property2": "string"
  },
  "id": 0,
  "name": "string",
  "priority": 0,
  "rule": {
    "mode": "BEFORE",
    "parameters": [
      {}
    ]
  },
  "ruleType": "ADD_DATE",
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

QueryRuleReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|action|[ActionInfo](#schemaactioninfo)|false|none||none|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dataSetId|integer(int64)|false|none||none|
|description|string|false|none||none|
|ext|object|false|none||none|
|» **additionalProperties**|string|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|priority|integer(int32)|false|none||none|
|rule|[RuleInfo](#schemaruleinfo)|true|none||none|
|ruleType|string|true|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|ruleType|ADD_DATE|
|ruleType|ADD_SELECT|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_QueryRuleFilter">QueryRuleFilter</h2>

<a id="schemaqueryrulefilter"></a>
<a id="schema_QueryRuleFilter"></a>
<a id="tocSqueryrulefilter"></a>
<a id="tocsqueryrulefilter"></a>

```json
{
  "dataSetIds": [
    0
  ],
  "ruleIds": [
    0
  ],
  "statusList": [
    0
  ]
}

```

QueryRuleFilter

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dataSetIds|[integer]|false|none||none|
|ruleIds|[integer]|false|none||none|
|statusList|[integer]|false|none||none|

<h2 id="tocS_QueryResult">QueryResult</h2>

<a id="schemaqueryresult"></a>
<a id="schema_QueryResult"></a>
<a id="tocSqueryresult"></a>
<a id="tocsqueryresult"></a>

```json
{
  "aggregateInfo": {
    "metricInfos": [
      {
        "date": "string",
        "dimension": "string",
        "name": "string",
        "statistics": {
          "property1": "string",
          "property2": "string"
        },
        "value": "string"
      }
    ]
  },
  "chatContext": {
    "aggType": "AVG",
    "dataSet": {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    },
    "dateInfo": {
      "dateList": [
        "string"
      ],
      "dateMode": "ALL",
      "detectWord": "string",
      "endDate": "string",
      "groupByDate": true,
      "inherited": true,
      "period": "string",
      "startDate": "string",
      "unit": 0
    },
    "dimensionFilters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "dimensions": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      }
    ],
    "elementMatches": [
      {
        "detectWord": "string",
        "element": {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        },
        "frequency": 0,
        "inherited": true,
        "similarity": 0,
        "word": "string"
      }
    ],
    "entity": {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    },
    "entityInfo": {
      "dataSetInfo": {
        "bizName": "string",
        "itemId": 0,
        "name": "string",
        "primaryKey": "string",
        "value": "string",
        "words": [
          "string"
        ]
      },
      "dimensions": [
        {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "value": "string"
        }
      ],
      "entityId": "string",
      "metrics": [
        {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "value": "string"
        }
      ]
    },
    "filterType": "AND",
    "id": 0,
    "limit": 0,
    "metricFilters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "metrics": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      }
    ],
    "orders": [
      {
        "column": "string",
        "direction": "string"
      }
    ],
    "properties": {},
    "queryMode": "string",
    "queryType": "DETAIL",
    "score": 0,
    "sqlEvaluation": {
      "isValidated": true,
      "validateMsg": "string"
    },
    "sqlInfo": {
      "correctS2SQL": "string",
      "querySQL": "string",
      "s2SQL": "string",
      "sourceId": "string"
    },
    "textInfo": "string"
  },
  "entityInfo": {
    "dataSetInfo": {
      "bizName": "string",
      "itemId": 0,
      "name": "string",
      "primaryKey": "string",
      "value": "string",
      "words": [
        "string"
      ]
    },
    "dimensions": [
      {
        "bizName": "string",
        "itemId": 0,
        "name": "string",
        "value": "string"
      }
    ],
    "entityId": "string",
    "metrics": [
      {
        "bizName": "string",
        "itemId": 0,
        "name": "string",
        "value": "string"
      }
    ]
  },
  "queryAuthorization": {
    "dimensionFilters": [
      "string"
    ],
    "dimensionFiltersDesc": [
      "string"
    ],
    "domainName": "string",
    "message": "string"
  },
  "queryColumns": [
    {
      "authorized": true,
      "comment": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "name": "string",
      "nameEn": "string",
      "showType": "string",
      "type": "string"
    }
  ],
  "queryId": 0,
  "queryMode": "string",
  "queryResults": [
    {
      "property1": {},
      "property2": {}
    }
  ],
  "querySql": "string",
  "queryState": "EMPTY",
  "queryTimeCost": 0,
  "recommendedDimensions": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "response": {},
  "textResult": "string"
}

```

QueryResult

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|aggregateInfo|[AggregateInfo](#schemaaggregateinfo)|false|none||none|
|chatContext|[SemanticParseInfo](#schemasemanticparseinfo)|false|none||none|
|entityInfo|[EntityInfo](#schemaentityinfo)|false|none||none|
|queryAuthorization|[QueryAuthorization](#schemaqueryauthorization)|false|none||none|
|queryColumns|[[QueryColumn](#schemaquerycolumn)]|false|none||none|
|queryId|integer(int64)|false|none||none|
|queryMode|string|false|none||none|
|queryResults|[object]|false|none||none|
|» **additionalProperties**|object|false|none||none|
|querySql|string|false|none||none|
|queryState|string|false|none||none|
|queryTimeCost|integer(int64)|false|none||none|
|recommendedDimensions|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|response|object|false|none||none|
|textResult|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|queryState|EMPTY|
|queryState|INVALID|
|queryState|SEARCH_EXCEPTION|
|queryState|SUCCESS|

<h2 id="tocS_QueryResp">QueryResp</h2>

<a id="schemaqueryresp"></a>
<a id="schema_QueryResp"></a>
<a id="tocSqueryresp"></a>
<a id="tocsqueryresp"></a>

```json
{
  "chatId": 0,
  "createTime": "2019-08-24T14:15:22Z",
  "feedback": "string",
  "parseInfos": [
    {
      "aggType": "AVG",
      "dataSet": {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      },
      "dateInfo": {
        "dateList": [
          "string"
        ],
        "dateMode": "ALL",
        "detectWord": "string",
        "endDate": "string",
        "groupByDate": true,
        "inherited": true,
        "period": "string",
        "startDate": "string",
        "unit": 0
      },
      "dimensionFilters": [
        {
          "bizName": "string",
          "elementID": 0,
          "function": "string",
          "name": "string",
          "operator": "!=",
          "value": {}
        }
      ],
      "dimensions": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            {}
          ],
          "schemaValueMaps": [
            {}
          ],
          "type": "DATASET",
          "useCnt": 0
        }
      ],
      "elementMatches": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "entity": {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      },
      "entityInfo": {
        "dataSetInfo": {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "primaryKey": "string",
          "value": "string",
          "words": [
            null
          ]
        },
        "dimensions": [
          {
            "bizName": null,
            "itemId": null,
            "name": null,
            "value": null
          }
        ],
        "entityId": "string",
        "metrics": [
          {
            "bizName": null,
            "itemId": null,
            "name": null,
            "value": null
          }
        ]
      },
      "filterType": "AND",
      "id": 0,
      "limit": 0,
      "metricFilters": [
        {
          "bizName": "string",
          "elementID": 0,
          "function": "string",
          "name": "string",
          "operator": "!=",
          "value": {}
        }
      ],
      "metrics": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            {}
          ],
          "schemaValueMaps": [
            {}
          ],
          "type": "DATASET",
          "useCnt": 0
        }
      ],
      "orders": [
        {
          "column": "string",
          "direction": "string"
        }
      ],
      "properties": {},
      "queryMode": "string",
      "queryType": "DETAIL",
      "score": 0,
      "sqlEvaluation": {
        "isValidated": true,
        "validateMsg": "string"
      },
      "sqlInfo": {
        "correctS2SQL": "string",
        "querySQL": "string",
        "s2SQL": "string",
        "sourceId": "string"
      },
      "textInfo": "string"
    }
  ],
  "parseTimeCost": {
    "parseStartTime": 0,
    "parseTime": 0,
    "sqlTime": 0
  },
  "queryResult": {
    "aggregateInfo": {
      "metricInfos": [
        {
          "date": "string",
          "dimension": "string",
          "name": "string",
          "statistics": {},
          "value": "string"
        }
      ]
    },
    "chatContext": {
      "aggType": "AVG",
      "dataSet": {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {}
        ],
        "schemaValueMaps": [
          {}
        ],
        "type": "DATASET",
        "useCnt": 0
      },
      "dateInfo": {
        "dateList": [
          "string"
        ],
        "dateMode": "ALL",
        "detectWord": "string",
        "endDate": "string",
        "groupByDate": true,
        "inherited": true,
        "period": "string",
        "startDate": "string",
        "unit": 0
      },
      "dimensionFilters": [
        {
          "bizName": "string",
          "elementID": 0,
          "function": "string",
          "name": "string",
          "operator": "[",
          "value": {}
        }
      ],
      "dimensions": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "elementMatches": [
        {
          "detectWord": "string",
          "element": {},
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "entity": {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {}
        ],
        "schemaValueMaps": [
          {}
        ],
        "type": "DATASET",
        "useCnt": 0
      },
      "entityInfo": {
        "dataSetInfo": {
          "bizName": null,
          "itemId": null,
          "name": null,
          "primaryKey": null,
          "value": null,
          "words": null
        },
        "dimensions": [
          {}
        ],
        "entityId": "string",
        "metrics": [
          {}
        ]
      },
      "filterType": "AND",
      "id": 0,
      "limit": 0,
      "metricFilters": [
        {
          "bizName": "string",
          "elementID": 0,
          "function": "string",
          "name": "string",
          "operator": "[",
          "value": {}
        }
      ],
      "metrics": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "orders": [
        {
          "column": "string",
          "direction": "string"
        }
      ],
      "properties": {},
      "queryMode": "string",
      "queryType": "DETAIL",
      "score": 0,
      "sqlEvaluation": {
        "isValidated": true,
        "validateMsg": "string"
      },
      "sqlInfo": {
        "correctS2SQL": "string",
        "querySQL": "string",
        "s2SQL": "string",
        "sourceId": "string"
      },
      "textInfo": "string"
    },
    "entityInfo": {
      "dataSetInfo": {
        "bizName": "string",
        "itemId": 0,
        "name": "string",
        "primaryKey": "string",
        "value": "string",
        "words": [
          "string"
        ]
      },
      "dimensions": [
        {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "value": "string"
        }
      ],
      "entityId": "string",
      "metrics": [
        {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "value": "string"
        }
      ]
    },
    "queryAuthorization": {
      "dimensionFilters": [
        "string"
      ],
      "dimensionFiltersDesc": [
        "string"
      ],
      "domainName": "string",
      "message": "string"
    },
    "queryColumns": [
      {
        "authorized": true,
        "comment": "string",
        "dataFormat": {
          "decimalPlaces": 0,
          "needMultiply100": true
        },
        "dataFormatType": "string",
        "name": "string",
        "nameEn": "string",
        "showType": "string",
        "type": "string"
      }
    ],
    "queryId": 0,
    "queryMode": "string",
    "queryResults": [
      {
        "property1": {},
        "property2": {}
      }
    ],
    "querySql": "string",
    "queryState": "EMPTY",
    "queryTimeCost": 0,
    "recommendedDimensions": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      }
    ],
    "response": {},
    "textResult": "string"
  },
  "queryText": "string",
  "questionId": 0,
  "score": 0,
  "similarQueries": [
    {
      "queryId": 0,
      "queryText": "string"
    }
  ]
}

```

QueryResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|chatId|integer(int64)|false|none||none|
|createTime|string(date-time)|false|none||none|
|feedback|string|false|none||none|
|parseInfos|[[SemanticParseInfo](#schemasemanticparseinfo)]|false|none||none|
|parseTimeCost|[ParseTimeCostResp](#schemaparsetimecostresp)|false|none||none|
|queryResult|[QueryResult](#schemaqueryresult)|false|none||none|
|queryText|string|false|none||none|
|questionId|integer(int64)|false|none||none|
|score|integer(int32)|false|none||none|
|similarQueries|[[SimilarQueryRecallResp](#schemasimilarqueryrecallresp)]|false|none||none|

<h2 id="tocS_QueryReq">QueryReq</h2>

<a id="schemaqueryreq"></a>
<a id="schema_QueryReq"></a>
<a id="tocSqueryreq"></a>
<a id="tocsqueryreq"></a>

```json
{
  "chatId": 0,
  "dataSetIds": [
    0
  ],
  "exemplars": [
    {
      "dbSchema": "string",
      "question": "string",
      "sql": "string"
    }
  ],
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    }
  },
  "mapModeEnum": "LOOSE",
  "queryDataType": "ALL",
  "queryFilters": {
    "filters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "params": {}
  },
  "queryText": "string",
  "saveAnswer": true,
  "text2SQLType": "ONLY_LLM",
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}

```

QueryReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|chatId|integer(int32)|false|none||none|
|dataSetIds|[integer]|false|none||none|
|exemplars|[[SqlExemplar](#schemasqlexemplar)]|false|none||none|
|llmConfig|[LLMConfig](#schemallmconfig)|false|none||none|
|mapInfo|[SchemaMapInfo](#schemaschemamapinfo)|false|none||none|
|mapModeEnum|string|false|none||none|
|queryDataType|string|false|none||none|
|queryFilters|[QueryFilters](#schemaqueryfilters)|false|none||none|
|queryText|string|false|none||none|
|saveAnswer|boolean|false|none||none|
|text2SQLType|string|false|none||none|
|user|[User](#schemauser)|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|mapModeEnum|LOOSE|
|mapModeEnum|MODERATE|
|mapModeEnum|STRICT|
|queryDataType|ALL|
|queryDataType|DIMENSION|
|queryDataType|METRIC|
|queryDataType|TAG|
|text2SQLType|ONLY_LLM|
|text2SQLType|ONLY_RULE|
|text2SQLType|RULE_AND_LLM|

<h2 id="tocS_QueryMetricReq">QueryMetricReq</h2>

<a id="schemaquerymetricreq"></a>
<a id="schema_QueryMetricReq"></a>
<a id="tocSquerymetricreq"></a>
<a id="tocsquerymetricreq"></a>

```json
{
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "dimensionIds": [
    0
  ],
  "dimensionNames": [
    "string"
  ],
  "domainId": 0,
  "filters": [
    {
      "bizName": "string",
      "children": [
        {
          "bizName": "string",
          "children": [
            {}
          ],
          "id": 0,
          "name": "string",
          "operator": "!=",
          "relation": "AND",
          "value": {}
        }
      ],
      "id": 0,
      "name": "string",
      "operator": "!=",
      "relation": "AND",
      "value": {}
    }
  ],
  "innerLayerNative": true,
  "limit": 0,
  "metricIds": [
    0
  ],
  "metricNames": [
    "string"
  ]
}

```

QueryMetricReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dateInfo|[DateConf](#schemadateconf)|false|none||none|
|dimensionIds|[integer]|false|none||none|
|dimensionNames|[string]|false|none||none|
|domainId|integer(int64)|false|none||none|
|filters|[[Filter](#schemafilter)]|false|none||none|
|innerLayerNative|boolean|false|none||none|
|limit|integer(int64)|false|none||none|
|metricIds|[integer]|false|none||none|
|metricNames|[string]|false|none||none|

<h2 id="tocS_QueryMapReq">QueryMapReq</h2>

<a id="schemaquerymapreq"></a>
<a id="schema_QueryMapReq"></a>
<a id="tocSquerymapreq"></a>
<a id="tocsquerymapreq"></a>

```json
{
  "dataSetNames": [
    "string"
  ],
  "mapModeEnum": "LOOSE",
  "queryDataType": "ALL",
  "queryText": "string",
  "topN": 0,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}

```

QueryMapReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dataSetNames|[string]|false|none||none|
|mapModeEnum|string|false|none||none|
|queryDataType|string|false|none||none|
|queryText|string|false|none||none|
|topN|integer(int32)|false|none||none|
|user|[User](#schemauser)|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|mapModeEnum|LOOSE|
|mapModeEnum|MODERATE|
|mapModeEnum|STRICT|
|queryDataType|ALL|
|queryDataType|DIMENSION|
|queryDataType|METRIC|
|queryDataType|TAG|

<h2 id="tocS_QueryFilters">QueryFilters</h2>

<a id="schemaqueryfilters"></a>
<a id="schema_QueryFilters"></a>
<a id="tocSqueryfilters"></a>
<a id="tocsqueryfilters"></a>

```json
{
  "filters": [
    {
      "bizName": "string",
      "elementID": 0,
      "function": "string",
      "name": "string",
      "operator": "!=",
      "value": {}
    }
  ],
  "params": {}
}

```

QueryFilters

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|filters|[[QueryFilter](#schemaqueryfilter)]|false|none||none|
|params|object|false|none||none|

<h2 id="tocS_QueryFilter">QueryFilter</h2>

<a id="schemaqueryfilter"></a>
<a id="schema_QueryFilter"></a>
<a id="tocSqueryfilter"></a>
<a id="tocsqueryfilter"></a>

```json
{
  "bizName": "string",
  "elementID": 0,
  "function": "string",
  "name": "string",
  "operator": "!=",
  "value": {}
}

```

QueryFilter

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|elementID|integer(int64)|false|none||none|
|function|string|false|none||none|
|name|string|false|none||none|
|operator|string|false|none||none|
|value|object|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|operator|!=|
|operator|<|
|operator|<=|
|operator|=|
|operator|>|
|operator|>=|
|operator|BETWEEN|
|operator|EXISTS|
|operator|IN|
|operator|IS_NOT_NULL|
|operator|IS_NULL|
|operator|LIKE|
|operator|NOT_IN|
|operator|SQL_PART|

<h2 id="tocS_QueryDimValueReq">QueryDimValueReq</h2>

<a id="schemaquerydimvaluereq"></a>
<a id="schema_QueryDimValueReq"></a>
<a id="tocSquerydimvaluereq"></a>
<a id="tocsquerydimvaluereq"></a>

```json
{
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "dimensionBizName": "string",
  "modelId": 0,
  "value": "string"
}

```

QueryDimValueReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dateInfo|[DateConf](#schemadateconf)|false|none||none|
|dimensionBizName|string|false|none||none|
|modelId|integer(int64)|false|none||none|
|value|string|false|none||none|

<h2 id="tocS_QueryDataSetReq">QueryDataSetReq</h2>

<a id="schemaquerydatasetreq"></a>
<a id="schema_QueryDataSetReq"></a>
<a id="tocSquerydatasetreq"></a>
<a id="tocsquerydatasetreq"></a>

```json
{
  "aggregators": [
    {
      "alias": "string",
      "args": [
        "string"
      ],
      "column": "string",
      "func": "AVG",
      "nameCh": "string"
    }
  ],
  "cacheInfo": {
    "cache": true
  },
  "dataSetId": 0,
  "dataSetName": "string",
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "dimensionFilters": [
    {
      "bizName": "string",
      "children": [
        {
          "bizName": "string",
          "children": [
            {}
          ],
          "id": 0,
          "name": "string",
          "operator": "!=",
          "relation": "AND",
          "value": {}
        }
      ],
      "id": 0,
      "name": "string",
      "operator": "!=",
      "relation": "AND",
      "value": {}
    }
  ],
  "groups": [
    "string"
  ],
  "innerLayerNative": true,
  "limit": 0,
  "metricFilters": [
    {
      "bizName": "string",
      "children": [
        {
          "bizName": "string",
          "children": [
            {}
          ],
          "id": 0,
          "name": "string",
          "operator": "!=",
          "relation": "AND",
          "value": {}
        }
      ],
      "id": 0,
      "name": "string",
      "operator": "!=",
      "relation": "AND",
      "value": {}
    }
  ],
  "needAuth": true,
  "orders": [
    {
      "column": "string",
      "direction": "string"
    }
  ],
  "params": [
    {
      "name": "string",
      "value": "string"
    }
  ],
  "queryType": "DETAIL",
  "sql": "string"
}

```

QueryDataSetReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|aggregators|[[Aggregator](#schemaaggregator)]|false|none||none|
|cacheInfo|[Cache](#schemacache)|false|none||none|
|dataSetId|integer(int64)|false|none||none|
|dataSetName|string|false|none||none|
|dateInfo|[DateConf](#schemadateconf)|false|none||none|
|dimensionFilters|[[Filter](#schemafilter)]|false|none||none|
|groups|[string]|false|none||none|
|innerLayerNative|boolean|false|none||none|
|limit|integer(int64)|false|none||none|
|metricFilters|[[Filter](#schemafilter)]|false|none||none|
|needAuth|boolean|false|none||none|
|orders|[[Order](#schemaorder)]|false|none||none|
|params|[[Param](#schemaparam)]|false|none||none|
|queryType|string|false|none||none|
|sql|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|queryType|DETAIL|
|queryType|ID|
|queryType|METRIC|

<h2 id="tocS_QueryConfig">QueryConfig</h2>

<a id="schemaqueryconfig"></a>
<a id="schema_QueryConfig"></a>
<a id="tocSqueryconfig"></a>
<a id="tocsqueryconfig"></a>

```json
{
  "metricTypeDefaultConfig": {
    "timeDefaultConfig": {
      "period": "string",
      "timeMode": "LAST",
      "unit": 0
    }
  },
  "tagTypeDefaultConfig": {
    "defaultDisplayInfo": {
      "dimensionIds": [
        0
      ],
      "metricIds": [
        0
      ]
    },
    "timeDefaultConfig": {
      "period": "string",
      "timeMode": "LAST",
      "unit": 0
    }
  }
}

```

QueryConfig

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|metricTypeDefaultConfig|[MetricTypeDefaultConfig](#schemametrictypedefaultconfig)|false|none||none|
|tagTypeDefaultConfig|[TagTypeDefaultConfig](#schematagtypedefaultconfig)|false|none||none|

<h2 id="tocS_QueryColumn">QueryColumn</h2>

<a id="schemaquerycolumn"></a>
<a id="schema_QueryColumn"></a>
<a id="tocSquerycolumn"></a>
<a id="tocsquerycolumn"></a>

```json
{
  "authorized": true,
  "comment": "string",
  "dataFormat": {
    "decimalPlaces": 0,
    "needMultiply100": true
  },
  "dataFormatType": "string",
  "name": "string",
  "nameEn": "string",
  "showType": "string",
  "type": "string"
}

```

QueryColumn

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|authorized|boolean|false|none||none|
|comment|string|false|none||none|
|dataFormat|[DataFormat](#schemadataformat)|false|none||none|
|dataFormatType|string|false|none||none|
|name|string|false|none||none|
|nameEn|string|false|none||none|
|showType|string|false|none||none|
|type|string|false|none||none|

<h2 id="tocS_QueryAuthorization">QueryAuthorization</h2>

<a id="schemaqueryauthorization"></a>
<a id="schema_QueryAuthorization"></a>
<a id="tocSqueryauthorization"></a>
<a id="tocsqueryauthorization"></a>

```json
{
  "dimensionFilters": [
    "string"
  ],
  "dimensionFiltersDesc": [
    "string"
  ],
  "domainName": "string",
  "message": "string"
}

```

QueryAuthorization

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dimensionFilters|[string]|false|none||none|
|dimensionFiltersDesc|[string]|false|none||none|
|domainName|string|false|none||none|
|message|string|false|none||none|

<h2 id="tocS_QueryAuthResReq">QueryAuthResReq</h2>

<a id="schemaqueryauthresreq"></a>
<a id="schema_QueryAuthResReq"></a>
<a id="tocSqueryauthresreq"></a>
<a id="tocsqueryauthresreq"></a>

```json
{
  "departmentIds": [
    "string"
  ],
  "modelId": 0,
  "modelIds": [
    0
  ],
  "resources": [
    {
      "modelId": 0,
      "name": "string"
    }
  ]
}

```

QueryAuthResReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|departmentIds|[string]|false|none||none|
|modelId|integer(int64)|false|none||none|
|modelIds|[integer]|false|none||none|
|resources|[[AuthRes](#schemaauthres)]|false|none||none|

<h2 id="tocS_PluginQueryReq">PluginQueryReq</h2>

<a id="schemapluginqueryreq"></a>
<a id="schema_PluginQueryReq"></a>
<a id="tocSpluginqueryreq"></a>
<a id="tocspluginqueryreq"></a>

```json
{
  "createdBy": "string",
  "dataSet": "string",
  "name": "string",
  "parseMode": "string",
  "pattern": "string",
  "type": "string"
}

```

PluginQueryReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|createdBy|string|false|none||none|
|dataSet|string|false|none||none|
|name|string|false|none||none|
|parseMode|string|false|none||none|
|pattern|string|false|none||none|
|type|string|false|none||none|

<h2 id="tocS_ParseTimeCostResp">ParseTimeCostResp</h2>

<a id="schemaparsetimecostresp"></a>
<a id="schema_ParseTimeCostResp"></a>
<a id="tocSparsetimecostresp"></a>
<a id="tocsparsetimecostresp"></a>

```json
{
  "parseStartTime": 0,
  "parseTime": 0,
  "sqlTime": 0
}

```

ParseTimeCostResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|parseStartTime|integer(int64)|false|none||none|
|parseTime|integer(int64)|false|none||none|
|sqlTime|integer(int64)|false|none||none|

<h2 id="tocS_Parameter">Parameter</h2>

<a id="schemaparameter"></a>
<a id="schema_Parameter"></a>
<a id="tocSparameter"></a>
<a id="tocsparameter"></a>

```json
{
  "candidateValues": [
    {}
  ],
  "comment": "string",
  "dataType": "string",
  "defaultValue": "string",
  "description": "string",
  "module": "string",
  "name": "string",
  "value": "string"
}

```

Parameter

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|candidateValues|[object]|false|none||none|
|comment|string|false|none||none|
|dataType|string|false|none||none|
|defaultValue|string|false|none||none|
|description|string|false|none||none|
|module|string|false|none||none|
|name|string|false|none||none|
|value|string|false|none||none|

<h2 id="tocS_Param">Param</h2>

<a id="schemaparam"></a>
<a id="schema_Param"></a>
<a id="tocSparam"></a>
<a id="tocsparam"></a>

```json
{
  "name": "string",
  "value": "string"
}

```

Param

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|name|string|true|none||none|
|value|string|true|none||none|

<h2 id="tocS_PageQueryInfoReq">PageQueryInfoReq</h2>

<a id="schemapagequeryinforeq"></a>
<a id="schema_PageQueryInfoReq"></a>
<a id="tocSpagequeryinforeq"></a>
<a id="tocspagequeryinforeq"></a>

```json
{
  "current": 0,
  "ids": [
    0
  ],
  "pageSize": 0,
  "userName": "string"
}

```

PageQueryInfoReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|current|integer(int32)|false|none||none|
|ids|[integer]|false|none||none|
|pageSize|integer(int32)|false|none||none|
|userName|string|false|none||none|

<h2 id="tocS_PageMetricReq">PageMetricReq</h2>

<a id="schemapagemetricreq"></a>
<a id="schema_PageMetricReq"></a>
<a id="tocSpagemetricreq"></a>
<a id="tocspagemetricreq"></a>

```json
{
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdBy": "string",
  "current": 0,
  "domainIds": [
    0
  ],
  "hasCollect": true,
  "id": "string",
  "ids": [
    0
  ],
  "isPublish": 0,
  "isTag": 0,
  "key": "string",
  "modelIds": [
    0
  ],
  "name": "string",
  "orderCondition": "string",
  "pageSize": 0,
  "sensitiveLevel": 0,
  "sort": "string",
  "status": 0,
  "type": "string"
}

```

PageMetricReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|classifications|[string]|false|none||none|
|createdBy|string|false|none||none|
|current|integer(int32)|false|none||none|
|domainIds|[integer]|false|none||none|
|hasCollect|boolean|false|none||none|
|id|string|false|none||none|
|ids|[integer]|false|none||none|
|isPublish|integer(int32)|false|none||none|
|isTag|integer(int32)|false|none||none|
|key|string|false|none||none|
|modelIds|[integer]|false|none||none|
|name|string|false|none||none|
|orderCondition|string|false|none||none|
|pageSize|integer(int32)|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|sort|string|false|none||none|
|status|integer(int32)|false|none||none|
|type|string|false|none||none|

<h2 id="tocS_PageMemoryReq">PageMemoryReq</h2>

<a id="schemapagememoryreq"></a>
<a id="schema_PageMemoryReq"></a>
<a id="tocSpagememoryreq"></a>
<a id="tocspagememoryreq"></a>

```json
{
  "chatMemoryFilter": {
    "agentId": 0,
    "humanReviewRet": "NEGATIVE",
    "llmReviewRet": "NEGATIVE",
    "question": "string",
    "questions": [
      "string"
    ],
    "status": "DISABLED"
  },
  "current": 0,
  "orderCondition": "string",
  "pageSize": 0,
  "sort": "string"
}

```

PageMemoryReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|chatMemoryFilter|[ChatMemoryFilter](#schemachatmemoryfilter)|false|none||none|
|current|integer(int32)|false|none||none|
|orderCondition|string|false|none||none|
|pageSize|integer(int32)|false|none||none|
|sort|string|false|none||none|

<h2 id="tocS_PageInfo«TagResp»">PageInfo«TagResp»</h2>

<a id="schemapageinfo«tagresp»"></a>
<a id="schema_PageInfo«TagResp»"></a>
<a id="tocSpageinfo«tagresp»"></a>
<a id="tocspageinfo«tagresp»"></a>

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "bizName": "string",
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "description": "string",
      "domainId": 0,
      "domainName": "string",
      "ext": {},
      "hasAdminRes": true,
      "id": 0,
      "isCollect": true,
      "itemId": 0,
      "modelId": 0,
      "modelName": "string",
      "name": "string",
      "sensitiveLevel": 0,
      "tagDefineType": "string",
      "tagObjectId": 0,
      "tagObjectName": "string",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}

```

PageInfo«TagResp»

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|endRow|integer(int64)|false|none||none|
|hasNextPage|boolean|false|none||none|
|hasPreviousPage|boolean|false|none||none|
|isFirstPage|boolean|false|none||none|
|isLastPage|boolean|false|none||none|
|list|[[TagResp](#schematagresp)]|false|none||none|
|navigateFirstPage|integer(int32)|false|none||none|
|navigateLastPage|integer(int32)|false|none||none|
|navigatePages|integer(int32)|false|none||none|
|navigatepageNums|[integer]|false|none||none|
|nextPage|integer(int32)|false|none||none|
|pageNum|integer(int32)|false|none||none|
|pageSize|integer(int32)|false|none||none|
|pages|integer(int32)|false|none||none|
|prePage|integer(int32)|false|none||none|
|size|integer(int32)|false|none||none|
|startRow|integer(int64)|false|none||none|
|total|integer(int64)|false|none||none|

<h2 id="tocS_PageInfo«QueryResp»">PageInfo«QueryResp»</h2>

<a id="schemapageinfo«queryresp»"></a>
<a id="schema_PageInfo«QueryResp»"></a>
<a id="tocSpageinfo«queryresp»"></a>
<a id="tocspageinfo«queryresp»"></a>

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "chatId": 0,
      "createTime": "2019-08-24T14:15:22Z",
      "feedback": "string",
      "parseInfos": [
        {
          "aggType": "AVG",
          "dataSet": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "dateInfo": {
            "dateList": null,
            "dateMode": null,
            "detectWord": null,
            "endDate": null,
            "groupByDate": null,
            "inherited": null,
            "period": null,
            "startDate": null,
            "unit": null
          },
          "dimensionFilters": [
            {}
          ],
          "dimensions": [
            {}
          ],
          "elementMatches": [
            {}
          ],
          "entity": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "entityInfo": {
            "dataSetInfo": null,
            "dimensions": null,
            "entityId": null,
            "metrics": null
          },
          "filterType": "AND",
          "id": 0,
          "limit": 0,
          "metricFilters": [
            {}
          ],
          "metrics": [
            {}
          ],
          "orders": [
            {}
          ],
          "properties": {},
          "queryMode": "string",
          "queryType": "DETAIL",
          "score": 0,
          "sqlEvaluation": {
            "isValidated": null,
            "validateMsg": null
          },
          "sqlInfo": {
            "correctS2SQL": null,
            "querySQL": null,
            "s2SQL": null,
            "sourceId": null
          },
          "textInfo": "string"
        }
      ],
      "parseTimeCost": {
        "parseStartTime": 0,
        "parseTime": 0,
        "sqlTime": 0
      },
      "queryResult": {
        "aggregateInfo": {
          "metricInfos": [
            null
          ]
        },
        "chatContext": {
          "aggType": "[",
          "dataSet": {},
          "dateInfo": {},
          "dimensionFilters": [
            null
          ],
          "dimensions": [
            null
          ],
          "elementMatches": [
            null
          ],
          "entity": {},
          "entityInfo": {},
          "filterType": "[",
          "id": 0,
          "limit": 0,
          "metricFilters": [
            null
          ],
          "metrics": [
            null
          ],
          "orders": [
            null
          ],
          "properties": {},
          "queryMode": "string",
          "queryType": "[",
          "score": 0,
          "sqlEvaluation": {},
          "sqlInfo": {},
          "textInfo": "string"
        },
        "entityInfo": {
          "dataSetInfo": {},
          "dimensions": [
            null
          ],
          "entityId": "string",
          "metrics": [
            null
          ]
        },
        "queryAuthorization": {
          "dimensionFilters": [
            null
          ],
          "dimensionFiltersDesc": [
            null
          ],
          "domainName": "string",
          "message": "string"
        },
        "queryColumns": [
          {
            "authorized": null,
            "comment": null,
            "dataFormat": null,
            "dataFormatType": null,
            "name": null,
            "nameEn": null,
            "showType": null,
            "type": null
          }
        ],
        "queryId": 0,
        "queryMode": "string",
        "queryResults": [
          {
            "property1": {},
            "property2": {}
          }
        ],
        "querySql": "string",
        "queryState": "EMPTY",
        "queryTimeCost": 0,
        "recommendedDimensions": [
          {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          }
        ],
        "response": {},
        "textResult": "string"
      },
      "queryText": "string",
      "questionId": 0,
      "score": 0,
      "similarQueries": [
        {
          "queryId": 0,
          "queryText": "string"
        }
      ]
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}

```

PageInfo«QueryResp»

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|endRow|integer(int64)|false|none||none|
|hasNextPage|boolean|false|none||none|
|hasPreviousPage|boolean|false|none||none|
|isFirstPage|boolean|false|none||none|
|isLastPage|boolean|false|none||none|
|list|[[QueryResp](#schemaqueryresp)]|false|none||none|
|navigateFirstPage|integer(int32)|false|none||none|
|navigateLastPage|integer(int32)|false|none||none|
|navigatePages|integer(int32)|false|none||none|
|navigatepageNums|[integer]|false|none||none|
|nextPage|integer(int32)|false|none||none|
|pageNum|integer(int32)|false|none||none|
|pageSize|integer(int32)|false|none||none|
|pages|integer(int32)|false|none||none|
|prePage|integer(int32)|false|none||none|
|size|integer(int32)|false|none||none|
|startRow|integer(int64)|false|none||none|
|total|integer(int64)|false|none||none|

<h2 id="tocS_PageInfo«MetricResp»">PageInfo«MetricResp»</h2>

<a id="schemapageinfo«metricresp»"></a>
<a id="schema_PageInfo«MetricResp»"></a>
<a id="tocSpageinfo«metricresp»"></a>
<a id="tocspageinfo«metricresp»"></a>

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "alias": "string",
      "bizName": "string",
      "classifications": [
        "string"
      ],
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "defaultAgg": "string",
      "description": "string",
      "domainId": 0,
      "drillDownDimensions": [
        {
          "dimensionId": 0,
          "inheritedFromModel": true,
          "necessary": true
        }
      ],
      "expr": "string",
      "ext": {},
      "hasAdminRes": true,
      "id": 0,
      "isCollect": true,
      "isPublish": 0,
      "isTag": 0,
      "metricDefineByFieldParams": {
        "expr": "string",
        "fields": [
          {
            "fieldName": null
          }
        ],
        "filterSql": "string"
      },
      "metricDefineByMeasureParams": {
        "expr": "string",
        "filterSql": "string",
        "measures": [
          {
            "agg": null,
            "bizName": null,
            "constraint": null
          }
        ]
      },
      "metricDefineByMetricParams": {
        "expr": "string",
        "filterSql": "string",
        "metrics": [
          {
            "bizName": null,
            "id": null
          }
        ]
      },
      "metricDefineType": "FIELD",
      "modelBizName": "string",
      "modelId": 0,
      "modelName": "string",
      "name": "string",
      "relaDimensionIdKey": "string",
      "relateDimension": {
        "drillDownDimensions": [
          {
            "dimensionId": null,
            "inheritedFromModel": null,
            "necessary": null
          }
        ]
      },
      "sensitiveLevel": 0,
      "similarity": 0,
      "status": 0,
      "type": "string",
      "typeEnum": "DATASET",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}

```

PageInfo«MetricResp»

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|endRow|integer(int64)|false|none||none|
|hasNextPage|boolean|false|none||none|
|hasPreviousPage|boolean|false|none||none|
|isFirstPage|boolean|false|none||none|
|isLastPage|boolean|false|none||none|
|list|[[MetricResp](#schemametricresp)]|false|none||none|
|navigateFirstPage|integer(int32)|false|none||none|
|navigateLastPage|integer(int32)|false|none||none|
|navigatePages|integer(int32)|false|none||none|
|navigatepageNums|[integer]|false|none||none|
|nextPage|integer(int32)|false|none||none|
|pageNum|integer(int32)|false|none||none|
|pageSize|integer(int32)|false|none||none|
|pages|integer(int32)|false|none||none|
|prePage|integer(int32)|false|none||none|
|size|integer(int32)|false|none||none|
|startRow|integer(int64)|false|none||none|
|total|integer(int64)|false|none||none|

<h2 id="tocS_PageInfo«DimensionResp»">PageInfo«DimensionResp»</h2>

<a id="schemapageinfo«dimensionresp»"></a>
<a id="schema_PageInfo«DimensionResp»"></a>
<a id="tocSpageinfo«dimensionresp»"></a>
<a id="tocspageinfo«dimensionresp»"></a>

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "alias": "string",
      "bizName": "string",
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dataType": "ARRAY",
      "defaultValues": [
        "string"
      ],
      "description": "string",
      "dimValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "expr": "string",
      "ext": {},
      "id": 0,
      "isTag": 0,
      "modelBizName": "string",
      "modelFilterSql": "string",
      "modelId": 0,
      "modelName": "string",
      "name": "string",
      "semanticType": "string",
      "sensitiveLevel": 0,
      "status": 0,
      "type": "string",
      "typeEnum": "DATASET",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}

```

PageInfo«DimensionResp»

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|endRow|integer(int64)|false|none||none|
|hasNextPage|boolean|false|none||none|
|hasPreviousPage|boolean|false|none||none|
|isFirstPage|boolean|false|none||none|
|isLastPage|boolean|false|none||none|
|list|[[DimensionResp](#schemadimensionresp)]|false|none||none|
|navigateFirstPage|integer(int32)|false|none||none|
|navigateLastPage|integer(int32)|false|none||none|
|navigatePages|integer(int32)|false|none||none|
|navigatepageNums|[integer]|false|none||none|
|nextPage|integer(int32)|false|none||none|
|pageNum|integer(int32)|false|none||none|
|pageSize|integer(int32)|false|none||none|
|pages|integer(int32)|false|none||none|
|prePage|integer(int32)|false|none||none|
|size|integer(int32)|false|none||none|
|startRow|integer(int64)|false|none||none|
|total|integer(int64)|false|none||none|

<h2 id="tocS_PageInfo«DictValueResp»">PageInfo«DictValueResp»</h2>

<a id="schemapageinfo«dictvalueresp»"></a>
<a id="schema_PageInfo«DictValueResp»"></a>
<a id="tocSpageinfo«dictvalueresp»"></a>
<a id="tocspageinfo«dictvalueresp»"></a>

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "frequency": 0,
      "nature": "string",
      "value": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}

```

PageInfo«DictValueResp»

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|endRow|integer(int64)|false|none||none|
|hasNextPage|boolean|false|none||none|
|hasPreviousPage|boolean|false|none||none|
|isFirstPage|boolean|false|none||none|
|isLastPage|boolean|false|none||none|
|list|[[DictValueResp](#schemadictvalueresp)]|false|none||none|
|navigateFirstPage|integer(int32)|false|none||none|
|navigateLastPage|integer(int32)|false|none||none|
|navigatePages|integer(int32)|false|none||none|
|navigatepageNums|[integer]|false|none||none|
|nextPage|integer(int32)|false|none||none|
|pageNum|integer(int32)|false|none||none|
|pageSize|integer(int32)|false|none||none|
|pages|integer(int32)|false|none||none|
|prePage|integer(int32)|false|none||none|
|size|integer(int32)|false|none||none|
|startRow|integer(int64)|false|none||none|
|total|integer(int64)|false|none||none|

<h2 id="tocS_PageInfo«ChatMemoryDO»">PageInfo«ChatMemoryDO»</h2>

<a id="schemapageinfo«chatmemorydo»"></a>
<a id="schema_PageInfo«ChatMemoryDO»"></a>
<a id="tocSpageinfo«chatmemorydo»"></a>
<a id="tocspageinfo«chatmemorydo»"></a>

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "agentId": 0,
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dbSchema": "string",
      "humanReviewCmt": "string",
      "humanReviewRet": "NEGATIVE",
      "id": 0,
      "llmReviewCmt": "string",
      "llmReviewRet": "NEGATIVE",
      "question": "string",
      "s2sql": "string",
      "status": "DISABLED",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}

```

PageInfo«ChatMemoryDO»

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|endRow|integer(int64)|false|none||none|
|hasNextPage|boolean|false|none||none|
|hasPreviousPage|boolean|false|none||none|
|isFirstPage|boolean|false|none||none|
|isLastPage|boolean|false|none||none|
|list|[[ChatMemoryDO](#schemachatmemorydo)]|false|none||none|
|navigateFirstPage|integer(int32)|false|none||none|
|navigateLastPage|integer(int32)|false|none||none|
|navigatePages|integer(int32)|false|none||none|
|navigatepageNums|[integer]|false|none||none|
|nextPage|integer(int32)|false|none||none|
|pageNum|integer(int32)|false|none||none|
|pageSize|integer(int32)|false|none||none|
|pages|integer(int32)|false|none||none|
|prePage|integer(int32)|false|none||none|
|size|integer(int32)|false|none||none|
|startRow|integer(int64)|false|none||none|
|total|integer(int64)|false|none||none|

<h2 id="tocS_PageInfo«AppResp»">PageInfo«AppResp»</h2>

<a id="schemapageinfo«appresp»"></a>
<a id="schema_PageInfo«AppResp»"></a>
<a id="tocSpageinfo«appresp»"></a>
<a id="tocspageinfo«appresp»"></a>

```json
{
  "endRow": 0,
  "hasNextPage": true,
  "hasPreviousPage": true,
  "isFirstPage": true,
  "isLastPage": true,
  "list": [
    {
      "appStatus": "DELETED",
      "config": {
        "items": [
          {
            "bizName": null,
            "createdBy": null,
            "id": null,
            "name": null,
            "relateItems": null,
            "type": null,
            "value": null
          }
        ]
      },
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "description": "string",
      "endDate": "2019-08-24T14:15:22Z",
      "hasAdminRes": true,
      "id": 0,
      "name": "string",
      "owners": [
        "string"
      ],
      "qps": 0,
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "navigateFirstPage": 0,
  "navigateLastPage": 0,
  "navigatePages": 0,
  "navigatepageNums": [
    0
  ],
  "nextPage": 0,
  "pageNum": 0,
  "pageSize": 0,
  "pages": 0,
  "prePage": 0,
  "size": 0,
  "startRow": 0,
  "total": 0
}

```

PageInfo«AppResp»

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|endRow|integer(int64)|false|none||none|
|hasNextPage|boolean|false|none||none|
|hasPreviousPage|boolean|false|none||none|
|isFirstPage|boolean|false|none||none|
|isLastPage|boolean|false|none||none|
|list|[[AppResp](#schemaappresp)]|false|none||none|
|navigateFirstPage|integer(int32)|false|none||none|
|navigateLastPage|integer(int32)|false|none||none|
|navigatePages|integer(int32)|false|none||none|
|navigatepageNums|[integer]|false|none||none|
|nextPage|integer(int32)|false|none||none|
|pageNum|integer(int32)|false|none||none|
|pageSize|integer(int32)|false|none||none|
|pages|integer(int32)|false|none||none|
|prePage|integer(int32)|false|none||none|
|size|integer(int32)|false|none||none|
|startRow|integer(int64)|false|none||none|
|total|integer(int64)|false|none||none|

<h2 id="tocS_PageDimensionReq">PageDimensionReq</h2>

<a id="schemapagedimensionreq"></a>
<a id="schema_PageDimensionReq"></a>
<a id="tocSpagedimensionreq"></a>
<a id="tocspagedimensionreq"></a>

```json
{
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdBy": "string",
  "current": 0,
  "domainIds": [
    0
  ],
  "hasCollect": true,
  "id": "string",
  "ids": [
    0
  ],
  "isTag": 0,
  "key": "string",
  "modelIds": [
    0
  ],
  "name": "string",
  "orderCondition": "string",
  "pageSize": 0,
  "sensitiveLevel": 0,
  "sort": "string",
  "status": 0
}

```

PageDimensionReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|classifications|[string]|false|none||none|
|createdBy|string|false|none||none|
|current|integer(int32)|false|none||none|
|domainIds|[integer]|false|none||none|
|hasCollect|boolean|false|none||none|
|id|string|false|none||none|
|ids|[integer]|false|none||none|
|isTag|integer(int32)|false|none||none|
|key|string|false|none||none|
|modelIds|[integer]|false|none||none|
|name|string|false|none||none|
|orderCondition|string|false|none||none|
|pageSize|integer(int32)|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|sort|string|false|none||none|
|status|integer(int32)|false|none||none|

<h2 id="tocS_Organization">Organization</h2>

<a id="schemaorganization"></a>
<a id="schema_Organization"></a>
<a id="tocSorganization"></a>
<a id="tocsorganization"></a>

```json
{
  "fullName": "string",
  "id": "string",
  "name": "string",
  "parentId": "string",
  "root": true,
  "subOrganizations": [
    {
      "fullName": "string",
      "id": "string",
      "name": "string",
      "parentId": "string",
      "root": true,
      "subOrganizations": [
        {
          "fullName": "string",
          "id": "string",
          "name": "string",
          "parentId": "string",
          "root": true,
          "subOrganizations": [
            {}
          ]
        }
      ]
    }
  ]
}

```

Organization

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|fullName|string|false|none||none|
|id|string|false|none||none|
|name|string|false|none||none|
|parentId|string|false|none||none|
|root|boolean|false|none||none|
|subOrganizations|[[Organization](#schemaorganization)]|false|none||none|

<h2 id="tocS_Order">Order</h2>

<a id="schemaorder"></a>
<a id="schema_Order"></a>
<a id="tocSorder"></a>
<a id="tocsorder"></a>

```json
{
  "column": "string",
  "direction": "string"
}

```

Order

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|column|string|true|none||none|
|direction|string|false|none||none|

<h2 id="tocS_MultiTurnConfig">MultiTurnConfig</h2>

<a id="schemamultiturnconfig"></a>
<a id="schema_MultiTurnConfig"></a>
<a id="tocSmultiturnconfig"></a>
<a id="tocsmultiturnconfig"></a>

```json
{
  "enableMultiTurn": true
}

```

MultiTurnConfig

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|enableMultiTurn|boolean|false|none||none|

<h2 id="tocS_ModelResp">ModelResp</h2>

<a id="schemamodelresp"></a>
<a id="schema_ModelResp"></a>
<a id="tocSmodelresp"></a>
<a id="tocsmodelresp"></a>

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "databaseId": 0,
  "depends": "string",
  "description": "string",
  "domainId": 0,
  "drillDownDimensions": [
    {
      "dimensionId": 0,
      "inheritedFromModel": true,
      "necessary": true
    }
  ],
  "ext": {},
  "fieldList": [
    "string"
  ],
  "filterSql": "string",
  "fullPath": "string",
  "id": 0,
  "isOpen": 0,
  "modelDetail": {
    "dimensions": [
      {
        "bizName": "string",
        "dateFormat": "string",
        "description": "string",
        "expr": "string",
        "fieldName": "string",
        "isCreateDimension": 0,
        "isTag": 0,
        "name": "string",
        "type": "string",
        "typeParams": {
          "isPrimary": "string",
          "timeGranularity": "string"
        }
      }
    ],
    "fields": [
      {
        "dataType": "string",
        "fieldName": "string"
      }
    ],
    "identifiers": [
      {
        "bizName": "string",
        "entityNames": [
          "string"
        ],
        "fieldName": "string",
        "isCreateDimension": 0,
        "name": "string",
        "type": "string"
      }
    ],
    "measures": [
      {
        "agg": "string",
        "alias": "string",
        "bizName": "string",
        "constraint": "string",
        "expr": "string",
        "fieldName": "string",
        "isCreateMetric": 0,
        "name": "string"
      }
    ],
    "queryType": "string",
    "sqlQuery": "string",
    "sqlVariables": [
      {
        "defaultValues": [
          {}
        ],
        "name": "string",
        "valueType": "EXPR"
      }
    ],
    "tableQuery": "string"
  },
  "name": "string",
  "primaryIdentify": {
    "bizName": "string",
    "entityNames": [
      "string"
    ],
    "fieldName": "string",
    "isCreateDimension": 0,
    "name": "string",
    "type": "string"
  },
  "sensitiveLevel": 0,
  "status": 0,
  "tagObjectId": 0,
  "timeDimension": [
    {
      "bizName": "string",
      "dateFormat": "string",
      "description": "string",
      "expr": "string",
      "fieldName": "string",
      "isCreateDimension": 0,
      "isTag": 0,
      "name": "string",
      "type": "string",
      "typeParams": {
        "isPrimary": "string",
        "timeGranularity": "string"
      }
    }
  ],
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "viewOrgs": [
    "string"
  ],
  "viewers": [
    "string"
  ]
}

```

ModelResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|adminOrgs|[string]|false|none||none|
|admins|[string]|false|none||none|
|alias|string|false|none||none|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|databaseId|integer(int64)|false|none||none|
|depends|string|false|none||none|
|description|string|false|none||none|
|domainId|integer(int64)|false|none||none|
|drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|ext|object|false|none||none|
|fieldList|[string]|false|none||none|
|filterSql|string|false|none||none|
|fullPath|string|false|none||none|
|id|integer(int64)|false|none||none|
|isOpen|integer(int32)|false|none||none|
|modelDetail|[ModelDetail](#schemamodeldetail)|false|none||none|
|name|string|false|none||none|
|primaryIdentify|[Identify](#schemaidentify)|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|tagObjectId|integer(int64)|false|none||none|
|timeDimension|[[Dim](#schemadim)]|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|
|viewOrgs|[string]|false|none||none|
|viewers|[string]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_ModelReq">ModelReq</h2>

<a id="schemamodelreq"></a>
<a id="schema_ModelReq"></a>
<a id="tocSmodelreq"></a>
<a id="tocsmodelreq"></a>

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "databaseId": 0,
  "description": "string",
  "domainId": 0,
  "drillDownDimensions": [
    {
      "dimensionId": 0,
      "inheritedFromModel": true,
      "necessary": true
    }
  ],
  "ext": {},
  "filterSql": "string",
  "id": 0,
  "isOpen": 0,
  "modelDetail": {
    "dimensions": [
      {
        "bizName": "string",
        "dateFormat": "string",
        "description": "string",
        "expr": "string",
        "isCreateDimension": 0,
        "isTag": 0,
        "name": "string",
        "type": "string",
        "typeParams": {
          "isPrimary": "string",
          "timeGranularity": "string"
        }
      }
    ],
    "fields": [
      {
        "dataType": "string",
        "fieldName": "string"
      }
    ],
    "identifiers": [
      {
        "bizName": "string",
        "entityNames": [
          "string"
        ],
        "isCreateDimension": 0,
        "name": "string",
        "type": "string"
      }
    ],
    "measures": [
      {
        "agg": "string",
        "alias": "string",
        "bizName": "string",
        "constraint": "string",
        "expr": "string",
        "isCreateMetric": 0,
        "name": "string"
      }
    ],
    "queryType": "string",
    "sqlQuery": "string",
    "sqlVariables": [
      {
        "defaultValues": [
          {}
        ],
        "name": "string",
        "valueType": "EXPR"
      }
    ],
    "tableQuery": "string"
  },
  "name": "string",
  "sensitiveLevel": 0,
  "sourceType": "string",
  "status": 0,
  "tagObjectId": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "viewOrgs": [
    "string"
  ],
  "viewers": [
    "string"
  ]
}

```

ModelReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|adminOrgs|[string]|false|none||none|
|admins|[string]|false|none||none|
|alias|string|false|none||none|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|databaseId|integer(int64)|false|none||none|
|description|string|false|none||none|
|domainId|integer(int64)|false|none||none|
|drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|ext|object|false|none||none|
|filterSql|string|false|none||none|
|id|integer(int64)|false|none||none|
|isOpen|integer(int32)|false|none||none|
|modelDetail|[ModelDetailReq](#schemamodeldetailreq)|false|none||none|
|name|string|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|sourceType|string|false|none||none|
|status|integer(int32)|false|none||none|
|tagObjectId|integer(int64)|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|
|viewOrgs|[string]|false|none||none|
|viewers|[string]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_ModelRela">ModelRela</h2>

<a id="schemamodelrela"></a>
<a id="schema_ModelRela"></a>
<a id="tocSmodelrela"></a>
<a id="tocsmodelrela"></a>

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "domainId": 0,
  "fromModelId": 0,
  "id": 0,
  "joinConditions": [
    {
      "leftField": "string",
      "operator": "!=",
      "rightField": "string"
    }
  ],
  "joinType": "string",
  "toModelId": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

ModelRela

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|domainId|integer(int64)|false|none||none|
|fromModelId|integer(int64)|false|none||none|
|id|integer(int64)|false|none||none|
|joinConditions|[[JoinCondition](#schemajoincondition)]|false|none||none|
|joinType|string|false|none||none|
|toModelId|integer(int64)|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

<h2 id="tocS_ModelDetailRes">ModelDetailRes</h2>

<a id="schemamodeldetailres"></a>
<a id="schema_ModelDetailRes"></a>
<a id="tocSmodeldetailres"></a>
<a id="tocsmodeldetailres"></a>

```json
{
  "dimensions": [
    {
      "bizName": "string",
      "dateFormat": "string",
      "description": "string",
      "expr": "string",
      "fieldName": "string",
      "isCreateDimension": 0,
      "isTag": 0,
      "name": "string",
      "type": "string",
      "typeParams": {
        "isPrimary": "string",
        "timeGranularity": "string"
      }
    }
  ],
  "fields": [
    {
      "dataType": "string",
      "fieldName": "string"
    }
  ],
  "identifiers": [
    {
      "bizName": "string",
      "entityNames": [
        "string"
      ],
      "fieldName": "string",
      "isCreateDimension": 0,
      "name": "string",
      "type": "string"
    }
  ],
  "measures": [
    {
      "agg": "string",
      "alias": "string",
      "bizName": "string",
      "constraint": "string",
      "expr": "string",
      "fieldName": "string",
      "isCreateMetric": 0,
      "name": "string"
    }
  ],
  "queryType": "string",
  "sqlQuery": "string",
  "sqlVariables": [
    {
      "defaultValues": [
        {}
      ],
      "name": "string",
      "valueType": "EXPR"
    }
  ],
  "tableQuery": "string"
}

```

ModelDetailRes

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dimensions|[[DimRes](#schemadimres)]|false|none||none|
|fields|[[Field](#schemafield)]|false|none||none|
|identifiers|[[IdentifyRes](#schemaidentifyres)]|false|none||none|
|measures|[[MeasureRes](#schemameasureres)]|false|none||none|
|queryType|string|false|none||none|
|sqlQuery|string|false|none||none|
|sqlVariables|[[SqlVariable](#schemasqlvariable)]|false|none||none|
|tableQuery|string|false|none||none|

<h2 id="tocS_ModelDetailReq">ModelDetailReq</h2>

<a id="schemamodeldetailreq"></a>
<a id="schema_ModelDetailReq"></a>
<a id="tocSmodeldetailreq"></a>
<a id="tocsmodeldetailreq"></a>

```json
{
  "dimensions": [
    {
      "bizName": "string",
      "dateFormat": "string",
      "description": "string",
      "expr": "string",
      "isCreateDimension": 0,
      "isTag": 0,
      "name": "string",
      "type": "string",
      "typeParams": {
        "isPrimary": "string",
        "timeGranularity": "string"
      }
    }
  ],
  "fields": [
    {
      "dataType": "string",
      "fieldName": "string"
    }
  ],
  "identifiers": [
    {
      "bizName": "string",
      "entityNames": [
        "string"
      ],
      "isCreateDimension": 0,
      "name": "string",
      "type": "string"
    }
  ],
  "measures": [
    {
      "agg": "string",
      "alias": "string",
      "bizName": "string",
      "constraint": "string",
      "expr": "string",
      "isCreateMetric": 0,
      "name": "string"
    }
  ],
  "queryType": "string",
  "sqlQuery": "string",
  "sqlVariables": [
    {
      "defaultValues": [
        {}
      ],
      "name": "string",
      "valueType": "EXPR"
    }
  ],
  "tableQuery": "string"
}

```

ModelDetailReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dimensions|[[DimReq](#schemadimreq)]|false|none||none|
|fields|[[Field](#schemafield)]|false|none||none|
|identifiers|[[IdentifyReq](#schemaidentifyreq)]|false|none||none|
|measures|[[MeasureReq](#schemameasurereq)]|false|none||none|
|queryType|string|false|none||none|
|sqlQuery|string|false|none||none|
|sqlVariables|[[SqlVariable](#schemasqlvariable)]|false|none||none|
|tableQuery|string|false|none||none|

<h2 id="tocS_ModelDetail">ModelDetail</h2>

<a id="schemamodeldetail"></a>
<a id="schema_ModelDetail"></a>
<a id="tocSmodeldetail"></a>
<a id="tocsmodeldetail"></a>

```json
{
  "dimensions": [
    {
      "bizName": "string",
      "dateFormat": "string",
      "description": "string",
      "expr": "string",
      "fieldName": "string",
      "isCreateDimension": 0,
      "isTag": 0,
      "name": "string",
      "type": "string",
      "typeParams": {
        "isPrimary": "string",
        "timeGranularity": "string"
      }
    }
  ],
  "fields": [
    {
      "dataType": "string",
      "fieldName": "string"
    }
  ],
  "identifiers": [
    {
      "bizName": "string",
      "entityNames": [
        "string"
      ],
      "fieldName": "string",
      "isCreateDimension": 0,
      "name": "string",
      "type": "string"
    }
  ],
  "measures": [
    {
      "agg": "string",
      "alias": "string",
      "bizName": "string",
      "constraint": "string",
      "expr": "string",
      "fieldName": "string",
      "isCreateMetric": 0,
      "name": "string"
    }
  ],
  "queryType": "string",
  "sqlQuery": "string",
  "sqlVariables": [
    {
      "defaultValues": [
        {}
      ],
      "name": "string",
      "valueType": "EXPR"
    }
  ],
  "tableQuery": "string"
}

```

ModelDetail

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dimensions|[[Dim](#schemadim)]|false|none||none|
|fields|[[Field](#schemafield)]|false|none||none|
|identifiers|[[Identify](#schemaidentify)]|false|none||none|
|measures|[[Measure](#schemameasure)]|false|none||none|
|queryType|string|false|none||none|
|sqlQuery|string|false|none||none|
|sqlVariables|[[SqlVariable](#schemasqlvariable)]|false|none||none|
|tableQuery|string|false|none||none|

<h2 id="tocS_MetricTypeDefaultConfig">MetricTypeDefaultConfig</h2>

<a id="schemametrictypedefaultconfig"></a>
<a id="schema_MetricTypeDefaultConfig"></a>
<a id="tocSmetrictypedefaultconfig"></a>
<a id="tocsmetrictypedefaultconfig"></a>

```json
{
  "timeDefaultConfig": {
    "period": "string",
    "timeMode": "LAST",
    "unit": 0
  }
}

```

MetricTypeDefaultConfig

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|timeDefaultConfig|[TimeDefaultConfig](#schematimedefaultconfig)|false|none||none|

<h2 id="tocS_MetricResp">MetricResp</h2>

<a id="schemametricresp"></a>
<a id="schema_MetricResp"></a>
<a id="tocSmetricresp"></a>
<a id="tocsmetricresp"></a>

```json
{
  "alias": "string",
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataFormat": {
    "decimalPlaces": 0,
    "needMultiply100": true
  },
  "dataFormatType": "string",
  "defaultAgg": "string",
  "description": "string",
  "domainId": 0,
  "drillDownDimensions": [
    {
      "dimensionId": 0,
      "inheritedFromModel": true,
      "necessary": true
    }
  ],
  "expr": "string",
  "ext": {},
  "hasAdminRes": true,
  "id": 0,
  "isCollect": true,
  "isPublish": 0,
  "isTag": 0,
  "metricDefineByFieldParams": {
    "expr": "string",
    "fields": [
      {
        "fieldName": "string"
      }
    ],
    "filterSql": "string"
  },
  "metricDefineByMeasureParams": {
    "expr": "string",
    "filterSql": "string",
    "measures": [
      {
        "agg": "string",
        "bizName": "string",
        "constraint": "string"
      }
    ]
  },
  "metricDefineByMetricParams": {
    "expr": "string",
    "filterSql": "string",
    "metrics": [
      {
        "bizName": "string",
        "id": 0
      }
    ]
  },
  "metricDefineType": "FIELD",
  "modelBizName": "string",
  "modelId": 0,
  "modelName": "string",
  "name": "string",
  "relaDimensionIdKey": "string",
  "relateDimension": {
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ]
  },
  "sensitiveLevel": 0,
  "similarity": 0,
  "status": 0,
  "type": "string",
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

MetricResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|alias|string|false|none||none|
|bizName|string|false|none||none|
|classifications|[string]|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dataFormat|[DataFormat](#schemadataformat)|false|none||none|
|dataFormatType|string|false|none||none|
|defaultAgg|string|false|none||none|
|description|string|false|none||none|
|domainId|integer(int64)|false|none||none|
|drillDownDimensions|[[DrillDownDimension](#schemadrilldowndimension)]|false|none||none|
|expr|string|false|none||none|
|ext|object|false|none||none|
|hasAdminRes|boolean|false|none||none|
|id|integer(int64)|false|none||none|
|isCollect|boolean|false|none||none|
|isPublish|integer(int32)|false|none||none|
|isTag|integer(int32)|false|none||none|
|metricDefineByFieldParams|[MetricDefineByFieldParams](#schemametricdefinebyfieldparams)|false|none||none|
|metricDefineByMeasureParams|[MetricDefineByMeasureParams](#schemametricdefinebymeasureparams)|false|none||none|
|metricDefineByMetricParams|[MetricDefineByMetricParams](#schemametricdefinebymetricparams)|false|none||none|
|metricDefineType|string|false|none||none|
|modelBizName|string|false|none||none|
|modelId|integer(int64)|false|none||none|
|modelName|string|false|none||none|
|name|string|false|none||none|
|relaDimensionIdKey|string|false|none||none|
|relateDimension|[RelateDimension](#schemarelatedimension)|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|similarity|number(double)|false|none||none|
|status|integer(int32)|false|none||none|
|type|string|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|metricDefineType|FIELD|
|metricDefineType|MEASURE|
|metricDefineType|METRIC|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_MetricReq">MetricReq</h2>

<a id="schemametricreq"></a>
<a id="schema_MetricReq"></a>
<a id="tocSmetricreq"></a>
<a id="tocsmetricreq"></a>

```json
{
  "alias": "string",
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataFormat": {
    "decimalPlaces": 0,
    "needMultiply100": true
  },
  "dataFormatType": "string",
  "description": "string",
  "ext": {},
  "id": 0,
  "isTag": 0,
  "metricDefineByFieldParams": {
    "expr": "string",
    "fields": [
      {
        "fieldName": "string"
      }
    ],
    "filterSql": "string"
  },
  "metricDefineByMeasureParams": {
    "expr": "string",
    "filterSql": "string",
    "measures": [
      {
        "agg": "string",
        "bizName": "string",
        "constraint": "string"
      }
    ]
  },
  "metricDefineByMetricParams": {
    "expr": "string",
    "filterSql": "string",
    "metrics": [
      {
        "bizName": "string",
        "id": 0
      }
    ]
  },
  "metricDefineType": "FIELD",
  "modelId": 0,
  "name": "string",
  "relateDimension": {
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ]
  },
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

MetricReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|alias|string|false|none||none|
|bizName|string|false|none||none|
|classifications|[string]|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dataFormat|[DataFormat](#schemadataformat)|false|none||none|
|dataFormatType|string|false|none||none|
|description|string|false|none||none|
|ext|object|false|none||none|
|id|integer(int64)|false|none||none|
|isTag|integer(int32)|false|none||none|
|metricDefineByFieldParams|[MetricDefineByFieldParams](#schemametricdefinebyfieldparams)|false|none||none|
|metricDefineByMeasureParams|[MetricDefineByMeasureParams](#schemametricdefinebymeasureparams)|false|none||none|
|metricDefineByMetricParams|[MetricDefineByMetricParams](#schemametricdefinebymetricparams)|false|none||none|
|metricDefineType|string|false|none||none|
|modelId|integer(int64)|false|none||none|
|name|string|false|none||none|
|relateDimension|[RelateDimension](#schemarelatedimension)|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|metricDefineType|FIELD|
|metricDefineType|MEASURE|
|metricDefineType|METRIC|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_MetricQueryDefaultConfig">MetricQueryDefaultConfig</h2>

<a id="schemametricquerydefaultconfig"></a>
<a id="schema_MetricQueryDefaultConfig"></a>
<a id="tocSmetricquerydefaultconfig"></a>
<a id="tocsmetricquerydefaultconfig"></a>

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "defaultConfig": "string",
  "id": 0,
  "metricId": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "userName": "string"
}

```

MetricQueryDefaultConfig

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|defaultConfig|string|false|none||none|
|id|integer(int64)|false|none||none|
|metricId|integer(int64)|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|
|userName|string|false|none||none|

<h2 id="tocS_MetricParam">MetricParam</h2>

<a id="schemametricparam"></a>
<a id="schema_MetricParam"></a>
<a id="tocSmetricparam"></a>
<a id="tocsmetricparam"></a>

```json
{
  "bizName": "string",
  "id": 0
}

```

MetricParam

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|id|integer(int64)|false|none||none|

<h2 id="tocS_MetricInfo">MetricInfo</h2>

<a id="schemametricinfo"></a>
<a id="schema_MetricInfo"></a>
<a id="tocSmetricinfo"></a>
<a id="tocsmetricinfo"></a>

```json
{
  "date": "string",
  "dimension": "string",
  "name": "string",
  "statistics": {
    "property1": "string",
    "property2": "string"
  },
  "value": "string"
}

```

MetricInfo

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|date|string|false|none||none|
|dimension|string|false|none||none|
|name|string|false|none||none|
|statistics|object|false|none||none|
|» **additionalProperties**|string|false|none||none|
|value|string|false|none||none|

<h2 id="tocS_MetricDefineByMetricParams">MetricDefineByMetricParams</h2>

<a id="schemametricdefinebymetricparams"></a>
<a id="schema_MetricDefineByMetricParams"></a>
<a id="tocSmetricdefinebymetricparams"></a>
<a id="tocsmetricdefinebymetricparams"></a>

```json
{
  "expr": "string",
  "filterSql": "string",
  "metrics": [
    {
      "bizName": "string",
      "id": 0
    }
  ]
}

```

MetricDefineByMetricParams

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|expr|string|false|none||none|
|filterSql|string|false|none||none|
|metrics|[[MetricParam](#schemametricparam)]|false|none||none|

<h2 id="tocS_MetricDefineByMeasureParams">MetricDefineByMeasureParams</h2>

<a id="schemametricdefinebymeasureparams"></a>
<a id="schema_MetricDefineByMeasureParams"></a>
<a id="tocSmetricdefinebymeasureparams"></a>
<a id="tocsmetricdefinebymeasureparams"></a>

```json
{
  "expr": "string",
  "filterSql": "string",
  "measures": [
    {
      "agg": "string",
      "bizName": "string",
      "constraint": "string"
    }
  ]
}

```

MetricDefineByMeasureParams

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|expr|string|false|none||none|
|filterSql|string|false|none||none|
|measures|[[MeasureParam](#schemameasureparam)]|false|none||none|

<h2 id="tocS_MetricDefineByFieldParams">MetricDefineByFieldParams</h2>

<a id="schemametricdefinebyfieldparams"></a>
<a id="schema_MetricDefineByFieldParams"></a>
<a id="tocSmetricdefinebyfieldparams"></a>
<a id="tocsmetricdefinebyfieldparams"></a>

```json
{
  "expr": "string",
  "fields": [
    {
      "fieldName": "string"
    }
  ],
  "filterSql": "string"
}

```

MetricDefineByFieldParams

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|expr|string|false|none||none|
|fields|[[FieldParam](#schemafieldparam)]|false|none||none|
|filterSql|string|false|none||none|

<h2 id="tocS_MetricBaseReq">MetricBaseReq</h2>

<a id="schemametricbasereq"></a>
<a id="schema_MetricBaseReq"></a>
<a id="tocSmetricbasereq"></a>
<a id="tocsmetricbasereq"></a>

```json
{
  "alias": "string",
  "bizName": "string",
  "classifications": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataFormat": {
    "decimalPlaces": 0,
    "needMultiply100": true
  },
  "dataFormatType": "string",
  "description": "string",
  "ext": {},
  "id": 0,
  "isTag": 0,
  "modelId": 0,
  "name": "string",
  "relateDimension": {
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ]
  },
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

MetricBaseReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|alias|string|false|none||none|
|bizName|string|false|none||none|
|classifications|[string]|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dataFormat|[DataFormat](#schemadataformat)|false|none||none|
|dataFormatType|string|false|none||none|
|description|string|false|none||none|
|ext|object|false|none||none|
|id|integer(int64)|false|none||none|
|isTag|integer(int32)|false|none||none|
|modelId|integer(int64)|false|none||none|
|name|string|false|none||none|
|relateDimension|[RelateDimension](#schemarelatedimension)|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_MetaBatchReq">MetaBatchReq</h2>

<a id="schemametabatchreq"></a>
<a id="schema_MetaBatchReq"></a>
<a id="tocSmetabatchreq"></a>
<a id="tocsmetabatchreq"></a>

```json
{
  "bizNames": [
    "string"
  ],
  "classifications": [
    "string"
  ],
  "ids": [
    0
  ],
  "modelIds": [
    0
  ],
  "sensitiveLevel": 0,
  "status": 0,
  "type": "ADD"
}

```

MetaBatchReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizNames|[string]|false|none||none|
|classifications|[string]|false|none||none|
|ids|[integer]|false|none||none|
|modelIds|[integer]|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|type|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|ADD|
|type|DELETE|
|type|UPDATE|

<h2 id="tocS_MeasureRes">MeasureRes</h2>

<a id="schemameasureres"></a>
<a id="schema_MeasureRes"></a>
<a id="tocSmeasureres"></a>
<a id="tocsmeasureres"></a>

```json
{
  "agg": "string",
  "alias": "string",
  "bizName": "string",
  "constraint": "string",
  "expr": "string",
  "fieldName": "string",
  "isCreateMetric": 0,
  "name": "string"
}

```

MeasureRes

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|agg|string|false|none||none|
|alias|string|false|none||none|
|bizName|string|false|none||none|
|constraint|string|false|none||none|
|expr|string|false|none||none|
|fieldName|string|false|none||none|
|isCreateMetric|integer(int32)|false|none||none|
|name|string|false|none||none|

<h2 id="tocS_MeasureReq">MeasureReq</h2>

<a id="schemameasurereq"></a>
<a id="schema_MeasureReq"></a>
<a id="tocSmeasurereq"></a>
<a id="tocsmeasurereq"></a>

```json
{
  "agg": "string",
  "alias": "string",
  "bizName": "string",
  "constraint": "string",
  "expr": "string",
  "isCreateMetric": 0,
  "name": "string"
}

```

MeasureReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|agg|string|false|none||none|
|alias|string|false|none||none|
|bizName|string|false|none||none|
|constraint|string|false|none||none|
|expr|string|false|none||none|
|isCreateMetric|integer(int32)|false|none||none|
|name|string|false|none||none|

<h2 id="tocS_MeasureParam">MeasureParam</h2>

<a id="schemameasureparam"></a>
<a id="schema_MeasureParam"></a>
<a id="tocSmeasureparam"></a>
<a id="tocsmeasureparam"></a>

```json
{
  "agg": "string",
  "bizName": "string",
  "constraint": "string"
}

```

MeasureParam

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|agg|string|false|none||none|
|bizName|string|false|none||none|
|constraint|string|false|none||none|

<h2 id="tocS_Measure">Measure</h2>

<a id="schemameasure"></a>
<a id="schema_Measure"></a>
<a id="tocSmeasure"></a>
<a id="tocsmeasure"></a>

```json
{
  "agg": "string",
  "alias": "string",
  "bizName": "string",
  "constraint": "string",
  "expr": "string",
  "fieldName": "string",
  "isCreateMetric": 0,
  "name": "string"
}

```

Measure

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|agg|string|false|none||none|
|alias|string|false|none||none|
|bizName|string|false|none||none|
|constraint|string|false|none||none|
|expr|string|false|none||none|
|fieldName|string|false|none||none|
|isCreateMetric|integer(int32)|false|none||none|
|name|string|false|none||none|

<h2 id="tocS_MapResp">MapResp</h2>

<a id="schemamapresp"></a>
<a id="schema_MapResp"></a>
<a id="tocSmapresp"></a>
<a id="tocsmapresp"></a>

```json
{
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    },
    "matchedDataSetInfos": [
      0
    ]
  },
  "queryText": "string"
}

```

MapResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|mapInfo|[SchemaMapInfoRes](#schemaschemamapinfores)|false|none||none|
|queryText|string|false|none||none|

<h2 id="tocS_LLMConfig">LLMConfig</h2>

<a id="schemallmconfig"></a>
<a id="schema_LLMConfig"></a>
<a id="tocSllmconfig"></a>
<a id="tocsllmconfig"></a>

```json
{
  "apiKey": "string",
  "baseUrl": "string",
  "modelName": "string",
  "provider": "string",
  "temperature": 0,
  "timeOut": 0
}

```

LLMConfig

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|apiKey|string|false|none||none|
|baseUrl|string|false|none||none|
|modelName|string|false|none||none|
|provider|string|false|none||none|
|temperature|number(double)|false|none||none|
|timeOut|integer(int64)|false|none||none|

<h2 id="tocS_KnowledgeInfoReq">KnowledgeInfoReq</h2>

<a id="schemaknowledgeinforeq"></a>
<a id="schema_KnowledgeInfoReq"></a>
<a id="tocSknowledgeinforeq"></a>
<a id="tocsknowledgeinforeq"></a>

```json
{
  "bizName": "string",
  "itemId": 0,
  "knowledgeAdvancedConfig": {
    "blackList": [
      "string"
    ],
    "ruleList": [
      "string"
    ],
    "whiteList": [
      "string"
    ]
  },
  "searchEnable": true,
  "type": "DATASET"
}

```

KnowledgeInfoReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|itemId|integer(int64)|false|none||none|
|knowledgeAdvancedConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none||none|
|searchEnable|boolean|false|none||none|
|type|string|true|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|

<h2 id="tocS_KnowledgeAdvancedConfig">KnowledgeAdvancedConfig</h2>

<a id="schemaknowledgeadvancedconfig"></a>
<a id="schema_KnowledgeAdvancedConfig"></a>
<a id="tocSknowledgeadvancedconfig"></a>
<a id="tocsknowledgeadvancedconfig"></a>

```json
{
  "blackList": [
    "string"
  ],
  "ruleList": [
    "string"
  ],
  "whiteList": [
    "string"
  ]
}

```

KnowledgeAdvancedConfig

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|blackList|[string]|false|none||none|
|ruleList|[string]|false|none||none|
|whiteList|[string]|false|none||none|

<h2 id="tocS_JoinCondition">JoinCondition</h2>

<a id="schemajoincondition"></a>
<a id="schema_JoinCondition"></a>
<a id="tocSjoincondition"></a>
<a id="tocsjoincondition"></a>

```json
{
  "leftField": "string",
  "operator": "!=",
  "rightField": "string"
}

```

JoinCondition

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|leftField|string|false|none||none|
|operator|string|false|none||none|
|rightField|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|operator|!=|
|operator|<|
|operator|<=|
|operator|=|
|operator|>|
|operator|>=|
|operator|BETWEEN|
|operator|EXISTS|
|operator|IN|
|operator|IS_NOT_NULL|
|operator|IS_NULL|
|operator|LIKE|
|operator|NOT_IN|
|operator|SQL_PART|

<h2 id="tocS_ItemVisibilityInfo">ItemVisibilityInfo</h2>

<a id="schemaitemvisibilityinfo"></a>
<a id="schema_ItemVisibilityInfo"></a>
<a id="tocSitemvisibilityinfo"></a>
<a id="tocsitemvisibilityinfo"></a>

```json
{
  "blackDimIdList": [
    0
  ],
  "blackMetricIdList": [
    0
  ],
  "whiteDimIdList": [
    0
  ],
  "whiteMetricIdList": [
    0
  ]
}

```

ItemVisibilityInfo

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|blackDimIdList|[integer]|false|none||none|
|blackMetricIdList|[integer]|false|none||none|
|whiteDimIdList|[integer]|false|none||none|
|whiteMetricIdList|[integer]|false|none||none|

<h2 id="tocS_ItemVisibility">ItemVisibility</h2>

<a id="schemaitemvisibility"></a>
<a id="schema_ItemVisibility"></a>
<a id="tocSitemvisibility"></a>
<a id="tocsitemvisibility"></a>

```json
{
  "blackDimIdList": [
    0
  ],
  "blackMetricIdList": [
    0
  ]
}

```

ItemVisibility

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|blackDimIdList|[integer]|false|none||none|
|blackMetricIdList|[integer]|false|none||none|

<h2 id="tocS_ItemValueResp">ItemValueResp</h2>

<a id="schemaitemvalueresp"></a>
<a id="schema_ItemValueResp"></a>
<a id="tocSitemvalueresp"></a>
<a id="tocsitemvalueresp"></a>

```json
{
  "bizName": "string",
  "itemId": 0,
  "name": "string",
  "type": "DATASET",
  "valueDistributionList": [
    {
      "ratio": 0,
      "totalCount": 0,
      "valueCount": 0,
      "valueMap": {}
    }
  ]
}

```

ItemValueResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|itemId|integer(int64)|false|none||none|
|name|string|false|none||none|
|type|string|false|none||none|
|valueDistributionList|[[ValueDistribution](#schemavaluedistribution)]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|DATASET|
|type|DATE|
|type|DIMENSION|
|type|ENTITY|
|type|ID|
|type|METRIC|
|type|TAG|
|type|TERM|
|type|VALUE|

<h2 id="tocS_ItemValueReq">ItemValueReq</h2>

<a id="schemaitemvaluereq"></a>
<a id="schema_ItemValueReq"></a>
<a id="tocSitemvaluereq"></a>
<a id="tocsitemvaluereq"></a>

```json
{
  "dateConf": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "id": 0,
  "limit": 0
}

```

ItemValueReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dateConf|[DateConf](#schemadateconf)|false|none||none|
|id|integer(int64)|true|none||none|
|limit|integer(int64)|false|none||none|

<h2 id="tocS_ItemValueConfigRes">ItemValueConfigRes</h2>

<a id="schemaitemvalueconfigres"></a>
<a id="schema_ItemValueConfigRes"></a>
<a id="tocSitemvalueconfigres"></a>
<a id="tocsitemvalueconfigres"></a>

```json
{
  "blackList": [
    "string"
  ],
  "dateConf": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "groupByTimeDimension": "string",
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "limit": 0,
  "metricId": 0,
  "ruleList": [
    "string"
  ],
  "whiteList": [
    "string"
  ]
}

```

ItemValueConfigRes

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|blackList|[string]|false|none||none|
|dateConf|[DateConfRes](#schemadateconfres)|false|none||none|
|limit|integer(int64)|false|none||none|
|metricId|integer(int64)|false|none||none|
|ruleList|[string]|false|none||none|
|whiteList|[string]|false|none||none|

<h2 id="tocS_ItemValueConfigReq">ItemValueConfigReq</h2>

<a id="schemaitemvalueconfigreq"></a>
<a id="schema_ItemValueConfigReq"></a>
<a id="tocSitemvalueconfigreq"></a>
<a id="tocsitemvalueconfigreq"></a>

```json
{
  "blackList": [
    "string"
  ],
  "dateConf": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "limit": 0,
  "metricId": 0,
  "ruleList": [
    "string"
  ],
  "whiteList": [
    "string"
  ]
}

```

ItemValueConfigReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|blackList|[string]|false|none||none|
|dateConf|[DateConfReq](#schemadateconfreq)|false|none||none|
|limit|integer(int64)|false|none||none|
|metricId|integer(int64)|false|none||none|
|ruleList|[string]|false|none||none|
|whiteList|[string]|false|none||none|

<h2 id="tocS_ItemResp">ItemResp</h2>

<a id="schemaitemresp"></a>
<a id="schema_ItemResp"></a>
<a id="tocSitemresp"></a>
<a id="tocsitemresp"></a>

```json
{
  "children": [
    {
      "children": [
        {
          "children": [
            {}
          ],
          "id": 0,
          "name": "string",
          "parentId": 0,
          "root": true,
          "type": "DATASET"
        }
      ],
      "id": 0,
      "name": "string",
      "parentId": 0,
      "root": true,
      "type": "DATASET"
    }
  ],
  "id": 0,
  "name": "string",
  "parentId": 0,
  "root": true,
  "type": "DATASET"
}

```

ItemResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|children|[[ItemResp](#schemaitemresp)]|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|parentId|integer(int64)|false|none||none|
|root|boolean|false|none||none|
|type|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|

<h2 id="tocS_ItemRes">ItemRes</h2>

<a id="schemaitemres"></a>
<a id="schema_ItemRes"></a>
<a id="tocSitemres"></a>
<a id="tocsitemres"></a>

```json
{
  "bizName": "string",
  "createdBy": "string",
  "id": 0,
  "name": "string",
  "relateItems": [
    {
      "bizName": "string",
      "createdBy": "string",
      "id": 0,
      "name": "string",
      "relateItems": [
        {
          "bizName": "string",
          "createdBy": "string",
          "id": 0,
          "name": "string",
          "relateItems": [
            {}
          ],
          "type": "DIMENSION",
          "value": "string"
        }
      ],
      "type": "DIMENSION",
      "value": "string"
    }
  ],
  "type": "DIMENSION",
  "value": "string"
}

```

ItemRes

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|createdBy|string|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|relateItems|[[ItemRes](#schemaitemres)]|false|none||none|
|type|string|false|none||none|
|value|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|DIMENSION|
|type|METRIC|
|type|TAG|

<h2 id="tocS_ItemReq">ItemReq</h2>

<a id="schemaitemreq"></a>
<a id="schema_ItemReq"></a>
<a id="tocSitemreq"></a>
<a id="tocsitemreq"></a>

```json
{
  "bizName": "string",
  "createdBy": "string",
  "id": 0,
  "name": "string",
  "relateItems": [
    {
      "bizName": "string",
      "createdBy": "string",
      "id": 0,
      "name": "string",
      "relateItems": [
        {
          "bizName": "string",
          "createdBy": "string",
          "id": 0,
          "name": "string",
          "relateItems": [
            {}
          ],
          "type": "DIMENSION"
        }
      ],
      "type": "DIMENSION"
    }
  ],
  "type": "DIMENSION"
}

```

ItemReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|createdBy|string|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|relateItems|[[ItemReq](#schemaitemreq)]|false|none||none|
|type|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|DIMENSION|
|type|METRIC|
|type|TAG|

<h2 id="tocS_IdentifyRes">IdentifyRes</h2>

<a id="schemaidentifyres"></a>
<a id="schema_IdentifyRes"></a>
<a id="tocSidentifyres"></a>
<a id="tocsidentifyres"></a>

```json
{
  "bizName": "string",
  "entityNames": [
    "string"
  ],
  "fieldName": "string",
  "isCreateDimension": 0,
  "name": "string",
  "type": "string"
}

```

IdentifyRes

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|entityNames|[string]|false|none||none|
|fieldName|string|false|none||none|
|isCreateDimension|integer(int32)|false|none||none|
|name|string|false|none||none|
|type|string|false|none||none|

<h2 id="tocS_IdentifyReq">IdentifyReq</h2>

<a id="schemaidentifyreq"></a>
<a id="schema_IdentifyReq"></a>
<a id="tocSidentifyreq"></a>
<a id="tocsidentifyreq"></a>

```json
{
  "bizName": "string",
  "entityNames": [
    "string"
  ],
  "isCreateDimension": 0,
  "name": "string",
  "type": "string"
}

```

IdentifyReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|entityNames|[string]|false|none||none|
|isCreateDimension|integer(int32)|false|none||none|
|name|string|false|none||none|
|type|string|false|none||none|

<h2 id="tocS_Identify">Identify</h2>

<a id="schemaidentify"></a>
<a id="schema_Identify"></a>
<a id="tocSidentify"></a>
<a id="tocsidentify"></a>

```json
{
  "bizName": "string",
  "entityNames": [
    "string"
  ],
  "fieldName": "string",
  "isCreateDimension": 0,
  "name": "string",
  "type": "string"
}

```

Identify

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|entityNames|[string]|false|none||none|
|fieldName|string|false|none||none|
|isCreateDimension|integer(int32)|false|none||none|
|name|string|false|none||none|
|type|string|false|none||none|

<h2 id="tocS_Filter">Filter</h2>

<a id="schemafilter"></a>
<a id="schema_Filter"></a>
<a id="tocSfilter"></a>
<a id="tocsfilter"></a>

```json
{
  "bizName": "string",
  "children": [
    {
      "bizName": "string",
      "children": [
        {
          "bizName": "string",
          "children": [
            {}
          ],
          "id": 0,
          "name": "string",
          "operator": "!=",
          "relation": "AND",
          "value": {}
        }
      ],
      "id": 0,
      "name": "string",
      "operator": "!=",
      "relation": "AND",
      "value": {}
    }
  ],
  "id": 0,
  "name": "string",
  "operator": "!=",
  "relation": "AND",
  "value": {}
}

```

Filter

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|children|[[Filter](#schemafilter)]|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|operator|string|false|none||none|
|relation|string|false|none||none|
|value|object|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|operator|!=|
|operator|<|
|operator|<=|
|operator|=|
|operator|>|
|operator|>=|
|operator|BETWEEN|
|operator|EXISTS|
|operator|IN|
|operator|IS_NOT_NULL|
|operator|IS_NULL|
|operator|LIKE|
|operator|NOT_IN|
|operator|SQL_PART|
|relation|AND|
|relation|FILTER|
|relation|OR|

<h2 id="tocS_FieldRemovedReq">FieldRemovedReq</h2>

<a id="schemafieldremovedreq"></a>
<a id="schema_FieldRemovedReq"></a>
<a id="tocSfieldremovedreq"></a>
<a id="tocsfieldremovedreq"></a>

```json
{
  "fields": [
    "string"
  ],
  "modelId": 0
}

```

FieldRemovedReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|fields|[string]|false|none||none|
|modelId|integer(int64)|false|none||none|

<h2 id="tocS_FieldParam">FieldParam</h2>

<a id="schemafieldparam"></a>
<a id="schema_FieldParam"></a>
<a id="tocSfieldparam"></a>
<a id="tocsfieldparam"></a>

```json
{
  "fieldName": "string"
}

```

FieldParam

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|fieldName|string|false|none||none|

<h2 id="tocS_Field">Field</h2>

<a id="schemafield"></a>
<a id="schema_Field"></a>
<a id="tocSfield"></a>
<a id="tocsfield"></a>

```json
{
  "dataType": "string",
  "fieldName": "string"
}

```

Field

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dataType|string|false|none||none|
|fieldName|string|false|none||none|

<h2 id="tocS_ExecuteQueryReq">ExecuteQueryReq</h2>

<a id="schemaexecutequeryreq"></a>
<a id="schema_ExecuteQueryReq"></a>
<a id="tocSexecutequeryreq"></a>
<a id="tocsexecutequeryreq"></a>

```json
{
  "chatId": 0,
  "parseInfo": {
    "aggType": "AVG",
    "dataSet": {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    },
    "dateInfo": {
      "dateList": [
        "string"
      ],
      "dateMode": "ALL",
      "detectWord": "string",
      "endDate": "string",
      "groupByDate": true,
      "inherited": true,
      "period": "string",
      "startDate": "string",
      "unit": 0
    },
    "dimensionFilters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "dimensions": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      }
    ],
    "elementMatches": [
      {
        "detectWord": "string",
        "element": {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        },
        "frequency": 0,
        "inherited": true,
        "similarity": 0,
        "word": "string"
      }
    ],
    "entity": {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    },
    "entityInfo": {
      "dataSetInfo": {
        "bizName": "string",
        "itemId": 0,
        "name": "string",
        "primaryKey": "string",
        "value": "string",
        "words": [
          "string"
        ]
      },
      "dimensions": [
        {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "value": "string"
        }
      ],
      "entityId": "string",
      "metrics": [
        {
          "bizName": "string",
          "itemId": 0,
          "name": "string",
          "value": "string"
        }
      ]
    },
    "filterType": "AND",
    "id": 0,
    "limit": 0,
    "metricFilters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "metrics": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      }
    ],
    "orders": [
      {
        "column": "string",
        "direction": "string"
      }
    ],
    "properties": {},
    "queryMode": "string",
    "queryType": "DETAIL",
    "score": 0,
    "sqlEvaluation": {
      "isValidated": true,
      "validateMsg": "string"
    },
    "sqlInfo": {
      "correctS2SQL": "string",
      "querySQL": "string",
      "s2SQL": "string",
      "sourceId": "string"
    },
    "textInfo": "string"
  },
  "queryId": 0,
  "queryText": "string",
  "saveAnswer": true,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}

```

ExecuteQueryReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|chatId|integer(int32)|false|none||none|
|parseInfo|[SemanticParseInfo](#schemasemanticparseinfo)|false|none||none|
|queryId|integer(int64)|false|none||none|
|queryText|string|false|none||none|
|saveAnswer|boolean|false|none||none|
|user|[User](#schemauser)|false|none||none|

<h2 id="tocS_EntityInfo">EntityInfo</h2>

<a id="schemaentityinfo"></a>
<a id="schema_EntityInfo"></a>
<a id="tocSentityinfo"></a>
<a id="tocsentityinfo"></a>

```json
{
  "dataSetInfo": {
    "bizName": "string",
    "itemId": 0,
    "name": "string",
    "primaryKey": "string",
    "value": "string",
    "words": [
      "string"
    ]
  },
  "dimensions": [
    {
      "bizName": "string",
      "itemId": 0,
      "name": "string",
      "value": "string"
    }
  ],
  "entityId": "string",
  "metrics": [
    {
      "bizName": "string",
      "itemId": 0,
      "name": "string",
      "value": "string"
    }
  ]
}

```

EntityInfo

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dataSetInfo|[DataSetInfo](#schemadatasetinfo)|false|none||none|
|dimensions|[[DataInfo](#schemadatainfo)]|false|none||none|
|entityId|string|false|none||none|
|metrics|[[DataInfo](#schemadatainfo)]|false|none||none|

<h2 id="tocS_DrillDownDimension">DrillDownDimension</h2>

<a id="schemadrilldowndimension"></a>
<a id="schema_DrillDownDimension"></a>
<a id="tocSdrilldowndimension"></a>
<a id="tocsdrilldowndimension"></a>

```json
{
  "dimensionId": 0,
  "inheritedFromModel": true,
  "necessary": true
}

```

DrillDownDimension

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dimensionId|integer(int64)|false|none||none|
|inheritedFromModel|boolean|false|none||none|
|necessary|boolean|false|none||none|

<h2 id="tocS_DownloadMetricReq">DownloadMetricReq</h2>

<a id="schemadownloadmetricreq"></a>
<a id="schema_DownloadMetricReq"></a>
<a id="tocSdownloadmetricreq"></a>
<a id="tocsdownloadmetricreq"></a>

```json
{
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "dimensionIds": [
    0
  ],
  "dimensionNames": [
    "string"
  ],
  "domainId": 0,
  "filters": [
    {
      "bizName": "string",
      "children": [
        {
          "bizName": "string",
          "children": [
            {}
          ],
          "id": 0,
          "name": "string",
          "operator": "!=",
          "relation": "AND",
          "value": {}
        }
      ],
      "id": 0,
      "name": "string",
      "operator": "!=",
      "relation": "AND",
      "value": {}
    }
  ],
  "innerLayerNative": true,
  "isTransform": true,
  "limit": 0,
  "metricIds": [
    0
  ],
  "metricNames": [
    "string"
  ]
}

```

DownloadMetricReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dateInfo|[DateConf](#schemadateconf)|false|none||none|
|dimensionIds|[integer]|false|none||none|
|dimensionNames|[string]|false|none||none|
|domainId|integer(int64)|false|none||none|
|filters|[[Filter](#schemafilter)]|false|none||none|
|innerLayerNative|boolean|false|none||none|
|isTransform|boolean|false|none||none|
|limit|integer(int64)|false|none||none|
|metricIds|[integer]|false|none||none|
|metricNames|[string]|false|none||none|

<h2 id="tocS_DomainUpdateReq">DomainUpdateReq</h2>

<a id="schemadomainupdatereq"></a>
<a id="schema_DomainUpdateReq"></a>
<a id="tocSdomainupdatereq"></a>
<a id="tocsdomainupdatereq"></a>

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "id": 0,
  "isOpen": 0,
  "name": "string",
  "parentId": 0,
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "viewOrgs": [
    "string"
  ],
  "viewers": [
    "string"
  ]
}

```

DomainUpdateReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|adminOrgs|[string]|false|none||none|
|admins|[string]|false|none||none|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|description|string|false|none||none|
|id|integer(int64)|false|none||none|
|isOpen|integer(int32)|false|none||none|
|name|string|false|none||none|
|parentId|integer(int64)|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|
|viewOrgs|[string]|false|none||none|
|viewers|[string]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_DomainResp">DomainResp</h2>

<a id="schemadomainresp"></a>
<a id="schema_DomainResp"></a>
<a id="tocSdomainresp"></a>
<a id="tocsdomainresp"></a>

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "fullPath": "string",
  "hasEditPermission": true,
  "hasModel": true,
  "id": 0,
  "isOpen": 0,
  "name": "string",
  "parentId": 0,
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "viewOrgs": [
    "string"
  ],
  "viewers": [
    "string"
  ]
}

```

DomainResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|adminOrgs|[string]|false|none||none|
|admins|[string]|false|none||none|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|description|string|false|none||none|
|fullPath|string|false|none||none|
|hasEditPermission|boolean|false|none||none|
|hasModel|boolean|false|none||none|
|id|integer(int64)|false|none||none|
|isOpen|integer(int32)|false|none||none|
|name|string|false|none||none|
|parentId|integer(int64)|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|
|viewOrgs|[string]|false|none||none|
|viewers|[string]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_DomainReq">DomainReq</h2>

<a id="schemadomainreq"></a>
<a id="schema_DomainReq"></a>
<a id="tocSdomainreq"></a>
<a id="tocsdomainreq"></a>

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "id": 0,
  "isOpen": 0,
  "name": "string",
  "parentId": 0,
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "viewOrgs": [
    "string"
  ],
  "viewers": [
    "string"
  ]
}

```

DomainReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|adminOrgs|[string]|false|none||none|
|admins|[string]|false|none||none|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|description|string|false|none||none|
|id|integer(int64)|false|none||none|
|isOpen|integer(int32)|false|none||none|
|name|string|false|none||none|
|parentId|integer(int64)|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|
|viewOrgs|[string]|false|none||none|
|viewers|[string]|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_DimensionValueReq">DimensionValueReq</h2>

<a id="schemadimensionvaluereq"></a>
<a id="schema_DimensionValueReq"></a>
<a id="tocSdimensionvaluereq"></a>
<a id="tocsdimensionvaluereq"></a>

```json
{
  "agentId": 0,
  "bizName": "string",
  "dataSetIds": [
    0
  ],
  "elementID": 0,
  "modelId": 0,
  "value": "string"
}

```

DimensionValueReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|agentId|integer(int32)|false|none||none|
|bizName|string|false|none||none|
|dataSetIds|[integer]|false|none||none|
|elementID|integer(int64)|true|none||none|
|modelId|integer(int64)|false|none||none|
|value|string|true|none||none|

<h2 id="tocS_DimensionTimeTypeParams">DimensionTimeTypeParams</h2>

<a id="schemadimensiontimetypeparams"></a>
<a id="schema_DimensionTimeTypeParams"></a>
<a id="tocSdimensiontimetypeparams"></a>
<a id="tocsdimensiontimetypeparams"></a>

```json
{
  "isPrimary": "string",
  "timeGranularity": "string"
}

```

DimensionTimeTypeParams

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|isPrimary|string|false|none||none|
|timeGranularity|string|false|none||none|

<h2 id="tocS_DimensionResp">DimensionResp</h2>

<a id="schemadimensionresp"></a>
<a id="schema_DimensionResp"></a>
<a id="tocSdimensionresp"></a>
<a id="tocsdimensionresp"></a>

```json
{
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataType": "ARRAY",
  "defaultValues": [
    "string"
  ],
  "description": "string",
  "dimValueMaps": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "techName": "string"
    }
  ],
  "expr": "string",
  "ext": {},
  "id": 0,
  "isTag": 0,
  "modelBizName": "string",
  "modelFilterSql": "string",
  "modelId": 0,
  "modelName": "string",
  "name": "string",
  "semanticType": "string",
  "sensitiveLevel": 0,
  "status": 0,
  "type": "string",
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

DimensionResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|alias|string|false|none||none|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dataType|string|false|none||none|
|defaultValues|[string]|false|none||none|
|description|string|false|none||none|
|dimValueMaps|[[DimValueMap](#schemadimvaluemap)]|false|none||none|
|expr|string|false|none||none|
|ext|object|false|none||none|
|id|integer(int64)|false|none||none|
|isTag|integer(int32)|false|none||none|
|modelBizName|string|false|none||none|
|modelFilterSql|string|false|none||none|
|modelId|integer(int64)|false|none||none|
|modelName|string|false|none||none|
|name|string|false|none||none|
|semanticType|string|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|type|string|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|dataType|ARRAY|
|dataType|BIGINT|
|dataType|DATE|
|dataType|DECIMAL|
|dataType|DOUBLE|
|dataType|FLOAT|
|dataType|INT|
|dataType|JSON|
|dataType|MAP|
|dataType|UNKNOWN|
|dataType|VARCHAR|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_DimensionReq">DimensionReq</h2>

<a id="schemadimensionreq"></a>
<a id="schema_DimensionReq"></a>
<a id="tocSdimensionreq"></a>
<a id="tocsdimensionreq"></a>

```json
{
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataType": "ARRAY",
  "defaultValues": [
    "string"
  ],
  "description": "string",
  "dimValueMaps": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "techName": "string"
    }
  ],
  "expr": "string",
  "ext": {},
  "id": 0,
  "isTag": 0,
  "modelId": 0,
  "name": "string",
  "semanticType": "string",
  "sensitiveLevel": 0,
  "status": 0,
  "type": "string",
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

DimensionReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|alias|string|false|none||none|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dataType|string|false|none||none|
|defaultValues|[string]|false|none||none|
|description|string|false|none||none|
|dimValueMaps|[[DimValueMap](#schemadimvaluemap)]|false|none||none|
|expr|string|true|none||none|
|ext|object|false|none||none|
|id|integer(int64)|false|none||none|
|isTag|integer(int32)|false|none||none|
|modelId|integer(int64)|false|none||none|
|name|string|false|none||none|
|semanticType|string|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|type|string|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|dataType|ARRAY|
|dataType|BIGINT|
|dataType|DATE|
|dataType|DECIMAL|
|dataType|DOUBLE|
|dataType|FLOAT|
|dataType|INT|
|dataType|JSON|
|dataType|MAP|
|dataType|UNKNOWN|
|dataType|VARCHAR|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_DimensionFilter">DimensionFilter</h2>

<a id="schemadimensionfilter"></a>
<a id="schema_DimensionFilter"></a>
<a id="tocSdimensionfilter"></a>
<a id="tocsdimensionfilter"></a>

```json
{
  "description": "string",
  "expressions": [
    "string"
  ]
}

```

DimensionFilter

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|description|string|false|none||none|
|expressions|[string]|false|none||none|

<h2 id="tocS_DimValueMap">DimValueMap</h2>

<a id="schemadimvaluemap"></a>
<a id="schema_DimValueMap"></a>
<a id="tocSdimvaluemap"></a>
<a id="tocsdimvaluemap"></a>

```json
{
  "alias": [
    "string"
  ],
  "bizName": "string",
  "techName": "string"
}

```

DimValueMap

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|alias|[string]|false|none||none|
|bizName|string|false|none||none|
|techName|string|false|none||none|

<h2 id="tocS_DimRes">DimRes</h2>

<a id="schemadimres"></a>
<a id="schema_DimRes"></a>
<a id="tocSdimres"></a>
<a id="tocsdimres"></a>

```json
{
  "bizName": "string",
  "dateFormat": "string",
  "description": "string",
  "expr": "string",
  "fieldName": "string",
  "isCreateDimension": 0,
  "isTag": 0,
  "name": "string",
  "type": "string",
  "typeParams": {
    "isPrimary": "string",
    "timeGranularity": "string"
  }
}

```

DimRes

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|dateFormat|string|false|none||none|
|description|string|false|none||none|
|expr|string|false|none||none|
|fieldName|string|false|none||none|
|isCreateDimension|integer(int32)|false|none||none|
|isTag|integer(int32)|false|none||none|
|name|string|false|none||none|
|type|string|false|none||none|
|typeParams|[DimensionTimeTypeParams](#schemadimensiontimetypeparams)|false|none||none|

<h2 id="tocS_DimReq">DimReq</h2>

<a id="schemadimreq"></a>
<a id="schema_DimReq"></a>
<a id="tocSdimreq"></a>
<a id="tocsdimreq"></a>

```json
{
  "bizName": "string",
  "dateFormat": "string",
  "description": "string",
  "expr": "string",
  "isCreateDimension": 0,
  "isTag": 0,
  "name": "string",
  "type": "string",
  "typeParams": {
    "isPrimary": "string",
    "timeGranularity": "string"
  }
}

```

DimReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|dateFormat|string|false|none||none|
|description|string|false|none||none|
|expr|string|false|none||none|
|isCreateDimension|integer(int32)|false|none||none|
|isTag|integer(int32)|false|none||none|
|name|string|false|none||none|
|type|string|false|none||none|
|typeParams|[DimensionTimeTypeParams](#schemadimensiontimetypeparams)|false|none||none|

<h2 id="tocS_Dim">Dim</h2>

<a id="schemadim"></a>
<a id="schema_Dim"></a>
<a id="tocSdim"></a>
<a id="tocsdim"></a>

```json
{
  "bizName": "string",
  "dateFormat": "string",
  "description": "string",
  "expr": "string",
  "fieldName": "string",
  "isCreateDimension": 0,
  "isTag": 0,
  "name": "string",
  "type": "string",
  "typeParams": {
    "isPrimary": "string",
    "timeGranularity": "string"
  }
}

```

Dim

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|dateFormat|string|false|none||none|
|description|string|false|none||none|
|expr|string|false|none||none|
|fieldName|string|false|none||none|
|isCreateDimension|integer(int32)|false|none||none|
|isTag|integer(int32)|false|none||none|
|name|string|false|none||none|
|type|string|false|none||none|
|typeParams|[DimensionTimeTypeParams](#schemadimensiontimetypeparams)|false|none||none|

<h2 id="tocS_DictValueResp">DictValueResp</h2>

<a id="schemadictvalueresp"></a>
<a id="schema_DictValueResp"></a>
<a id="tocSdictvalueresp"></a>
<a id="tocsdictvalueresp"></a>

```json
{
  "frequency": 0,
  "nature": "string",
  "value": "string"
}

```

DictValueResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|frequency|integer(int64)|false|none||none|
|nature|string|false|none||none|
|value|string|false|none||none|

<h2 id="tocS_DictValueReq">DictValueReq</h2>

<a id="schemadictvaluereq"></a>
<a id="schema_DictValueReq"></a>
<a id="tocSdictvaluereq"></a>
<a id="tocsdictvaluereq"></a>

```json
{
  "current": 0,
  "itemId": 0,
  "modelId": 0,
  "orderCondition": "string",
  "pageSize": 0,
  "sort": "string",
  "type": "DATASET"
}

```

DictValueReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|current|integer(int32)|false|none||none|
|itemId|integer(int64)|false|none||none|
|modelId|integer(int64)|false|none||none|
|orderCondition|string|false|none||none|
|pageSize|integer(int32)|false|none||none|
|sort|string|false|none||none|
|type|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|

<h2 id="tocS_DictTaskResp">DictTaskResp</h2>

<a id="schemadicttaskresp"></a>
<a id="schema_DictTaskResp"></a>
<a id="tocSdicttaskresp"></a>
<a id="tocsdicttaskresp"></a>

```json
{
  "bizName": "string",
  "config": {
    "blackList": [
      "string"
    ],
    "dateConf": {
      "dateList": [
        "string"
      ],
      "dateMode": "ALL",
      "detectWord": "string",
      "endDate": "string",
      "groupByDate": true,
      "groupByTimeDimension": "string",
      "inherited": true,
      "period": "string",
      "startDate": "string",
      "unit": 0
    },
    "limit": 0,
    "metricId": 0,
    "ruleList": [
      "string"
    ],
    "whiteList": [
      "string"
    ]
  },
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "elapsedMs": 0,
  "id": 0,
  "itemId": 0,
  "modelId": 0,
  "name": "string",
  "nature": "string",
  "status": "DELETED",
  "taskStatus": "string",
  "type": "DATASET"
}

```

DictTaskResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|config|[ItemValueConfigRes](#schemaitemvalueconfigres)|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|description|string|false|none||none|
|elapsedMs|integer(int64)|false|none||none|
|id|integer(int64)|false|none||none|
|itemId|integer(int64)|true|none||none|
|modelId|integer(int64)|false|none||none|
|name|string|false|none||none|
|nature|string|false|none||none|
|status|string|true|none||none|
|taskStatus|string|false|none||none|
|type|string|true|none||none|

#### 枚举值

|属性|值|
|---|---|
|status|DELETED|
|status|INITIALIZED|
|status|OFFLINE|
|status|ONLINE|
|status|UNAVAILABLE|
|status|UNKNOWN|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|

<h2 id="tocS_DictSingleTaskReq">DictSingleTaskReq</h2>

<a id="schemadictsingletaskreq"></a>
<a id="schema_DictSingleTaskReq"></a>
<a id="tocSdictsingletaskreq"></a>
<a id="tocsdictsingletaskreq"></a>

```json
{
  "itemId": 0,
  "type": "DATASET"
}

```

DictSingleTaskReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|itemId|integer(int64)|true|none||none|
|type|string|true|none||none|

#### 枚举值

|属性|值|
|---|---|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|

<h2 id="tocS_DictItemResp">DictItemResp</h2>

<a id="schemadictitemresp"></a>
<a id="schema_DictItemResp"></a>
<a id="tocSdictitemresp"></a>
<a id="tocsdictitemresp"></a>

```json
{
  "bizName": "string",
  "config": {
    "blackList": [
      "string"
    ],
    "dateConf": {
      "dateList": [
        "string"
      ],
      "dateMode": "ALL",
      "detectWord": "string",
      "endDate": "string",
      "groupByDate": true,
      "groupByTimeDimension": "string",
      "inherited": true,
      "period": "string",
      "startDate": "string",
      "unit": 0
    },
    "limit": 0,
    "metricId": 0,
    "ruleList": [
      "string"
    ],
    "whiteList": [
      "string"
    ]
  },
  "id": 0,
  "itemId": 0,
  "modelId": 0,
  "nature": "string",
  "status": "DELETED",
  "type": "DATASET"
}

```

DictItemResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|config|[ItemValueConfigRes](#schemaitemvalueconfigres)|false|none||none|
|id|integer(int64)|false|none||none|
|itemId|integer(int64)|true|none||none|
|modelId|integer(int64)|false|none||none|
|nature|string|false|none||none|
|status|string|true|none||none|
|type|string|true|none||none|

#### 枚举值

|属性|值|
|---|---|
|status|DELETED|
|status|INITIALIZED|
|status|OFFLINE|
|status|ONLINE|
|status|UNAVAILABLE|
|status|UNKNOWN|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|

<h2 id="tocS_DictItemReq">DictItemReq</h2>

<a id="schemadictitemreq"></a>
<a id="schema_DictItemReq"></a>
<a id="tocSdictitemreq"></a>
<a id="tocsdictitemreq"></a>

```json
{
  "config": {
    "blackList": [
      "string"
    ],
    "dateConf": {
      "dateList": [
        "string"
      ],
      "dateMode": "ALL",
      "detectWord": "string",
      "endDate": "string",
      "groupByDate": true,
      "inherited": true,
      "period": "string",
      "startDate": "string",
      "unit": 0
    },
    "limit": 0,
    "metricId": 0,
    "ruleList": [
      "string"
    ],
    "whiteList": [
      "string"
    ]
  },
  "id": 0,
  "itemId": 0,
  "status": "DELETED",
  "type": "DATASET"
}

```

DictItemReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|config|[ItemValueConfigReq](#schemaitemvalueconfigreq)|false|none||none|
|id|integer(int64)|false|none||none|
|itemId|integer(int64)|true|none||none|
|status|string|true|none||none|
|type|string|true|none||none|

#### 枚举值

|属性|值|
|---|---|
|status|DELETED|
|status|INITIALIZED|
|status|OFFLINE|
|status|ONLINE|
|status|UNAVAILABLE|
|status|UNKNOWN|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|

<h2 id="tocS_DictItemFilter">DictItemFilter</h2>

<a id="schemadictitemfilter"></a>
<a id="schema_DictItemFilter"></a>
<a id="tocSdictitemfilter"></a>
<a id="tocsdictitemfilter"></a>

```json
{
  "id": 0,
  "itemId": 0,
  "status": "DELETED",
  "type": "DATASET"
}

```

DictItemFilter

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||none|
|itemId|integer(int64)|false|none||none|
|status|string|false|none||none|
|type|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|status|DELETED|
|status|INITIALIZED|
|status|OFFLINE|
|status|ONLINE|
|status|UNAVAILABLE|
|status|UNKNOWN|
|type|DATASET|
|type|DIMENSION|
|type|DOMAIN|
|type|ENTITY|
|type|METRIC|
|type|MODEL|
|type|TAG|
|type|TAG_OBJECT|
|type|UNKNOWN|

<h2 id="tocS_DefaultDisplayInfo">DefaultDisplayInfo</h2>

<a id="schemadefaultdisplayinfo"></a>
<a id="schema_DefaultDisplayInfo"></a>
<a id="tocSdefaultdisplayinfo"></a>
<a id="tocsdefaultdisplayinfo"></a>

```json
{
  "dimensionIds": [
    0
  ],
  "metricIds": [
    0
  ]
}

```

DefaultDisplayInfo

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dimensionIds|[integer]|false|none||none|
|metricIds|[integer]|false|none||none|

<h2 id="tocS_DateConfRes">DateConfRes</h2>

<a id="schemadateconfres"></a>
<a id="schema_DateConfRes"></a>
<a id="tocSdateconfres"></a>
<a id="tocsdateconfres"></a>

```json
{
  "dateList": [
    "string"
  ],
  "dateMode": "ALL",
  "detectWord": "string",
  "endDate": "string",
  "groupByDate": true,
  "groupByTimeDimension": "string",
  "inherited": true,
  "period": "string",
  "startDate": "string",
  "unit": 0
}

```

DateConfRes

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dateList|[string]|false|none||none|
|dateMode|string|false|none||none|
|detectWord|string|false|none||none|
|endDate|string|false|none||none|
|groupByDate|boolean|false|none||none|
|groupByTimeDimension|string|false|none||none|
|inherited|boolean|false|none||none|
|period|string|false|none||none|
|startDate|string|false|none||none|
|unit|integer(int32)|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|dateMode|ALL|
|dateMode|AVAILABLE|
|dateMode|BETWEEN|
|dateMode|LIST|
|dateMode|RECENT|

<h2 id="tocS_DateConfReq">DateConfReq</h2>

<a id="schemadateconfreq"></a>
<a id="schema_DateConfReq"></a>
<a id="tocSdateconfreq"></a>
<a id="tocsdateconfreq"></a>

```json
{
  "dateList": [
    "string"
  ],
  "dateMode": "ALL",
  "detectWord": "string",
  "endDate": "string",
  "groupByDate": true,
  "inherited": true,
  "period": "string",
  "startDate": "string",
  "unit": 0
}

```

DateConfReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dateList|[string]|false|none||none|
|dateMode|string|false|none||none|
|detectWord|string|false|none||none|
|endDate|string|false|none||none|
|groupByDate|boolean|false|none||none|
|inherited|boolean|false|none||none|
|period|string|false|none||none|
|startDate|string|false|none||none|
|unit|integer(int32)|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|dateMode|ALL|
|dateMode|AVAILABLE|
|dateMode|BETWEEN|
|dateMode|LIST|
|dateMode|RECENT|

<h2 id="tocS_DateConf">DateConf</h2>

<a id="schemadateconf"></a>
<a id="schema_DateConf"></a>
<a id="tocSdateconf"></a>
<a id="tocsdateconf"></a>

```json
{
  "dateList": [
    "string"
  ],
  "dateMode": "ALL",
  "detectWord": "string",
  "endDate": "string",
  "groupByDate": true,
  "inherited": true,
  "period": "string",
  "startDate": "string",
  "unit": 0
}

```

DateConf

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dateList|[string]|false|none||none|
|dateMode|string|false|none||none|
|detectWord|string|false|none||none|
|endDate|string|false|none||none|
|groupByDate|boolean|false|none||none|
|inherited|boolean|false|none||none|
|period|string|false|none||none|
|startDate|string|false|none||none|
|unit|integer(int32)|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|dateMode|ALL|
|dateMode|AVAILABLE|
|dateMode|BETWEEN|
|dateMode|LIST|
|dateMode|RECENT|

<h2 id="tocS_DatabaseResp">DatabaseResp</h2>

<a id="schemadatabaseresp"></a>
<a id="schema_DatabaseResp"></a>
<a id="tocSdatabaseresp"></a>
<a id="tocsdatabaseresp"></a>

```json
{
  "admins": [
    "string"
  ],
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "database": "string",
  "description": "string",
  "hasEditPermission": true,
  "hasPermission": true,
  "hasUsePermission": true,
  "host": "string",
  "id": 0,
  "name": "string",
  "password": "string",
  "port": "string",
  "schema": "string",
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "url": "string",
  "username": "string",
  "version": "string",
  "viewers": [
    "string"
  ]
}

```

DatabaseResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|admins|[string]|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|database|string|false|none||none|
|description|string|false|none||none|
|hasEditPermission|boolean|false|none||none|
|hasPermission|boolean|false|none||none|
|hasUsePermission|boolean|false|none||none|
|host|string|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|password|string|false|none||none|
|port|string|false|none||none|
|schema|string|false|none||none|
|type|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|
|url|string|false|none||none|
|username|string|false|none||none|
|version|string|false|none||none|
|viewers|[string]|false|none||none|

<h2 id="tocS_DatabaseReq">DatabaseReq</h2>

<a id="schemadatabasereq"></a>
<a id="schema_DatabaseReq"></a>
<a id="tocSdatabasereq"></a>
<a id="tocsdatabasereq"></a>

```json
{
  "admins": [
    "string"
  ],
  "database": "string",
  "description": "string",
  "host": "string",
  "id": 0,
  "name": "string",
  "password": "string",
  "port": "string",
  "schema": "string",
  "type": "string",
  "url": "string",
  "username": "string",
  "version": "string",
  "viewers": [
    "string"
  ]
}

```

DatabaseReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|admins|[string]|false|none||none|
|database|string|false|none||none|
|description|string|false|none||none|
|host|string|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|password|string|false|none||none|
|port|string|false|none||none|
|schema|string|false|none||none|
|type|string|false|none||none|
|url|string|false|none||none|
|username|string|false|none||none|
|version|string|false|none||none|
|viewers|[string]|false|none||none|

<h2 id="tocS_DatabaseParameter">DatabaseParameter</h2>

<a id="schemadatabaseparameter"></a>
<a id="schema_DatabaseParameter"></a>
<a id="tocSdatabaseparameter"></a>
<a id="tocsdatabaseparameter"></a>

```json
{
  "candidateValues": [
    {}
  ],
  "comment": "string",
  "dataType": "string",
  "name": "string",
  "placeholder": "string",
  "require": true,
  "value": "string"
}

```

DatabaseParameter

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|candidateValues|[object]|false|none||none|
|comment|string|false|none||none|
|dataType|string|false|none||none|
|name|string|false|none||none|
|placeholder|string|false|none||none|
|require|boolean|false|none||none|
|value|string|false|none||none|

<h2 id="tocS_DataSetSchema">DataSetSchema</h2>

<a id="schemadatasetschema"></a>
<a id="schema_DataSetSchema"></a>
<a id="tocSdatasetschema"></a>
<a id="tocsdatasetschema"></a>

```json
{
  "dataSet": {
    "alias": [
      "string"
    ],
    "bizName": "string",
    "dataFormatType": "string",
    "dataSet": 0,
    "dataSetName": "string",
    "defaultAgg": "string",
    "description": "string",
    "id": 0,
    "isTag": 0,
    "model": 0,
    "name": "string",
    "order": 0,
    "relatedSchemaElements": [
      {
        "dimensionId": 0,
        "necessary": true
      }
    ],
    "schemaValueMaps": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "techName": "string"
      }
    ],
    "type": "DATASET",
    "useCnt": 0
  },
  "dimensionValues": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "dimensions": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "entity": {
    "alias": [
      "string"
    ],
    "bizName": "string",
    "dataFormatType": "string",
    "dataSet": 0,
    "dataSetName": "string",
    "defaultAgg": "string",
    "description": "string",
    "id": 0,
    "isTag": 0,
    "model": 0,
    "name": "string",
    "order": 0,
    "relatedSchemaElements": [
      {
        "dimensionId": 0,
        "necessary": true
      }
    ],
    "schemaValueMaps": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "techName": "string"
      }
    ],
    "type": "DATASET",
    "useCnt": 0
  },
  "metricTypeTimeDefaultConfig": {
    "period": "string",
    "timeMode": "LAST",
    "unit": 0
  },
  "metrics": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "queryConfig": {
    "metricTypeDefaultConfig": {
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    },
    "tagTypeDefaultConfig": {
      "defaultDisplayInfo": {
        "dimensionIds": [
          0
        ],
        "metricIds": [
          0
        ]
      },
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    }
  },
  "tagDefaultDimensions": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "tagDefaultMetrics": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "tagTypeDefaultConfig": {
    "defaultDisplayInfo": {
      "dimensionIds": [
        0
      ],
      "metricIds": [
        0
      ]
    },
    "timeDefaultConfig": {
      "period": "string",
      "timeMode": "LAST",
      "unit": 0
    }
  },
  "tagTypeTimeDefaultConfig": {
    "period": "string",
    "timeMode": "LAST",
    "unit": 0
  },
  "tags": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "terms": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ]
}

```

DataSetSchema

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dataSet|[SchemaElement](#schemaschemaelement)|false|none||none|
|dimensionValues|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|dimensions|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|entity|[SchemaElement](#schemaschemaelement)|false|none||none|
|metricTypeTimeDefaultConfig|[TimeDefaultConfig](#schematimedefaultconfig)|false|none||none|
|metrics|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|queryConfig|[QueryConfig](#schemaqueryconfig)|false|none||none|
|tagDefaultDimensions|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|tagDefaultMetrics|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|tagTypeDefaultConfig|[TagTypeDefaultConfig](#schematagtypedefaultconfig)|false|none||none|
|tagTypeTimeDefaultConfig|[TimeDefaultConfig](#schematimedefaultconfig)|false|none||none|
|tags|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|terms|[[SchemaElement](#schemaschemaelement)]|false|none||none|

<h2 id="tocS_DataSetResp">DataSetResp</h2>

<a id="schemadatasetresp"></a>
<a id="schema_DataSetResp"></a>
<a id="tocSdatasetresp"></a>
<a id="tocsdatasetresp"></a>

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "alias": "string",
  "allDimensions": [
    {
      "isTag": 0,
      "itemId": 0
    }
  ],
  "allIncludeAllModels": [
    0
  ],
  "allMetrics": [
    {
      "isTag": 0,
      "itemId": 0
    }
  ],
  "allModels": [
    0
  ],
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetDetail": {
    "dataSetModelConfigs": [
      {
        "dimensions": [
          0
        ],
        "id": 0,
        "includesAll": true,
        "metrics": [
          0
        ]
      }
    ]
  },
  "description": "string",
  "domainId": 0,
  "filterSql": "string",
  "id": 0,
  "name": "string",
  "queryConfig": {
    "metricTypeDefaultConfig": {
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    },
    "tagTypeDefaultConfig": {
      "defaultDisplayInfo": {
        "dimensionIds": [
          0
        ],
        "metricIds": [
          0
        ]
      },
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    }
  },
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

DataSetResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|adminOrgs|[string]|false|none||none|
|admins|[string]|false|none||none|
|alias|string|false|none||none|
|allDimensions|[[TagItem](#schematagitem)]|false|none||none|
|allIncludeAllModels|[integer]|false|none||none|
|allMetrics|[[TagItem](#schematagitem)]|false|none||none|
|allModels|[integer]|false|none||none|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dataSetDetail|[DataSetDetail](#schemadatasetdetail)|false|none||none|
|description|string|false|none||none|
|domainId|integer(int64)|false|none||none|
|filterSql|string|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|queryConfig|[QueryConfig](#schemaqueryconfig)|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_DataSetReq">DataSetReq</h2>

<a id="schemadatasetreq"></a>
<a id="schema_DataSetReq"></a>
<a id="tocSdatasetreq"></a>
<a id="tocsdatasetreq"></a>

```json
{
  "adminOrgs": [
    "string"
  ],
  "admins": [
    "string"
  ],
  "alias": "string",
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetDetail": {
    "dataSetModelConfigs": [
      {
        "dimensions": [
          0
        ],
        "id": 0,
        "includesAll": true,
        "metrics": [
          0
        ]
      }
    ]
  },
  "description": "string",
  "domainId": 0,
  "id": 0,
  "name": "string",
  "queryConfig": {
    "metricTypeDefaultConfig": {
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    },
    "tagTypeDefaultConfig": {
      "defaultDisplayInfo": {
        "dimensionIds": [
          0
        ],
        "metricIds": [
          0
        ]
      },
      "timeDefaultConfig": {
        "period": "string",
        "timeMode": "LAST",
        "unit": 0
      }
    }
  },
  "sensitiveLevel": 0,
  "status": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

DataSetReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|adminOrgs|[string]|false|none||none|
|admins|[string]|false|none||none|
|alias|string|false|none||none|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dataSetDetail|[DataSetDetail](#schemadatasetdetail)|false|none||none|
|description|string|false|none||none|
|domainId|integer(int64)|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|queryConfig|[QueryConfig](#schemaqueryconfig)|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_DataSetModelConfig">DataSetModelConfig</h2>

<a id="schemadatasetmodelconfig"></a>
<a id="schema_DataSetModelConfig"></a>
<a id="tocSdatasetmodelconfig"></a>
<a id="tocsdatasetmodelconfig"></a>

```json
{
  "dimensions": [
    0
  ],
  "id": 0,
  "includesAll": true,
  "metrics": [
    0
  ]
}

```

DataSetModelConfig

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dimensions|[integer]|false|none||none|
|id|integer(int64)|false|none||none|
|includesAll|boolean|false|none||none|
|metrics|[integer]|false|none||none|

<h2 id="tocS_DataSetInfo">DataSetInfo</h2>

<a id="schemadatasetinfo"></a>
<a id="schema_DataSetInfo"></a>
<a id="tocSdatasetinfo"></a>
<a id="tocsdatasetinfo"></a>

```json
{
  "bizName": "string",
  "itemId": 0,
  "name": "string",
  "primaryKey": "string",
  "value": "string",
  "words": [
    "string"
  ]
}

```

DataSetInfo

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|itemId|integer(int32)|false|none||none|
|name|string|false|none||none|
|primaryKey|string|false|none||none|
|value|string|false|none||none|
|words|[string]|false|none||none|

<h2 id="tocS_DataSetDetail">DataSetDetail</h2>

<a id="schemadatasetdetail"></a>
<a id="schema_DataSetDetail"></a>
<a id="tocSdatasetdetail"></a>
<a id="tocsdatasetdetail"></a>

```json
{
  "dataSetModelConfigs": [
    {
      "dimensions": [
        0
      ],
      "id": 0,
      "includesAll": true,
      "metrics": [
        0
      ]
    }
  ]
}

```

DataSetDetail

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dataSetModelConfigs|[[DataSetModelConfig](#schemadatasetmodelconfig)]|false|none||none|

<h2 id="tocS_DataInfo">DataInfo</h2>

<a id="schemadatainfo"></a>
<a id="schema_DataInfo"></a>
<a id="tocSdatainfo"></a>
<a id="tocsdatainfo"></a>

```json
{
  "bizName": "string",
  "itemId": 0,
  "name": "string",
  "value": "string"
}

```

DataInfo

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|itemId|integer(int32)|false|none||none|
|name|string|false|none||none|
|value|string|false|none||none|

<h2 id="tocS_DataFormat">DataFormat</h2>

<a id="schemadataformat"></a>
<a id="schema_DataFormat"></a>
<a id="tocSdataformat"></a>
<a id="tocsdataformat"></a>

```json
{
  "decimalPlaces": 0,
  "needMultiply100": true
}

```

DataFormat

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|decimalPlaces|integer(int32)|false|none||none|
|needMultiply100|boolean|false|none||none|

<h2 id="tocS_CollectDO">CollectDO</h2>

<a id="schemacollectdo"></a>
<a id="schema_CollectDO"></a>
<a id="tocScollectdo"></a>
<a id="tocscollectdo"></a>

```json
{
  "collectId": 0,
  "createTime": "2019-08-24T14:15:22Z",
  "id": 0,
  "type": "string",
  "updateTime": "2019-08-24T14:15:22Z",
  "username": "string"
}

```

CollectDO

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|collectId|integer(int64)|false|none||none|
|createTime|string(date-time)|false|none||none|
|id|integer(int64)|false|none||none|
|type|string|false|none||none|
|updateTime|string(date-time)|false|none||none|
|username|string|false|none||none|

<h2 id="tocS_ClassResp">ClassResp</h2>

<a id="schemaclassresp"></a>
<a id="schema_ClassResp"></a>
<a id="tocSclassresp"></a>
<a id="tocsclassresp"></a>

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetId": 0,
  "description": "string",
  "domainId": 0,
  "domainName": "string",
  "fullPath": "string",
  "id": 0,
  "itemIds": [
    0
  ],
  "name": "string",
  "status": 0,
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

ClassResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dataSetId|integer(int64)|false|none||none|
|description|string|false|none||none|
|domainId|integer(int64)|false|none||none|
|domainName|string|false|none||none|
|fullPath|string|false|none||none|
|id|integer(int64)|false|none||none|
|itemIds|[integer]|false|none||none|
|name|string|false|none||none|
|status|integer(int32)|false|none||none|
|type|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

<h2 id="tocS_ClassReq">ClassReq</h2>

<a id="schemaclassreq"></a>
<a id="schema_ClassReq"></a>
<a id="tocSclassreq"></a>
<a id="tocsclassreq"></a>

```json
{
  "bizName": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "domainId": 0,
  "id": 0,
  "itemIds": [
    0
  ],
  "name": "string",
  "parentId": 0,
  "sensitiveLevel": 0,
  "status": 0,
  "tagObjectId": 0,
  "typeEnum": "DATASET",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

ClassReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|description|string|false|none||none|
|domainId|integer(int64)|false|none||none|
|id|integer(int64)|false|none||none|
|itemIds|[integer]|false|none||none|
|name|string|false|none||none|
|parentId|integer(int64)|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|tagObjectId|integer(int64)|false|none||none|
|typeEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|typeEnum|DATASET|
|typeEnum|DIMENSION|
|typeEnum|DOMAIN|
|typeEnum|ENTITY|
|typeEnum|METRIC|
|typeEnum|MODEL|
|typeEnum|TAG|
|typeEnum|TAG_OBJECT|
|typeEnum|UNKNOWN|

<h2 id="tocS_ClassFilter">ClassFilter</h2>

<a id="schemaclassfilter"></a>
<a id="schema_ClassFilter"></a>
<a id="tocSclassfilter"></a>
<a id="tocsclassfilter"></a>

```json
{
  "bizName": "string",
  "classId": 0,
  "createdBy": "string",
  "dataSetId": 0,
  "domainId": 0,
  "fieldsDepend": [
    "string"
  ],
  "id": "string",
  "ids": [
    0
  ],
  "isTag": 0,
  "key": "string",
  "modelIds": [
    0
  ],
  "name": "string",
  "names": [
    "string"
  ],
  "sensitiveLevel": 0,
  "status": 0,
  "type": "string"
}

```

ClassFilter

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|classId|integer(int64)|false|none||none|
|createdBy|string|false|none||none|
|dataSetId|integer(int64)|false|none||none|
|domainId|integer(int64)|false|none||none|
|fieldsDepend|[string]|false|none||none|
|id|string|false|none||none|
|ids|[integer]|false|none||none|
|isTag|integer(int32)|false|none||none|
|key|string|false|none||none|
|modelIds|[integer]|false|none||none|
|name|string|false|none||none|
|names|[string]|false|none||none|
|sensitiveLevel|integer(int32)|false|none||none|
|status|integer(int32)|false|none||none|
|type|string|false|none||none|

<h2 id="tocS_ChatQueryDataReq">ChatQueryDataReq</h2>

<a id="schemachatquerydatareq"></a>
<a id="schema_ChatQueryDataReq"></a>
<a id="tocSchatquerydatareq"></a>
<a id="tocschatquerydatareq"></a>

```json
{
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "dimensionFilters": [
    {
      "bizName": "string",
      "elementID": 0,
      "function": "string",
      "name": "string",
      "operator": "!=",
      "value": {}
    }
  ],
  "dimensions": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "metricFilters": [
    {
      "bizName": "string",
      "elementID": 0,
      "function": "string",
      "name": "string",
      "operator": "!=",
      "value": {}
    }
  ],
  "metrics": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "parseId": 0,
  "queryId": 0,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}

```

ChatQueryDataReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dateInfo|[DateConf](#schemadateconf)|false|none||none|
|dimensionFilters|[[QueryFilter](#schemaqueryfilter)]|false|none||none|
|dimensions|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|metricFilters|[[QueryFilter](#schemaqueryfilter)]|false|none||none|
|metrics|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|parseId|integer(int32)|false|none||none|
|queryId|integer(int64)|false|none||none|
|user|[User](#schemauser)|false|none||none|

<h2 id="tocS_ChatPluginRes">ChatPluginRes</h2>

<a id="schemachatpluginres"></a>
<a id="schema_ChatPluginRes"></a>
<a id="tocSchatpluginres"></a>
<a id="tocschatpluginres"></a>

```json
{
  "comment": "string",
  "config": "string",
  "containsAllDataSet": true,
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetList": [
    0
  ],
  "defaultMode": 0,
  "exampleQuestionList": [
    "string"
  ],
  "id": 0,
  "name": "string",
  "parseMode": "EMBEDDING_RECALL",
  "parseModeConfig": "string",
  "pattern": "string",
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

ChatPluginRes

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|comment|string|false|none||none|
|config|string|false|none||none|
|containsAllDataSet|boolean|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dataSetList|[integer]|false|none||none|
|defaultMode|integer(int64)|false|none||none|
|exampleQuestionList|[string]|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|parseMode|string|false|none||none|
|parseModeConfig|string|false|none||none|
|pattern|string|false|none||none|
|type|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|parseMode|EMBEDDING_RECALL|
|parseMode|FUNCTION_CALL|

<h2 id="tocS_ChatPluginReq">ChatPluginReq</h2>

<a id="schemachatpluginreq"></a>
<a id="schema_ChatPluginReq"></a>
<a id="tocSchatpluginreq"></a>
<a id="tocschatpluginreq"></a>

```json
{
  "comment": "string",
  "config": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetList": [
    0
  ],
  "id": 0,
  "name": "string",
  "parseMode": "EMBEDDING_RECALL",
  "parseModeConfig": "string",
  "pattern": "string",
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

ChatPluginReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|comment|string|false|none||none|
|config|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dataSetList|[integer]|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|parseMode|string|false|none||none|
|parseModeConfig|string|false|none||none|
|pattern|string|false|none||none|
|type|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|parseMode|EMBEDDING_RECALL|
|parseMode|FUNCTION_CALL|

<h2 id="tocS_ChatParseReq">ChatParseReq</h2>

<a id="schemachatparsereq"></a>
<a id="schema_ChatParseReq"></a>
<a id="tocSchatparsereq"></a>
<a id="tocschatparsereq"></a>

```json
{
  "agentId": 0,
  "chatId": 0,
  "mapInfo": {
    "dataSetElementMatches": {
      "property1": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ],
      "property2": [
        {
          "detectWord": "string",
          "element": {
            "alias": null,
            "bizName": null,
            "dataFormatType": null,
            "dataSet": null,
            "dataSetName": null,
            "defaultAgg": null,
            "description": null,
            "id": null,
            "isTag": null,
            "model": null,
            "name": null,
            "order": null,
            "relatedSchemaElements": null,
            "schemaValueMaps": null,
            "type": null,
            "useCnt": null
          },
          "frequency": 0,
          "inherited": true,
          "similarity": 0,
          "word": "string"
        }
      ]
    }
  },
  "queryFilters": {
    "filters": [
      {
        "bizName": "string",
        "elementID": 0,
        "function": "string",
        "name": "string",
        "operator": "!=",
        "value": {}
      }
    ],
    "params": {}
  },
  "queryText": "string",
  "saveAnswer": true,
  "topN": 0,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}

```

ChatParseReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|agentId|integer(int32)|false|none||none|
|chatId|integer(int32)|false|none||none|
|mapInfo|[SchemaMapInfo](#schemaschemamapinfo)|false|none||none|
|queryFilters|[QueryFilters](#schemaqueryfilters)|false|none||none|
|queryText|string|false|none||none|
|saveAnswer|boolean|false|none||none|
|topN|integer(int32)|false|none||none|
|user|[User](#schemauser)|false|none||none|

<h2 id="tocS_ChatMemoryUpdateReq">ChatMemoryUpdateReq</h2>

<a id="schemachatmemoryupdatereq"></a>
<a id="schema_ChatMemoryUpdateReq"></a>
<a id="tocSchatmemoryupdatereq"></a>
<a id="tocschatmemoryupdatereq"></a>

```json
{
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dbSchema": "string",
  "humanReviewCmt": "string",
  "humanReviewRet": "NEGATIVE",
  "id": 0,
  "s2sql": "string",
  "status": "DISABLED",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

ChatMemoryUpdateReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dbSchema|string|false|none||none|
|humanReviewCmt|string|false|none||none|
|humanReviewRet|string|false|none||none|
|id|integer(int64)|true|none||none|
|s2sql|string|false|none||none|
|status|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|humanReviewRet|NEGATIVE|
|humanReviewRet|POSITIVE|
|status|DISABLED|
|status|ENABLED|
|status|PENDING|

<h2 id="tocS_ChatMemoryFilter">ChatMemoryFilter</h2>

<a id="schemachatmemoryfilter"></a>
<a id="schema_ChatMemoryFilter"></a>
<a id="tocSchatmemoryfilter"></a>
<a id="tocschatmemoryfilter"></a>

```json
{
  "agentId": 0,
  "humanReviewRet": "NEGATIVE",
  "llmReviewRet": "NEGATIVE",
  "question": "string",
  "questions": [
    "string"
  ],
  "status": "DISABLED"
}

```

ChatMemoryFilter

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|agentId|integer(int32)|false|none||none|
|humanReviewRet|string|false|none||none|
|llmReviewRet|string|false|none||none|
|question|string|false|none||none|
|questions|[string]|false|none||none|
|status|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|humanReviewRet|NEGATIVE|
|humanReviewRet|POSITIVE|
|llmReviewRet|NEGATIVE|
|llmReviewRet|POSITIVE|
|status|DISABLED|
|status|ENABLED|
|status|PENDING|

<h2 id="tocS_ChatMemoryDO">ChatMemoryDO</h2>

<a id="schemachatmemorydo"></a>
<a id="schema_ChatMemoryDO"></a>
<a id="tocSchatmemorydo"></a>
<a id="tocschatmemorydo"></a>

```json
{
  "agentId": 0,
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dbSchema": "string",
  "humanReviewCmt": "string",
  "humanReviewRet": "NEGATIVE",
  "id": 0,
  "llmReviewCmt": "string",
  "llmReviewRet": "NEGATIVE",
  "question": "string",
  "s2sql": "string",
  "status": "DISABLED",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

ChatMemoryDO

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|agentId|integer(int32)|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dbSchema|string|false|none||none|
|humanReviewCmt|string|false|none||none|
|humanReviewRet|string|false|none||none|
|id|integer(int64)|false|none||none|
|llmReviewCmt|string|false|none||none|
|llmReviewRet|string|false|none||none|
|question|string|false|none||none|
|s2sql|string|false|none||none|
|status|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|humanReviewRet|NEGATIVE|
|humanReviewRet|POSITIVE|
|llmReviewRet|NEGATIVE|
|llmReviewRet|POSITIVE|
|status|DISABLED|
|status|ENABLED|
|status|PENDING|

<h2 id="tocS_ChatExecuteReq">ChatExecuteReq</h2>

<a id="schemachatexecutereq"></a>
<a id="schema_ChatExecuteReq"></a>
<a id="tocSchatexecutereq"></a>
<a id="tocschatexecutereq"></a>

```json
{
  "agentId": 0,
  "chatId": 0,
  "parseId": 0,
  "queryId": 0,
  "queryText": "string",
  "saveAnswer": true,
  "user": {
    "displayName": "string",
    "email": "string",
    "id": 0,
    "isAdmin": 0,
    "name": "string",
    "superAdmin": true
  }
}

```

ChatExecuteReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|agentId|integer(int32)|false|none||none|
|chatId|integer(int32)|false|none||none|
|parseId|integer(int32)|false|none||none|
|queryId|integer(int64)|false|none||none|
|queryText|string|false|none||none|
|saveAnswer|boolean|false|none||none|
|user|[User](#schemauser)|false|none||none|

<h2 id="tocS_ChatDetailRichConfigResp">ChatDetailRichConfigResp</h2>

<a id="schemachatdetailrichconfigresp"></a>
<a id="schema_ChatDetailRichConfigResp"></a>
<a id="tocSchatdetailrichconfigresp"></a>
<a id="tocschatdetailrichconfigresp"></a>

```json
{
  "chatDefaultConfig": {
    "dimensions": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      }
    ],
    "metrics": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      }
    ],
    "period": "string",
    "timeMode": "LAST",
    "unit": 0
  },
  "globalKnowledgeConfig": {
    "blackList": [
      "string"
    ],
    "ruleList": [
      "string"
    ],
    "whiteList": [
      "string"
    ]
  },
  "knowledgeInfos": [
    {
      "bizName": "string",
      "itemId": 0,
      "knowledgeAdvancedConfig": {
        "blackList": [
          "string"
        ],
        "ruleList": [
          "string"
        ],
        "whiteList": [
          "string"
        ]
      },
      "searchEnable": true,
      "type": "DATASET"
    }
  ],
  "visibility": {
    "blackDimIdList": [
      0
    ],
    "blackMetricIdList": [
      0
    ],
    "whiteDimIdList": [
      0
    ],
    "whiteMetricIdList": [
      0
    ]
  }
}

```

ChatDetailRichConfigResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|chatDefaultConfig|[ChatDefaultRichConfigResp](#schemachatdefaultrichconfigresp)|false|none||none|
|globalKnowledgeConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none||none|
|knowledgeInfos|[[KnowledgeInfoReq](#schemaknowledgeinforeq)]|false|none||none|
|visibility|[ItemVisibilityInfo](#schemaitemvisibilityinfo)|false|none||none|

<h2 id="tocS_ChatDetailConfigReq">ChatDetailConfigReq</h2>

<a id="schemachatdetailconfigreq"></a>
<a id="schema_ChatDetailConfigReq"></a>
<a id="tocSchatdetailconfigreq"></a>
<a id="tocschatdetailconfigreq"></a>

```json
{
  "chatDefaultConfig": {
    "dimensionIds": [
      0
    ],
    "metricIds": [
      0
    ]
  },
  "globalKnowledgeConfig": {
    "blackList": [
      "string"
    ],
    "ruleList": [
      "string"
    ],
    "whiteList": [
      "string"
    ]
  },
  "knowledgeInfos": [
    {
      "bizName": "string",
      "itemId": 0,
      "knowledgeAdvancedConfig": {
        "blackList": [
          "string"
        ],
        "ruleList": [
          "string"
        ],
        "whiteList": [
          "string"
        ]
      },
      "searchEnable": true,
      "type": "DATASET"
    }
  ],
  "visibility": {
    "blackDimIdList": [
      0
    ],
    "blackMetricIdList": [
      0
    ]
  }
}

```

ChatDetailConfigReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|chatDefaultConfig|[ChatDefaultConfigReq](#schemachatdefaultconfigreq)|false|none||none|
|globalKnowledgeConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none||none|
|knowledgeInfos|[[KnowledgeInfoReq](#schemaknowledgeinforeq)]|false|none||none|
|visibility|[ItemVisibility](#schemaitemvisibility)|false|none||none|

<h2 id="tocS_ChatDefaultRichConfigResp">ChatDefaultRichConfigResp</h2>

<a id="schemachatdefaultrichconfigresp"></a>
<a id="schema_ChatDefaultRichConfigResp"></a>
<a id="tocSchatdefaultrichconfigresp"></a>
<a id="tocschatdefaultrichconfigresp"></a>

```json
{
  "dimensions": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "metrics": [
    {
      "alias": [
        "string"
      ],
      "bizName": "string",
      "dataFormatType": "string",
      "dataSet": 0,
      "dataSetName": "string",
      "defaultAgg": "string",
      "description": "string",
      "id": 0,
      "isTag": 0,
      "model": 0,
      "name": "string",
      "order": 0,
      "relatedSchemaElements": [
        {
          "dimensionId": 0,
          "necessary": true
        }
      ],
      "schemaValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "type": "DATASET",
      "useCnt": 0
    }
  ],
  "period": "string",
  "timeMode": "LAST",
  "unit": 0
}

```

ChatDefaultRichConfigResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dimensions|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|metrics|[[SchemaElement](#schemaschemaelement)]|false|none||none|
|period|string|false|none||none|
|timeMode|string|false|none||none|
|unit|integer(int32)|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|timeMode|LAST|
|timeMode|RECENT|

<h2 id="tocS_ChatDefaultConfigReq">ChatDefaultConfigReq</h2>

<a id="schemachatdefaultconfigreq"></a>
<a id="schema_ChatDefaultConfigReq"></a>
<a id="tocSchatdefaultconfigreq"></a>
<a id="tocschatdefaultconfigreq"></a>

```json
{
  "dimensionIds": [
    0
  ],
  "metricIds": [
    0
  ]
}

```

ChatDefaultConfigReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dimensionIds|[integer]|false|none||none|
|metricIds|[integer]|false|none||none|

<h2 id="tocS_ChatDO">ChatDO</h2>

<a id="schemachatdo"></a>
<a id="schema_ChatDO"></a>
<a id="tocSchatdo"></a>
<a id="tocschatdo"></a>

```json
{
  "agentId": 0,
  "chatId": 0,
  "chatName": "string",
  "createTime": "string",
  "creator": "string",
  "isDelete": 0,
  "isTop": 0,
  "lastQuestion": "string",
  "lastTime": "string"
}

```

ChatDO

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|agentId|integer(int32)|false|none||none|
|chatId|integer(int64)|false|none||none|
|chatName|string|false|none||none|
|createTime|string|false|none||none|
|creator|string|false|none||none|
|isDelete|integer(int32)|false|none||none|
|isTop|integer(int32)|false|none||none|
|lastQuestion|string|false|none||none|
|lastTime|string|false|none||none|

<h2 id="tocS_ChatConfigRichResp">ChatConfigRichResp</h2>

<a id="schemachatconfigrichresp"></a>
<a id="schema_ChatConfigRichResp"></a>
<a id="tocSchatconfigrichresp"></a>
<a id="tocschatconfigrichresp"></a>

```json
{
  "bizName": "string",
  "chatAggRichConfig": {
    "chatDefaultConfig": {
      "dimensions": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "metrics": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "period": "string",
      "timeMode": "LAST",
      "unit": 0
    },
    "globalKnowledgeConfig": {
      "blackList": [
        "string"
      ],
      "ruleList": [
        "string"
      ],
      "whiteList": [
        "string"
      ]
    },
    "knowledgeInfos": [
      {
        "bizName": "string",
        "itemId": 0,
        "knowledgeAdvancedConfig": {
          "blackList": [
            null
          ],
          "ruleList": [
            null
          ],
          "whiteList": [
            null
          ]
        },
        "searchEnable": true,
        "type": "DATASET"
      }
    ],
    "visibility": {
      "blackDimIdList": [
        0
      ],
      "blackMetricIdList": [
        0
      ],
      "whiteDimIdList": [
        0
      ],
      "whiteMetricIdList": [
        0
      ]
    }
  },
  "chatDetailRichConfig": {
    "chatDefaultConfig": {
      "dimensions": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "metrics": [
        {
          "alias": [
            null
          ],
          "bizName": "string",
          "dataFormatType": "string",
          "dataSet": 0,
          "dataSetName": "string",
          "defaultAgg": "string",
          "description": "string",
          "id": 0,
          "isTag": 0,
          "model": 0,
          "name": "string",
          "order": 0,
          "relatedSchemaElements": [
            null
          ],
          "schemaValueMaps": [
            null
          ],
          "type": "[",
          "useCnt": 0
        }
      ],
      "period": "string",
      "timeMode": "LAST",
      "unit": 0
    },
    "globalKnowledgeConfig": {
      "blackList": [
        "string"
      ],
      "ruleList": [
        "string"
      ],
      "whiteList": [
        "string"
      ]
    },
    "knowledgeInfos": [
      {
        "bizName": "string",
        "itemId": 0,
        "knowledgeAdvancedConfig": {
          "blackList": [
            null
          ],
          "ruleList": [
            null
          ],
          "whiteList": [
            null
          ]
        },
        "searchEnable": true,
        "type": "DATASET"
      }
    ],
    "visibility": {
      "blackDimIdList": [
        0
      ],
      "blackMetricIdList": [
        0
      ],
      "whiteDimIdList": [
        0
      ],
      "whiteMetricIdList": [
        0
      ]
    }
  },
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "id": 0,
  "modelId": 0,
  "modelName": "string",
  "recommendedQuestions": [
    {
      "question": "string"
    }
  ],
  "statusEnum": "DELETED",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

ChatConfigRichResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|bizName|string|false|none||none|
|chatAggRichConfig|[ChatAggRichConfigResp](#schemachataggrichconfigresp)|false|none||none|
|chatDetailRichConfig|[ChatDetailRichConfigResp](#schemachatdetailrichconfigresp)|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|id|integer(int64)|false|none||none|
|modelId|integer(int64)|false|none||none|
|modelName|string|false|none||none|
|recommendedQuestions|[[RecommendedQuestionReq](#schemarecommendedquestionreq)]|false|none||none|
|statusEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|statusEnum|DELETED|
|statusEnum|INITIALIZED|
|statusEnum|OFFLINE|
|statusEnum|ONLINE|
|statusEnum|UNAVAILABLE|
|statusEnum|UNKNOWN|

<h2 id="tocS_ChatConfigResp">ChatConfigResp</h2>

<a id="schemachatconfigresp"></a>
<a id="schema_ChatConfigResp"></a>
<a id="tocSchatconfigresp"></a>
<a id="tocschatconfigresp"></a>

```json
{
  "chatAggConfig": {
    "chatDefaultConfig": {
      "dimensionIds": [
        0
      ],
      "metricIds": [
        0
      ]
    },
    "globalKnowledgeConfig": {
      "blackList": [
        "string"
      ],
      "ruleList": [
        "string"
      ],
      "whiteList": [
        "string"
      ]
    },
    "knowledgeInfos": [
      {
        "bizName": "string",
        "itemId": 0,
        "knowledgeAdvancedConfig": {
          "blackList": [
            null
          ],
          "ruleList": [
            null
          ],
          "whiteList": [
            null
          ]
        },
        "searchEnable": true,
        "type": "DATASET"
      }
    ],
    "visibility": {
      "blackDimIdList": [
        0
      ],
      "blackMetricIdList": [
        0
      ]
    }
  },
  "chatDetailConfig": {
    "chatDefaultConfig": {
      "dimensionIds": [
        0
      ],
      "metricIds": [
        0
      ]
    },
    "globalKnowledgeConfig": {
      "blackList": [
        "string"
      ],
      "ruleList": [
        "string"
      ],
      "whiteList": [
        "string"
      ]
    },
    "knowledgeInfos": [
      {
        "bizName": "string",
        "itemId": 0,
        "knowledgeAdvancedConfig": {
          "blackList": [
            null
          ],
          "ruleList": [
            null
          ],
          "whiteList": [
            null
          ]
        },
        "searchEnable": true,
        "type": "DATASET"
      }
    ],
    "visibility": {
      "blackDimIdList": [
        0
      ],
      "blackMetricIdList": [
        0
      ]
    }
  },
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "id": 0,
  "llmExamples": "string",
  "modelId": 0,
  "recommendedQuestions": [
    {
      "question": "string"
    }
  ],
  "statusEnum": "DELETED",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

ChatConfigResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|chatAggConfig|[ChatAggConfigReq](#schemachataggconfigreq)|false|none||none|
|chatDetailConfig|[ChatDetailConfigReq](#schemachatdetailconfigreq)|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|id|integer(int64)|false|none||none|
|llmExamples|string|false|none||none|
|modelId|integer(int64)|false|none||none|
|recommendedQuestions|[[RecommendedQuestionReq](#schemarecommendedquestionreq)]|false|none||none|
|statusEnum|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|statusEnum|DELETED|
|statusEnum|INITIALIZED|
|statusEnum|OFFLINE|
|statusEnum|ONLINE|
|statusEnum|UNAVAILABLE|
|statusEnum|UNKNOWN|

<h2 id="tocS_ChatConfigFilter">ChatConfigFilter</h2>

<a id="schemachatconfigfilter"></a>
<a id="schema_ChatConfigFilter"></a>
<a id="tocSchatconfigfilter"></a>
<a id="tocschatconfigfilter"></a>

```json
{
  "id": 0,
  "modelId": 0,
  "status": "DELETED"
}

```

ChatConfigFilter

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||none|
|modelId|integer(int64)|false|none||none|
|status|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|status|DELETED|
|status|INITIALIZED|
|status|OFFLINE|
|status|ONLINE|
|status|UNAVAILABLE|
|status|UNKNOWN|

<h2 id="tocS_ChatConfigEditReqReq">ChatConfigEditReqReq</h2>

<a id="schemachatconfigeditreqreq"></a>
<a id="schema_ChatConfigEditReqReq"></a>
<a id="tocSchatconfigeditreqreq"></a>
<a id="tocschatconfigeditreqreq"></a>

```json
{
  "id": 0,
  "llmExamples": "string",
  "modelId": 0,
  "recommendedQuestions": [
    {
      "question": "string"
    }
  ],
  "status": "DELETED"
}

```

ChatConfigEditReqReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||none|
|llmExamples|string|false|none||none|
|modelId|integer(int64)|false|none||none|
|recommendedQuestions|[[RecommendedQuestionReq](#schemarecommendedquestionreq)]|false|none||none|
|status|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|status|DELETED|
|status|INITIALIZED|
|status|OFFLINE|
|status|ONLINE|
|status|UNAVAILABLE|
|status|UNKNOWN|

<h2 id="tocS_ChatConfigBaseReq">ChatConfigBaseReq</h2>

<a id="schemachatconfigbasereq"></a>
<a id="schema_ChatConfigBaseReq"></a>
<a id="tocSchatconfigbasereq"></a>
<a id="tocschatconfigbasereq"></a>

```json
{
  "llmExamples": "string",
  "modelId": 0,
  "recommendedQuestions": [
    {
      "question": "string"
    }
  ],
  "status": "DELETED"
}

```

ChatConfigBaseReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|llmExamples|string|false|none||none|
|modelId|integer(int64)|false|none||none|
|recommendedQuestions|[[RecommendedQuestionReq](#schemarecommendedquestionreq)]|false|none||none|
|status|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|status|DELETED|
|status|INITIALIZED|
|status|OFFLINE|
|status|ONLINE|
|status|UNAVAILABLE|
|status|UNKNOWN|

<h2 id="tocS_ChatAggRichConfigResp">ChatAggRichConfigResp</h2>

<a id="schemachataggrichconfigresp"></a>
<a id="schema_ChatAggRichConfigResp"></a>
<a id="tocSchataggrichconfigresp"></a>
<a id="tocschataggrichconfigresp"></a>

```json
{
  "chatDefaultConfig": {
    "dimensions": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      }
    ],
    "metrics": [
      {
        "alias": [
          "string"
        ],
        "bizName": "string",
        "dataFormatType": "string",
        "dataSet": 0,
        "dataSetName": "string",
        "defaultAgg": "string",
        "description": "string",
        "id": 0,
        "isTag": 0,
        "model": 0,
        "name": "string",
        "order": 0,
        "relatedSchemaElements": [
          {
            "dimensionId": null,
            "necessary": null
          }
        ],
        "schemaValueMaps": [
          {
            "alias": null,
            "bizName": null,
            "techName": null
          }
        ],
        "type": "DATASET",
        "useCnt": 0
      }
    ],
    "period": "string",
    "timeMode": "LAST",
    "unit": 0
  },
  "globalKnowledgeConfig": {
    "blackList": [
      "string"
    ],
    "ruleList": [
      "string"
    ],
    "whiteList": [
      "string"
    ]
  },
  "knowledgeInfos": [
    {
      "bizName": "string",
      "itemId": 0,
      "knowledgeAdvancedConfig": {
        "blackList": [
          "string"
        ],
        "ruleList": [
          "string"
        ],
        "whiteList": [
          "string"
        ]
      },
      "searchEnable": true,
      "type": "DATASET"
    }
  ],
  "visibility": {
    "blackDimIdList": [
      0
    ],
    "blackMetricIdList": [
      0
    ],
    "whiteDimIdList": [
      0
    ],
    "whiteMetricIdList": [
      0
    ]
  }
}

```

ChatAggRichConfigResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|chatDefaultConfig|[ChatDefaultRichConfigResp](#schemachatdefaultrichconfigresp)|false|none||none|
|globalKnowledgeConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none||none|
|knowledgeInfos|[[KnowledgeInfoReq](#schemaknowledgeinforeq)]|false|none||none|
|visibility|[ItemVisibilityInfo](#schemaitemvisibilityinfo)|false|none||none|

<h2 id="tocS_ChatAggConfigReq">ChatAggConfigReq</h2>

<a id="schemachataggconfigreq"></a>
<a id="schema_ChatAggConfigReq"></a>
<a id="tocSchataggconfigreq"></a>
<a id="tocschataggconfigreq"></a>

```json
{
  "chatDefaultConfig": {
    "dimensionIds": [
      0
    ],
    "metricIds": [
      0
    ]
  },
  "globalKnowledgeConfig": {
    "blackList": [
      "string"
    ],
    "ruleList": [
      "string"
    ],
    "whiteList": [
      "string"
    ]
  },
  "knowledgeInfos": [
    {
      "bizName": "string",
      "itemId": 0,
      "knowledgeAdvancedConfig": {
        "blackList": [
          "string"
        ],
        "ruleList": [
          "string"
        ],
        "whiteList": [
          "string"
        ]
      },
      "searchEnable": true,
      "type": "DATASET"
    }
  ],
  "visibility": {
    "blackDimIdList": [
      0
    ],
    "blackMetricIdList": [
      0
    ]
  }
}

```

ChatAggConfigReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|chatDefaultConfig|[ChatDefaultConfigReq](#schemachatdefaultconfigreq)|false|none||none|
|globalKnowledgeConfig|[KnowledgeAdvancedConfig](#schemaknowledgeadvancedconfig)|false|none||none|
|knowledgeInfos|[[KnowledgeInfoReq](#schemaknowledgeinforeq)]|false|none||none|
|visibility|[ItemVisibility](#schemaitemvisibility)|false|none||none|

<h2 id="tocS_CanvasSchemaResp">CanvasSchemaResp</h2>

<a id="schemacanvasschemaresp"></a>
<a id="schema_CanvasSchemaResp"></a>
<a id="tocScanvasschemaresp"></a>
<a id="tocscanvasschemaresp"></a>

```json
{
  "dimensions": [
    {
      "alias": "string",
      "bizName": "string",
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dataType": "ARRAY",
      "defaultValues": [
        "string"
      ],
      "description": "string",
      "dimValueMaps": [
        {
          "alias": [
            "string"
          ],
          "bizName": "string",
          "techName": "string"
        }
      ],
      "expr": "string",
      "ext": {},
      "id": 0,
      "isTag": 0,
      "modelBizName": "string",
      "modelFilterSql": "string",
      "modelId": 0,
      "modelName": "string",
      "name": "string",
      "semanticType": "string",
      "sensitiveLevel": 0,
      "status": 0,
      "type": "string",
      "typeEnum": "DATASET",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "domainId": 0,
  "metrics": [
    {
      "alias": "string",
      "bizName": "string",
      "classifications": [
        "string"
      ],
      "createdAt": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "dataFormat": {
        "decimalPlaces": 0,
        "needMultiply100": true
      },
      "dataFormatType": "string",
      "defaultAgg": "string",
      "description": "string",
      "domainId": 0,
      "drillDownDimensions": [
        {
          "dimensionId": 0,
          "inheritedFromModel": true,
          "necessary": true
        }
      ],
      "expr": "string",
      "ext": {},
      "hasAdminRes": true,
      "id": 0,
      "isCollect": true,
      "isPublish": 0,
      "isTag": 0,
      "metricDefineByFieldParams": {
        "expr": "string",
        "fields": [
          {
            "fieldName": null
          }
        ],
        "filterSql": "string"
      },
      "metricDefineByMeasureParams": {
        "expr": "string",
        "filterSql": "string",
        "measures": [
          {
            "agg": null,
            "bizName": null,
            "constraint": null
          }
        ]
      },
      "metricDefineByMetricParams": {
        "expr": "string",
        "filterSql": "string",
        "metrics": [
          {
            "bizName": null,
            "id": null
          }
        ]
      },
      "metricDefineType": "FIELD",
      "modelBizName": "string",
      "modelId": 0,
      "modelName": "string",
      "name": "string",
      "relaDimensionIdKey": "string",
      "relateDimension": {
        "drillDownDimensions": [
          {
            "dimensionId": null,
            "inheritedFromModel": null,
            "necessary": null
          }
        ]
      },
      "sensitiveLevel": 0,
      "similarity": 0,
      "status": 0,
      "type": "string",
      "typeEnum": "DATASET",
      "updatedAt": "2019-08-24T14:15:22Z",
      "updatedBy": "string"
    }
  ],
  "model": {
    "adminOrgs": [
      "string"
    ],
    "admins": [
      "string"
    ],
    "alias": "string",
    "bizName": "string",
    "createdAt": "2019-08-24T14:15:22Z",
    "createdBy": "string",
    "databaseId": 0,
    "depends": "string",
    "description": "string",
    "domainId": 0,
    "drillDownDimensions": [
      {
        "dimensionId": 0,
        "inheritedFromModel": true,
        "necessary": true
      }
    ],
    "ext": {},
    "fieldList": [
      "string"
    ],
    "filterSql": "string",
    "fullPath": "string",
    "id": 0,
    "isOpen": 0,
    "modelDetail": {
      "dimensions": [
        {
          "bizName": "string",
          "dateFormat": "string",
          "description": "string",
          "expr": "string",
          "fieldName": "string",
          "isCreateDimension": 0,
          "isTag": 0,
          "name": "string",
          "type": "string",
          "typeParams": {}
        }
      ],
      "fields": [
        {
          "dataType": "string",
          "fieldName": "string"
        }
      ],
      "identifiers": [
        {
          "bizName": "string",
          "entityNames": [
            null
          ],
          "fieldName": "string",
          "isCreateDimension": 0,
          "name": "string",
          "type": "string"
        }
      ],
      "measures": [
        {
          "agg": "string",
          "alias": "string",
          "bizName": "string",
          "constraint": "string",
          "expr": "string",
          "fieldName": "string",
          "isCreateMetric": 0,
          "name": "string"
        }
      ],
      "queryType": "string",
      "sqlQuery": "string",
      "sqlVariables": [
        {
          "defaultValues": [
            null
          ],
          "name": "string",
          "valueType": "["
        }
      ],
      "tableQuery": "string"
    },
    "name": "string",
    "primaryIdentify": {
      "bizName": "string",
      "entityNames": [
        "string"
      ],
      "fieldName": "string",
      "isCreateDimension": 0,
      "name": "string",
      "type": "string"
    },
    "sensitiveLevel": 0,
    "status": 0,
    "tagObjectId": 0,
    "timeDimension": [
      {
        "bizName": "string",
        "dateFormat": "string",
        "description": "string",
        "expr": "string",
        "fieldName": "string",
        "isCreateDimension": 0,
        "isTag": 0,
        "name": "string",
        "type": "string",
        "typeParams": {
          "isPrimary": "string",
          "timeGranularity": "string"
        }
      }
    ],
    "typeEnum": "DATASET",
    "updatedAt": "2019-08-24T14:15:22Z",
    "updatedBy": "string",
    "viewOrgs": [
      "string"
    ],
    "viewers": [
      "string"
    ]
  }
}

```

CanvasSchemaResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dimensions|[[DimensionResp](#schemadimensionresp)]|false|none||none|
|domainId|integer(int64)|false|none||none|
|metrics|[[MetricResp](#schemametricresp)]|false|none||none|
|model|[ModelResp](#schemamodelresp)|false|none||none|

<h2 id="tocS_CanvasReq">CanvasReq</h2>

<a id="schemacanvasreq"></a>
<a id="schema_CanvasReq"></a>
<a id="tocScanvasreq"></a>
<a id="tocscanvasreq"></a>

```json
{
  "config": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "domainId": 0,
  "id": 0,
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

CanvasReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|config|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|domainId|integer(int64)|false|none||none|
|id|integer(int64)|false|none||none|
|type|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

<h2 id="tocS_CanvasDO">CanvasDO</h2>

<a id="schemacanvasdo"></a>
<a id="schema_CanvasDO"></a>
<a id="tocScanvasdo"></a>
<a id="tocscanvasdo"></a>

```json
{
  "config": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "domainId": 0,
  "id": 0,
  "type": "string",
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

CanvasDO

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|config|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|domainId|integer(int64)|false|none||none|
|id|integer(int64)|false|none||none|
|type|string|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

<h2 id="tocS_Cache">Cache</h2>

<a id="schemacache"></a>
<a id="schema_Cache"></a>
<a id="tocScache"></a>
<a id="tocscache"></a>

```json
{
  "cache": true
}

```

Cache

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|cache|boolean|false|none||none|

<h2 id="tocS_BatchDownloadReq">BatchDownloadReq</h2>

<a id="schemabatchdownloadreq"></a>
<a id="schema_BatchDownloadReq"></a>
<a id="tocSbatchdownloadreq"></a>
<a id="tocsbatchdownloadreq"></a>

```json
{
  "dateInfo": {
    "dateList": [
      "string"
    ],
    "dateMode": "ALL",
    "detectWord": "string",
    "endDate": "string",
    "groupByDate": true,
    "inherited": true,
    "period": "string",
    "startDate": "string",
    "unit": 0
  },
  "metricIds": [
    0
  ],
  "transform": true
}

```

BatchDownloadReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|dateInfo|[DateConf](#schemadateconf)|false|none||none|
|metricIds|[integer]|false|none||none|
|transform|boolean|false|none||none|

<h2 id="tocS_AuthorizedResourceResp">AuthorizedResourceResp</h2>

<a id="schemaauthorizedresourceresp"></a>
<a id="schema_AuthorizedResourceResp"></a>
<a id="tocSauthorizedresourceresp"></a>
<a id="tocsauthorizedresourceresp"></a>

```json
{
  "filters": [
    {
      "description": "string",
      "expressions": [
        "string"
      ]
    }
  ],
  "resources": [
    {
      "group": [
        {
          "modelId": 0,
          "name": "string"
        }
      ]
    }
  ]
}

```

AuthorizedResourceResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|filters|[[DimensionFilter](#schemadimensionfilter)]|false|none||none|
|resources|[[AuthResGrp](#schemaauthresgrp)]|false|none||none|

<h2 id="tocS_AuthRule">AuthRule</h2>

<a id="schemaauthrule"></a>
<a id="schema_AuthRule"></a>
<a id="tocSauthrule"></a>
<a id="tocsauthrule"></a>

```json
{
  "description": "string",
  "dimensions": [
    "string"
  ],
  "metrics": [
    "string"
  ],
  "name": "string"
}

```

AuthRule

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|description|string|false|none||none|
|dimensions|[string]|false|none||none|
|metrics|[string]|false|none||none|
|name|string|false|none||none|

<h2 id="tocS_AuthResGrp">AuthResGrp</h2>

<a id="schemaauthresgrp"></a>
<a id="schema_AuthResGrp"></a>
<a id="tocSauthresgrp"></a>
<a id="tocsauthresgrp"></a>

```json
{
  "group": [
    {
      "modelId": 0,
      "name": "string"
    }
  ]
}

```

AuthResGrp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|group|[[AuthRes](#schemaauthres)]|false|none||none|

<h2 id="tocS_AuthRes">AuthRes</h2>

<a id="schemaauthres"></a>
<a id="schema_AuthRes"></a>
<a id="tocSauthres"></a>
<a id="tocsauthres"></a>

```json
{
  "modelId": 0,
  "name": "string"
}

```

AuthRes

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|modelId|integer(int64)|false|none||none|
|name|string|false|none||none|

<h2 id="tocS_AuthGroup">AuthGroup</h2>

<a id="schemaauthgroup"></a>
<a id="schema_AuthGroup"></a>
<a id="tocSauthgroup"></a>
<a id="tocsauthgroup"></a>

```json
{
  "authRules": [
    {
      "description": "string",
      "dimensions": [
        "string"
      ],
      "metrics": [
        "string"
      ],
      "name": "string"
    }
  ],
  "authorizedDepartmentIds": [
    "string"
  ],
  "authorizedUsers": [
    "string"
  ],
  "dimensionFilterDescription": "string",
  "dimensionFilters": [
    "string"
  ],
  "groupId": 0,
  "modelId": 0,
  "name": "string"
}

```

AuthGroup

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|authRules|[[AuthRule](#schemaauthrule)]|false|none||none|
|authorizedDepartmentIds|[string]|false|none||none|
|authorizedUsers|[string]|false|none||none|
|dimensionFilterDescription|string|false|none||none|
|dimensionFilters|[string]|false|none||none|
|groupId|integer(int32)|false|none||none|
|modelId|integer(int64)|false|none||none|
|name|string|false|none||none|

<h2 id="tocS_AppResp">AppResp</h2>

<a id="schemaappresp"></a>
<a id="schema_AppResp"></a>
<a id="tocSappresp"></a>
<a id="tocsappresp"></a>

```json
{
  "appStatus": "DELETED",
  "config": {
    "items": [
      {
        "bizName": "string",
        "createdBy": "string",
        "id": 0,
        "name": "string",
        "relateItems": [
          {
            "bizName": null,
            "createdBy": null,
            "id": null,
            "name": null,
            "relateItems": null,
            "type": null,
            "value": null
          }
        ],
        "type": "DIMENSION",
        "value": "string"
      }
    ]
  },
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "endDate": "2019-08-24T14:15:22Z",
  "hasAdminRes": true,
  "id": 0,
  "name": "string",
  "owners": [
    "string"
  ],
  "qps": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

AppResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|appStatus|string|false|none||none|
|config|[AppConfigRes](#schemaappconfigres)|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|description|string|false|none||none|
|endDate|string(date-time)|false|none||none|
|hasAdminRes|boolean|false|none||none|
|id|integer(int32)|false|none||none|
|name|string|false|none||none|
|owners|[string]|false|none||none|
|qps|integer(int32)|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|appStatus|DELETED|
|appStatus|INIT|
|appStatus|OFFLINE|
|appStatus|ONLINE|
|appStatus|UNKNOWN|

<h2 id="tocS_AppReq">AppReq</h2>

<a id="schemaappreq"></a>
<a id="schema_AppReq"></a>
<a id="tocSappreq"></a>
<a id="tocsappreq"></a>

```json
{
  "config": {
    "items": [
      {
        "bizName": "string",
        "createdBy": "string",
        "id": 0,
        "name": "string",
        "relateItems": [
          {
            "bizName": null,
            "createdBy": null,
            "id": null,
            "name": null,
            "relateItems": null,
            "type": null
          }
        ],
        "type": "DIMENSION"
      }
    ]
  },
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "endDate": "2019-08-24T14:15:22Z",
  "id": 0,
  "name": "string",
  "owners": [
    "string"
  ],
  "qps": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

AppReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|config|[AppConfigReq](#schemaappconfigreq)|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|description|string|false|none||none|
|endDate|string(date-time)|false|none||none|
|id|integer(int64)|false|none||none|
|name|string|false|none||none|
|owners|[string]|false|none||none|
|qps|integer(int32)|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

<h2 id="tocS_AppQueryReq">AppQueryReq</h2>

<a id="schemaappqueryreq"></a>
<a id="schema_AppQueryReq"></a>
<a id="tocSappqueryreq"></a>
<a id="tocsappqueryreq"></a>

```json
{
  "appStatus": [
    "DELETED"
  ],
  "createdBy": "string",
  "current": 0,
  "name": "string",
  "orderCondition": "string",
  "pageSize": 0,
  "sort": "string"
}

```

AppQueryReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|appStatus|[string]|false|none||none|
|createdBy|string|false|none||none|
|current|integer(int32)|false|none||none|
|name|string|false|none||none|
|orderCondition|string|false|none||none|
|pageSize|integer(int32)|false|none||none|
|sort|string|false|none||none|

<h2 id="tocS_AppDetailResp">AppDetailResp</h2>

<a id="schemaappdetailresp"></a>
<a id="schema_AppDetailResp"></a>
<a id="tocSappdetailresp"></a>
<a id="tocsappdetailresp"></a>

```json
{
  "appSecret": "string",
  "appStatus": "DELETED",
  "config": {
    "items": [
      {
        "bizName": "string",
        "createdBy": "string",
        "id": 0,
        "name": "string",
        "relateItems": [
          {
            "bizName": null,
            "createdBy": null,
            "id": null,
            "name": null,
            "relateItems": null,
            "type": null,
            "value": null
          }
        ],
        "type": "DIMENSION",
        "value": "string"
      }
    ]
  },
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "endDate": "2019-08-24T14:15:22Z",
  "hasAdminRes": true,
  "id": 0,
  "name": "string",
  "owners": [
    "string"
  ],
  "qps": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string"
}

```

AppDetailResp

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|appSecret|string|false|none||none|
|appStatus|string|false|none||none|
|config|[AppConfigRes](#schemaappconfigres)|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|description|string|false|none||none|
|endDate|string(date-time)|false|none||none|
|hasAdminRes|boolean|false|none||none|
|id|integer(int32)|false|none||none|
|name|string|false|none||none|
|owners|[string]|false|none||none|
|qps|integer(int32)|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|appStatus|DELETED|
|appStatus|INIT|
|appStatus|OFFLINE|
|appStatus|ONLINE|
|appStatus|UNKNOWN|

<h2 id="tocS_AppConfigRes">AppConfigRes</h2>

<a id="schemaappconfigres"></a>
<a id="schema_AppConfigRes"></a>
<a id="tocSappconfigres"></a>
<a id="tocsappconfigres"></a>

```json
{
  "items": [
    {
      "bizName": "string",
      "createdBy": "string",
      "id": 0,
      "name": "string",
      "relateItems": [
        {
          "bizName": "string",
          "createdBy": "string",
          "id": 0,
          "name": "string",
          "relateItems": [
            {}
          ],
          "type": "DIMENSION",
          "value": "string"
        }
      ],
      "type": "DIMENSION",
      "value": "string"
    }
  ]
}

```

AppConfigRes

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|items|[[ItemRes](#schemaitemres)]|false|none||none|

<h2 id="tocS_AppConfigReq">AppConfigReq</h2>

<a id="schemaappconfigreq"></a>
<a id="schema_AppConfigReq"></a>
<a id="tocSappconfigreq"></a>
<a id="tocsappconfigreq"></a>

```json
{
  "items": [
    {
      "bizName": "string",
      "createdBy": "string",
      "id": 0,
      "name": "string",
      "relateItems": [
        {
          "bizName": "string",
          "createdBy": "string",
          "id": 0,
          "name": "string",
          "relateItems": [
            {}
          ],
          "type": "DIMENSION"
        }
      ],
      "type": "DIMENSION"
    }
  ]
}

```

AppConfigReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|items|[[ItemReq](#schemaitemreq)]|false|none||none|

<h2 id="tocS_Aggregator">Aggregator</h2>

<a id="schemaaggregator"></a>
<a id="schema_Aggregator"></a>
<a id="tocSaggregator"></a>
<a id="tocsaggregator"></a>

```json
{
  "alias": "string",
  "args": [
    "string"
  ],
  "column": "string",
  "func": "AVG",
  "nameCh": "string"
}

```

Aggregator

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|alias|string|false|none||none|
|args|[string]|false|none||none|
|column|string|true|none||none|
|func|string|false|none||none|
|nameCh|string|false|none||none|

#### 枚举值

|属性|值|
|---|---|
|func|AVG|
|func|COUNT|
|func|COUNT_DISTINCT|
|func|DISTINCT|
|func|MAX|
|func|MIN|
|func|PERCENTILE|
|func|RATIO_OVER|
|func|RATIO_ROLL|
|func|SUM|
|func|TOPN|
|func|UNKNOWN|

<h2 id="tocS_AggregateInfo">AggregateInfo</h2>

<a id="schemaaggregateinfo"></a>
<a id="schema_AggregateInfo"></a>
<a id="tocSaggregateinfo"></a>
<a id="tocsaggregateinfo"></a>

```json
{
  "metricInfos": [
    {
      "date": "string",
      "dimension": "string",
      "name": "string",
      "statistics": {
        "property1": "string",
        "property2": "string"
      },
      "value": "string"
    }
  ]
}

```

AggregateInfo

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|metricInfos|[[MetricInfo](#schemametricinfo)]|false|none||none|

<h2 id="tocS_AgentRes">AgentRes</h2>

<a id="schemaagentres"></a>
<a id="schema_AgentRes"></a>
<a id="tocSagentres"></a>
<a id="tocsagentres"></a>

```json
{
  "agentConfig": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "dataSetIds": [
    0
  ],
  "description": "string",
  "enableSearch": 0,
  "examples": [
    "string"
  ],
  "id": 0,
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "multiTurnConfig": {
    "enableMultiTurn": true
  },
  "name": "string",
  "status": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "visualConfig": {
    "enableSimpleMode": true,
    "showDebugInfo": true
  }
}

```

AgentRes

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|agentConfig|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|dataSetIds|[integer]|false|none||none|
|description|string|false|none||none|
|enableSearch|integer(int32)|false|none||none|
|examples|[string]|false|none||none|
|id|integer(int32)|false|none||none|
|llmConfig|[LLMConfig](#schemallmconfig)|false|none||none|
|multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none||none|
|name|string|false|none||none|
|status|integer(int32)|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|
|visualConfig|[VisualConfig](#schemavisualconfig)|false|none||none|

<h2 id="tocS_Tag">Tag</h2>

<a id="schematag"></a>
<a id="schema_Tag"></a>
<a id="tocStag"></a>
<a id="tocstag"></a>

```json
{
  "id": 1,
  "name": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||标签ID编号|
|name|string|false|none||标签名称|

<h2 id="tocS_AgentReq">AgentReq</h2>

<a id="schemaagentreq"></a>
<a id="schema_AgentReq"></a>
<a id="tocSagentreq"></a>
<a id="tocsagentreq"></a>

```json
{
  "agentConfig": "string",
  "createdAt": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "description": "string",
  "enableSearch": 0,
  "examples": [
    "string"
  ],
  "id": 0,
  "llmConfig": {
    "apiKey": "string",
    "baseUrl": "string",
    "modelName": "string",
    "provider": "string",
    "temperature": 0,
    "timeOut": 0
  },
  "multiTurnConfig": {
    "enableMultiTurn": true
  },
  "name": "string",
  "status": 0,
  "updatedAt": "2019-08-24T14:15:22Z",
  "updatedBy": "string",
  "visualConfig": {
    "enableSimpleMode": true,
    "showDebugInfo": true
  }
}

```

AgentReq

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|agentConfig|string|false|none||none|
|createdAt|string(date-time)|false|none||none|
|createdBy|string|false|none||none|
|description|string|false|none||none|
|enableSearch|integer(int32)|false|none||none|
|examples|[string]|false|none||none|
|id|integer(int32)|false|none||none|
|llmConfig|[LLMConfig](#schemallmconfig)|false|none||none|
|multiTurnConfig|[MultiTurnConfig](#schemamultiturnconfig)|false|none||none|
|name|string|false|none||none|
|status|integer(int32)|false|none||none|
|updatedAt|string(date-time)|false|none||none|
|updatedBy|string|false|none||none|
|visualConfig|[VisualConfig](#schemavisualconfig)|false|none||none|

<h2 id="tocS_Category">Category</h2>

<a id="schemacategory"></a>
<a id="schema_Category"></a>
<a id="tocScategory"></a>
<a id="tocscategory"></a>

```json
{
  "id": 1,
  "name": "string"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||分组ID编号|
|name|string|false|none||分组名称|

<h2 id="tocS_ActionInfo">ActionInfo</h2>

<a id="schemaactioninfo"></a>
<a id="schema_ActionInfo"></a>
<a id="tocSactioninfo"></a>
<a id="tocsactioninfo"></a>

```json
{
  "out": [
    {}
  ]
}

```

ActionInfo

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|out|[object]|false|none||none|

<h2 id="tocS_Pet">Pet</h2>

<a id="schemapet"></a>
<a id="schema_Pet"></a>
<a id="tocSpet"></a>
<a id="tocspet"></a>

```json
{
  "id": 1,
  "category": {
    "id": 1,
    "name": "string"
  },
  "name": "doggie",
  "photoUrls": [
    "string"
  ],
  "tags": [
    {
      "id": 1,
      "name": "string"
    }
  ],
  "status": "available"
}

```

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|true|none||宠物ID编号|
|category|[Category](#schemacategory)|true|none||分组|
|name|string|true|none||名称|
|photoUrls|[string]|true|none||照片URL|
|tags|[[Tag](#schematag)]|true|none||标签|
|status|string|true|none||宠物销售状态|

#### 枚举值

|属性|值|
|---|---|
|status|available|
|status|pending|
|status|sold|

