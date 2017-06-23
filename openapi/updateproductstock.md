### 更新商品库存 （ymatou.sku.stock.update）

---

#### 接口描述

* 按商家商品编码同步商品的库存信息，支持批量修改库存


#### 业务参数


| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| sku\_stocks |SkuStock[] | 是 |  |待更新的Sku及其库存列表 |


* 数据类型（SkuStock）

| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| outer\_sku\_id | String | 是 | 393992 | 买手填写的SkuId |
| stock\_num | Integer | 是 | 10 | 最新的可销售商品库存，必须大于等于0 |

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

#### 业务响应码描述
无

#### 示例报文

* url：https://open.ymatou.com/apigateway/v1?app_id=CgZcxYhQaCXOt31YQe&method=ymatou.sku.stock.update
* 请求报文:    
<br  />


```
{
	"app_id": "CgZcxYhQaCXOt31YQe",
	"method": "ymatou.sku.stock.update",
	"sign_method": "MD5",
	"auth_code": "JmhUXrDRP4Mw7zEHs2p3iQJ4T7mUOGr3",
	"timestamp": "2017-06-07 14:23:05",
	"sign": "8674B04AC90BC832F30F96F722AE737A",
	"nonce_str": "9766600700979402217096246554958",
	"biz_content": "{\"sku_stocks\":[{\"outer_sku_id\":\"SKU1155239418\",\"stock_num\":79},{\"outer_sku_id\":\"SKU171412919\",\"stock_num\":41},{\"outer_sku_id\":\"SKU217813146\",\"stock_num\":70},{\"outer_sku_id\":\"SKU1330677937\",\"stock_num\":38},{\"outer_sku_id\":\"SKU1256079248\",\"stock_num\":26},{\"outer_sku_id\":\"SKU354224187\",\"stock_num\":82},{\"outer_sku_id\":\"SKU860303309\",\"stock_num\":50},{\"outer_sku_id\":\"SKU100948397\",\"stock_num\":84}]}"
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
			"outer_sku_id": "SKU1155239418",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU171412919",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU217813146",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU1330677937",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU1256079248",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU354224187",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU860303309",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU100948397",
			"success": true
		}]
	}
}
```