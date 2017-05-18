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
| order_id | long | 是 | 1729299393 | 待发货的订单编号 |
| logistics_company\_id | String | 是 | 001 | 平台物流公司标识 |
| tracking_number | String | 是 | 10010993S | 物流面单号 |
| is_domestic_delivery | boolean | 是 | true | 是否国内段发货 |

### 返回参数

* 返回类型 

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| results | results[] |  | 发货结果 |
| order_id | long | 0 | 订单号 |
| exec_success | boolean | true | 是否执行成功 |
| msg | string |  | 处理信息 |

### 错误信息描述