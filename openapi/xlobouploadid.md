### 身份证上传（xlobo.idcard.upload）

---

### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)

### 业务参数

| 字段名 | 类型 | 可空 | 含义 |
| :--- | :--- | :--- | :--- |
| request_id | String | N | 请求编号。无实际意义，每次请求唯一即可；仅作为请求编号查询使用 |
| name | String | N | 姓名 |
| phone | String | N | 手机号码 |
| idcode | String | N | 身份证号码 |
| front_picture | String | N | 正面身份证图片。图片转换为二进制流byte，再通过base64编码成字符串提交；注：现仅支持JPG.JPEG.PNG.BMP格式图片 |
| back_picture | String | N | 背面身份证图片。图片转换为二进制流byte，再通过base64编码成字符串提交；注：现仅支持JPG.JPEG.PNG.BMP格式图片 |
| billcode | String | N | 可为空；有面单号则会自动匹配|

注：

（1）图片需要压缩，尽量在300kb以内，避免超时情况发生

（2）需要将图片转换为二进制流byte，再通过base64编码成字符串提交

（3）现仅支持JPG.JPEG.PNG.BMP格式图片


### 返回参数

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String |  |  |
| content | JSON Object |  |  |


*  类型描述

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| update_count | Int | N | 更新数量 |
| error_count | Int | N | 出错数量 |
| error_info_list | ErrorInfo[] |  |错误描述   |
| result | UploadResultInfo |  |结果   |
| succeed | boolean |  |true成功 false失败    |

*  类型描述 （UploadResultInfo）

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| upload_result | int | Y | 结果  |

*  类型描述 （ErrorInfo）

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| identity | String | Y | 错误数据的标识 |
| error_code | String | Y | 错误代码 |
| error_description | String | Y | 错误描述 |


* url：https://open.ymatou.com/apigateway/v1?app_id=aBNgc6RkDwYkdckavF&method=xlobo.idcard.upload
* 请求报文:    
<br  />


```
{
	"app_id" : "1iFUMvKfOOxPpDsYsZ",
	"method" : "xlobo.idcard.add",
	"sign_method" : "MD5",
	"auth_code" : "idQZDeKTAlqlXnbMlzF1hszexlhQqRVJ",
	"timestamp" : "2017-06-22 20:04:08",
	"sign" : "8FBC20994B601C144CE21499E391369D",
	"nonce_str" : "6986329570663933509293875761510",
	"biz_content" : "{\"request_id\":\"615779214445\",\"name\":\"彭志邦\",\"phone\":\"15678998765\",\"idcode\":\"430225198901291015\",\"front_picture\":\"/9j/4AAQSkZJRgABAgAAAQABAAD/2wBJL+URt1VcLn8hXLbie9LZlpH/2Q==\"}"
}
```



* 返回报文:   
<br  />


```
{
	"code" : "0000",
	"message" : null,
	"content" : {
		"result" : {
			"upload_result" : 1
		},
		"succeed" : true,
		"update_count" : 0,
		"error_info_list" : [],
		"error_count" : 0
	}
}
```