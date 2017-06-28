### 获取面单文件（xlobo.labels.file.get.a4 / xlobo.labels.file.get.10x15）

---

xlobo.labels.file.get.a4  A4 格式面单

xlobo.labels.file.get.10x15 EMS10×15 热敏纸面单


调用接口时，选择BillCodes或者DBNS其中一个参数进行查询，两个参数都不为空时以BillCodes进行查询

1. 面单查询PDF后，既设为面单已打印状态，打印后则不能修改收件人信息和取消面单。
2. 每一天上传过十分钟则不能查询面单PDF信息。

### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)

### 业务参数
| 字段名 | 类型 | 可空 | 含义 |
| :--- | :--- | :--- | :--- |
| billcodes | String | N | 一个或者多个面单号，不能超过10个 |


### 返回参数

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String |  |  |
| content | JSON Object |  |  |


*  类型描述

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| total_count | Int | N | 更新数量 |
| error_count | Int | N | 出错数量 |
| error_info_list | ErrorInfo[] |  |错误描述   |
| result | ResultInfo[] |  |结果  |


*  类型类型描述 （ErrorInfo）

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| identity | String | Y | 错误数据的标识 |
| error_code | String | Y | 错误代码 |
| error_description | String | Y | 错误描述 |


*  类型类型描述 （ResultInfo）

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| billcode | String | N | 面单号 |
| bill_pdf_label | String | N | 面单PDF字节流，需要base64解码成byte。 |

注：BillpdfLabel类型为String，需要base64解码成byte

### 返回参数

### 错误信息描述

| 错误码 | 描述 |
| :--- | :--- |
| Xlobo.bill.param\_missing | 参数{0}为空，检查传入的参数是否正确 |
| Xlobo.bill.param\_error | 参数{0}错误或者不合法，检查传入的参数是否正确 |
| Xlobo.bill.param\_length\_over | 面单/运单信息列表过长，最多支持同时查询20个面单/运单 |
| Xlobo.bill.param\_code\_not\_exists | 面单/运单号{0}不存在，检查传入的面单运单号是否有效 |
| Xlobo.bill.param\_not\_upload\_id | 面单/运单号{0}没有上传身份证，用户上传身份证即可查询到PDF信息 |

#### 示例报文

* url：https://open.ymatou.com/apigateway/v1?app_id=aBNgc6RkDwYkdckavF&method=xlobo.labels.file.get.10x15
* 请求报文:    
<br  />


```
{
	"app_id" : "aBNgc6RkDwYkdckavF",
	"method" : "xlobo.labels.file.get.10x15",
	"sign_method" : "MD5",
	"auth_code" : "8UyV9ryKksAAlPwpduneO5rJ4l369yDT",
	"timestamp" : "2017-06-28 19:24:47",
	"sign" : "8CB45D127967A88CAB5AE72A30F03EA8",
	"nonce_str" : "6369433585988772684417364223266",
	"biz_content" : "{\"billcodes\":[\"DB033235531US\",\"DB033235644US\",\"DB003203478FR\"]}"
}
```


* 返回报文:   
<br  />


```
{
	"code" : "0000",
	"message" : null,
	"content" : {
		"result" : [{
				"billcode" : "DB493222256US",
				"bill_pdf_label" : "JVBERi0xLjUKJeLjz9MKMiAwIMzExMDcwIDAwMDAwIG4gCnRyYWlsZXIKPDwvU2l6ZSA1Ni9Sb290IDEzIDAgUi9JbmZvIDU1IDAgUi9JRCBbPGE2YWEyOTEzMTgxYjBlMDEzMzc1Y2ZkOTE4ODYzOTg4PjwyZjViYWEzM2U4MWNhZGFmMzJkMDdmZGEyMmFmOGRjNT5dPj4Kc3RhcnR4cmVmCjMxMTM2MAolJUVPRgo="
			}, {
				"billcode" : "DB493222256US",
				"bill_pdf_label" : "JVBERi0xLjUKJeLjz9MKMiAwIG9iago8PC9UeXBlwMzExMDcwIDAwMDAwIG4gCnRyYWlsZXIKPDwvU2l6ZSA1Ni9Sb290IDEzIDAgUi9JbmZvIDU1IDAgUi9JRCBbPGE5OTcwNDQwNDBkNzE0Y2M4ZGJiNGJlNTk0NmDQ4ZTFkOTE4NGExZDYwMWU1ZGRhYmVhMDE0Zj5dPj4Kc3RhcnR4cmVmCjMxMTM2MAolJUVPRgo="
			}
		],
		"total_count" : 3,
		"error_info_list" : [{
				"error_description" : "检查传入的面单号/运单号是否有效",
				"identity" : "DB003203478FR",
				"error_code" : "xlobo.bill.param_code_not_exists"
			}
		],
		"error_count" : 1
	}
}
```