# MySite概要
このシステムは、学校の
授業の一環で・・・
# 野菜炒め

## 材料
- ニンジン
- キャベツ
- モヤシ

## 作り方
1. 野菜を切る
    - よく洗いましょう
    - 一口大に、大きさを揃えましょう
1. フライパンで炒める
1. 塩、コショウで味を調える




| ページ | URL | サーブレット |
|:----------:|:----------|---------------:|
| ホーム | /home | HomeServlet |
| 会社概要 | /about | AboutServlet |
| 製品リスト | /products | ProductServlet |


# システム仕様書

## 以下は処理の流れです。(フローチャート)

```mermaid
graph TD
    Start[開始] --> Input[ID/Pass入力]
    Input --> Judge{認証一致?}
    Judge -- Yes --> Success[ログイン成功]
    Judge -- No --> Fail[エラー表示]
    Fail --> Input
```

## 以下は機能の流れです。(シーケンス図)
```mermaid
sequenceDiagram
    participant ブラウザ
    participant サーバー
    participant DB
    ブラウザ->>サーバー: ログイン情報送信
    サーバー->>DB: ユーザー照会
    DB-->>サーバー: 照会結果(一致)
    サーバー-->>ブラウザ: ログイン成功画面
```