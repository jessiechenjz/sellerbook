### 任意发件人不使用商品编码做单接口\(同步xlobo.labels.createNoVerification\)

---

| 字段名 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| BusinessNo | String | N | 业务编号，一个业务编号只能绑定一个物流面单 |
| Weight | Decimal（10,1） | N | 重量，为包裹实际重量，精确到1位小数，如2.5，重量单位美国为磅，其它国家为公斤，重量需要在分类允许的重量范围内 |
|  |  |  |  |
| Insure | Decimal\(10,2\) | Y | 保险费，整数金额，单位元，如100，表示100元，如果有金额默认表示同意《贝海丢单保险委托协议》协议,保险金在允许范围内 |
| IsRePacking | Integer | Y | 是否代打包，0-无需代打包 1-简易代打包 2-加固代打包 |
| IsPreTax | Integer | Y | 是否预交税费，0-非预缴税 1-预交税（电商默认预缴税） |
| IsRecTax | Integer | Y | 是否收件人缴税，0-商家缴税 1-收件人缴税 |
| Comment | String | N | 面单备注 |
| LogisticId | Integer | N | 货站Id，验证有效性，货站是否存在，用版本进行验证 |
| LogisticVersion | String | N | 货站最新版本时间，格式为（yyyy-MM-dd HH：mm：ss），验证版本有效性 |
| LineTypeId | Integer | N | 线路类型Id，1-个人快件 3-电商快件 9-奶粉专线 |
| IsContainTax | Integer | Y | 价格是否包税，0-不包税 1-包税（电商快件必填） |
| 面单收件人信息， |  |  |  |



### 输出：

面单信息



| 字段名称 | 描述 | 类型 | 长度 | 可空 | 备注 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| UpdateCount | 更新数量 | Int |  | N |  |
| ErrorCount | 出错数量 | Int |  | N |  |
| ErrorInfoList |  |  |  |  |  |



### 错误信息

| 错误码 | 描述 |
| :--- | :--- |
| Xlobo.bill.param\_missing | 参数{0}为空，检查传入的参数是否正确 |
| Xlobo.bill.param\_error | 参数错误或者不合法，检查传入的参数是否正确 |
| Xlobo.bill.receiver\_address\_invalid | 收货地址无效，检查收货地址是否正确，不能是港澳台 |
| Xlobo.bill.phone\_invalid | 收件人手机号规则无效，必须为11为数字手机号，同时第一位是1第二位为345789 |
| Xlobo.bill.category\_invalid | 分类信息不存在，检查分类信息是否正确 |
| Xlobo.bill.category\_desc\_invalid | 分类型号规格材质不能同时为空 |
| Xlobo.bill.insure\_invalid | 保险费1.5-10000RMB或者0.00RMB |
| Xlobo.bill.user.banlance | 用户余额不足，检查用户余额 |
| Xlobo.bill.good\_length\_over | 包裹物品种类只能选择10个以内，包含10个。 |
| Xlobo.bill.extra\_money\_exists | 存在补款，请先补款再做单 |



