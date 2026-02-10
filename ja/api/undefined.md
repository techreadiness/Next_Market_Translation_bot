metaLinks:
  alternates:
    - https://app.gitbook.com/s/pt4moEMpSf4BGvjJCzQm/api-usage-guide/account
---

# アカウント

## Next Market ➡️ Game

### ゲームアカウント状態照会

`preview` `prod`

<mark style="color:green;">`POST`</mark> `/next-market/character-info`

ユーザーが認証トークンでストアにアクセスしたり、商品購入による配送を試みる前に、ゲームアカウントの正常性を確認するため、状態を照会し基本情報を取得します。ゲームの構造に応じて、アカウントが保有するキャラクターや所属サーバーの情報などを通じて、ユーザーが自身のアカウントであることを認識できるよう、取得した情報をユーザーに表示します。

```bash
curl -X POST {{endpoint}}/next-market/character-info \
-H &quot;Content-Type: application/json&quot; \
-d &#x27;{
  &quot;guid&quot;: &quot;user123-guid-xxxx&quot;
}&#x27;
```

**ヘッダー**

| 名前                                                                                   | 値              |
| -------------------------------------------------------------------------------------- | ------------------ |
| <p>Content-Type <mark style="color:$danger;">*必須</mark><br><em>(ヘッダー)</em></p> | `application/json` |

**Body**

<table><thead><tr><th width="219.88970947265625">Field</th><th width="219.6478271484375">Type</th><th>Description</th></tr></thead><tbody><tr><td>guid</td><td>String <mark style="color:$danger;">*必須</mark></td><td>ゲーム会社側が定義したアカウントの識別子です。ユーザー間で共有されることで、未承認のユーザーにも公開される可能性があるため、個人情報取扱上問題のない識別子である必要があります。</td></tr></tbody></table>**Response**\
[Error response format](undefined-5.md#error-response-format)に準拠し、各エラーの詳細を独自に定義できます。ストア側では503応答を受信した場合、再試行を繰り返します。403、406、500応答を受信した場合は、モニタリングを通じて復旧またはリクエストを強制的にキャンセルする手順を実行します。

<table><thead><tr><th width="219.88970947265625">Field</th><th width="219.6478271484375">Type</th><th>Description</th></tr></thead><tbody><tr><td>signature</td><td>List</td></tr></tbody></table>
