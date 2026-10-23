# SEO・LLMO・読みやすさ 3つの目で文章を直す

日本語の記事を、**3つの目** で点検して直すための指示書です。

| 目 | 何に効くか |
|---|---|
| SEO | Google 検索で上に出る |
| LLMO(GEO・AEO) | ChatGPT・Gemini・Claude などの AI の答えの中で、引用・紹介される |
| 読みやすさ | 人が最後まで読める |

3つは向きが同じです。**結論が先で、根拠がはっきりしていて、見出しごとに話が完結している文章** はどれにも効きます。

## できること

- **点検**: 文章を貼ると、3つの目で採点し、直すと効く所を上から5つ出す
- **直す**: 点検してから書き直し、何をどう変えたかを並べる
- **書く**: テーマを渡すと、構成 → 本文 → よくある質問 → 題名3案 まで書く

数字や誰かの発言は作りません。必要な所には `【要出典】` の印を付けるので、自分の体験の数字で埋めてください。

## 使い方は2通り

### A. Claude Code で使う(スキルとして入れる)

1. 緑の **Code** ボタン → **Download ZIP** で落として、すべて展開する
2. 中の `skills/seo-llmo-writer` フォルダを、次の場所にフォルダごとコピーする
   - Windows: `C:\Users\<あなたの名前>\.claude\skills\`
   - Mac: `~/.claude/skills/`
3. Claude Code を開き直して「この記事を SEO と LLMO の目で点検して」と文章を貼る

または、Claude Code にこう頼めば入れてくれます:

```
https://github.com/yubokumin28/seo-llmo-writer の skills/seo-llmo-writer を、私の ~/.claude/skills/ に入れて
```

### B. ChatGPT・Gemini・Claude(ブラウザ)で使う

1. `skills/seo-llmo-writer/SKILL.md` を開き、先頭の `---` で囲まれた部分より下を全部コピーする
2. 貼る場所:
   - ChatGPT: プロジェクトの「指示」か、カスタム GPT の「指示」
   - Gemini: Gem の「カスタム指示」
   - Claude: プロジェクトの「指示」
3. そのプロジェクトで「点検して」「直して」「書いて」と頼む

## 外し方

- **Claude Code**: `.claude\skills\seo-llmo-writer` フォルダを消すだけ。ほかの動きは何も変わりません
- **ChatGPT・Gemini・Claude**: 貼った指示を消すだけ

## 中身

```
skills/seo-llmo-writer/SKILL.md   … 指示書の本体(これ1枚で動く)
references/sources.md             … 参考にした公開リポジトリと研究の一覧
```

## 出典

公開リポジトリ(claude-seo・BlogPilot・llmopt・llm-docs-builder ほか)と、GEO の研究(KDD 2024)の考え方を、日本語の記事向けにまとめ直した物です。コードは含みません。詳しくは `references/sources.md`。

作者: 遊牧民(yubokumin28) / クロコ🐊相談会で配布(2026-10-24)
