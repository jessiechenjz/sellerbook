### 做单接口 \(xlobo.labels.createNoVerification\)

---

| 字段名 | 类型 | 必须 | 描述 |
| :--- | :--- | :--- | :--- |
| BusinessNo | String | 是 | 业务编号，一个业务编号只能绑定一个物流面单 |
| Weight | Decimal | 是 | 重量，为包裹实际重量，精确到1位小数，如2.5，重量单位美国为磅，其它国家为公斤，重量需要在分类允许的重量范围内
|
| Insure | Decimal |是  | 保险费，整数金额，单位元，如100，表示100元，如果有金额默认表示同意《贝海丢单保险委托协议》协议 |
| IsRePacking |  |  |  |
| IsPreTax |  |  |  |
| IsRecTax |  |  |  |
| IsRecTax |  |  |  |
| Comment | | ||




        decimal\(10,1\)    11    N    

    

decimal\(10,2\)    12    Y    保险金额在允许范围内

    是否代打包    Integer    1    Y    0-无需代打包 1-简易代打包 2-加固代打包

    是否预缴税费    Integer    1    Y    0-非预缴税 1 预缴税  （电商件默认预缴税）

    是否收件人缴税    Integer    1    Y    0-商家缴税 1-收件人缴税

    面单备注    String    512    N

LogisticId    货站Id    Integer    11    N    验证有效性，货站是否存在, 用版本进行验证

LogisticVersion    货站最新版本时间,格式为（yyyy-MM-dd HH:mm:ss）    String    20    N    验证版本有效性。

LineTypeId    线路类型Id    Integer    11    N    1-个人快件 3-电商快件

9-奶粉专线

IsContainTax    价格是否包税    Integer    1    Y    0-不包税 1-包税  （电商快件必填）

发件人信息

BillSenderInfo    Name    发件人改名    String     64    N

```
Address    发件人地址    String     256    N    

Phone    发件人手机号    String    32    N    

OtherPhone    发件人电话    String     32    Y    
```

面单收件人信息

BillReceiverInfo    Name    收件人姓名    String    64    N

```
Province    收件人省份    String    64    N    

City    收件人城市    String    64    N    

District    收件人区县    String    64    N    

Address    收件人详细地址    String    256    N    

Phone    收件人手机号    String    32    N    

OtherPhone    收件人电话号码    String    32    Y    

Email    收件人Email    String    128    Y    

PostCode    收件人邮编    String    16    N    

IdCode    收件人身份证号码    String    32    Y    
```

渠道信息

BillSupplyInfo    OrderCode    渠道订单号    String    128    Y    电商快件必填

```
TradingNo    订单支付单号    String    128    Y    电商快件必填

ChannelName    渠道名称    String    128

Y    例：洋码头、淘宝、天猫等；注：电商快件只支持传入渠道： 洋码头、淘宝、天猫、苏宁、京东、一号店、当当、Higo
```

货物信息

BillCategoryList\[\]

型号、规格、材质不能同时为空，

最多只能有10个货物，包含10个    CategoryId    分类Id    Integer    11    N    验证有效性

```
CategoryVersion    分类最新版本时间,格式为（yyyy-MM-dd HH:mm:ss）    String    20    N    验证版本有效性。

Count    购买数量    Integer    11    N    

UnitPrice    购买单价，精确到2位小数，单位元,如100.25,表示100.25元    decimal\(10,2\)    11    N    

ProductName    品名    String    128    N    

Brand    品牌    String    128    N    

Model    型号    String    128    Y    不能同时为空，特殊分类规格不能为空（奶粉，调味品等）

Specification    规格    String    128    Y    

Size    材质    String    128    Y    
```



