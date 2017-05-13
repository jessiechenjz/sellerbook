### 获取平台物流公司列表 （ymatou.order.detail.get）

---

### 接口描述

* 获取单个订单的信息

### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)

### 业务参数

* 请求参数

| 名称 | 类型 | 是否必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| order\_id | String | 是 | 17392939 | 订单编号 |

### 返回参数

* 返回类型 

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code |  |  |  |
| message |  |  |  |
| order\_info | OrderInfo |  |  |

* 类型描述 \(OrderInfo\)

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| seller\_name | String | 洋妈咪甄选 | 买手名称 |
| order\_id | String | 121736528 | 订单编号 |
| trade\_id | String | 232654104 | 主单号，合并支付产生的id |
| order\_status | Integer | ORDER\_PAID | 订单状态  ORDER\_WAIT\_PAY:  等待支付 ORDER\_PAID: 订单已支付 WAIT\_SELLER\_SEND\_GOODS 订单买手发货 WAIT\_BUYER\_CONFIRM\_GOODS 等待买家确认收货  ORDER\_FINISH：订单完成 ORDER\_CANCEL:订单取消 |
|  |  |  |  |
| amount | Decimal | 200.00 | 订单金额 |
| payment | Decimal | 180.00 | 买家实付金额 |
| shipping\_fee | Decimal | 20.00 | 订单邮费分摊金额 |
| p\_coupon\_discount | Decimal |  | 平台优惠券分摊金额 |
| m\_coupon\_discount | Decimal |  | 买手优惠券分摊金额 |
| m\_promoption\_discount | Decimal |  | 买手促销活动分摊金额 |
| shipping\_time | String |  |  |
| seller\_memo | String |  | 买手备注 |
| buyer\_remark | String |  | 买家留言 |
| buyer\_id | String | vera\_1214 | 买家id |
| receiver\_name | String | 李四 | 收件人姓名 |
| receiver\_state | String |  | 收件人国家 |
| receiver\_address | String |  | 收件人地址 |
| receiver\_zip | String |  | 收件人邮编 |
| receiver\_mobile | String |  | 收件人手机 |
| receiver\_phone | String |  | 收件人电话 |
| order\_items\_info | OrderItemInfo\[\] |  |  |
| oid | String |  | 订单号 |
| order\_id | String |  | 子订单编号 |
| refund\_id | String |  | 退货退款单ID |
| refund\_status | String | 1 | 退货退款状态 |
| sku\_id | String | 399393920-333 | SkuId |
| outer\_sku\_id | String | 3838822 | 买手商品编码 |
| product\_title | String |  | 商品名称 |
| sku\_properties\_name | String | 颜色:红色;尺码:36 | SKU的属性值 |
| price | Decimal | 200.00 | 商品价格 |
| num | Integer | 1 | 商品数量 |
| total\_fee | Decimal | 200.00 |  |
| payment | Decimal | 160.00 | 支付金额 |
| discount\_fee | Decimal | 20.00 | 折扣金额 |
| adjust\_fee | Decimal | -20.00 | 调整金额 |
| modified\_time | String | 2017-01-01 12:00:00 | 变更时间 |

### 错误信息描述





