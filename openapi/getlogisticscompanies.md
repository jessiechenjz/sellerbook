### 获取买手可用物流公司列表 （ymatou.logistics.companies.get）

---

### 接口描述

* 获取买手可用的平台物流公司


### 业务参数

无

### 返回参数

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String | 更新库存成功 | 接口调用返回信息 |
| content | JSON Object |  | BizResult的JSON报文体 |

* 数据类型(BizResult）

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| logistics_companies | LogisticsCompany[] |  | 物流公司列表 |

* 数据类型（LogisticsCompany）

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| company_code | String | A003 | 物流公司平台代码 |
| short_name | String | shunfeng | 物流公司简称 |
| company_name | String | 顺丰速递 | 物流公司名称 |


#### 示例报文

* url：http://open.ymatou.com/apigateway/v1?app_id=CgZcxYhQaCXOt31YQe&method=ymatou.logistics.companies.get
* 请求报文:    
<br  />


```
{
	"app_id": "CgZcxYhQaCXOt31YQe",
	"method": "ymatou.logistics.companies.get",
	"sign_method": "MD5",
	"auth_code": "JmhUXrDRP4Mw7zEHs2p3iQJ4T7mUOGr3",
	"timestamp": "2017-06-07 14:47:36",
	"sign": "6D4FEFCFFF51190559983D229D54A8C0",
	"nonce_str": "6836813925599717793509842715568"
}
```


* 返回报文:   
<br  />


```
{
	"code": "0000",
	"message": "",
	"content": {
		"logistics_companies": [{
			"company_name": "测试公司123",
			"company_code": "Y080",
			"short_name": "111"
		}, {
			"company_name": "呃呃呃",
			"company_code": "Y083",
			"short_name": "99333333"
		}, {
			"company_name": "洋码头官方合作物流（xLobo贝海国际速递）",
			"company_code": "Y068",
			"short_name": "xlobo"
		}, {
			"company_name": "韩国邮政（Korea Post）",
			"company_code": "Y071",
			"short_name": "koreapost"
		}, {
			"company_name": "日本邮政（Japan Post）",
			"company_code": "Y048",
			"short_name": "japanposten"
		}, {
			"company_name": "顺丰速运（SF-Express）",
			"company_code": "Y073",
			"short_name": "shunfeng"
		}, {
			"company_name": "意大利邮政(Poste Italiane)",
			"company_code": "Y042",
			"short_name": "italiane"
		}, {
			"company_name": "英国皇家邮政(Parcel Force)",
			"company_code": "Y062",
			"short_name": "parcelforce"
		}, {
			"company_name": "英国皇家邮政国际挂号包裹（Royal Mail）",
			"company_code": "Y063",
			"short_name": "royalmail"
		}, {
			"company_name": "呃呃呃",
			"company_code": "Y083",
			"short_name": "99333333"
		}, {
			"company_name": "我test",
			"company_code": "Y081",
			"short_name": "test"
		}, {
			"company_name": "申通快递（STO Express）",
			"company_code": "Y057",
			"short_name": "shentong11"
		}, {
			"company_name": "顺丰速运（SF-Express）",
			"company_code": "Y073",
			"short_name": "shunfeng"
		}]
	}
}
```

