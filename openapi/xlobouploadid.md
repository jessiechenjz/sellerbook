### 身份证上传（xlobo.idcard.add）

---

### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)

### 业务参数

| 字段名 | 类型 | 可空 | 含义 |
| :--- | :--- | :--- | :--- |
| RequestId | String | N | 请求编号。无实际意义，每次请求唯一即可；仅作为请求编号查询使用 |
| Name | String | N | 姓名 |
| Phone | String | N | 手机号码 |
| IdCode | String | N | 身份证号码 |
| FrontPicture | String | N | 正面身份证图片。图片转换为二进制流byte，再通过base64编码成字符串提交；注：现仅支持JPG.JPEG.PNG.BMP格式图片 |
| BackPicture | String | N | 背面身份证图片。图片转换为二进制流byte，再通过base64编码成字符串提交；注：现仅支持JPG.JPEG.PNG.BMP格式图片 |
| BillCode | String | Y | 贝海面单号。可为空；有面单号则会自动匹配 |

注：

（1）图片需要压缩，尽量在300kb以内，避免潮湿情况发生

（2）需要将图片转换为二进制流byte，再通过base64编码成字符串提交

（3）现仅支持JPG.JPEG.PNG.BMP格式图片

### 返回参数

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| UpdateCount | Int | N | 更新数量 |
| ErrorCount | Int | N | 出错数量 |
| ErrorInfoList\(ErrorInfo\) |  |  |  |
| Identity | String | Y | 错误数据的标识 |
| ErrorCode | String |  | 错误代码 |
| ErrorDescription | String | Y | 错误描述 |

### 错误信息描述


