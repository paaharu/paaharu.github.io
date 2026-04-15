# プロジェクト概要: paaharu-github-io

このプロジェクトは、コンテンツ重視のウェブサイト向けに設計されたモダンなウェブフレームワークである **Astro** を使用して構築されています。[Astro Starter Kit: Basics](https://docs.astro.build/en/basics/project-structure/) をベースにしています。

## 主要技術
- **Astro**: メインのウェブフレームワーク (version 6.1.6)
- **TypeScript**: 厳格な型チェックとモダンなJavaScript機能
- **Node.js**: 推奨バージョン `^22.12.0`
- **Vanilla CSS**: Astroコンポーネント内でのスコープ付きスタイリング

## プロジェクト構造
- `src/pages/`: サイトのルート（ページ）が含まれます。
- `src/components/`: 再利用可能なAstroコンポーネント。
- `src/layouts/`: 複数のページで共通して使用されるレイアウト。
- `src/assets/`: 画像やフォントなどの静的アセット。
- `public/`: ファビコンなどの公開ファイル。
- `astro.config.mjs`: Astroの設定ファイル。
- `tsconfig.json`: TypeScriptの設定（Astroの厳格なルールを継承）。

## ビルドと実行
すべてのコマンドはプロジェクトのルートディレクトリで実行してください。

| コマンド | 内容 |
| :--- | :--- |
| `npm install` | プロジェクトの依存関係をインストールします。 |
| `npm run dev` | ローカル開発サーバーを `localhost:4321` で起動します。 |
| `npm run build` | 本番用サイトを `./dist/` フォルダにビルドします。 |
| `npm run preview` | ビルドされた本番用サイトをローカルでプレビューします。 |
| `npm run astro ...` | Astro CLIコマンド（例: `astro add`, `astro check`）を実行します。 |

## デザインシステム (Design System)
本プロジェクトは、[design-rules](https://github.com/konoe-akitoshi/design-rules) に基づき、モダンで調和のとれたデザインを採用します。

- **Spacing & Layout**: 4pt/8ptグリッドシステム（4px, 8px, 16px, 32px...）を厳守し、一貫したリズムを維持する。
- **Typography & Geometry**: 黄金比を用いた比率調整や、視覚的に滑らかな「Squircle」形状の角丸を採用する。
- **Color & Accessibility**: WCAG基準を満たすコントラストを確保し、包括的で読みやすいインターフェースとする。
- **Interaction**: Fittsの法則に基づき、タッチターゲットは最小48ptとし、インタラクティブな要素間には最低8pxの余白を設ける。
- **Visual Theory**: ゲシュタルト原則や光学補正を取り入れ、バランスの取れた professional なデザインを目指す。

