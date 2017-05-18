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


### 返回参数

* 返回类型 

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0 | 返回代码 |
| message | String | 更新价格成功 | 接口调用返回信息 |

### 错误信息描述