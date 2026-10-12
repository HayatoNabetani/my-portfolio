# Hayato Nabetani — Portfolio

Astro 7 + TypeScript の静的ポートフォリオです。pnuts.dev を参考に、中央のプロフィール、淡い背景、控えめなカードと下部ナビゲーションを使ったシンプルな構成にしています。

## 開発

Node.js 22.12 以上の偶数メジャー版を使用します。

```sh
npm ci
npm run dev
npm run check
npm run build
```

`dist/` が静的サイトの出力です。`npm run preview` で本番ビルドを確認できます。

ホームへの書き込みが制限される環境では `ASTRO_TELEMETRY_DISABLED=1 npm run dev` のように実行してください。

## 編集

- `src/data/profile.ts`: 名前・Xの連絡先・GitHub・スキル・経歴
- `src/pages/index.astro`: 制作実績、自己紹介、ナビゲーション、テーマ切り替え
- `src/styles/global.css`: ライト／ダークの配色、レスポンシブレイアウト

テーマ設定はブラウザのlocalStorageに保存します。初回はOSのテーマに従います。InterとNoto Sans JPをローカル配信し、本文は16pxを基準にしています。外部フォントサービスやSNSの埋め込みは読み込みません。

## 個人開発と画像

機能・技術スタックはユーザーの各プロジェクトのREADMEと依存設定、nhc-toolsの公開サイトから確認しました。担当規模や定量的な成果は未提供のため記載していません。

- `public/avatar.png`: ユーザー提供のアバター
- `public/nhc-tools.jpg`: 公開サイトの実際の画面
- `public/my-duet-display-screenshot.jpg`: 起動した実アプリの待機中の設定画面。リンクから拡大可能
- `public/my-postico-icon.png`: My Posticoの実アプリアイコン。保存済み接続情報を含むスクリーンショットは未掲載

My Duet Displayは公開GitHubリポジトリを確認できなかったため、スクリーンショットへのリンクのみ設けています。

以前生成したヒーローイラストはファイルとして残していますが、現在のページでは使用していません。

## 公開

`npm run build` の出力を静的ホスティングへ配置できます。公開ドメインが決まったら `astro.config.mjs` の `site`、canonical、OGP画像、サイトマップを設定してください。現在はローカル開発のみです。

## アイコン

技術ロゴとGitHub / XロゴはSimple Iconsを使用し、SVGをビルド時に埋め込みます。Databaseは一般的なカテゴリなので汎用のデータベースアイコンです。個人開発の装飾アイコンは、線幅・サイズを統一したSVGです。

## 個人開発一覧と経歴

個人開発は常時表示し、PCでは画像左・説明右のコンパクトな縦並び、スマートフォンでは画像上・説明下になります。Tech Stackのロゴは横に自動で流れ、ホバー・フォーカスで停止できます。動きを減らす設定では自動スクロールを止め、手動の横スクロールに変わります。About Meはアイコン付きの項目名と本文の強弱をつけています。

Experienceは元の経歴情報を保ち、期間・会社名・役割の強弱とSVGアイコンで読みやすく整理しています。
