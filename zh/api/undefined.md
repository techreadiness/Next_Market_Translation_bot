metaLinks:
  alternates:
    - https://app.gitbook.com/s/pt4moEMpSf4BGvjJCzQm/api-usage-guide/account
---

# 账户

## Next Market ➡️ 游戏

### 游戏账户状态查询

`预览环境` `生产环境`

<mark style="color:green;">`POST`</mark> `/next-market/character-info`

在用户通过认证令牌进入商店或尝试购买商品配送前，需查询游戏账户状态以确认账户有效性并获取基础信息。根据游戏架构，通过账户持有的角色及所属服务器等信息，将获取的信息展示给用户以确认账户归属。

```bash
curl -X POST {{endpoint}}/next-market/character-info \
-H &quot;Content-Type: application/json&quot; \
-d &#x27;{
  &quot;guid&quot;: &quot;user123-guid-xxxx&quot;
}&#x27;
```

**请求头**

| 名称                                                                                   | 值              |
| -------------------------------------------------------------------------------------- | ------------------ |
| <p>Content-Type <mark style="color:$danger;">*必填</mark><br><em>(标头)</em></p> | `application/json` |

**正文**

<table><thead><tr><th width="219.88970947265625">字段</th><th width="219.6478271484375">类型</th><th>描述</th></tr></thead><tbody><tr><td>guid</td><td>字符串 <mark style="color:$danger;">*必填</mark></td><td>游戏公司定义的账户标识符。由于存在通过用户间共享而暴露给未授权用户的风险，该标识符必须确保符合个人信息处理规范。</td></tr></tbody></table>**响应格式**\
可参照[错误响应格式](undefined-5.md#error-response-format)自定义各类错误详情。当商店端收到503响应时将自动重试；若收到403、406或500响应，则通过监控系统执行恢复或强制取消请求的流程。

<table><thead><tr><th width="219.88970947265625">字段</th><th width="219.6478271484375">类型</th><th>Description</th></tr></thead><tbody><tr><td>签名</td><td>列表</td></tr></tbody></table>
