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

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String |  |  |
| content | JSON Object |  |  |



*  类型描述

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| Product\_Info | ProductInfo |  | 商品信息 |  



*  类型描述（ProductInfo）  

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| product_id | String |  | 商品ID |
| product\_name | String |  | 商品名称 |
| category\_id | int |  | 三级类目ID |
| category\_name | String |  | 三级类目名称 |
| brand\_id | int |  | 品牌ID |
| brand\_name | String |  | 品牌名称 |
| product\_images | String\[\] |  | 商品图片链接地址 |
| product\_url | String |  | 商品显示URL |
| create\_time | String |  | 创建时间yyyy-MM-dd HH:mm:ss |
| update\_time | String |  | 最后一次更新时间yyyy-MM-dd HH:mm:ss |
| listing\_start\_time | String |  | 上架开始时间yyyy-MM-dd HH:mm:ss |
| listing\_end\_time | String |  | 上架结束时间yyyy-MM-dd HH:mm:ss |
| delivery\_type | int |  | 商品物流方式 <br> 2. 直邮 3. 官方（贝海）直邮 4. 第三方保税 5. 官方（贝海）保税 7. 拼邮  |
| fbx | Boolean | | 是否FBX商品标识 |
| skus |SkuInfo[] |  | sku信息  |



* 类型描述（SkuInfo）  

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| sku\_id | String |  | SKU ID |
| properties | String |  | SKU属性信息 |
| outer\_id | String |  | 外部商品编码 |
| used | Boolean |  | 是否启用 |
| price | Decimal |  | 商品价格 |
| vip\_price | Decimal |  | vip商品价 |
| new\_price | Decimal |  | 新客价 |
| stock\_num | Integer |  | 库存数量 |
| weight | double |  | 规格重量 |
| weight\_unit | Int |  | 重量单位（公斤、磅） |
| extra\_info | String |  | 扩充信息 |
| properties |  PropertyInfo[]|  |SKU属性信息 |

*  类型描述（PropertyInfo）  

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| name | String |  | 名称 |
| value | String |  | 值  |
| pic_url | String |  | 规格图片链接 |



#### 示例报文

* url：http://open.ymatou.com/apigateway/v1?app_id=aBNgc6RkDwYkdckavF&method=ymatou.product.detail.get
* 请求报文:    
<br  />


```
{
	"app_id" : "aBNgc6RkDwYkdckavF",
	"method" : "ymatou.product.detail.get",
	"sign_method" : "MD5",
	"auth_code" : "8UyV9ryKksAAlPwpduneO5rJ4l369yDT",
	"timestamp" : "2017-06-14 10:33:42",
	"sign" : "51E281A8E259D382D496DA88ECA87E61",
	"nonce_str" : "5083898275981716678561226722216",
	"biz_content" : "{\"product_id\":\"883a4206-957f-409a-86e3-6aa734d1bade\"}"
}
```


* 返回报文:   
<br  />


```
{
	"code" : "0000",
	"message" : "",
	"content" : {
		"product_info" : {
			"category_name" : "按键手机",
			"product_url" : "www.ymatou.com/product/883a4206-957f-409a-86e3-6aa734d1bade.html",
			"skus" : [{
					"extra_info" : null,
					"weight_unit" : 0,
					"price" : 10.00,
					"stock_num" : 300,
					"weight" : 0.0,
					"new_price" : 8.00,
					"sku_id" : "ec21b8a1-e439-4bb4-9706-4818b3664149",
					"used" : true,
					"vip_price" : 9.00,
					"outer_id" : "shangpinbianma123456",
					"properties" : null
				}
			],
			"create_time" : "2017-06-13 15:37:16",
			"listing_start_time" : "2017-06-13 15:37:16",
			"brand_name" : "IBM",
			"product_name" : "自动化测试_立即上架商品 06-13 15:27:59",
			"brand_id" : 10145,
			"product_images" : ["http://pc1.img.ymatou.com/G01/shangou/M00/2A/17/rBBlD1eqnq-AEvUHAANhqAY9_CQ839_n_w_o.jpg"],
			"update_time" : "2017-06-13 15:37:16",
			"category_id" : 1003,
			"delivery_type" : 2,
			"product_id" : "883a4206-957f-409a-86e3-6aa734d1bade",
			"listing_end_time" : "2017-06-20 15:37:16",
			"fbx" : false
		}
	}
}
```