metaLinks:
  alternates:
    - &gt;-
      https://app.gitbook.com/s/pt4moEMpSf4BGvjJCzQm/api-usage-guide/api-version-information
---

# 版本信息

## 发布说明

### v1.10\_2025.09.10

* 提供销售量统计API

### v1.9\_2025.09.08

* 发行一次性令牌时新增推荐码与自定义有效负载
* 配送时新增自定义有效负载参数
* 新增配送记录查询API

### v1.8\_2025.08.22

* 移动应用WebView指南变更：Cookie → URL参数(inapp=true)

### v1.7\_2025.07.24

* [商店认证一次性令牌请求](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-1#undefined-2)中，若Region参数对应制裁国家则返回BadRequest

### v1.6\_2025.07.18

* 添加[移动应用WebView指南](https://next-market-admin.gitbook.io/next-market-docs/api/undefined#v1.8_2025.08.22)

### v1.5\_2025.07.08

* [销售数据查询](https://github.com/tech-support-trade/docs/wiki/API-Guide#매출-데이터-조회)新增items\[].skus, items\[].quantity字段
* [销售注册请求](https://github.com/tech-support-trade/docs/wiki/API-Guide#판매-등록-요청)中limitPurchaseCount改为可选字段，说明内容更新。

### v1.4\_2025.07.04

* 支持B2C销售注册时多货币注册。
  * 删除price、currency输入字段
  * 新增multiCurrencyPrice输入字段
* periodType字段名称变更 → periodicType

### v1.3\_2025.07.01

* color输入字段新增GREY、NONE选项
* link.deviceType的PC → WEB变更

### v1.2\_2025.06.26

* 将物品能力设置中的color修改为content.color
* 新增[C2C销售取消请求](https://github.com/tech-support-trade/docs/wiki/API-Guide#C2C-판매-취소-요청)功能

### v1.1\_2025.06.24

* 在[商店认证一次性令牌请求](https://github.com/tech-support-trade/docs/wiki/API-Guide#스토어-인증용-원타임-토큰-요청)中新增C2C销售注册令牌发行参数定义
* 在[封装请求](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#undefined-20)中新增c2cSaleId响应字段
* 添加API可用环境标签(`preview` `prod`)
* 新增[销售数据查询](https://github.com/tech-support-trade/docs/wiki/API-Guide#매출-데이터-조회)功能（7月10日起可用）

### v1.0\_2025.05.27

* B2C、C2C、Mission\
