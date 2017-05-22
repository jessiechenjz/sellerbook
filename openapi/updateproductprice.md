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