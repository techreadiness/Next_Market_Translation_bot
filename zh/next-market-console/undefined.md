# 物品管理

在物品管理页面，您可以注册和管理用于B2C及C2C交易的物品。

该页面通过Console环境提供物品注册API功能。

* 提供功能
  * [媒体文件上传](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#post-api-v1-media-upload)
  * [商品注册](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#post-api-v1-item)
  * [商品修改](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#put-api-v1-item-sku)

## 商品注册（单件注册）

商品注册支持**单件注册模式**。
当需注册少量商品时，可通过单件注册创建商品。

{% stepper %}
{% step %}
### 选择商品管理页面

* 登录NEXT Market控制台
* 在左侧菜单选择**商品管理**页面
{% endstep %}

{% step %}
### 选择商品注册

* 点击商品注册按钮进入注册界面

<figure><img src="../../.gitbook/assets/아이템 관리_아이템 등록.png" alt=""><figcaption></figcaption></figure>{% endstep %}

{% step %}
### 媒体文件上传

* 上传商品所需的媒体文件。

#### 上传方式

* 输入URL：填写已上传媒体文件的URL
* 文件上传：选择本地文件后上传

#### 支持格式

* 图片：JPG、PNG、WebP

⚠️ 视频格式上传虽可选择，但**官方不支持该功能，请仅以图片格式注册。**

#### 上传限制

* 文件大小：10MB以内
* 图片尺寸：含背景72x72像素

<figure><img src="../../.gitbook/assets/아이템 관리_미디어 파일 업로드.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### 基本信息输入

请填写物品的基本信息。

| 字段             | 值                                                                                                                                                                                                                                                              |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| SKU (必填)    | <ul><li>用于识别和管理商品的唯一商品代码</li><li>禁止重复注册</li><li><p>格式：200字符以内，用户可推测的值，可使用英文字母、数字及特殊字符</p><ul><li>特殊字符仅限下划线 <code>_</code> 不可使用，建议使用连字符 <code>-</code>  建议使用</li></ul><p>⚠️ 请确保SKU与实际游戏中使用的物品标识符保持一致。</p></li></ul> |
| 物品名称 (必填) | <ul><li>支持多语言输入：en, ko, ja, th, zh</li><li><p>物品列表及详情页显示值</p><ul><li>必须注册市场提供的所有语言版本</li></ul></li></ul>                                                                                                                                  |
| 物品描述 (必填) | <ul><li>在物品注册页面中设置为物品名称</li><li>需详细说明时，需通过<strong>CSV上传方式</strong>单独注册</li></ul>                                                                                                                                                        |

<figure><img src="../../.gitbook/assets/아이템 등록_기본정보.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### 套装物品注册（可选）

* 若为套装物品，可选择性设置。

⚠️ 套装物品包含的**子物品必须预先完成注册。**

| 字段        | 值                                    |
| --------- | ---------------------------------------- |
| 子商品SKU | <ul><li>输入组合商品的构成商品SKU</li></ul> |
| 数量        | <ul><li>输入子商品的数量</li></ul>          |

<figure><img src="../../.gitbook/assets/아이템 등록_서브아이템.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### C2C销售用商品注册（可选）

* 若为C2C交易使用的商品，可选择性设置。

⚠️ 注册C2C销售商品时，能力值需按商品（SKU）单位输入。该信息将用于C2C交易中的商品能力展示及条件验证。

| 字段        | 值                                                                                                                                                                                                                                                                                                                                                                                               |
| ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 能力名称        | <ul><li>多语言输入支持：en, ko, ja, th, zh</li><li>能力显示名称</li><li>必须注册市场提供的语言</li></ul>                                                                                                                                                                                                                                                                                                                         |
| 选项类型        | <ul><li>定义能力值属于何种性质的信息</li><li><p>选项类型选择</p><ul><li>基础能力值 (<code>BASIC</code>): 基础能力值</li><li>限制选项 (<code>CONSTRAINT</code>): 因变化而追加或变更的限制条件</li><li>物品包含数量 (<code>AMOUNT</code>): 用于表示物品内含数量的数值</li></ul></li><li>物品注册API的 <code>abilties.optionType</code> 值传递</li></ul><p>⚠️ <strong>建议</strong>在物品管理页面<strong>注册SKU时，将不随物品变动的基础能力值一并注册。</strong></p> |
| 显示格式        | <ul><li>设置能力值向用户<strong>展示的形式</strong></li><li><p>显示格式选择</p><ul><li>原始数值 (<code>NONE</code>): 直接显示输入数值</li><li>100% (<code>PPERCENTAGE</code>)</li><li> 100 (<code>NUMERIC</code>)</li><li>100Lv (<code>LEVEL</code>)</li></ul></li><li>物品注册API的 <code>abilties.unitType</code> 值传递</li></ul>                                                                                                    |
| 值            | <ul><li>以十进制格式输入</li><li>根据设置的选项类型及显示格式在界面呈现</li><li>项目注册API的 <code>abilties.value</code> 值传递</li></ul>                                                                                                                                                                                                                                                                                               |
| 国家访问限制设置  | <ul><li>设置C2C商品的国家访问限制政策</li><li><p>限制国家访问选项选择</p><ul><li>无限制</li><li>白名单 (<code>policies.whitelist</code>)</li><li>黑名单（<code>policies.blacklist</code>)</li><li>注：白名单与黑名单不可<strong>同时启用</strong></li></ul></li></ul>                                                                                                                                                                      |
| 最低价格（USDt） | <ul><li><p>限制C2C商品最低售价的政策</p><ul><li>禁止以低于设定最低价格的金额发布C2C商品</li></ul></li><li><code>policies.minPrice</code></li></ul>                                                                                                                                                                                                                                                                                  |

<figure><img src="../../.gitbook/assets/아이템 등록_C2C.png" alt=""><figcaption></figcaption></figure>{% endstep %}
{% endstepper %}

## 商品批量注册

商品批量注册功能适用于**需一次性注册大量商品**的情况，可通过上传CSV文件实现商品批量注册。

{% stepper %}
{% step %}
### 选择商品管理页面

* 登录NEXT Market控制台
* 在左侧菜单选择**商品管理**页面
{% endstep %}

{% step %}
### 下载模板

* 点击**模板下载**按钮获取商品批量注册专用**CSV模板文件**。
* 模板包含商品注册所需的基本字段。

<figure><img src="../../.gitbook/assets/아이템 관리_템플릿.png" alt=""><figcaption></figcaption></figure>{% endstep %}

{% step %}
### 编写商品清单

* 在下载的**CSV模板文件**中填写待注册商品信息。
* 每项填写方式请参照**商品注册（单个注册）**指南进行操作。
* 注意：imageUrl字段仅支持输入已上传媒体文件的URL，不支持文件上传功能。

⚠️ 若必填项缺失或格式不符，可能导致上传失败。

<figure><img src="../../.gitbook/assets/아이템 관리_csv 템플릿.png" alt=""><figcaption></figcaption></figure>{% endstep %}

{% step %}
### CSV上传

* 选择填写完成的CSV文件进行上传。
* 选择文件后点击**上传**按钮，即可开始批量注册商品。

#### ⚠️ 批量注册注意事项

* CSV上传功能仅适用于**新增商品或修改已注册商品信息**。
* 建议在批量注册前进行**小批量测试上传**。

<figure><img src="../../.gitbook/assets/아이템 관리_csv 업로드.png" alt=""><figcaption></figcaption></figure>{% endstep %}
{% endstepper %}

## 商品修改

商品修改功能适用于**需变更已注册商品信息的情况**。
NEXT Market Console提供**单项修改**与**批量修改**两种操作方式。

### 商品修改方式

#### 单项修改

用于修改单个商品信息。

* 登录**NEXT Market控制台**
* 在左侧菜单选择**商品管理**页面
* 在商品列表中选定待修改商品
* 点击**修改**按钮
* 修改商品信息后保存

<figure><img src="../../.gitbook/assets/아이템 관리_수정.png" alt=""><figcaption></figcaption></figure>#### 批量修改

适用于需同时修改多个商品信息的情况。

* 在**商品管理**页面点击**CSV下载**按钮
* 在下载的CSV文件中修改商品信息
* 上传修改完成的CSV文件
* 上传完成后确认修改结果

<figure><img src="../../.gitbook/assets/아이템 관리_csv 다운로드.png" alt=""><figcaption></figcaption></figure>### ⚠️ 修改注意事项

* 修改在售商品信息可能影响服务运营。
* 批量修改前建议进行**小范围测试修改**。
