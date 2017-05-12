
### API调用指南
---

#### 调用URL

https://open.ymatou.com/api/v1/{app_id}/{method}

#### 系统参数格式

* 统一接口调用参数

| 名称 | 类型 | 必填 | 描述 | 示例值 |
| :--- | :--- | :---: | :--- | :--- |
| app\_id | String\(32\) | 是 | 洋码头分配的应用appId 此参数在url上替换{app\_id} | zWYVVFagTfenOHDPTm |
| method | String\(128\) | 是 | api名称 此参数在url上替换{method} | ymatou.skus.stock.update |
| sign\_method | String\(32\) | 是 | 签名摘要算法，目前只支持：MD5 | MD5 |
| auth\_code | String\(32\) | 是 | 授权码，针对买手与应用的唯一授权码 | VlERCP4fZzHzqK7vnr8weOYqepkXriKL |
| timestamp | String\(19\) | 是 | 时间戳，格式为yyyy-MM-dd HH:mm:ss，时区为GMT+8，例如：2017-01-01 12:00:00。洋码头API服务端允许客户端请求最大时间误差为10分钟。 | 2017-01-01 12:00:00 |
| sign | String\(32\) | 是 | API输入参数签名结果，签名算法介绍 | A950EEDA1342BBDB83AB8C79B759BE44 |
| nonce\_str | String\(32\) | 是 | 随机字符串，长度要求在32位以内。推荐随机算法 | 3g3jJVfI9CWwKMr45x9SkB0gbi9kAn28 |
| biz\_content | String | 是 | 业务请求参数的集合，最大长度不限，除公共参数外所有请求参数都必须放在这个参数中传递，具体参照各api请求参数。 传入的是json格式字符串 | "{\"skuStocks\":\[{\"outer\_sku\_id\":\"393992\",\"stock\_num\":10},{\"outer\_sku\_id\":\"393993\",\"stock\_num\":12}\]}" |

* 统一返回参数

| 名称 | 类型 | 必填 | 描述 | 示例值 |
| :--- | :--- | :---: | :--- | :--- |
| code | String\(16\) | 是 | 0000 成功  ，非成功以及公共返回码其他由各接口确定 | 0000 |
| message | String\(128\) | 否 | 返回信息，如非空，为错误原因： 验签失败、参数格式校验错误等 | 验签失败 |
| content | json object | 否 | 返回数据，具体内容由各个api确定 |  |
 
* 公共返回码

| 返回码 | 描述 |
| :--- | :--- |
| 0000 | 成功 |
| 0001 | 缺少必填参数 |
| 0002 | 非法授权码 |
| 0003 | 非法请求时间 |
| 0004 | 验签失败 |
| 0005 | 非法api名称 |
| 0009 | 处理失败,请稍后重试 |
| 1001 | 业务请求参数JSON格式不正确 |

* 请求示例\(ymatou.skus.stock.update 修改商品库存\)

  * appId : zWYVVFagTfenOHDPTm
  * appSecret: UkeV6CUfk8OKKv1UkjEmfBDU75ZjunA0
  * url:  [https:\/\/open.ymatou.com\/api\/v1\/zWYVVFagTfenOHDPTm\/ymatou.skus.stock.update](https://open.ymatou.com/api/v1/zWYVVFagTfenOHDPTm/ymatou.skus.stock.update)

  * header: Content-Type:application\/json

  * body:

    > {
    >     "sign\_method":"MD5",
    >     "auth\_code":"VlERCP4fZzHzqK7vnr8weOYqepkXriKL",
    >     "timestamp":"2017-01-01 12:00:00",
    >     "sign":"A950EEDA1342BBDB83AB8C79B759BE44",
    >     "nonce\_str":"3g3jJVfI9CWwKMr45x9SkB0gbi9kAn28",
    >     "biz\_content": "{\"skuStocks\":      \[{\"outer\_sku\_id\":\"393992\",\"stock\_num\":10},{\"outer\_sku\_id\":\"393993\",\"stock\_num\":12}\]}"
    >   }