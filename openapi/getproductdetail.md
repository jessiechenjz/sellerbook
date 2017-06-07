### 获取单个商品详细信息 （ymatou.product.detail.get）

---

### 接口描述

* 获取单个商品详细信息

### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)

### 业务参数

* 请求参数

| 名称 | 类型 | 是否必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| product\_id | String | 是 | 0000069e-7361-4986-b626-9aa5ed61ad03 | 商品ID |

### 返回参数

* Product\_Info

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| productId | String |  | 商品ID |
| product\_name | String |  | 商品名称 |
| category\_id | int |  | 三级类目ID |
| category\_name | String |  | 三级类目名称 |
| brand\_id | int |  | 品牌ID |
| brand\_name | String |  | 品牌名称 |
| product\_images | String\[\] |  | 商品图片链接地址 |
| product\_url | String |  | 商品显示URL |
| create\_time | Datetime |  | 创建时间 |
| update\_time | Datetime |  | 最后一次更新时间 |
| listing\_start\_time | Datetime |  | 上架开始时间 |
| listing\_end\_time | Datetime |  | 上架结束时间 |
| delivery\_type | int |  | 商品物流方式  |
| is_fbx | int | | 是否FBX商品标识 |
| skus\[\] | sku信息 |  |  |
| sku\_id | String |  | SKU ID |
| outer\_id | String |  | 外部商品编码 |
| is\_used | Boolean |  | 是否启用 |
| price | Decimal |  | 商品价格 |
| vip\_price | Decimal |  | vip商品价 |
| new\_price | Decimal |  | 新客价 |
| stock\_num | Integer |  | 库存数量 |
| weight | double |  | 规格重量 |
| weight\_unit | Int |  | 重量单位（公斤、磅） |
| extra\_info | String |  | 扩充信息 |
| properties[] | SKU属性信息 |  | |
| name | String |  | 名称 |
| value | String |  | 值  |
| picUrl | String |  | 规格图片链接 |



#### 示例报文

* url：http://open.ymatou.com/apigateway/v1?app_id=CgZcxYhQaCXOt31YQe&method=ymatou.order.detail.get
* 请求报文:    
<br  />
{"app_id":"aBNgc6RkDwYkdckavF","method":"ymatou.order.detail.get","sign_method":"MD5","auth_code":"8UyV9ryKksAAlPwpduneO5rJ4l369yDT","timestamp":"2017-06-07 15:19:14","sign":"D69BD086ACFD99EF65F1A97D0643943D","nonce_str":"5878893037341814334175660900460","biz_content":"{\"order_id\":112532332}"}
* 返回报文:   
<br  />
{"code":"0000","message":null,"content":{"order_info":{"m_adjust_discount":0.00,"receiver_email":null,"order_time":"2017-06-07 15:19:12","buyer_id":null,"receiver_state":null,"m_coupon_discount":0.00,"order_status":1,"trade_id":"14180600","receiver_zip":"100100","receiver_name":"autotest","payment":443.00,"p_coupon_discount":0.00,"shipping_time":null,"seller_id":null,"cancel_time":null,"amount":401.00,"seller_memo":null,"paid_time":null,"receiver_mobile":"13938393374","shipping_fee":42.00,"buyer_remark":"尽快发货","order_items_info":[{"outer_sku_id":null,"m_adjust_discount":0.00,"refund_status":null,"num":5,"sku_id":"1da69d4c-91ed-4966-b620-ad8eb9f2d05a","sku_properties_name":"06f25e0c-e431-44ae-8a07-4d0bc824e3bd#尺寸:951a814e-2ded-4241-b9a0-91b2cd9a44fd#6,d2f663ea-3214-4344-abce-a8eaffcc43ce#颜色:f3ed3ad7-a084-450b-b698-256542963306#红色","refund_id":null,"product_title":"自动化测试商品+9430290420","order_item_id":"5937a903ef2e883c3a2cfb6e","shipping_fee":19.37,"m_coupon_discount":0.00,"price":37.00,"product_id":"1e58ed92-ae44-433c-8c24-086310b3456b","refund_num":null,"payment":185.00,"p_coupon_discount":0.00,"order_id":112532332,"m_promotion_discount":0.00},{"outer_sku_id":null,"m_adjust_discount":0.00,"refund_status":null,"num":4,"sku_id":"e4629e62-d500-4c26-a945-811a12b27268","sku_properties_name":"06f25e0c-e431-44ae-8a07-4d0bc824e3bd#尺寸:951a814e-2ded-4241-b9a0-91b2cd9a44fd#6,d2f663ea-3214-4344-abce-a8eaffcc43ce#颜色:f3ed3ad7-a084-450b-b698-256542963306#红色","refund_id":null,"product_title":"自动化测试商品+5356257995","order_item_id":"5937a903ef2e883c3a2cfb6f","shipping_fee":22.63,"m_coupon_discount":0.00,"price":54.00,"product_id":"abdb3649-e910-4910-aafa-3675a40c4a8d","refund_num":null,"payment":216.00,"p_coupon_discount":0.00,"order_id":112532332,"m_promotion_discount":0.00}],"receiver_address":"autotest11131113","receiver_phone":"100100","order_id":112532332,"m_promotion_discount":0.00}}}
