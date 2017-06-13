### 获取申报分类（xlobo.catalogue.get）

---
### 系统参数

* 接口调用参数

| 名称 | 类型 | 必须 | 描述 |
| :--- | :--- | :--- | :--- |
| method | String | 是 | API名称 |
| app\_key | String | 是 | 洋码头分配给买手的AppKey。 |
| sign\_method | String | 是 | 签名的摘要算法，可选值为：md5。 |
| sign | String | 是 | API输入参数签名结果，签名算法介绍请[点击这里](/openapi/README.md#signmethod)。 |
| session\_key | String | 是 | 用户登录授权成功后，TOP颁发给应用的授权信息，详细介绍请[点击这里](/openapi/README.md#getappkey)。 |
| timestamp | String | 是 | 时间戳，格式为yyyy-MM-dd HH:mm:ss，时区为GMT+8，例如：2017-01-01 12:00:00。洋码头API服务端允许客户端请求最大时间误差为10分钟。 |
| format | String | 否 | 响应格式。默认为json格式。 |



### 返回参数

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String |  |  |
| categorys | JSON Object |  |  |  |
| version | String | N | 版本号（yyyy-MM-dd HH：mm：ss） |


### 类型描述（CategoryInfo） 

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| category_id | String | N | 分类Id |
| category_cn_name | String | N | 分类中文名 |
| category_en_name | String | N | 分类英文名 |
| category_level | Int | N | 分类级别 |
| category_parent_id | Int | N | 分类父ID |

### 返回结果的格式