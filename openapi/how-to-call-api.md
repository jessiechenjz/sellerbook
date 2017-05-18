****### API调用指南

---

#### 调用URL(POST)

[https://open.ymatou.com/api/v1?app_id={appId}&method={method}](https://open.ymatou.com/api/v1app_id={appId}&method={method})

其中：<br/>
{appId}：洋码头分配的应用appId。示例值: zWYVVFagTfenOHDPTm
{method}：api名称。此参数在url上替换{method}。 <br/> 示例值: ymatou.sku.stock.update

POST报文体是如下请求参数组成的JSON报文
响应报文体是如下响应参数组成JSON报文

#### 请求参数格式

| 名称 | 类型 | 必填 | 描述 |
| :--- | :--- | :---: | :--- |
| sign\_method | String\(32\) | 是 | 签名摘要算法。目前只支持：MD5。 |
| auth\_code | String\(32\) | 是 | 授权码。买手授权应用访问的凭证。 <br/> 示例值: VlERCP4fZzHzqK7vnr8weOYqepkXriKL |
| timestamp | String\(19\) | 是 | 时间戳，格式为yyyy-MM-dd HH:mm:ss，时区为GMT+8。 洋码头API服务端允该时间戳与当前时间最大误差为10分钟。 <br/> 示例值：2017-01-01 12:00:00 |
| sign | String\(32\) | 是 | API输入参数签名结果，签名算法介绍[签名算法](sign.md) <br/> 示例值: A950EEDA1342BBDB83AB8C79B759BE44 |
| nonce\_str | String\(32\) | 是 | 随机字符串，长度要求在32位以内。建议每笔请求传入一个随机字符串 <br/> 示例值: 3g3jJVfI9CWwKMr45x9SkB0gbi9kAn28 |
| biz\_content | String | 是 | 请求的业务参数组成的JSON字符串，请至请求详情页查看每个请求的具体业务参数定义。 <br/>示例值: "{\"sku_stocks\":\[{\"outer\_sku\_id\":\"393992\",\"stock\_num\":10},{\"outer\_sku\_id\":\"393993\",\"stock\_num\":12}\]}" |

#### 响应参数格式

| 名称 | 类型 | 必填 | 描述 | 示例值 |
| :--- | :--- | :---: | :--- | :--- |
| code | String\(16\) | 是 | 响应码。请至各请求详情页查看请求有无公共返回码之外的业务返回码 | 0000 |
| message | String\(128\) | 否 | 响应码描述 |
| content | json object | 否 | 返回业务数据，具体内容由各个api确定 | |

* 公共返回码

| 返回码 | 描述 |
| :--- | :--- |
| 0000 | 成功 |
| 0001 | 缺少必填参数 |
| 0002 | 非法授权码 |
| 0003 | 非法请求时间 |
| 0004 | 验签失败 |
| 0005 | 非法api名称 |
| 0006 | 业务请求参数JSON格式不正确 |
| 0009 | 处理失败,请稍后重试 |

* 请求示例\(ymatou.sku.stock.update 修改商品库存\)

* url: [https://open.ymatou.com/api/v1?app_id=zWYVVFagTfenOHDPTm&method=ymatou.sku.stock.update](https://open.ymatou.com/api/v1?app_id=zWYVVFagTfenOHDPTm&method=ymatou.sku.stock.update)

* header: Content-Type:application\/json

* body:

> {
> "sign\_method":"MD5",
> "auth\_code":"VlERCP4fZzHzqK7vnr8weOYqepkXriKL",
> "timestamp":"2017-01-01 12:00:00",
> "sign":"A950EEDA1342BBDB83AB8C79B759BE44",
> "nonce\_str":"3g3jJVfI9CWwKMr45x9SkB0gbi9kAn28",
> "biz\_content": "{\"sku_stocks\": \[{\"outer\_sku\_id\":\"393992\",\"stock\_num\":10},{\"outer\_sku\_id\":\"393993\",\"stock\_num\":12}\]}"
> }

* resp
> {
> "code":"0000",
> "message":"成功",
> "content": {"results":[{"msg":"成功","outer_sku_id":"393992","success":true},{"msg":"成功","outer_sku_id":"393993","success":true}]}}


#### 签名算法

##### 签名生成的通用步骤如下

* 第一步，设所有发送的数据为集合M，将集合M内非空参数值的参数按照参数名ASCII码从小到大排序（字典序），使用URL查询参数键值对的格式（即key1=value1&key2=value2…）拼接成字符串stringA。
特别注意以下重要规则
1. 参数名ASCII码从小到大排序（字典序）；
2. 如果参数的值为空不参与签名；
3. 参数名区分大小写 ；
4，请求url中的app_id和method参数也参与签名
4. 请求报文体内的sign参数不参与签名

```
例如将foo=1,bar=2,baz=3 排序为bar=2,baz=3,foo=1, 参数名和参数值链接后，得到拼装字符串bar=2&baz=3&=foo1
```

* 第二步，在stringA最后拼接上&app_secret=${appSecret}得到stringSignTemp字符串，并对stringSignTemp进行MD5运算，再将得到的字符串所有字符转换为大写，得到sign值signValue。


* 示例
```
app_id: zWYVVFagTfenOHDPTm
app_secret: cvxEvN7q2ixmN6Y8DFRJmuP79H2zxctK
method: ymatou.sku.stock.update
sign_method: MD5
timestamp: 2017-01-01 12:00:00
nonce_str: 3g3jJVfI9CWwKMr45x9SkB0gbi9kAn28
auth_code: UkeV6CUfk8OKKv1UkjEmfBDU75ZjunA0
biz_content: {"sku_stocks": [{"outer_sku_id":"393992","stock_num":10},{"outer_sku_id":"393993","stock_num":12}]}
1: stringA <br/>app_id=zWYVVFagTfenOHDPTm&auth_code=UkeV6CUfk8OKKv1UkjEmfBDU75ZjunA0&biz_content={"sku_stocks": [{"outer_sku_id":"393992","stock_num":10},{"outer_sku_id":"393993","stock_num":12}]}&method=ymatou.skus.stock.update&nonce_str=3g3jJVfI9CWwKMr45x9SkB0gbi9kAn28&sign_method=MD5&amp;timestamp=2017-01-01 12:00:00
<br/><br/>
2: stringSignTemp = stringA + "&app_secret=" + app_secret
app_id=zWYVVFagTfenOHDPTm&auth_code=UkeV6CUfk8OKKv1UkjEmfBDU75ZjunA0&biz_content={"sku_stocks": [{"outer_sku_id":"393992","stock_num":10},{"outer_sku_id":"393993","stock_num":12}]}&method=ymatou.skus.stock.update&nonce_str=3g3jJVfI9CWwKMr45x9SkB0gbi9kAn28&sign_method=MD5&timestamp=2017-01-01 12:00:00&app_secret=cvxEvN7q2ixmN6Y8DFRJmuP79H2zxctK

3: sign = MD5(stringSignTemp).toUpperCase()
加密后生成的sign：AC153D8C7F8D0EFEB1BA55177DEA2031
```