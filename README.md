# みなみクリニック

## 開発環境
- PHP v-xx
- WordPress v-xx
- node v-xx

## ビルドツール
- gulp

## gulp コマンド
- パッケージのダウンロード
  - `npm i`
- コンパイル
  - `npx gulp`

## Git運用ルール
- GitHubのissueでタスク管理をする
- mainブランチを起点に作業用ブランチを作成して作業。プルリクエスト作成画面で**Closes #Issue番号**のメッセージを残すことでプルリクエストとIssueが紐付いてissueを閉じる。
### ブランチルール
  - [main]
      - 本流ブランチ、ここでは直接作業しない
  - [feature/#issue番号_対応事項]
      - 小〜大規模な機能追加
      - 小〜中規模な修正・改修などを行う作業ブランチ
  - [fix/#issue番号_動詞]
      - 中〜大規模なバグ修正
### コミットルール
- `[頭文字]作業内容`
  - ディスクリプションは、対象issueまたはプルリクに記載
- コミットメッセージには対応内容に応じて頭文字を付与
    - 追加 [add]
    - 修正 [update]
    - バグ修正 [fix]
    - 仕様変更 [change]
    - 削除 [remove]
    - 取り消し [revert]
    - 整理 [clean]

## ファイル構造
- wp-theme・・・テーマファイル
- devsrc・・・開発用パッケージ
  - sass
  - package.json
  - gulpfile.js
- editorconfig・・・共通のエディタルール

## CSS
### 設計
[FLOCSS](https://github.com/hiloki/flocss "FLOCSS") を採用
### クラスの命名規則
- `Block__Element--Modifire`
- 単語の繋がりはハイフンで繋ぎ、頭文字-役割-名前空間で統一。
  - 例) フッターのボタン `c-btn-footer`


## 画像ファイル名の基本ルール
### 基本となるベース
  - ページ/役割_位置
    - 例) コンタクトページのトップの背景画像
      - `contact/bg_top.jpg`
### 基本となるベース + 補足として、詳細・番号・状態を指定
  - ページ/役割_位置-詳細+番号_状態
    - 例) お問い合わせページのトップのスワイパー1枚目のスマホの背景画像
      - `contact/bg_top-swiper01_sp.jpg`
### グローバル画像
  - ページ/役割-詳細+番号_状態
    - 例) 右向きの矢印
      - `common/arrow-right.png　`
    - 例) ツイッターのアイコンのホバー状態
      - `common/icon-twitter_hover.png`
