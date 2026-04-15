# プロジェクト概要: paaharu.github.io

**Astro** を使って構築するポートフォリオサイト。[Astro Starter Kit: Basics](https://docs.astro.build/en/basics/project-structure/) をベース。

## 主要技術
- **Astro** v6.1.6 — メインフレームワーク
- **TypeScript** — 厳格モード (`tsconfig.json` は Astro strict を継承)
- **Vanilla CSS** — Astroコンポーネント内スコープスタイル + `src/styles/global.css`
- **Node.js** `^22.12.0`

## プロジェクト構造
```
src/
  pages/      # ルート (index.astro, projects.astro, ...)
  components/ # 再利用コンポーネント (Button.astro, ...)
  layouts/    # 共通レイアウト (Layout.astro)
  styles/     # グローバルCSS (global.css)
  data/       # 静的データ (projects.json)
  assets/     # 画像など
public/       # ファビコンなど直接配信するファイル
```

## コマンド
| コマンド | 内容 |
| :--- | :--- |
| `npm run dev` | 開発サーバー起動 (`localhost:4321`) |
| `npm run build` | 本番ビルド → `./dist/` |
| `npm run preview` | ビルド結果をローカルプレビュー |
| `npm run astro check` | 型チェック |

## デザインシステム
[design-rules](https://github.com/konoe-akitoshi/design-rules) に準拠。

### スペーシング
CSS変数 (`--space-*`) を使い、4pt/8ptグリッドを厳守する。
```css
--space-4: 4px  --space-8: 8px  --space-16: 16px  --space-32: 32px  --space-64: 64px
```
マジックナンバーで余白を書かない。

### タイポグラフィ・形状
- 黄金比ベースの比率
- 角丸は「Squircle」的な滑らかさを意識

### カラー・アクセシビリティ
- WCAG基準のコントラスト確保
- CSS変数: `--bg-color` / `--text-color` / `--accent-color` / `--border-color`

### インタラクション
- タッチターゲット最小 **48px**
- インタラクティブ要素間に最低 **8px** の余白

## コーディング規約
- コンポーネントは `src/components/` に配置
- スタイルはコンポーネントスコープ (`<style>`) を優先、グローバルスタイルは `global.css` のみ
- インラインスタイル (`style="..."`) はプロトタイプ段階のみ、仕上げ時は `<style>` に移す
- 新しいCSS変数が必要なら `global.css` の `:root` に追加する

## サイジングと余白
- 高さを `h-*` などの固定値でハードコードしない。padding で余白を与えてコンテンツに高さを決めさせる
- マジックナンバー（`px-[37px]` など任意の数値）は使わず、Tailwind のスケール (`p-4`, `p-5`...) か CSS変数を使う
- **要素間の余白は `gap` で管理する**。Grid / Flexbox のコンテナに `gap-*` を置き、子要素に `mt-*` / `mb-*` を点在させない
  - `gap` → 兄弟要素間の距離（セクション間、カード間、ナビ項目間）
  - `padding` → コンテナ内側の余白（ページ端からのオフセット、カード内余白）
  - `margin` は原則使わない
