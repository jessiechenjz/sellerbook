### 订单发货 （ymatou.order.deliver）

---

### 接口描述

* 订单发货(录入物流单号进行发货处理)

#### 业务参数


| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| deliver_orders |DeliverOrder[] | 是 |  |待发货的订单物流信息 |

* 数据类型（DeliverOrder）

| 名称 | 类型 | 必须 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- | :--- |
| order_id | long | 是 | 1729299393 | 待发货的订单编号 |
| logistics_company\_id | String | 是 | Y073 | 平台物流公司标识 |
| tracking_number | String | 是 | DB1234567800111 | 物流面单号 |
| is_domestic_delivery | boolean | 是 | true | 是否国内段发货 |


### 返回参数

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String | 更新库存成功 | 接口调用返回信息 |
| content | JSON Object |  | BizResult的JSON报文体 |

* 数据类型(BizResult）

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| results | DeliverResult[] |  | 发货结果 |

* 数据类型（DeliverResult）

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| order_id | long | 105913276 | 订单号 |
| exec_success | boolean | true | 是否执行成功 |
| msg | string |  | 处理信息 |


#### 示例报文

* url：https://open.ymatou.com/apigateway/v1?app_id=CgZcxYhQaCXOt31YQe&method=ymatou.order.deliver
* 请求报文:    
<br  />


```
{
	"app_id": "CgZcxYhQaCXOt31YQe",
	"method": "ymatou.order.deliver",
	"sign_method": "MD5",
	"auth_code": "JmhUXrDRP4Mw7zEHs2p3iQJ4T7mUOGr3",
	"timestamp": "2017-06-07 14:49:38",
	"sign": "8F01503D6352988B8CDB3CE4EA5FAF0C",
	"nonce_str": "9204667338768330660933423992945",
	"biz_content": "{\"deliver_orders\":[{\"order_id\":112532318,\"logistics_company_id\":\"Y073\",\"tracking_number\":\"89049482110\",\"is_domestic_delivery\":false}]}"
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
		}]
	}
}
```