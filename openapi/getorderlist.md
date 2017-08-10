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
 	"timestamp": "2017-08-10 12:39:43",
 	"sign": "57499A817AD5C2EE28182177A44D30C3",
 	"nonce_str": "4639249722857931507841291306017",
 	"biz_content": "{\"order_status\":\"3\",\"date_type\":1,\"sort_type\":1,\"start_date\":\"2017-08-09 12:39:43\",\"end_date\":\"2017-08-10 12:39:43\",\"page_no\":1,\"page_rows\":10,\"needs_delivery_info\":true}"
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
				"order_time": "2017-08-09 16:20:44",
				"buyer_id": "autotest_Dw8x9EvLqS",
				"domestic_delivered": false,
				"receiver_state": null,
				"m_coupon_discount": 7.98,
				"order_status": 3,
				"trade_id": "2133467514",
				"receiver_zip": "200001",
				"receiver_name": "钱翼",
				"pay_type": null,
				"payment": 563.11,
				"p_coupon_discount": 6.91,
				"accept_time": "2017-08-09 16:20:51",
				"shipping_time": "2017-08-09 16:20:53",
				"seller_id": "wesper",
				"cancel_time": null,
				"amount": 578.00,
				"seller_memo": null,
				"paid_time": "2017-08-09 16:20:50",
				"receiver_mobile": "13673201578",
				"shipping_fee": 0.00,
				"buyer_remark": "尽快发货",
				"order_items_info": [{
						"outer_sku_id": null,
						"m_adjust_discount": 0.00,
						"refund_status": null,
						"num": 1,
						"sku_id": "f0e13532-94df-4bb5-8134-85aca519161a",
						"sku_properties_name": "06f25e0c-e431-44ae-8a07-4d0bc824e3bd#尺寸:951a814e-2ded-4241-b9a0-91b2cd9a44fd#6,d2f663ea-3214-4344-abce-a8eaffcc43ce#颜色:f3ed3ad7-a084-450b-b698-256542963306#红色",
						"refund_id": null,
						"product_title": "自动化测试商品+7127588616",
						"order_item_id": "598ac5e6ef2e8868031330e2",
						"shipping_fee": 0.00,
						"m_coupon_discount": 0.52,
						"delivery_type": 7,
						"price": 38.00,
						"product_id": "41f5e894-dc8f-412e-bc64-e11ed388e9c1",
						"refund_num": null,
						"payment": 37.03,
						"p_coupon_discount": 0.45,
						"order_id": 2138527573,
						"m_promotion_discount": 0.00
					}
				],
				"delivery_info": [{
						"logistics_company_code": "",
						"tracking_number": "DB683214922US",
						"delivery_time": 1502266852031,
						"logistics_type": 1
					}
				],
				"id_cards": null,
				"receiver_address": "灵石路695号3号楼1404室",
				"receiver_phone": "",
				"order_id": 2138527573,
				"m_promotion_discount": 0.00
			}, 
			...
		]
	}
}
```