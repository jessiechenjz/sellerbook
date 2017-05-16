### 获取买手订单列表 （ymatou.order.list.get）

---

### 接口描述

* 获取单个订单的信息

### 业务参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)


### 请求参数

| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| order\_status | String | 是 | 1:2:3 | 订单状态  <br> ORDER\_WAIT\_PAY:  等待支付 <br> ORDER\_PAID: 订单已支付 <br> WAIT\_SELLER\_SEND\_GOODS 订单买手发货 <br> WAIT\_BUYER\_CONFIRM\_GOODS 等待买家确认收货  <br> ORDER\_FINISH：订单完成 <br> ORDER\_CANCEL:订单取消 |
| date\_type | Integer | 是 | 1 | 1  订单生成时间  <br> 2 订单付款时间 <br> 3. 订单发货时间  |
| start\_date | DateTime | 是 | 2017-01-02 00:00:00 | 查询开始时间 |
| end\_date | DateTime | 是 | 2017-03-30 23:59:59 | 查询结束时间 |
| page\_no | Integer | 是 | 3 | 请求分页代码 |
| page\_rows | Integer | 是 | 50 | 每页的记录数量 |

### 返回参数

| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| code |  |  |  |  |
| message |  |  |  |  |
| order\_info | OrderInfo\[\] |  |  |  |
|  |  |  |  |  |


### 错误信息描述



