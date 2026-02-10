metaLinks:
  alternates:
    - &gt;-
      https://app.gitbook.com/s/pt4moEMpSf4BGvjJCzQm/api-usage-guide/api-version-information
---

# バージョン情報

## リリースノート

### v1.10\_2025.09.10

* 販売量統計APIの提供

### v1.9\_2025.09.08

* ワンタイムトークン発行時に紹介コードとカスタムペイロードを追加
* 配送時にカスタムペイロードパラメータを追加
* 配送履歴照会APIを追加

### v1.8\_2025.08.22

* モバイルアプリWebViewガイド変更。Cookie → URLパラメータ(inapp=true)

### v1.7\_2025.07.24

* [ストア認証用ワンタイムトークンリクエスト](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-1#undefined-2)のRegion基準でSanction Countryの場合、BadRequestを追加

### v1.6\_2025.07.18

* [モバイルアプリ WebView ガイド](https://next-market-admin.gitbook.io/next-market-docs/api/undefined#v1.8_2025.08.22)を追加

### v1.5\_2025.07.08

* [売上データ照会](https://github.com/tech-support-trade/docs/wiki/API-Guide#매출-데이터-조회)にitems\[].skus, items\[].quantityを追加
* [販売登録リクエスト](https://github.com/tech-support-trade/docs/wiki/API-Guide#판매-등록-요청)のlimitPurchaseCountが選択フィールドに変更され、説明が更新されました。

### v1.4\_2025.07.04

* B2C販売登録時の複数通貨登録をサポート。
  * price, currency 入力値削除
  * multiCurrencyPrice 入力値追加
* periodType フィールド名称変更 → periodicType

### v1.3\_2025.07.01

* color 入力値に GREY, NONE 値追加
* link.deviceType の PC → WEB に変更

### v1.2\_2025.06.26

* アイテム能力設定のcolorをcontent.colorに修正
* [C2C販売キャンセルリクエスト](https://github.com/tech-support-trade/docs/wiki/API-Guide#C2C-판매-취소-요청)を追加

### v1.1\_2025.06.24

* [ストア認証用ワンタイムトークンリクエスト](https://github.com/tech-support-trade/docs/wiki/API-Guide#스토어-인증용-원타임-토큰-요청)にC2C販売登録用トークン発行のためのパラメータを追加定義
* [シリングリクエスト](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#undefined-20)にc2cSaleIdレスポンスフィールドを追加
* API利用可能環境に関するラベルを追加(`preview` `prod`)
* [売上データ照会](https://github.com/tech-support-trade/docs/wiki/API-Guide#매출-데이터-조회)を追加（7/10以降利用可能）

### v1.0\_2025.05.27

* B2C、C2C、Mission\
