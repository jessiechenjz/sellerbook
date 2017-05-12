### API调用指南

---

#### 调用URL

[https://open.ymatou.com/api/v1/{app\_id}/{method}](https://open.ymatou.com/api/v1/{app_id}/{method})

#### 系统参数格式

* 统一接口调用参数

| 名称 | 类型 | 必填 | 描述 |
| :--- | :--- | :---: | :--- |
| app\_id | String\(32\) | 是 | 洋码头分配的应用appId 此参数在url上替换{app\_id} <br/> 示例值: zWYVVFagTfenOHDPTm |
| method | String\(128\) | 是 | api名称 此参数在url上替换{method} <br/> 示例值: ymatou.skus.stock.update |
| sign\_method | String\(32\) | 是 | 签名摘要算法，目前只支持：MD5 |
| auth\_code | String\(32\) | 是 | 授权码，针对买手与应用的唯一授权码 <br/> 示例值: VlERCP4fZzHzqK7vnr8weOYqepkXriKL |
| timestamp | String\(19\) | 是 | 时间戳，格式为yyyy-MM-dd HH:mm:ss，时区为GMT+8 洋码头API服务端允许客户端请求最大时间误差为10分钟。 <br/> 示例值：2017-01-01 12:00:00 |
| sign | String\(32\) | 是 | API输入参数签名结果，签名算法介绍[签名算法](sign.md) <br/> 示例值: A950EEDA1342BBDB83AB8C79B759BE44 |
| nonce\_str | String\(32\) | 是 | 随机字符串，长度要求在32位以内。推荐随机算法 <br/> 示例值: 3g3jJVfI9CWwKMr45x9SkB0gbi9kAn28 |
| biz\_content | String | 是 | 业务请求参数的集合，最大长度不限，除公共参数外所有请求参数都必须放在这个参数中传递，具体参照各api请求参数。 传入的是json格式字符串 <br/> 示例值:  "{\"skuStocks\":\[{\"outer\_sku\_id\":\"393992\",\"stock\_num\":10},{\"outer\_sku\_id\":\"393993\",\"stock\_num\":12}\]}" |

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
  * url:  [https://open.ymatou.com/api/v1/zWYVVFagTfenOHDPTm/ymatou.skus.stock.update](https://open.ymatou.com/api/v1/zWYVVFagTfenOHDPTm/ymatou.skus.stock.update)

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



#### 签名算法

##### 签名生成的通用步骤如下

  * 第一步，设所有发送或者接收到的数据为集合M，将集合M内非空参数值的参数按照参数名ASCII码从小到大排序（字典序），使用URL键值对的格式（即key1=value1&key2=value2…）拼接成字符串stringA。
    
    特别注意以下重要规则
    
     1. 参数名ASCII码从小到大排序（字典序）；
     2. 如果参数的值为空不参与签名；
     3. 参数名区分大小写 ；
     4. 验证调用返回或微信主动通知签名时，传送的sign参数不参与签名，将生成的签名与该sign值作校验；
     

    ```
      例如将foo=1,bar=2,baz=3 排序为bar=2,baz=3,foo=1, 参数名和参数值链接后，得到拼装字符串bar=2&baz=3&=foo1
    ```

  * 第二步，在stringA最后拼接上app_secret得到stringSignTemp字符串，并对stringSignTemp进行MD5运算，再将得到的字符串所有字符转换为大写，得到sign值signValue。
    
     
    
  * 将排序后的参数与其对应值，组合成“参数=参数值”的格式，并且把这些参数用字符连接起来，此时生成的字符串为待签名字符串。MD5签名的商户需要将key的值拼接在字符串后面，调用MD5算法生成sign；



    ```
    app_id: zWYVVFagTfenOHDPTm
    app_secret: cvxEvN7q2ixmN6Y8DFRJmuP79H2zxctK
    method: ymatou.skus.stock.update
    sign_method: MD5
    timestamp: 2017-01-01 12:00:00
    nonce_str: 3g3jJVfI9CWwKMr45x9SkB0gbi9kAn28
    auth_code: UkeV6CUfk8OKKv1UkjEmfBDU75ZjunA0
    
    1: stringA ="app_id=zWYVVFagTfenOHDPTm&auth_code=UkeV6CUfk8OKKv1UkjEmfBDU75ZjunA0&method=ymatou.skus.stock.update&nonce_str=3g3jJVfI9CWwKMr45x9SkB0gbi9kAn28&sign_method=MD5&timestamp=2017-01-01 12:00:00"
    2: stringSignTemp = stringA + "&app_secret=" + app_secret
    3: sign = MD5(stringSignTemp).toUpperCase()
    
    加密后生成的sign：AC153D8C7F8D0EFEB1BA55177DEA2031
    
    ```
    
