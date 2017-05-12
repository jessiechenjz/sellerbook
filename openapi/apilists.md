#### 接口一览表

---

#### 码头业务接口

| 接口名称 | 接口描述 |
| :--- | :--- |
| [ymatou.skus.stock.update](/openapi/updateproductstock.md) | 批量更新商品库存数量 |
| [ymatou.skus.price.update](/openapi/updateproductprice.md) | 批量更新商品价格 |
| [ymatou.order.list.get](/openapi/getorderlist.md) | 获取订单列表信息 |
| [ymatou.order.detail.get](/openapi/getorderdetail.md) | 获取单个订单详情 |
| [ymatou.logistics.send](/openapi/sendlogistics.md) | 订单发货接口 |
| [ymatou.logistics.companies.get](/openapi/getlogisticscompanies.md) | 获取买手物流公司信息 |

#### 贝海物流接口

| 接口名称 | 接口描述 |
| :--- | :--- |
| xlobo.labels.createNoVerification | 任意发件人不使用商品编码做单接口 |
| xlobo.labels.file.getFileA4 / xlobo.labels.file.getFile10x15 | 获得单个面单文件 |
| xlobo.status.get | 贝海运单物流状态获取 |
| xlobo.catalogue.get | 获取贝海发货申报分类 |



#### Open Api 统一接口

https://open.ymatou.com/api/v1/{app_id}/{method} 

| 名称 | 类型 | 必填 | 描述 | 示例值 |
| :--- | :--- | :--- | :--- | :--- |
| app_id | String(32) | 是 | 洋码头分配的应用appId 此参数在url上替换{app_id} | 02QFbmsgvkw3M0Yyal  
| method | String(128) | 是 | api名称 此参数在url上替换{method} | ymatou.skus.stock.update
| sign_method | String(32) | 是 | 签名摘要算法，目前只支持：MD5 | MD5 
| auth_code | String(32) | 是 | 授权码，针对买手与应用的唯一授权码 | VlERCP4fZzHzqK7vnr8weOYqepkXriKL
| timestamp | String(19) | 是 | 时间戳，格式为yyyy-MM-dd HH:mm:ss，时区为GMT+8，例如：2017-01-01 12:00:00。洋码头API服务端允许客户端请求最大时间误差为10分钟。 | 2017-01-01 12:00:00
| sign | String(32) | 是 | API输入参数签名结果，签名算法介绍 | 
| nonce_str | String(32) | 是 | 随机字符串，长度要求在32位以内。推荐随机算法 |
| biz_content | String | 是 | 业务请求参数的集合，最大长度不限，除公共参数外所有请求参数都必须放在这个参数中传递，具体参照各api请求参数。 传入的是json格式字符串 | "{\"skuStocks\":[{\"outer_sku_id\":\"393992\",\"stock_num\":10},{\"outer_sku_id\":\"393993\",\"stock_num\":12}]}" 





