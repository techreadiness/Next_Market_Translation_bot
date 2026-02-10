# NEXT Market Console ご利用ガイド

## NEXT Market Console 紹介

**NEXT Market Console**は、NEXT Marketが提供する主要なAPI機能を**ウェブベースのコンソール形式で提供**し、開発および運用プロセスにおいて**アイテム・商品・ミッションを簡単かつ直感的に登録・管理できるように支援する管理ツール**です。

## NEXT Market Console へのアクセス方法

### Preview Environment

* URL: [https://app-console.nextmarket.games/](https://app-console.nextmarket.games/)
* 認証情報: Preview API Key

### Prod Environment

* URL: [https://console.nextmarket.games/](https://console.nextmarket.games/)
* 認証情報: Prod API Key

## NEXT Market Console提供機能

NEXT Market Consoleでは、NEXT Market APIで提供される主要機能を**ウェブベースのコンソール**環境で**直接登録・管理**できます。

### [アイテム管理](https://next-market-admin.gitbook.io/copy-of-next-market-docs/~/revisions/80r3cbY8BxZFGmdGSqV2/next-market-console/undefined)

B2CおよびC2C取引で使用されるアイテムを登録・管理できます。

* 提供機能
  * [メディアファイルアップロード](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#post-api-v1-media-upload)
  * [アイテム登録](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#post-api-v1-item)
  * [アイテム変更](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#put-api-v1-item-sku)

### [B2C商品管理](https://next-market-admin.gitbook.io/copy-of-next-market-docs/~/revisions/80r3cbY8BxZFGmdGSqV2/next-market-console/b2c)

B2C商品の販売情報を登録し、販売状態を管理できます。

* 提供機能
  * [セクション登録](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-3#post-api-v1-sale-b2c-section)
  * [セクション変更](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-3#patch-api-v1-sale-b2c-section-sectionid)
  * [販売登録](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-4#post-api-v1-sale-b2c)
  * [販売変更](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-4#patch-api-v1-sale-b2c-b2csaleid)

### [C2Cアイテム能力管理](https://next-market-admin.gitbook.io/copy-of-next-market-docs/~/revisions/80r3cbY8BxZFGmdGSqV2/next-market-console/c2c)

C2Cアイテムに適用可能な**能力（属性）**を設定・管理できます。

* 提供機能
  * [アイテム能力設定登録](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#post-api-v1-item-ability)
  * [アイテム能力設定の修正](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-2#put-api-v1-item-ability-code)

### [ミッション管理](https://next-market-admin.gitbook.io/copy-of-next-market-docs/~/revisions/80r3cbY8BxZFGmdGSqV2/next-market-console/undefined-1)

ミッションを作成し、運営状態を管理できます。

* 提供機能
  * [ミッション作成](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-7#post-api-v1-incentive-mission)
  * [ミッション編集](https://next-market-admin.gitbook.io/next-market-docs/api/undefined-7#put-api-v1-incentive-mission-missionid)

## 注意事項

⚠️ アイテム、商品、ミッションの登録に関しては、LINE NEXTと事前に協議の上、進めてください。

NEXT Market Consoleは、開発者だけでなく運営者も直接**アイテム、商品、ミッションを登録・管理**できるウェブベースの管理ツールであり、Consoleで生成されたデータは**NEXT Market APIと同様の動作をします。**

運営管理上修正が必要な場合は、**各変更項目ごとの注意事項を必ず確認した上で修正**してください。
また、**既に登録されたデータに対する削除機能はConsoleでは提供しておらず、削除が必要な場合はAPIを通じて行ってください。**
