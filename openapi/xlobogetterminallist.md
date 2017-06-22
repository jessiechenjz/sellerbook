### 获取货站（xlobo.hub.get）

---

#### 接口描述

* 获取贝海货站的ID信息，在创建面单时候使用

### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)

### 业务参数


### 返回参数

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String |  |  |
| content | JSON Object |  |  |



*  类型描述

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| version | String | N | 版本号（yyyy-MM-dd HH：mm：ss） |
| logistic_info_list | LogisticInfo[] |  |结果  |



*  类型描述 （LogisticInfo）

| 字段名称 | 类型 | 可空 | 描述 |
| :--- | :--- | :--- | :--- |
| logistic_id | integer | N | 货站Id |
| logistic_name | String | N | 货站名称 |
| logistic_address | String | N | 货站地址 |


### 错误信息描述