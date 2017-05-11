### 任意发件人不使用商品编码做单接口\(同步xlobo.labels.createNoVerification\)

---

| 字段名 |  | 描述 | 类型 | 可否为空 |  |
| :--- | :--- | :--- | :--- | :--- | :--- |
| BusinessNo |  | 业务编号，一个业务编号只能绑定一个物流面单 | String | N |  |
| Weight |  | 重量，为包裹实际重量，精确到1位小数，如2.5，重量单位美国为磅，其它国家为公斤，重量需要在分类允许的重量范围内 | decimal（10.1） | N |  |
| Insure |  | 保险费，整数金额，单位元，如100，表示100元，如果有金额默认表示同意《贝海丢单保险委托协议》协议,保险金在允许范围内 | decimal（10.2） | Y |  |
| IsRePacking |  | 是否代打包，0-无需代打包 1-简易代打包 2-加固代打包 | Integer | Y |  |
| IsPreTax |  | 是否预交税费，0-非预缴税 1-预交税（电商默认预缴税） | Integer | Y |  |
| IsRecTax |  | 是否收件人缴税，0-商家缴税 1-收件人缴税 | Integer | Y |  |
| Comment |  | 面单备注 | String | N |  |
| LogisticId |  | 货站Id，验证有效性，货站是否存在，用版本进行验证 | Integer | N |  |
| LogisticVersion |  | 货站最新版本时间，格式为（yyyy-MM-dd HH：mm：ss），验证版本有效性 | String | N |  |
| LineTypeId |  | 线路类型Id，1-个人快件 3-电商快件 9-奶粉专线 | Integer | N |  |
| IsContainTax |  | 价格是否包税，0-不包税 1-包税（电商快件必填） | Integer | Y |  |
| 发件人信息，BillSenderInfo |  | 发件人姓名 | String | N |  |
| Name |  | 发件人地址 | String | N |  |
| Address |  | 发件人手机号 | String | N |  |
| Phine |  | 发件人电话 | String | Y |  |
| OtherPHone |  |  |  |  |  |
| 面单收件人信息，BillReceiverInfo | Name | 收件人姓名 | String | N |  |
|  | Province | 收件人省份 | String | N |  |
|  | City | 收件人城市 | String | N |  |
|  | District | 收件人区县 | String | N |  |
|  | Address | 收件人详细地址 | String | N |  |
|  | Phone | 收件人手机号 | String | N |  |
|  | OtherPhone | 收件人电话号码 | String | Y |  |
|  | Email | 收件人Email | String | Y |  |
|  | PostCode | 收件人邮编 | String | N |  |
|  | IdCode | 收件人身份证号码 | String | Y |  |
| 渠道信息，BillSupplyInfo | OtherCode | 渠道订单号 | String | Y | 电商快件必填 |
|  | TradingNo | 订单支付号 | String | Y | 电商快件必填 |
|  | ChanneName | 渠道名称 | String | Y | 例：洋码头，淘宝，天猫等；注：电商快件只支持传入渠道：洋码头，淘宝，天猫，苏宁，京东，一号店，当当，Higo |
| 货物信息，BillCategoryList,型号，规格，材质不能同时为空，最多只能有10个货物，包含10个 | CategoryId | 分类Id | Integer | N | 验证有效性 |
|  | CateGoryVersion | 分类最新版本时间，格式为（yyyy-MM-dd HH：mm：ss） | String | N | 验证版本有效性 |
|  | Count | 购买数量 | Integer | N |  |
|  | UnitPrice | 购买单价，精确到2位小数，单位元，如 100.25，表示100.25元 | decimal\(10.2\) | N |  |
|  | ProductName | 品名 | String | N |  |
|  | Brand | 品牌 | String | N |  |
|  | Model | 型号 | String | N | 不能同时为空，特殊分类规格不能为空（奶粉，调味品等） |
|  | Specification | 规格 | String | N |  |
|  | Size | 材质 | String | N |  |

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



