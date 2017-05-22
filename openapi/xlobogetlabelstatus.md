### 获取面单物流状态（xlobo.status.get）

---


### 系统参数

* 接口调用参数 [接口调用指南](/openapi/how-to-call-api.md)

### 业务参数

| 字段名 | 类型 | 可否为空 | 含义 |
| :--- | :--- | :--- | :--- |
| BillCodes |  | N | 一个或者多个面单号 |

### 输出：

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| TotalCount | Int | N | 更新数量 |
| ErrorCount | Int | N | 出错数量 |
| ErrorInfoList\(ErroInfo\) |  |  |  |
| Identity | String | Y | 错误数据的标识 |
| ErrorCode | String | Y | 错误代码 |
| ErrorDescription | String | Y | 错误描述 |
| Result\(BillTrackInfo\) |  |  |  |
| BillCode | String | N | 面单号 |
| BusinessNo | String | Y | 业务编号 |
| BillStatusList |  |  | 面单状态列表 |
| StartTime | String | N | 状态发生时间 |
| Operator | String | N | 操作人 |
| Status | String | N | 状态名称 |
| StatusDetail | String | Y | 状态描述 |


### 错误信息描述

| 错误码 | 描述 |
| :--- | :--- |
| Xlobo.bill.param\_missing | 参数{0}为空，检查传入参数是否正确 |
| Xlobo.bill.param\_error | 参数{0}错误或者不合法，检查传入的参数是否正确 |
| Xlobo.bill.parm\_length\_over | 面单/运单信息列表过长，最多支持同时查询20个面单运单 |
| Xlobo.bill.param\_code\_not\_exists | 面单/运单号{0}不存在，检查传入的面单/运单号是否有效 |


