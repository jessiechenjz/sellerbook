### 获取买手可用物流公司列表 （ymatou.logistics.companies.get）

---

### 接口描述

* 获取买手可用的平台物流公司，用于发货接口

### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)


### 业务参数

无

### 返回参数

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String | 更新库存成功 | 接口调用返回信息 |
| content | JSON Object |  | 结果明细. |

* 数据类型(BizResult）

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| logistics_companies | LogisticsCompany[] |  | 更新明细列表 |

* 数据类型（LogisticsCompany）

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| company_code | String | A003 | 物流公司平台代码 |
| short_name | String | shunfeng | 物流公司简称 |
| company_name | String | 顺丰速递 | 物流公司名称 |