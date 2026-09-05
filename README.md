# Skills

Claude Code で使える汎用スキル集。

## スキル一覧

| スキル | 説明 |
|---|---|
| [japanese-technical-writing](./skills/japanese-technical-writing/) | 日本語テクニカルライティングのルール集。冗長表現の排除、漢字/ひらがなの使い分けなど、文章品質を向上させる。レビュー時は7観点をsubagentで並列チェック |
| [test-principles](./skills/test-principles/) | Google の "Software Engineering at Google" に基づくテスト設計原則。Go のテーブルドリブンテストと go-cmp に最適化 |
| [code-reviewer](./skills/code-reviewer/) | Google's Code Review Guidelines に基づく段階的コードレビュー。設計レビューから詳細レビューまでワークフローで実施 |

## 文章の Lint

スキルの Markdown は [textlint](https://textlint.github.io/) でチェックする。ルールは
`preset-ja-technical-writing` / `preset-ja-spacing` / `preset-ai-writing` を使う。

```bash
pnpm install
pnpm lint:text      # チェック
pnpm lint:text:fix  # 自動修正
```

対象は `skills/**/SKILL.md` と `skills/**/agents/*.md`。
`skills/japanese-technical-writing/docs/` は原典の写しのため対象外とする。

## インストール

[`skills` CLI](https://www.npmjs.com/package/skills) を使ってインストールできます。

### インタラクティブにインストール

```bash
npx skills add p1ass/skills
```

## ライセンス

MIT
