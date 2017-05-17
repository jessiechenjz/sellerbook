### 平台订单发货 （ymatou.order.deliver）

---

### 接口描述

* 录入平台物流单号，给平台的订单发货

### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)


### 业务参数

* 请求参数

| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| deliver_orders |DeliverOrder[]  | | | 待发货的订单物流信息 |
| order\_id | long | 是 | 1729299393 | 待发货的订单编号 |
| logistics\_company\_id | String | 是 | 001 | 平台物流公司标识 |
| tracking\_number | String | 是 | 10010993S | 物流面单号 |

### 返回参数

* 返回类型 

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0 | 返回码 |
| message | String | 发货成功 | 返回结果描述 |

### 错误信息描述