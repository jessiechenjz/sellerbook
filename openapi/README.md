### 码头API服务介绍

---

码头API服务是帮助买手更高效的管理交易流程而提供的接口层的服务。首先开放的API服务涉及主要涉及到交易流程的部分，譬如获取订单信息，订单发货，商品的库存同步等；随着业务的进一步开放，码头的API会开放更多的服务。

#### 使用流程

* 登录码头后台，申请使用API的权限
* 阅读接口文档和DEMO代码，对接码头的平台
* 使用ERP的买手，联系相关的ERP厂商，检查是否已经支持洋码头平台

#### 接入准备 {#signmethod}

* ##### 获取APPKEY {#getappkey}

  ```
  insert image
  ```

![](/openapi/images/getappkey.png)

* ##### 参数签名 {#signmethod}

  * 获取所有请求参数，不包括字节类型参数，如文件、字节流，剔除sign与sign\_method参数

* 将筛选的参数按照第一个字符的键值ASCII码递增排序（字母升序排序），如果遇到相同字符则按照第二个字符的键值ASCII码递增排序，以此类推。

  ```
  例如将foo=1,bar=2,baz=3 排序为bar=2,baz=3,foo=1
  参数名和参数值链接后，得到拼装字符串bar2baz3foo1
  ```

* 将排序后的参数与其对应值，组合成“参数=参数值”的格式，并且把这些参数用字符连接起来，此时生成的字符串为待签名字符串。MD5签名的商户需要将key的值拼接在字符串后面，调用MD5算法生成sign；

```
appKey：10210015121700112233、sessionKey：SESSIONKEYFORLIUYUETOTEST0123456、format：json、ver：1.0、
method：ymatou.skus.price.update、timestamp：2017-2-17 10:00:00、appSecret：APPSECRETFORLIUYUETOTEST01234567

APPSECRETFORLIUYUETOTEST01234567appKey10210015121700112233formatjsonmethodyhd.category.brands.get
sessionKeySESSIONKEYFORLIUYUETOTEST0123456timestamp2015-12-17 00:00:00
ver1.0APPSECRETFORLIUYUETOTEST01234567

加密后生成的sign：72c33f6b5c2d555b3527e510ade690cd
```

参考格式

```
http request
```

```
http request with signature
```

#### 接口一览表

| 接口名称 | 接口描述 |
| :--- | :--- |
| [ymatou.skus.stock.update](/openapi/updateproductstock.md) | 批量更新商品库存数量 |
| [ymatou.skus.price.update](/openapi/updateproductprice.md) | 批量更新商品价格 |
| [ymatou.order.list.get](/openapi/getorderlist.md) | 获取订单列表信息 |
| [ymatou.order.detail.get](/openapi/getorderdetail.md) | 获取单个订单详情 |
| [ymatou.logistics.send](/openapi/sendlogistics.md) | 订单发货接口 |
| [ymatou.logistics.companies.get](/openapi/getlogisticscompanies.md) | 获取平台物流公司信息 |

#### 合作厂商

| 厂商名称 | 厂商官网地址 | 厂商联系人 | 支持状态 |
| :--- | :--- | :--- | :--- |
| 管家婆 |  |  | 洽谈中 |



