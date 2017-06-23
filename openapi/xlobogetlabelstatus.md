### 获取面单物流状态（xlobo.status.get）

---


### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)

### 业务参数


| 字段名 | 类型 | 可否为空 | 含义 |
| :--- | :--- | :--- | :--- |
| billcodes |  | N | 一个或者多个面单号，不能超过50个 |

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
| result | BillTrackInfo[] |  |结果  |


*  类型描述 （ErrorInfo）

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| identity | String | Y | 错误数据的标识 |
| error_code | String | Y | 错误代码 |
| error_description | String | Y | 错误描述 |



*  类型描述 （BillTrackInfo）

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| billcode | String | N | 面单号 |
| business_no | String | Y | 业务编号 |
| bill_status_list |BillStatusInfo[]  |  | 面单状态列表 |



*  类型描述 （BillStatusInfo）

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| start_time | String | N | 状态发生时间 |
| operator | String | N | 操作人 |
| status | String | N | 状态名称 |
| status_detail | String | Y | 状态描述 |


### 错误信息描述

| 错误码 | 描述 |
| :--- | :--- |
| Xlobo.bill.param\_missing | 参数{0}为空，检查传入参数是否正确 |
| Xlobo.bill.param\_error | 参数{0}错误或者不合法，检查传入的参数是否正确 |
| Xlobo.bill.parm\_length\_over | 面单/运单信息列表过长，最多支持同时查询20个面单运单 |
| Xlobo.bill.param\_code\_not\_exists | 面单/运单号{0}不存在，检查传入的面单/运单号是否有效 |

#### 示例报文

* url：https://open.ymatou.com/apigateway/v1?app_id=T5vkxW5NPb64YdhXPo&method=xlobo.status.get
* 请求报文:    
<br  />


```
{
	"code" : "0000",
	"message" : null,
	"content" : {
		"result" : [{
				"bill_status_list" : [{
						"start_time" : "2017-02-15 16:15:06",
						"operator" : "",
						"status" : "面单已生成",
						"status_detail" : "面单已生成"
					}
				],
				"business_no" : "DB493222256US",
				"billcode" : "DB493222256US"
			}, {
				"bill_status_list" : [{
						"start_time" : "2017-02-15 16:15:06",
						"operator" : "",
						"status" : "面单已生成",
						"status_detail" : "面单已生成"
					}
				],
				"business_no" : "DB493222256US",
				"billcode" : "DB493222256US"
			}, {
				"bill_status_list" : [{
						"start_time" : "2017-02-10 13:23:31",
						"operator" : "",
						"status" : "面单已生成",
						"status_detail" : "您的包裹尚未提交身份证明. 请至 www.xlobo.com/b 提交"
					}
				],
				"business_no" : "DB003203478FR",
				"billcode" : "DB003203478FR"
			}
		],
		"total_count" : 3,
		"error_info_list" : [],
		"error_count" : 0
	}
}
```


* 返回报文:   
<br  />


```
{
	"code": "0000",
	"message": "操作成功",
	"content": {
		"results": [{
			"msg": "成功",
			"outer_sku_id": "SKU1155239418",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU171412919",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU217813146",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU1330677937",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU1256079248",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU354224187",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU860303309",
			"success": true
		}, {
			"msg": "成功",
			"outer_sku_id": "SKU100948397",
			"success": true
		}]
	}
}
```