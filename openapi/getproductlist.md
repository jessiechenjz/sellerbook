### 获取买手商品列表 （ymatou.products.list.get）

---

### 接口描述

* 获取买手商品列表

| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| page\_no | Integer | 是 | 3 | 请求分页页码(大于0) |
| page\_rows | Integer | 是 | 50 | 每页记录数量(大于0且小于等于100 )|

### 返回参数

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String |  |  |
| product\_infos | ProductInfo\[\] |  |  |  |
| productId |  |  | 商品ID |
| product\_name |  |  | 商品名称 |
| category\_id |  |  | 类目ID |
| brand\_id |  |  | 品牌ID |
| brand\_name |  |  | 品牌名称 |
| product\_images |  |  | 商品图片 |
| product\_url |  |  | 商品显示URL |
| create\_time |  |  | 创建时间 |
| update\_time |  |  | 最后一次更新时间 |
| skus\[\] | sku信息 |  |  |
| sku\_id |  |  | SKU ID |
| properties |  |  | SKU属性信息 |
| outer\_id |  |  | 外部商品编码 |
| price |  |  | 商品价格 |
| vip\_price |  |  | vip商品价 |
| new\_price |  |  | 新客价 |
| stock\_num |  |  | 库存数量 |
| weight |  |  | 规格重量 |
| extra\_info |  |  | 扩充信息 |



















