# NEXT Market控制台使用指南

## NEXT Market控制台简介

**NEXT Market控制台**是NEXT Market提供的核心API功能，以**基于网页的控制台形式呈现**，作为一款管理工具，旨在支持开发及运营过程中**轻松直观地注册和管理道具·商品·任务**。

## 访问 NEXT Market Console

### 预览环境

* 网址：[https://app-console.nextmarket.games/](https://app-console.nextmarket.games/)
* 认证信息：预览版 API 密钥

### 生产环境

* 网址：[https://console.nextmarket.games/](https://console.nextmarket.games/)
* 认证信息：Prod API Key

## NEXT Market控制台提供功能

通过NEXT Market控制台，您可在**基于网页的控制台**环境中直接**注册·管理**NEXT Market API提供的核心功能。

### [商品管理](https://next-market-admin.gitbook.io/copy-of-next-market-docs/~/revisions/80r3cbY8BxZFGmdGSqV2/next-market-console/undefined)

可注册并管理用于B2C及C2C交易的商品。

* 提供功能
  * [媒体文件上传](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#post-api-v1-media-upload)
  * [商品注册](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#post-api-v1-item)
  * [商品修改](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#put-api-v1-item-sku)

### [B2C商品管理](https://next-market-admin.gitbook.io/copy-of-next-market-docs/~/revisions/80r3cbY8BxZFGmdGSqV2/next-market-console/b2c)

可注册B2C商品的销售信息并管理销售状态。

* 提供功能
  * [版块注册](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-3#post-api-v1-sale-b2c-section)
  * [分区变更](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-3#patch-api-v1-sale-b2c-section-sectionid)
  * [销售注册](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-4#post-api-v1-sale-b2c)
  * [销售修改](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-4#patch-api-v1-sale-b2c-b2csaleid)

### [C2C商品能力管理](https://next-market-admin.gitbook.io/copy-of-next-market-docs/~/revisions/80r3cbY8BxZFGmdGSqV2/next-market-console/c2c)

可设置并管理适用于C2C商品的**能力（属性）**。

* 提供功能
  * [商品能力设置注册](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#post-api-v1-item-ability)
  * [修改物品能力设置](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#put-api-v1-item-ability-code)

### [任务管理](https://next-market-admin.gitbook.io/copy-of-next-market-docs/~/revisions/80r3cbY8BxZFGmdGSqV2/next-market-console/undefined-1)

可创建任务并管理其运营状态。

* 提供功能
  * [任务创建](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-7#post-api-v1-incentive-mission)
  * [任务修改](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-7#put-api-v1-incentive-mission-missionid)

## 注意事项

⚠️ 涉及道具、商品、任务注册时，请务必与LINE NEXT事先协商后进行。

NEXT Market控制台是面向开发者及运营者、可直接**注册·管理道具、商品、任务**的网页端管理工具，控制台生成的数据**将以与NEXT Market API完全相同的方式运行。**

若需进行运营管理修改，请务必**确认各变更项的注意事项后再进行修改**。
此外，**Console不提供已注册数据的删除功能，如需删除请通过API操作**。
