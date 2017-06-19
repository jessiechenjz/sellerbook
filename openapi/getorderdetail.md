### 获取买手指定订单 （ymatou.order.detail.get）

---

### 接口描述

* 获取单个订单的信息

### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)

### 业务参数

* 请求参数

| 名称 | 类型 | 是否必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| order\_id | Long | 是 | 17392939 | 订单编号 |

### 返回参数

* 返回类型 

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code |  |  |  |
| message |  |  |  |
| content | JSON Object |  |OrderInfo的JSON报文体  |

  
* 类型描述 \(OrderInfo\)

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| seller\_id | String | 洋妈咪甄选 | 买手名称 |
| order\_id | Long | 121736528 | 订单编号 |
| trade\_id | String | 232654104 | 主单号，合并支付产生的id |
| order\_status | Integer | 4 | 1 未付款:ORDER_ESTABLISH, <br> 2 已付款待接单:ACCOUNT_PAID <br> 3 已发货:SHIPPED <br> 4 确认收货:RECEIVED <br> 12 买家取消订单:USER_ACCEPT_CANCEL <br> 13 卖家取消订单:SELLER_ACCEPT_CANCEL <br> 14 系统自动取消:SYSTEM_CANCEL <br> 17 已接单:SELLER_ACCEPT |
| amount | Decimal | 200.00 | 订单金额 |
| payment | Decimal | 190.00 | 买家应付金额 |
| shipping\_fee | Decimal | 20.00 | 订单运费金额 |
| p\_coupon\_discount | Decimal | 10 | 平台优惠券分摊金额 |
| m\_coupon\_discount | Decimal | 5 | 买手优惠券分摊金额 |
| m\_promotion\_discount | Decimal | 10 | 买手促销活动分摊金额 |
| m\_adjust\_discount | Decimal |  -5.00| 买手调价金额 |
| order\_time | String |  | 下单时间 yyyy-MM-dd HH:mm:ss|
| paid\_time | String |  | 付款时间 yyyy-MM-dd HH:mm:ss|
| shipping\_time | String |  | 发货时间 yyyy-MM-dd HH:mm:ss |
| cancel\_time | String |  | 取消时间 yyyy-MM-dd HH:mm:ss|
| seller\_memo | String |  | 买手备注 |
| buyer\_remark | String |  | 买家留言 |
| buyer\_id | String | vera\_1214 | 买家id |
| receiver\_name | String | 李四 | 收件人姓名 |
| receiver\_state | String |  | 收件人国家 |
| receiver\_address | String |  | 收件人地址 |
| receiver\_zip | String |  | 收件人邮编 |
| receiver\_mobile | String |  | 收件人手机 |
| receiver\_phone | String |  | 收件人电话 |
| receiver\_email | String |  | 收件人邮箱 |
| payment\_order\_no | String | 17061511145643596 | 支付订单号 |
| pay\_type | String | Alipay | 支付类型 CmbPay:招行一网通, Alipay:支付宝, Weixin:微信, ApplePay:ApplePay|
| id\_cards | IdCard[\] | | 证件信息列表   |
| order\_items\_info | OrderItemInfo\[\] |  | 订单商品明细 |  

  
* 类型描述 \(IdCard\)

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| receiver\_id\_type | Int | 1 | 支付人证件类型 1:身份证, 2:护照  |
| receiver\_id\_no | String | 411222199701018674 | 支付人证件号 |

  
* 类型描述 \(OrderItemInfo\)

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| order\_id | Long |  | 订单号 |
| order\_item\_id | String |  | 子订单编号 |
| refund\_id | String |  | 退货退款单ID |
| refund\_status | Integer | 1 | 退货退款状态 -1审核拒绝, 0:退款审核中, 1:退款审核成功 |
| refund\_num | Integer | 1 | 退货数量 |
| sku\_id | String | 399393920-333 | SkuId |
| outer\_sku\_id | String | 3838822 | 买手商品编码 |
| product\_id | String |  | 商品Id |
| product\_title | String |  | 商品名称 |
| sku\_properties\_name | String | 颜色:红色;尺码:36 | SKU的属性值 |
| delivery\_type | int |  | 商品物流方式 <br> 2. 直邮 3. 官方（贝海）直邮 4. 第三方保税 5. 官方（贝海）保税 7. 拼邮  |
| price | Decimal | 200.00 | 商品价格 |
| num | Integer | 2 | 商品数量 |
| payment | Decimal | 380.00 | 支付金额 |
| shipping\_fee | Decimal | 20.00 | 运费分摊金额 |
| p\_coupon\_discount| Decimal|20 |	平台优惠券分摊金额 |
| m\_coupon\_discount| Decimal |10 | 买手优惠券分摊金额 |
| m\_promotion\_discount| Decimal |5 |买手促销活动分摊金额 |
| m\_adjust\_discount | Decimal | -5.00 | 买手调整分摊金额 |

### 错误信息描述



#### 示例报文

* url：http://open.ymatou.com/apigateway/v1?app_id=CgZcxYhQaCXOt31YQe&method=ymatou.order.detail.get
* 请求报文:    
<br  />

```
{
	"app_id": "aBNgc6RkDwYkdckavF",
	"method": "ymatou.order.detail.get",
	"sign_method": "MD5",
	"auth_code": "8UyV9ryKksAAlPwpduneO5rJ4l369yDT",
	"timestamp": "2017-06-07 15:19:14",
	"sign": "D69BD086ACFD99EF65F1A97D0643943D",
	"nonce_str": "5878893037341814334175660900460",
	"biz_content": "{\"order_id\":112532332}"
}
```


* 返回报文:   
<br  />


```
{
	"code": "0000",
	"message": null,
	"content": {
		"order_info": {
			"m_adjust_discount": 0.00,
			"receiver_email": null,
			"order_time": "2017-06-07 15:19:12",
			"buyer_id": null,
			"receiver_state": null,
			"m_coupon_discount": 0.00,
			"order_status": 1,
			"trade_id": "14180600",
			"receiver_zip": "100100",
			"receiver_name": "autotest",
			"payment": 443.00,
			"p_coupon_discount": 0.00,
			"shipping_time": null,
			"seller_id": null,
			"cancel_time": null,
			"amount": 401.00,
			"seller_memo": null,
			"paid_time": null,
			"receiver_mobile": "13938393374",
			"shipping_fee": 42.00,
			"buyer_remark": "尽快发货",
			"order_items_info": [{
				"outer_sku_id": null,
				"m_adjust_discount": 0.00,
				"refund_status": null,
				"num": 5,
				"sku_id": "1da69d4c-91ed-4966-b620-ad8eb9f2d05a",
				"sku_properties_name": "06f25e0c-e431-44ae-8a07-4d0bc824e3bd#尺寸:951a814e-2ded-4241-b9a0-91b2cd9a44fd#6,d2f663ea-3214-4344-abce-a8eaffcc43ce#颜色:f3ed3ad7-a084-450b-b698-256542963306#红色",
				"refund_id": null,
				"product_title": "自动化测试商品+9430290420",
				"order_item_id": "5937a903ef2e883c3a2cfb6e",
				"shipping_fee": 19.37,
				"m_coupon_discount": 0.00,
				"price": 37.00,
				"product_id": "1e58ed92-ae44-433c-8c24-086310b3456b",
				"refund_num": null,
				"payment": 185.00,
				"p_coupon_discount": 0.00,
				"order_id": 112532332,
				"m_promotion_discount": 0.00
			}, {
				"outer_sku_id": null,
				"m_adjust_discount": 0.00,
				"refund_status": null,
				"num": 4,
				"sku_id": "e4629e62-d500-4c26-a945-811a12b27268",
				"sku_properties_name": "06f25e0c-e431-44ae-8a07-4d0bc824e3bd#尺寸:951a814e-2ded-4241-b9a0-91b2cd9a44fd#6,d2f663ea-3214-4344-abce-a8eaffcc43ce#颜色:f3ed3ad7-a084-450b-b698-256542963306#红色",
				"refund_id": null,
				"product_title": "自动化测试商品+5356257995",
				"order_item_id": "5937a903ef2e883c3a2cfb6f",
				"shipping_fee": 22.63,
				"m_coupon_discount": 0.00,
				"price": 54.00,
				"product_id": "abdb3649-e910-4910-aafa-3675a40c4a8d",
				"refund_num": null,
				"payment": 216.00,
				"p_coupon_discount": 0.00,
				"order_id": 112532332,
				"m_promotion_discount": 0.00
			}],
			"receiver_address": "autotest11131113",
			"receiver_phone": "100100",
			"order_id": 112532332,
			"m_promotion_discount": 0.00
		}
	}
}
```