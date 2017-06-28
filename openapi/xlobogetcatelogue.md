### 获取申报分类（xlobo.catalogue.get）

---
### 系统参数

* 接口调用参数


### 返回参数

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String |  |  |
| content | JSON Object |  |  |


*  类型描述

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| categorys | JSON Object |  |  |  |
| version | String | N | 版本号（yyyy-MM-dd HH：mm：ss） |


*  类型描述（CategoryInfo） 

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| category_id | String | N | 分类Id |
| category_cn_name | String | N | 分类中文名 |
| category_en_name | String | N | 分类英文名 |
| category_level | Int | N | 分类级别 |
| category_parent_id | Int | N | 分类父ID |

### 返回结果的格式

#### 示例报文

* url：https://open.ymatou.com/apigateway/v1?app_id=1iFUMvKfOOxPpDsYsZ&method=xlobo.catalogue.get
* 请求报文:    
<br  />


```
{
	"app_id" : "1iFUMvKfOOxPpDsYsZ",
	"method" : "xlobo.catalogue.get",
	"sign_method" : "MD5",
	"auth_code" : "idQZDeKTAlqlXnbMlzF1hszexlhQqRVJ",
	"timestamp" : "2017-06-22 17:15:20",
	"sign" : "A1CB7B1190B4DD3E9E3D9C1BA4A5E821",
	"nonce_str" : "2901431669163333446162957056584"
}
```


* 返回报文:   
<br  />


```
{
	"code" : "0000",
	"message" : null,
	"content" : {
		"categorys" : [{
				"category_level" : 1,
				"category_id" : "1",
				"category_en_name" : "Cosmetics/Skin Care",
				"category_cn_name" : "彩妆护理",
				"category_parent_id" : 0
			}, {
				"category_level" : 1,
				"category_id" : "2",
				"category_en_name" : "Vehicle Equipments/Travel/Outdoor",
				"category_cn_name" : "车载/旅游/户外",
				"category_parent_id" : 0
			}, {
				"category_level" : 2,
				"category_id" : "352",
				"category_en_name" : "",
				"category_cn_name" : "面膜（以“毫升/克”计算）",
				"category_parent_id" : 1
			}
		],
		"version" : "1.0"
	}
}
```