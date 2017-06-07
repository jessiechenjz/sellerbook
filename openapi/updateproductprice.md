### 更新商品价格 （ymatou.sku.price.update）

---

### 接口描述

* 按商家商品编码同步商品的价格信息，支持批量改价


### 业务参数

| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| sku\_prices |SkuPrice[]  |  |  |  待更新sku及其价格列表|

* 数据类型（SkuPrice）

| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| outer_sku_id |String |  是|  |  SkuId|
| product_price |BigDecimal |  是|  |  商品原价，小数点后最多2位，必须大于0|
| product_vip_price |BigDecimal |  否|  |  商品VIP价，小数点后最多2位，必须大于等于0（0代表无VIP价）|
| product_newuser_price |BigDecimal |  否|  |  商品新客价，小数点后最多2位，必须大于等于0（0代表新客价）|


#### 返回参数


| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String | 更新库存成功 | 接口调用返回信息 |
| content | JSON Object |  | 更新结果明细. BizResult的JSON报文体 |

* 数据类型(BizResult）

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| results | SkuResult[] |  | 更新明细列表 |

* 数据类型（SkuResult）

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| success | Boolean | true | 是否更新成功 |
| msg | String | 更新成功 | 更新结果描述 |
| outer_sku_id | String | 393992 | SkuId |

### 业务响应码描述
无


#### 示例报文

* url：http://open.ymatou.com/apigateway/v1?app_id=CgZcxYhQaCXOt31YQe&method=ymatou.sku.price.update
* 请求报文:    
<br  />


```
{
	"app_id": "CgZcxYhQaCXOt31YQe",
	"method": "ymatou.sku.price.update",
	"sign_method": "MD5",
	"auth_code": "JmhUXrDRP4Mw7zEHs2p3iQJ4T7mUOGr3",
	"timestamp": "2017-06-07 14:43:58",
	"sign": "F945939585DFCD03EB14A3C2D9A93E87",
	"nonce_str": "1008683644611559580007241663284",
	"biz_content": "{\"sku_prices\":[{\"outer_sku_id\":\"SKU1186243233\",\"product_price\":3616.18,\"product_vip_price\":190.09,\"product_newuser_price\":18.38},{\"outer_sku_id\":\"SKU762135311\",\"product_price\":2052.64,\"product_vip_price\":492.56,\"product_newuser_price\":48.62},{\"outer_sku_id\":\"SKU1104016908\",\"product_price\":5548.32,\"product_vip_price\":961.57,\"product_newuser_price\":63.70},{\"outer_sku_id\":\"SKU433961823\",\"product_price\":4194.38,\"product_vip_price\":710.87,\"product_newuser_price\":94.46},{\"outer_sku_id\":\"SKU867183967\",\"product_price\":7127.79,\"product_vip_price\":282.46,\"product_newuser_price\":1.53},{\"outer_sku_id\":\"SKU482472743\",\"product_price\":516.54,\"product_vip_price\":828.61,\"product_newuser_price\":95.28},{\"outer_sku_id\":\"SKU83659384\",\"product_price\":4106.42,\"product_vip_price\":194.65,\"product_newuser_price\":2.00},{\"outer_sku_id\":\"SKU411660022\",\"product_price\":4505.02,\"product_vip_price\":624.28,\"product_newuser_price\":29.38}]}"
}
```



* 返回报文:   
<br  />


```
{
	"code": "0000",
	"message": "操作成功",
	"content": {
		"results": [{
			"msg": "成功",
			"outer_sku_id": "SKU1186243233",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU762135311",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU1104016908",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU433961823",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU867183967",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU482472743",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU83659384",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU411660022",
			"success": true
		}]
	}
}
```


