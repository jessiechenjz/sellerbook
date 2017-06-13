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
| product_id | String |  | 商品ID |
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
| delivery\_type | int |  | 商品物流方式 <br> 2. 直邮 3. 官方（贝海）直邮 4. 第三方保税 5. 官方（贝海）保税 7. 拼邮  |
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
| pic_url | String |  | 规格图片链接 |