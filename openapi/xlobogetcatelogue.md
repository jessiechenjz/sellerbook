### 获取申报分类（xlobo.catalogue.get）

---
### 系统参数

* 接口调用参数


### 返回参数

| 名称 | 类型 | 示例值 | 描述 |
| :--- | :--- | :--- | :--- |
| code | String | 0000 | 返回响应代码，都是公共返回码，无特殊业务响应码 |
| message | String |  |  |
| content | JSON Object |  |  |


*  类型描述

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
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