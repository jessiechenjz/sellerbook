### 签名算法


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
    