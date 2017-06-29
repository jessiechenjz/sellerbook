### 订单发货 （ymatou.order.accept）

---

### 接口描述

* 订单接单

#### 业务参数


| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| order_ids |Long[] | 是 |  |待接单的订单号 |


### 返回参数

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String | 接口调用返回信息 |
| content | JSON Object |  | BizResult的JSON报文体 |

* 数据类型(BizResult）

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| results | AcceptOrderResult[] |  | 接单结果 |

* 数据类型（AcceptOrderResult）

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| order_id | long | 105913276 | 订单号 |
| exec_success | boolean | true | 是否执行成功 |
| msg | string |  | 处理信息 |


#### 示例报文

* url：https://open.ymatou.com/apigateway/v1?app_id=CgZcxYhQaCXOt31YQe&method=ymatou.order.accept
* 请求报文:    
<br  />


```
{
	"app_id": "CgZcxYhQaCXOt31YQe",
	"method": "ymatou.order.accept",
	"sign_method": "MD5",
	"auth_code": "JmhUXrDRP4Mw7zEHs2p3iQJ4T7mUOGr3",
	"timestamp": "2017-06-07 14:49:38",
	"sign": "8F01503D6352988B8CDB3CE4EA5FAF0C",
	"nonce_str": "9204667338768330660933423992945",
	"biz_content": "{\"order_ids\":[112532318,112532310]}"
}
```


* 返回报文:   
<br  />


```
{
	"code": "0000",
	"message": "",
	"content": {
		"results": [{
			"msg": "",
			"exec_success": true,
			"order_id": 112532318
		},{
			"msg": "",
			"exec_success": true,
			"order_id": 112532310
		}]
	}
}
```