# 参考にした公開リポジトリと研究

このリポジトリは下の物を **読んで考え方をまとめ直した物** で、コードはコピーしていません。
もっと深くやりたい人は、元のリポジトリを直接どうぞ。

## SEO

| リポジトリ | ひとこと |
|---|---|
| [AgriciDaniel/claude-seo](https://github.com/AgriciDaniel/claude-seo) | Claude Code 用の本格的な SEO 分析。技術面・E-E-A-T・構造化データ・AI 検索向けの引用されやすさまで |
| [IamRamgarhia/BlogPilot-Open-Source-AI-SEO-Content-Studio](https://github.com/IamRamgarhia/BlogPilot-Open-Source-AI-SEO-Content-Studio) | 自分で動かす AI SEO 記事スタジオ。45種類の手法ファイル(Markdown)が読み物としても役立つ |
| [sethblack/python-seo-analyzer](https://github.com/sethblack/python-seo-analyzer) | サイトをたどって技術的な SEO の問題を見つける Python ツール |

## LLMO(GEO / AEO)

| リポジトリ | ひとこと |
|---|---|
| [amplifying-ai/awesome-generative-engine-optimization](https://github.com/amplifying-ai/awesome-generative-engine-optimization) | GEO・AEO の論文・ガイド・道具・llms.txt の情報を集めた一覧 |
| [jonradoff/llmopt](https://github.com/jonradoff/llmopt) | ChatGPT・Claude・Gemini などに自分のブランドがどう紹介されるかを点数にする |
| [akii-technologies-ltd/akii-seo-ai-search-optimizer](https://github.com/akii-technologies-ltd/akii-seo-ai-search-optimizer) | 研究に基づく GEO のリライトと llms.txt の生成 |
| [mensfeld/llm-docs-builder](https://github.com/mensfeld/llm-docs-builder) | AI 向けに Markdown を整え、llms.txt を作る。見出しに親の文脈を足す考え方 |
| [plainsignal/llmstxt](https://github.com/plainsignal/llmstxt) | サイトマップから llms.txt を作る Chrome 拡張 |

## 読みやすさ

| リポジトリ | ひとこと |
|---|---|
| [textstat/textstat](https://github.com/textstat/textstat) | 文章の難しさを測る定番の Python ライブラリ(英語向けの指標が中心) |
| [Rebilly/lexi](https://github.com/Rebilly/lexi) | Markdown の読みやすさを測る GitHub Action |

## そのほかの道具(元にした資料のツール集に載っていた物)

| リポジトリ | ひとこと |
|---|---|
| [cleven12/seo_optimizer](https://github.com/cleven12/seo_optimizer) | Gemini や OpenAI を使い、狙う言葉との合い方と SEO の要因を点数にする Python のコマンド |
| [MervinPraison/WordPressAISEO](https://github.com/MervinPraison/WordPressAISEO) | WordPress で、説明文・題名・構造化データを AI で作るプラグイン |
| [adaptive-enforcement-lab/readability](https://github.com/adaptive-enforcement-lab/readability) | 文書の読みやすさを自動で測り、基準を下回ったら止める GitHub Action |
| [realMNohgee/prosecheck](https://github.com/realMNohgee/prosecheck) | Python の標準機能だけで読みやすさの点数を出すコマンド(公開されたばかりの小さな物) |
| [kozodoi/Text_Readability_Prediction](https://github.com/kozodoi/Text_Readability_Prediction) | AI のモデルで文章の難しさを予想する研究用の Web アプリ(2022年から更新なし) |
| [magicrew/doc7](https://github.com/magicrew/doc7) | PDF や図表を、AI が読みやすい Markdown に直す道具 |
| [sebastienrousseau/html-generator](https://github.com/sebastienrousseau/html-generator) | Markdown から、SEO と見やすさに気を配った HTML・構造化データ・目次を作る Rust のライブラリ |

## 研究

- Aggarwal ほか「GEO: Generative Engine Optimization」(KDD 2024)
  生成 AI の答えの中での見え方を上げる書き方を比べた研究。引用や統計を足すと見え方が上がり、言葉の詰め込みは逆効果だった、という結果が知られている
- Google 検索セントラル「有用で信頼性の高い、ユーザー第一のコンテンツの作成」
  https://developers.google.com/search/docs/fundamentals/creating-helpful-content?hl=ja
