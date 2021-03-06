### 码头API服务介绍

---

码头API服务是帮助买手更高效的管理交易流程而提供的接口层的服务。首先开放的API服务涉及主要涉及到交易流程的部分，譬如获取订单信息，订单发货，商品的库存同步等；随着业务的进一步开放，码头的API会开放更多的服务。

#### 使用流程

* 登录码头后台，申请使用API的权限
* 阅读接口文档和DEMO代码，对接码头的平台
* 使用ERP的买手，联系相关的ERP厂商，检查是否已经支持洋码头平台
* 其他信息

#### 接入准备 {#signmethod}

* ##### 获取APPKEY {#getappkey}

买手登录seller.ymatou.com, 选择“买手服务-&gt;第三方应用授权“ ，点击“新增授权”，获取API调用的配置信息。

![](/openapi/images/getappkey.png)

#### 了解系统调用

* 平台调用URL, 接口采用HTTPS加密协议 \([https://open.ymatou.com/apigateway/v1/{app\_id}/{method}](https://open.ymatou.com/apigateway/v1/{app_id}/{method})

* 接口系统参数说明 [指南](/openapi/how-to-call-api.md)

* 接口SDK包下载 （开发中）

#### 

#### 合作厂商

| 厂商名称 | 厂商官网地址 | 厂商联系人 | 支持状态 |
| :--- | :--- | :--- | :--- |
| [网店管家](/openapi/openapi-partners.md#wdgj) | 试用通道 c.wdgj.com注册 客服代码：sq08 |  | 对接完成 |
| 管家婆 |  |  | 洽谈中 |
| 电商大师 |  |  | 对接中 |
| 旺店通 |  |  | 洽谈中 |



