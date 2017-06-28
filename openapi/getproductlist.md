### 获取买手商品列表 （ymatou.products.list.get）

---

### 接口描述

* 获取买手商品列表

| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| productid_list|String[]|否| | 产品id列表，最多100个|
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
| product_infos | ProductInfo[] |  | 商品信息   |
| total_count | Integer | 是 |  总行数 |


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


*  类型描述（SkuInfo）  

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
| properties |  propertieInfo[]|  |SKU属性信息 |

*  类型描述（propertieInfo）  

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| name | String |  | 名称 |
| value | String |  | 值  |
| pic_url | String |  | 规格图片链接 |


#### 示例报文


#### 示例报文

* url：https://open.ymatou.com/apigateway/v1?app_id=aBNgc6RkDwYkdckavF&method=ymatou.products.list.get
* 请求报文:    
<br  />


```
{
	"app_id" : "aBNgc6RkDwYkdckavF",
	"method" : "ymatou.products.list.get",
	"sign_method" : "MD5",
	"auth_code" : "8UyV9ryKksAAlPwpduneO5rJ4l369yDT",
	"timestamp" : "2017-06-14 10:29:14",
	"sign" : "8902FC85F63E434B68BB484975A51E7A",
	"nonce_str" : "0370396742786436508050743559877",
	"biz_content" : "{\"productid_list\":[\"2b1809ac-3b1e-4ddf-a0f3-00c97e507a23\",\"0d46b251-9d91-42fb-b67e-112023fc9d6a\"],\"page_no\":1,\"page_rows\":10}"
}
```


* 返回报文:   
<br  />


```
{
	"code" : "0000",
	"message" : "",
	"content" : {
		"total_count" : 4,
		"product_infos" : [{
				"category_name" : "按键手机",
				"product_url" : "www.ymatou.com/product/0d46b251-9d91-42fb-b67e-112023fc9d6a.html",
				"skus" : [{
						"extra_info" : null,
						"weight_unit" : 0,
						"price" : 10.00,
						"stock_num" : 300,
						"weight" : 0.0,
						"new_price" : 8.00,
						"sku_id" : "e6461b0f-814a-4810-b1a4-0b0d5c3a5759",
						"used" : true,
						"vip_price" : 9.00,
						"outer_id" : "shangpinbianma123456",
						"properties" : null
					}
				],
				"create_time" : "2017-06-14 10:38:21",
				"listing_start_time" : "2017-06-14 10:38:21",
				"brand_name" : "IBM",
				"product_name" : "自动化测试_立即上架商品 06-14 10:29:07",
				"brand_id" : 10145,
				"product_images" : ["http://pc1.img.ymatou.com/G01/shangou/M00/2A/17/rBBlD1eqnq-AEvUHAANhqAY9_CQ839_n_w_o.jpg"],
				"update_time" : "2017-06-14 10:38:21",
				"category_id" : 1003,
				"delivery_type" : 2,
				"product_id" : "0d46b251-9d91-42fb-b67e-112023fc9d6a",
				"listing_end_time" : "2017-06-21 10:38:21",
				"fbx" : false
			}, {
				"category_name" : "按键手机",
				"product_url" : "www.ymatou.com/product/2b1809ac-3b1e-4ddf-a0f3-00c97e507a23.html",
				"skus" : [{
						"extra_info" : null,
						"weight_unit" : 0,
						"price" : 10.00,
						"stock_num" : 300,
						"weight" : 0.0,
						"new_price" : 8.00,
						"sku_id" : "17e2d4b2-bab7-4e3d-abe0-e7d069c57db0",
						"used" : true,
						"vip_price" : 9.00,
						"outer_id" : "shangpinbianma123456",
						"properties" : null
					}
				],
				"create_time" : "2017-06-14 10:38:18",
				"listing_start_time" : "2017-06-14 10:38:18",
				"brand_name" : "IBM",
				"product_name" : "自动化测试_立即上架商品 06-14 10:29:04",
				"brand_id" : 10145,
				"product_images" : ["http://pc1.img.ymatou.com/G01/shangou/M00/2A/17/rBBlD1eqnq-AEvUHAANhqAY9_CQ839_n_w_o.jpg"],
				"update_time" : "2017-06-14 10:38:18",
				"category_id" : 1003,
				"delivery_type" : 2,
				"product_id" : "2b1809ac-3b1e-4ddf-a0f3-00c97e507a23",
				"listing_end_time" : "2017-06-21 10:38:18",
				"fbx" : false
			}
				],
				"create_time" : "2017-06-14 10:38:17",
				"listing_start_time" : "2017-06-14 10:38:17",
				"brand_name" : "IBM",
				"product_name" : "自动化测试_立即上架商品 06-14 10:29:03",
				"brand_id" : 10145,
				"product_images" : ["http://pc1.img.ymatou.com/G01/shangou/M00/2A/17/rBBlD1eqnq-AEvUHAANhqAY9_CQ839_n_w_o.jpg"],
				"update_time" : "2017-06-14 10:38:17",
				"category_id" : 1003,
				"delivery_type" : 2,
				"product_id" : "6e05b989-6f99-4cc1-a64e-65168324961b",
				"listing_end_time" : "2017-06-21 10:38:17",
				"fbx" : false
			}
		]
	}
}
```