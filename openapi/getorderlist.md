### 获取买手订单列表 （ymatou.order.list.get）

---

### 接口描述

* 获取单个订单的信息

### 业务参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)


### 请求参数

| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| date\_type | Integer | 是 | 1 | 1  订单生成时间  <br> 2 订单付款时间 <br> 3. 订单发货时间  |
| order\_status | Integer | 是 | 1:2:3 | 订单状态 |
| date\_type | Integer | 是 | 1 | 1.订单生成时间  2.订单付款时间  3. 订单发货时间 |
| start\_date | DateTime | 是 | 2017-01-02 00:00:00 | 查询开始时间 |
| end\_date | DateTime | 是 | 2017-03-30 23:59:59 | 查询结束时间 |
| page\_no | Integer | 是 | 3 | 请求分页页码 |
| page\_rows | Integer | 是 | 50 | 每页记录数量 |

### 返回参数

| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| code |  |  |  |  |
| message |  |  |  |  |
| orders\_info | OrderInfo\[\] |  |  |  |
|  |  |  |  |  |


### 错误信息描述



