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

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String |  |  |
| content | JSON Object |  |  |

*  类型描述

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| orders\_info | OrderInfo[] |  |  |  

*  类型描述 \(OrderInfo\)
<br/>见ymatou.order.list.get


### 错误信息描述



#### 示例报文

* url：https://open.ymatou.com/apigateway/v1?app_id=CgZcxYhQaCXOt31YQe&method=ymatou.order.list.get
* 请求报文:    
<br  />


```
{
	"app_id": "aBNgc6RkDwYkdckavF",
	"method": "ymatou.order.list.get",
	"sign_method": "MD5",
	"auth_code": "8UyV9ryKksAAlPwpduneO5rJ4l369yDT",
	"timestamp": "2017-06-07 15:20:18",
	"sign": "33D7771F1FB23E95BB492A3B754F1911",
	"nonce_str": "4448184147744143703122180081252",
	"biz_content": "{\"order_status\":\"2\",\"date_type\":1,\"sort_type\":1,\"start_date\":\"2017-06-02 15:20:18\",\"end_date\":\"2017-06-07 15:20:18\",\"page_no\":1,\"page_rows\":3}"
}
```


* 返回报文:   
<br  />


```
{
	"code": "0000",
	"message": null,
	"content": {
		"orders_info": [{
			"m_adjust_discount": 0.00,
			"receiver_email": "tCj3lEq3Ogzt@163.com",
			"order_time": "2017-06-05 10:49:18",
			"buyer_id": "autotest_Dw8x9EvLqS",
			"receiver_state": null,
			"m_coupon_discount": 0.00,
			"order_status": 2,
			"trade_id": "14179563",
			"receiver_zip": "200001",
			"receiver_name": "李四",
			"payment": 41.00,
			"p_coupon_discount": 0.00,
			"shipping_time": null,
			"seller_id": "wesper",
			"cancel_time": null,
			"amount": 20.00,
			"seller_memo": null,
			"paid_time": "2017-06-05 10:49:24",
			"receiver_mobile": "13100000001",
			"shipping_fee": 21.00,
			"buyer_remark": "ymt autotest",
			"order_items_info": [{
				"outer_sku_id": null,
				"m_adjust_discount": 0.00,
				"refund_status": null,
				"num": 2,
				"sku_id": "42f8cb44-271d-4e96-a2b3-60ae34dfd21a",
				"sku_properties_name": "06f25e0c-e431-44ae-8a07-4d0bc824e3bd#尺寸:951a814e-2ded-4241-b9a0-91b2cd9a44fd#6,d2f663ea-3214-4344-abce-a8eaffcc43ce#颜色:f3ed3ad7-a084-450b-b698-256542963306#红色",
				"refund_id": null,
				"product_title": "自动化测试商品",
				"order_item_id": "5934c6bdef2e882cae981d60",
				"shipping_fee": 21.00,
				"m_coupon_discount": 0.00,
				"price": 10.00,
				"product_id": "d3d3efe5-96d4-48d7-9480-e8c66e881c0e",
				"refund_num": null,
				"payment": 20.00,
				"p_coupon_discount": 0.00,
				"order_id": 112531338,
				"m_promotion_discount": 0.00
			}],
			"receiver_address": "上海市闸北区灵石路636号",
			"receiver_phone": "021-51002100",
			"order_id": 112531338,
			"m_promotion_discount": 0.00
		}, {
			"m_adjust_discount": 0.00,
			"receiver_email": "tCj3lEq3Ogzt@163.com",
			"order_time": "2017-06-05 10:49:48",
			"buyer_id": "autotest_Dw8x9EvLqS",
			"receiver_state": null,
			"m_coupon_discount": 0.00,
			"order_status": 2,
			"trade_id": "14179584",
			"receiver_zip": "200001",
			"receiver_name": "钱翼",
			"payment": 396.00,
			"p_coupon_discount": 0.00,
			"shipping_time": null,
			"seller_id": "wesper",
			"cancel_time": null,
			"amount": 337.00,
			"seller_memo": null,
			"paid_time": "2017-06-05 10:49:50",
			"receiver_mobile": "13673201578",
			"shipping_fee": 59.00,
			"buyer_remark": "尽快发货",
			"order_items_info": [{
				"outer_sku_id": null,
				"m_adjust_discount": 0.00,
				"refund_status": null,
				"num": 2,
				"sku_id": "6bfd136e-36fc-4848-8869-d2d25a357445",
				"sku_properties_name": "06f25e0c-e431-44ae-8a07-4d0bc824e3bd#尺寸:951a814e-2ded-4241-b9a0-91b2cd9a44fd#6,d2f663ea-3214-4344-abce-a8eaffcc43ce#颜色:f3ed3ad7-a084-450b-b698-256542963306#红色",
				"refund_id": null,
				"product_title": "自动化测试商品+5809205607",
				"order_item_id": "5934c6dbef2e882cae981dfe",
				"shipping_fee": 25.91,
				"m_coupon_discount": 0.00,
				"price": 74.00,
				"product_id": "e3db3461-7cfb-444a-94aa-1d189f5f1e96",
				"refund_num": null,
				"payment": 148.00,
				"p_coupon_discount": 0.00,
				"order_id": 112531353,
				"m_promotion_discount": 0.00
			}, {
				"outer_sku_id": null,
				"m_adjust_discount": 0.00,
				"refund_status": null,
				"num": 1,
				"sku_id": "72b6510e-b033-4366-9643-79bdf3d122f3",
				"sku_properties_name": "06f25e0c-e431-44ae-8a07-4d0bc824e3bd#尺寸:951a814e-2ded-4241-b9a0-91b2cd9a44fd#6,d2f663ea-3214-4344-abce-a8eaffcc43ce#颜色:f3ed3ad7-a084-450b-b698-256542963306#红色",
				"refund_id": null,
				"product_title": "自动化测试商品+3752854981",
				"order_item_id": "5934c6dbef2e882cae981dff",
				"shipping_fee": 6.82,
				"m_coupon_discount": 0.00,
				"price": 39.00,
				"product_id": "8dff9498-f4e8-4854-8907-88ee5750a006",
				"refund_num": null,
				"payment": 39.00,
				"p_coupon_discount": 0.00,
				"order_id": 112531353,
				"m_promotion_discount": 0.00
			}
		}]
	}
}
```