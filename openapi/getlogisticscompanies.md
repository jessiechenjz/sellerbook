### 获取买手可用物流公司列表 （ymatou.logistics.companies.get）

---

### 接口描述

* 获取买手可用的平台物流公司，用于发货接口，可按国家维度查询

### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)


### 业务参数

无

### 返回参数

* 返回类型 （**LogisticsCompany**）

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code |  |  |  |
| message |  |  |  |
| logistics\_companies[] |  |  |  |
| code | String | A003 | 物流公司平台代码 |
| short\_name | String | shunfeng | 物流公司简称 |
| name | String | 顺丰速递 | 物流公司名称 |

### 错误信息描述