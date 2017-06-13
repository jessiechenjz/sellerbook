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
| product\_infos | ProductInfo\[\] |  |  |  |
| total_count | Integer | 是 | 50 | 总行数 |

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
| properties | String |  | SKU属性信息 |
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



#### 示例报文

* url：http://open.ymatou.com/apigateway/v1?app_id=CgZcxYhQaCXOt31YQe&method=ymatou.order.list.get
* 请求报文:    
<br  />


```
{
	"app_id": "aBNgc6RkDwYkdckavF",
	"method": "ymatou.order.list.get",
	"sign_method": "MD5",
	"auth_code": "8UyV9ryKksAAlPwpduneO5rJ4l369yDT",
	"timestamp": "2017-06-07 14:56:40",
	"sign": "725C28BE74AD25364B572127456052D8",
	"nonce_str": "0059636705582427847896181253219",
	"biz_content": "{\"order_status\":\"2\",\"date_type\":1,\"sort_type\":1,\"start_date\":\"2017-06-02 14:56:40\",\"end_date\":\"2017-06-07 14:56:40\",\"page_no\":1,\"page_rows\":10}"
}
```