### 物流状态获取（xlobo.status.get）

---

### 字段定义

### 输入：



| 字段名 | 类型 | 可否为空 | 含义 |
| :--- | :--- | :--- | :--- |
| BillCodes |  | N | 一个或者多个面单号 |

### 输出：

| 字段名称 | 类型 | 可否为空 | 描述 |
| :--- | :--- | :--- | :--- |
| TotalCount |  | N | 更新数量 |
| ErrorCount |  | N | 出错数量 |
| ErrorInfoList\(ErroInfo\) |  |  |  |
| Identity |  | Y | 错误数据的标识 |
| ErrorCode |  | Y | 错误代码 |
| ErrorDescription |  | Y | 错误描述 |
| Result\(BillTrackInfo\) |  |  |  |
| BillCode |  | N | 面单号 |
| BusinessNo |  | Y | 业务编号 |
| 面单状态列表，BillStatusList |  | N | 状态发生时间 |
| StartTime |  | N | 操作人 |
| Operator |  |  |  |
| Status |  | N | 状态名称 |
|  |  | Y | 状态描述 |



