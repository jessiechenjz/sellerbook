### 更新商品价格 （ymatou.skus.stock.price）

---

### 接口描述

* 获取平台支持的物流公司，用于发货接口，可按国家维度查询

### 系统参数

* 接口调用参数

| 名称 | 类型 | 是否必须 | 描述 |
| :--- | :--- | :--- | :--- |
| method | String | 是 | API名称 |
| app\_key | String | 是 | 洋码头分配给买手的AppKey。 |
| sign\_method | String | 是 | 签名的摘要算法，可选值为：md5。 |
| sign | String | 是 | API输入参数签名结果，签名算法介绍请[点击这里](/openapi/README.md#signmethod)。 |
| session\_key | String | 是 | 用户登录授权成功后，TOP颁发给应用的授权信息，详细介绍请[点击这里](/openapi/README.md#getappkey)。 |
| timestamp | String | 是 | 时间戳，格式为yyyy-MM-dd HH:mm:ss，时区为GMT+8，例如：2017-01-01 12:00:00。洋码头API服务端允许客户端请求最大时间误差为10分钟。 |
| format | String | 否 | 响应格式。默认为json格式。 |

### 业务参数

* 请求参数

| 名称 | 类型 | 是否必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| SkuPrice\[\] | SkuPrice |  |  |  |

* 请求参数 （SkuPrice）

| 名称 | 类型 | 是否必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
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



