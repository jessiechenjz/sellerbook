### 更新商品库存 （ymatou.sku.stock.update）

---

#### 接口描述

* 按商家商品编码同步商品的库存信息，支持批量修改库存

#### 系统参数

* 参考 [接口调用指南](/openapi/how-to-call-api.md)

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

### 业务响应码描述
无