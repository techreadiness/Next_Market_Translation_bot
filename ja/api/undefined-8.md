metaLinks:
  alternates:
    - /broken/spaces/pt4moEMpSf4BGvjJCzQm/pages/1yx4GJhhoYrra0NzZTb8
---

# 参考事項

### Marketテストのためのメンテナンス回避方法

#### 基本方針

LINE NEXT側でMarketの設定および開設が完了すると、Marketオープン前まで外部からのアクセスを制限するためメンテナンスモードを維持します。ゲーム開発会社はLINE NEXTが提供するメンテナンス回避URLを使用してアクセスできます。メンテナンス回避URLの確認が必要な場合は、担当者へお問い合わせください。

#### Webviewでテストする場合

APIリクエスト時に、メンテナンス回避URLで確認できるCookie値をヘッダーに追加してください。

```
key: MAINTENANNCE_COOKIE
value: xxxxxxx-....
```

メンテナンス回避URLが変更されるとvalueも変更される可能性があるため、ランタイムでの設定が必要です。
