# C2C商品属性管理

**商品属性管理页面用于注册和管理C2C商品所使用的&quot;属性项目（类型）&quot;。**
需预先注册属性名称/显示单位等基础信息，在商品注册或C2C销售注册时即可选择使用相应属性。

提供功能

* [物品能力设置注册](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#post-api-v1-item-ability)
* [物品能力设置修改](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#put-api-v1-item-ability-code)

## C2C物品能力注册（单独注册）

C2C物品能力注册支持**单独注册方式**。
当需要注册少量物品能力时，可通过单独注册创建物品能力。

{% stepper %}
{% step %}
### 选择C2C物品能力管理页面

* 登录NEXT Market控制台
* 在左侧菜单选择**C2C物品能力管理**页面
{% endstep %}

{% step %}
### 选择能力注册

* 点击能力注册按钮进入物品能力注册界面。

<figure><img src="../.gitbook/assets/아이템 능력 관리_등록.png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### 基础信息录入

填写物品能力的基准信息。

| 字段 | 值                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ----- | -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | 能力代码 | <ul><li><p>用于识别和管理物品能力的代码</p><ul><li>物品能力：物品所具备的属性及能力值</li></ul></li><li>格式：3～36字符限制，可使用英文字母、数字及特殊字符，需为用户可推测的值</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 能力名称 | <ul><li>支持多语言输入：en, ko, ja, th, zh</li><li><p>在交易所物品详情页显示的数值</p><ul><li>必须针对市场提供的语言进行注册</li></ul></li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 选项类型 | <ul><li>定义能力值属于何种性质的信息</li><li><p>属性类型</p><ul><li>基础能力值 (<code>BASIC</code>)</li><li>强化能力值 (<code>ENHANCE</code>）：通过强化改变的能力</li><li>附加能力值 (<code>ADDITIONAL</code>): 通过鉴定或镶嵌改变的能力</li><li>精炼属性 (<code>SMELTING</code>): 通过精炼或属性赋予改变的能力</li><li>限制选项 (<code>CONSTRAINT</code>）：因变化而新增或修改的限制条件</li><li>物品包含数量 (<code>AMOUNT</code>): 用于表示物品内含数量的数值</li></ul></li><li>物品能力设置注册API的 <code>keys.optionType</code> 作为参数传递</li></ul><p>⚠️注意事项</p><ul><li><strong>建议</strong>在物品管理页面<strong>注册SKU时，同时登记不随物品变动的基础能力值。</strong></li><li><strong>C2C商品能力管理页面用于登记交易过程中可能变动的能力项。</strong></li><li><strong>请注意避免</strong>在两个菜单中<strong>重复注册相同能力。</strong></li></ul> |
| 显示格式 | <ul><li>设置能力值向用户<strong>展示的形式</strong></li><li><p>显示格式选择</p><ul><li>原始数值 (<code>NONE</code>）：直接显示输入数值</li><li>100% (<code>PPERCENTAGE</code>)</li><li> 100 (<code>NUMERIC</code>)</li><li>100Lv (<code>LEVEL</code>)</li></ul></li><li>物品能力设置注册API的 <code>keys.unitType</code> 值传递</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 颜色    | <ul><li>设置显示能力值的颜色</li><li><p>可选颜色</p><ul><li><p>黄色、绿色、蓝色、品红色、橙色、红色、灰色、无颜色</p><ul><li>无颜色时将显示为默认颜色</li></ul></li></ul></li><li>通过物品能力设置注册API的 <code>keys.color</code> 传递值</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |

<figure><img src="../.gitbook/assets/아이템 능력 관리_기본정보.png" alt=""><figcaption></figcaption></figure>{% endstep %}
{% endstepper %}

## C2C物品能力批量注册

**当需一次性注册多个物品能力时**，可通过上传CSV文件实现批量注册。

{% stepper %}
{% step %}
### 选择C2C物品能力管理页面

* 登录NEXT Market控制台
* 在左侧菜单选择C2C **物品能力管理**页面
{% endstep %}

{% step %}
### 下载模板

* 点击**模板下载**按钮获取物品能力批量注册用**CSV模板文件**。
* 模板包含物品能力注册所需的基本列。

<figure><img src="../.gitbook/assets/아이템 능력 관리_템플릿.png" alt=""><figcaption></figcaption></figure>{% endstep %}

{% step %}
### 编写物品能力清单

* 在下载的**CSV模板文件**中填写待注册物品能力信息。
* 各项填写方式请参照**物品能力注册（单独注册）**指南进行编写。

⚠️ 若必填项遗漏或格式不符，可能导致上传失败。

<figure><img src="../.gitbook/assets/아이템 능력 관리_템플릿 엑셀.png" alt=""><figcaption></figcaption></figure>{% endstep %}

{% step %}
### CSV上传

* 选择填写完成的CSV文件进行上传。
* 选定文件后点击**上传**按钮，即可批量注册道具能力。

#### ⚠️ 批量注册注意事项

* CSV上传功能仅适用于**新增物品能力或修改现有注册信息**。
* 建议在批量上传前进行**小规模测试上传**。

<figure><img src="../.gitbook/assets/아이템 능력 관리_CSV 업로드.png" alt=""><figcaption></figcaption></figure>{% endstep %}
{% endstepper %}

## C2C商品属性修改

**若需变更已注册属性的信息，**可通过**单独修改**与**批量修改**两种方式进行调整。

### C2C商品属性修改方式

#### 单独修改

用于修改单个商品属性的信息。

* 登录**NEXT Market管理后台**
* 左侧菜单选择**C2C商品属性管理**页面
* 在商品属性列表中选定待修改属性
* 点击**编辑**按钮
* 修改商品信息后保存

<figure><img src="../.gitbook/assets/아이템 능력 관리_수정.png" alt=""><figcaption></figcaption></figure>#### 批量修改

需同时修改多个商品能力的场景适用。

* 在**C2C商品能力管理**页面点击**CSV下载**按钮
* 在下载的CSV文件中修改商品能力信息
* 上传修改完成的CSV文件
* 上传后确认修改结果

<figure><img src="../.gitbook/assets/C2C 아이템 능력 관리_업로드.png" alt=""><figcaption></figcaption></figure>### ⚠️ 修改注意事项

* 请在与LINE NEXT事先协商后进行道具能力注册。
* 销售中道具的信息变更可能影响服务运营。
* 批量修改前建议进行**小规模测试修改**。
