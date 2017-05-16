### 更新商品价格 （ymatou.sku.price.update）

---

### 接口描述

* 按商家商品编码同步商品的价格信息，支持批量改价

### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)

### 业务参数

* 请求参数

| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| sku\_prices |SkuPrice[]  |  |  |  如下四个参数组成的结构体的数组|
| outer\_sku\_id | String | 是 | 393992 | 买手填写的SKUid |
| product\_price | Decimal | 是 | 100.00 | 商品售价 |
| product\_newuser\_price | Decimal | 否 | 99.00 | 商品新客价 |
| product\_vip\_price | Decimal | 否 | 95.00 | 商品VIP价 |

### 返回参数

* 返回类型 

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0 | 返回代码 |
| message | String | 更新价格成功 | 接口调用返回信息 |

### 错误信息描述