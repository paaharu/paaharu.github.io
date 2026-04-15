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

## 開発コンポーネント
- **コンポーネント**: [Astroコンポーネント構造](https://docs.astro.build/en/basics/astro-components/)に従ってください（ロジックはFrontmatter、構造はHTML/JSX、スタイルは`<style>`）。
- **スタイリング**: グローバルスタイルが必要な場合を除き、コンポーネントにスコープされたVanilla CSSを推奨します。
- **厳格モード**: `astro/tsconfigs/strict` を使用しているため、可能な限り型安全性を確保し、`any` の使用を避けてください。
- **アセット管理**: Astroによる最適化が必要な画像は `src/assets/` に、そのまま配信する静的ファイルは `public/` に配置してください。
