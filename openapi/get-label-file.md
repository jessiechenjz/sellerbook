### 获取面单文件（xlobo.labels.file.getFileA4 / xlobo.labels.file.getFile10x15）

---

xlobo.labels.file.getfileA4  A4 格式面单

xlobo.labels.file.getFile10×15 EMS10×15 热敏纸面单


调用接口时，选择BillCodes或者DBNS其中一个参数进行查询，两个参数都不为空时以BillCodes进行查询

1. 面单查询PDF后，既设为面单已打印状态，打印后则不能修改收件人信息和取消面单。
2. 每一天上传过十分钟则不能查询面单PDF信息。

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


| 字段名 | 类型 | 可空 | 含义 |
| :--- | :--- | :--- | :--- |
| BillCodes | String | N | 一个或者多个面单号 |

输出：

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| TotalCount | Int | N | 更新数量 |
| ErroCount | Int | N | 出错数量 |
| ErrorInfoList\(ErrorInfo\) |  |  |  |
| Identity | String | Y | 错误数据的标识 |
| ErrorCode | String | Y | 错误代码 |
| ErrorDescription | String | Y | 错误描述 |
| Result |  |  |  |
| BillCode | String | N | 面单号 |
| \(Billpdf\) |  |  |  |
| BillpdfLabel | String | N | 面单PDF字节流，需要base64解码成byte。 |

注：BillpdfLabel类型为String，需要base64解码成byte

### 请求格式



获取查询pdf信息JSON格式

### 错误信息描述

| 错误码 | 描述 |
| :--- | :--- |
| Xlobo.bill.param\_missing | 参数{0}为空，检查传入的参数是否正确 |
| Xlobo.bill.param\_error | 参数{0}错误或者不合法，检查传入的参数是否正确 |
| Xlobo.bill.param\_length\_over | 面单/运单信息列表过长，最多支持同时查询20个面单/运单 |
| Xlobo.bill.param\_code\_not\_exists | 面单/运单号{0}不存在，检查传入的面单运单号是否有效 |
| Xlobo.bill.param\_not\_upload\_id | 面单/运单号{0}没有上传身份证，用户上传身份证即可查询到PDF信息 |



