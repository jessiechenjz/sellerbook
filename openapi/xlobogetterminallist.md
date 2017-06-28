### 获取货站（xlobo.hub.get）

---

#### 接口描述

* 获取贝海货站的ID信息，在创建面单时候使用

### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)

### 业务参数


### 返回参数

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String |  |  |
| content | JSON Object |  |  |



*  类型描述

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| version | String | N | 版本号（yyyy-MM-dd HH：mm：ss） |
| logistic_info_list | LogisticInfo[] |  |结果  |



*  类型描述 （LogisticInfo）

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| logistic_id | integer | N | 货站Id |
| logistic_name | String | N | 货站名称 |
| logistic_address | String | N | 货站地址 |


### 错误信息描述


#### 示例报文

* url：https://open.ymatou.com/apigateway/v1?app_id=aBNgc6RkDwYkdckavF&method=xlobo.hub.get
* 请求报文:    
<br  />

```
{
	"app_id" : "aBNgc6RkDwYkdckavF",
	"method" : "xlobo.hub.get",
	"sign_method" : "MD5",
	"auth_code" : "8UyV9ryKksAAlPwpduneO5rJ4l369yDT",
	"timestamp" : "2017-06-28 19:28:20",
	"sign" : "B4AE0AAD15A7634E8528BA90461A3E8F",
	"nonce_str" : "6802635001988213352467966797509"
}
```


* 返回报文:   
<br  />


```
{
	"code" : "0000",
	"message" : null,
	"content" : {
		"logistic_info_list" : [{
				"logistic_id" : 1,
				"logistic_address" : "147-04 183rd st. Springfield Garden, NY 11413",
				"logistic_name" : "纽约分拨中心"
			}, {
				"logistic_id" : 2,
				"logistic_address" : "434 S Abbott Ave Milpitas,CA 95035",
				"logistic_name" : "旧金山分拨中心"
			}, {
				"logistic_id" : 12,
				"logistic_address" : "14351 Bonelli St. City of Industry CA 91746",
				"logistic_name" : "洛杉矶分拨中心"
			}
		],
		"version" : "1.0"
	}
}
```