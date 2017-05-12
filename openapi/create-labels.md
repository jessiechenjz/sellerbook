### 任意发件人不使用商品编码做单接口\(同步xlobo.labels.createNoVerification\)

---

### 接口描述

* 获取平台支持的物流公司，用于发货接口，可按国家维度查询

### 系统参数

* 接口调用参数

| 名称 | 类型 | 必须 | 描述 |
| :--- | :--- | :--- | :--- |
| method | String | 是 | API名称 |
| app\_key | String | 是 | 洋码头分配给买手的AppKey。 |
| sign\_method | String | 是 | 签名的摘要算法，可选值为：md5。 |
| sign | String | 是 | API输入参数签名结果，签名算法介绍请[点击这里](/openapi/README.md#signmethod)。 |
| session\_key | String | 是 | 用户登录授权成功后，TOP颁发给应用的授权信息，详细介绍请[点击这里](/openapi/README.md#getappkey)。 |
| timestamp | String | 是 | 时间戳，格式为yyyy-MM-dd HH:mm:ss，时区为GMT+8，例如：2017-01-01 12:00:00。洋码头API服务端允许客户端请求最大时间误差为10分钟。 |
| format | String | 否 | 响应格式。默认为json格式。 |

### 业务参数

| 字段名 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| BusinessNo | String | N | 业务编号，一个业务编号只能绑定一个物流面单 |
| Weight | decimal（10.1） | N | 重量，为包裹实际重量，精确到1位小数，如2.5，重量单位美国为磅，其它国家为公斤，重量需要在分类允许的重量范围内 |
| Insure | decimal（10.2） | Y | 保险费，整数金额，单位元，如100，表示100元，如果有金额默认表示同意《贝海丢单保险委托协议》协议,保险金在允许范围内 |
| IsRePacking | Integer | Y | 是否代打包，0-无需代打包 1-简易代打包 2-加固代打包 |
| IsPreTax | Integer | Y | 是否预交税费，0-非预缴税 1-预交税（电商默认预缴税） |
| IsRecTax | Integer | Y | 是否收件人缴税，0-商家缴税 1-收件人缴税 |
| Comment | String | N | 面单备注 |
| LogisticId | Integer | N | 货站Id，验证有效性，货站是否存在，用版本进行验证 |
| LogisticVersion | String | N | 货站最新版本时间，格式为（yyyy-MM-dd HH：mm：ss），验证版本有效性 |
| LineTypeId | Integer | N | 线路类型Id，1-个人快件 3-电商快件 9-奶粉专线 |
| IsContainTax | Integer | Y | 价格是否包税，0-不包税 1-包税（电商快件必填） |
| BillSenderInfo |  |  | 发件人信息 |
| Name | String | N | 发件人姓名 |
| Address | String | N | 发件人地址 |
| Phone | String | N | 发件人手机号 |
| OtherPhone | String | Y | 发件人电话 |
| BillReceiverInfo |  |  | 面单收件人信息 |
| Name | String | N | 收件人姓名 |
| Province | String | N | 收件人省份 |
| City | String | N | 收件人城市 |
| District | String | N | 收件人区县 |
| Address | String | N | 收件人详细地址 |
| Phone | String | N | 收件人手机号 |
| OtherPhone | String | Y | 收件人电话号码 |
| Email | String | Y | 收件人Email |
| PostCode | String | N | 收件人邮编 |
| Idcode | String | Y | 收件人身份证号码 |
| BillSupplyInfo |  |  | 渠道信息 |
| OtherCode | String | Y | 渠道订单号。电商快件必填 |
| TradingNo | String | Y | 渠道支付号。电商快件必填 |
| ChanneName | String | Y | 渠道名称。例：洋码头，淘宝，天猫等；注：电商快件只支持传入渠道：洋码头，淘宝，天猫，苏宁，京东，一号店，当当，Higo |
| BillCategoryList\[\] |  |  | 货物信息，型号，规格，材质不能同时为空，最多只能有10个货物，包含10个 |
| Categoryld | Integer | N | 分类Id。验证有效性 |
| CateGoryVersion | String | N | 分类最新版本时间，格式为（yyyy-MM-dd HH：mm：ss） 验证版本有效性 |
| Count | Integer | N |  |
| UniePrice | Decimal\(10.2\) | N | 购买数量 购买单价，精确到2位小数，单位元，如 100.25，表示100.25元 |
| ProductName | String | N | 品名 |
| Brand | String | N | 品牌 |
| Model | String | Y | 型号。不能同时为空，特殊分类规格不能为空（奶粉，调味品等） |
| Specification | String | Y | 规格 |
| Size | String | Y | 材质 |

### 输出：

面单信息

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| UpdateCount | Int | N | 更新数量 |
| ErrorCount | Int | N | 出错数量 |
| ErrorInfoList（ErrorInfo） |  |  |  |
| Identity | String | Y | 错误数据的标识 |
| ErrorCode | String | Y | 错误代码 |
| ErrorDescription | String | Y | 错误描述 |
| Result |  |  |  |
| BillCode | String | Y | 面单号 |
| BusinessNo | String | N | 业务编号，传入的业务编号 |
| IsPostPay | Int | Y | 是否后付费，1：后付费，0：预付费 |
| DeliveryFee | decimal\(10.2\) | Y | 运费 |
| Insurance | decimal\(10.2\) | Y | 保险费 |
| TaxFee | decimal\(10.2\) | Y | 预交税费 |

### 错误信息

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



