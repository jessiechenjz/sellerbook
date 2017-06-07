### 获取买手订单列表 （ymatou.order.list.get）

---

### 接口描述

* 获取订单列表

### 业务参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)


### 请求参数

| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| order\_status | String | 否 | 1,2,3 | 订单状态(逗号分隔多个状态,传空为全状态) 未付款:ORDER_ESTABLISH(1),已付款待接单:ACCOUNT_PAID(2),已发货:SHIPPED(3),确认收货:RECEIVED(4),买家取消订单:USER_ACCEPT_CANCEL(12),卖家取消订单:SELLER_ACCEPT_CANCEL(13),系统自动取消:SYSTEM_CANCEL(18),已接单:SELLER_ACCEPT(17)  |
| date\_type | Integer | 是 | 1 | 时间排序类型 1.订单生成时间  2.订单付款时间  3. 订单发货时间 |
| sort\_type | Integer | 是 | 1 | 0.倒序  1.升序 |
| start\_date | DateTime | 是 | 2017-01-02 00:00:00 | 查询开始时间 |
| end\_date | DateTime | 是 | 2017-03-30 23:59:59 | 查询结束时间 |
| page\_no | Integer | 是 | 3 | 请求分页页码(大于0) |
| page\_rows | Integer | 是 | 50 | 每页记录数量(大于0且小于等于100 )|

### 返回参数

| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| code |  |  |  |  |
| message |  |  |  |  |
| orders\_info | JSON Object |  |  |  OrderInfo\[\] JSON报文体|
|  |  |  |  |  |


### 错误信息描述



#### 示例报文

* url：http://open.ymatou.com/apigateway/v1?app_id=CgZcxYhQaCXOt31YQe&method=ymatou.order.list.get
* 请求报文:    
<br  />
{"app_id":"CgZcxYhQaCXOt31YQe","method":"ymatou.order.list.get","sign_method":"MD5","auth_code":"JmhUXrDRP4Mw7zEHs2p3iQJ4T7mUOGr3","timestamp":"2017-06-07 14:51:21","sign":"7A3C0386906D77997A1B1AA4947A996D","nonce_str":"3376836157552545834527182511616","biz_content":"{\"order_status\":\"2\",\"date_type\":1,\"sort_type\":1,\"start_date\":\"2017-06-02 14:51:21\",\"end_date\":\"2017-06-07 14:51:21\",\"page_no\":1,\"page_rows\":10}"}
* 返回报文:   
<br  />
