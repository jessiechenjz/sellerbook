### 贝海做单 \(xlobo.labels.createNoVerification\)

---

### 接口描述

* 调用贝海的物流接口，创建面单，生成待发货面单信息

### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)

### 业务参数
| 字段名 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| business_no | String | N | 业务编号，一个业务编号只能绑定一个物流面单 |
| weight | decimal（10.1） | N | 重量，为包裹实际重量，精确到1位小数，如2.5，重量单位美国为磅，其它国家为公斤，重量需要在分类允许的重量范围内 |
| insure | decimal（10.2） | Y | 保险费，整数金额，单位元，如100，表示100元，如果有金额默认表示同意《贝海丢单保险委托协议》协议,保险金在允许范围内 |
| is_repacking | Integer | Y | 是否代打包，0-无需代打包 1-简易代打包 2-加固代打包 |
| is_pre_tax | Integer | Y | 是否预交税费，0-非预缴税 1-预交税（电商默认预缴税） |
| is_rec_tax | Integer | Y | 是否收件人缴税，0-商家缴税 1-收件人缴税 |
| comment | String | N | 面单备注 |
| logistic_id | Integer | N | 货站Id，验证有效性，货站是否存在，用版本进行验证 |
| logistic_version | String | N | 货站最新版本时间，格式为（yyyy-MM-dd HH：mm：ss），验证版本有效性 |
| line_type_id | Integer | N | 线路类型Id，1-个人快件 3-电商快件 9-奶粉专线 |
| is_contain_tax | Integer | Y | 价格是否包税，0-不包税 1-包税（电商快件必填） |
| bill_sender_info |  |  | 发件人信息 |
| name | String | N | 发件人姓名 |
| address | String | N | 发件人地址 |
| phone | String | N | 发件人手机号 |
| other_phone | String | Y | 发件人电话 |
| bill_receiver_info |  |  | 面单收件人信息 |
| name | String | N | 收件人姓名 |
| province | String | N | 收件人省份 |
| city | String | N | 收件人城市 |
| district | String | N | 收件人区县 |
| address | String | N | 收件人详细地址 |
| phone | String | N | 收件人手机号 |
| other_phone | String | Y | 收件人电话号码 |
| email | String | Y | 收件人Email |
| post_code | String | N | 收件人邮编 |
| id_code | String | Y | 收件人身份证号码 |
| bill_supply_info |  |  | 渠道信息 |
| other_code | String | Y | 渠道订单号。电商快件必填 |
| trading_no | String | Y | 渠道支付号。电商快件必填 |
| channe_name | String | Y | 渠道名称。例：洋码头，淘宝，天猫等；注：电商快件只支持传入渠道：洋码头，淘宝，天猫，苏宁，京东，一号店，当当，Higo |
| bill_category_list\[\] |  |  | 货物信息，型号，规格，材质不能同时为空，最多只能有10个货物，包含10个 |
| category_id | Integer | N | 分类Id。验证有效性 |
| category_version | String | N | 分类最新版本时间，格式为（yyyy-MM-dd HH：mm：ss） 验证版本有效性 |
| count | Integer | N |  |
| unit_price | Decimal\(10.2\) | N | 购买数量 购买单价，精确到2位小数，单位元，如 100.25，表示100.25元 |
| product_name | String | N | 品名 |
| brand | String | N | 品牌 |
| model | String | Y | 型号。不能同时为空，特殊分类规格不能为空（奶粉，调味品等） |
| specification | String | Y | 规格 |
| size | String | Y | 材质 |

### 返回参数

面单信息

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| update_count | Int | N | 更新数量 |
| error_count | Int | N | 出错数量 |
| error_info_list（errorinfo） |  |  |  |
| identity | String | Y | 错误数据的标识 |
| error_code | String | Y | 错误代码 |
| error_description | String | Y | 错误描述 |
| result |  |  |  |
| billcode | String | Y | 面单号 |
| business_no | String | N | 业务编号，传入的业务编号 |
| is_post_pay | Int | Y | 是否后付费，1：后付费，0：预付费 |
| delivery_fee | decimal\(10.2\) | Y | 运费 |
| insurance | decimal\(10.2\) | Y | 保险费 |
| tax_fee | decimal\(10.2\) | Y | 预交税费 |


### 错误信息描述

| 错误码 | 描述 |
| :--- | :--- |
| Xlobo.bill.param\_missing | 参数{0}为空，检查传入的参数是否正确 |
| Xlobo.bill.param\_error | 参数{0}错误或者不合法，检查传入的参数是否正确 |
| Xlobo.bill.receiver\_address\_invalid | 收货地址无效，检查收货地址是否正确，不能是港澳台 |
| Xlobo.bill.phone\_invalid | 收件人手机号规则无效，必须为11为数字手机号，同时第一位是1第二位为345789 |
| Xlobo.bill.category\_invalid | 分类信息不存在，检查分类信息是否正确 |
| Xlobo.bill.category\_desc\_invalid | 分类型号规格材质不能同时为空 |
| Xlobo.bill.insure\_invalid | 保险费1.5-10000RMB或者0.00RMB |
| Xlobo.bill.user.banlance | 用户余额不足，检查用户余额 |
| Xlobo.bill.good\_length\_over | 包裹物品种类只能选择10个以内，包含10个。 |
| Xlobo.bill.extra\_money\_exists | 存在补款，请先补款再做单 |