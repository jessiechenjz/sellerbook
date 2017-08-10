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
| date\_type | Integer | 是 | 1 | 时间筛选和排序类型 1.订单生成时间  2.订单付款时间  3.订单发货时间  4.接单时间  |
| sort\_type | Integer | 是 | 1 | 0.倒序  1.升序 | 
| start\_date | DateTime | 是 | 2017-01-02 00:00:00 | 查询开始时间 |
| end\_date | DateTime | 是 | 2017-03-30 23:59:59 | 查询结束时间 |
| page\_no | Integer | 是 | 3 | 请求分页页码(大于0) |
| page\_rows | Integer | 是 | 50 | 每页记录数量(大于0且小于等于100 )|
| needs\_delivery\_info | Boolean | 否 | true | 是否需要发货信息(默认否 ) |

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
	"app_id": "CgZcxYhQaCXOt31YQe",
	"method": "ymatou.order.list.get",
	"sign_method": "MD5",
	"auth_code": "JmhUXrDRP4Mw7zEHs2p3iQJ4T7mUOGr3",
	"timestamp": "2017-08-10 17:45:15",
	"sign": "1A948C3B6847AAACDC1FCBBFAD139691",
	"nonce_str": "5569277264602105594588084588512",
	"biz_content": "{\"order_status\":\"3\",\"date_type\":1,\"sort_type\":1,\"start_date\":\"2017-08-09 17:45:15\",\"end_date\":\"2017-08-10 17:45:15\",\"page_no\":1,\"page_rows\":10,\"needs_delivery_info\":true}"
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
				"payment_order_no": null,
				"m_adjust_discount": 0.00,
				"receiver_email": "tCj3lEq3Ogzt@163.com",
				"order_time": "2017-08-09 17:47:02",
				"buyer_id": "autotest_Dw8x9EvLqS",
				"domestic_delivered": false,
				"receiver_state": null,
				"m_coupon_discount": 8.46,
				"order_status": 3,
				"trade_id": "2133467589",
				"receiver_zip": "200001",
				"receiver_name": "钱翼",
				"pay_type": null,
				"payment": 585.21,
				"p_coupon_discount": 7.33,
				"accept_time": "2017-08-09 17:47:11",
				"shipping_time": "2017-08-09 17:47:17",
				"seller_id": "wesper",
				"cancel_time": null,
				"amount": 601.00,
				"seller_memo": null,
				"paid_time": "2017-08-09 17:47:11",
				"receiver_mobile": "13673201578",
				"shipping_fee": 0.00,
				"buyer_remark": "尽快发货",
				"order_items_info": [{
						"outer_sku_id": null,
						"m_adjust_discount": 0.00,
						"refund_status": null,
						"num": 3,
						"sku_id": "77c76165-2ecc-4d45-aeb2-b3889e778b1d",
						"sku_properties_name": "06f25e0c-e431-44ae-8a07-4d0bc824e3bd#尺寸:951a814e-2ded-4241-b9a0-91b2cd9a44fd#6,d2f663ea-3214-4344-abce-a8eaffcc43ce#颜色:f3ed3ad7-a084-450b-b698-256542963306#红色",
						"refund_id": null,
						"product_title": "自动化测试商品+9072908752",
						"order_item_id": "598ada20ef2e886803133a87",
						"shipping_fee": 0.00,
						"m_coupon_discount": 2.28,
						"delivery_type": 7,
						"price": 54.00,
						"product_id": "84794c53-35d8-4071-9805-fc87a08ebb0c",
						"refund_num": null,
						"payment": 157.75,
						"p_coupon_discount": 1.97,
						"order_id": 2138527683,
						"m_promotion_discount": 0.00
					}, {
						"outer_sku_id": null,
						"m_adjust_discount": 0.00,
						"refund_status": null,
						"num": 2,
						"sku_id": "a29a25a1-1bd2-4b8a-bb11-e3e9e930467f",
						"sku_properties_name": "06f25e0c-e431-44ae-8a07-4d0bc824e3bd#尺寸:951a814e-2ded-4241-b9a0-91b2cd9a44fd#6,d2f663ea-3214-4344-abce-a8eaffcc43ce#颜色:f3ed3ad7-a084-450b-b698-256542963306#红色",
						"refund_id": null,
						"product_title": "自动化测试商品+2838317599",
						"order_item_id": "598ada20ef2e886803133a88",
						"shipping_fee": 0.00,
						"m_coupon_discount": 1.88,
						"delivery_type": 7,
						"price": 67.00,
						"product_id": "11edd10c-6612-4593-af81-9aca21b53c67",
						"refund_num": null,
						"payment": 130.49,
						"p_coupon_discount": 1.63,
						"order_id": 2138527683,
						"m_promotion_discount": 0.00
					}, {
						"outer_sku_id": null,
						"m_adjust_discount": 0.00,
						"refund_status": null,
						"num": 5,
						"sku_id": "d375539c-6b13-456d-8e2b-c0e9da27e2e2",
						"sku_properties_name": "06f25e0c-e431-44ae-8a07-4d0bc824e3bd#尺寸:951a814e-2ded-4241-b9a0-91b2cd9a44fd#6,d2f663ea-3214-4344-abce-a8eaffcc43ce#颜色:f3ed3ad7-a084-450b-b698-256542963306#红色",
						"refund_id": null,
						"product_title": "自动化测试商品+9739491439",
						"order_item_id": "598ada20ef2e886803133a89",
						"shipping_fee": 0.00,
						"m_coupon_discount": 4.30,
						"delivery_type": 7,
						"price": 61.00,
						"product_id": "779173d8-4179-482a-bf36-e33885783815",
						"refund_num": null,
						"payment": 296.97,
						"p_coupon_discount": 3.73,
						"order_id": 2138527683,
						"m_promotion_discount": 0.00
					}
				],
				"delivery_info": [{
						"logistics_company_code": "",
						"tracking_number": "DB683214922US",
						"delivery_time": "2017-08-09 17:47:15",
						"logistics_type": 1
					}
				],
				"id_cards": null,
				"receiver_address": "灵石路695号3号楼1404室",
				"receiver_phone": "",
				"order_id": 2138527683,
				"m_promotion_discount": 0.00
			}
			...
		]
	}
}
```