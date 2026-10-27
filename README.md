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
- **直す**: 点検してから書き直し、何をどう変えたかを並べる。画像があれば1枚ずつ説明文(キャプション)も出す
- **書く**: テーマを渡すと、構成 → 本文 → よくある質問 → 題名3案 まで書く

数字や誰かの発言は作りません。必要な所には `【要出典】` の印を付けるので、自分の体験の数字で埋めてください。

## 使い方は3通り

### A. Claude Code で使う(おすすめ: いつでも止める・戻す・外すができる)

**入れる**(最初の1回だけ)

Claude Code のチャット欄に、1行ずつ貼って Enter を押します。

```
/plugin marketplace add yubokumin28/seo-llmo-writer
```

```
/plugin install seo-llmo-writer@seo-llmo-writer
```

2行目を押すと確認の画面が開くので「Install for you」を選びます。
入れたら「この記事を SEO と LLMO の目で点検して」と文章を貼るだけで動きます。名前で呼ぶ時は `/seo-llmo-writer:seo-llmo-writer` です。

**止める・また使う・新しい版にする**

チャット欄で `/plugin` と打つと一覧の画面が開きます。Tab キーで「Installed」へ移り、seo-llmo-writer を選んで、

| したい事 | 押すキー |
|---|---|
| しばらく止める(消さずに眠らせる) | スペースキー |
| また使う | もう一度スペースキー |
| 新しい版にする | Enter →「Update now」 |

画面を閉じると、開き直さなくてもその場で効きます。

**完全に外す**

```
/plugin marketplace remove seo-llmo-writer
```

この1行で、スキルも入れた設定もまとめて消えます。

**画面を使わずにやる時**(ターミナルで打つ。Claude Code の外から操作できる)

| したい事 | 打つ1行 |
|---|---|
| 入れる | `claude plugin marketplace add yubokumin28/seo-llmo-writer` のあと `claude plugin install seo-llmo-writer@seo-llmo-writer` |
| 止める | `claude plugin disable seo-llmo-writer@seo-llmo-writer` |
| また使う | `claude plugin enable seo-llmo-writer@seo-llmo-writer` |
| 新しい版にする | `claude plugin update seo-llmo-writer@seo-llmo-writer` |
| 完全に外す | `claude plugin marketplace remove seo-llmo-writer` |

ターミナルで変えた時は、開いている Claude Code で `/reload-plugins` と打つか、開き直すと効きます。

### B. Claude Code で使う(フォルダを置くだけの方法)

1. 緑の **Code** ボタン → **Download ZIP** で落として、すべて展開する
2. 中の `skills/seo-llmo-writer` フォルダを、次の場所にフォルダごとコピーする
   - Windows: `C:\Users\<あなたの名前>\.claude\skills\`
   - Mac: `~/.claude/skills/`
3. Claude Code を開き直して「この記事を SEO と LLMO の目で点検して」と文章を貼る

この方法で入れた時は、止める = そのフォルダを別の場所へ移す、外す = そのフォルダを消す、です。

### C. ChatGPT・Gemini・Claude(ブラウザ)で使う

1. `skills/seo-llmo-writer/SKILL.md` を開き、先頭の `---` で囲まれた部分より下を全部コピーする
2. 貼る場所:
   - ChatGPT: プロジェクトの「指示」か、カスタム GPT の「指示」
   - Gemini: Gem の「カスタム指示」
   - Claude: プロジェクトの「指示」
3. そのプロジェクトで「点検して」「直して」「書いて」と頼む

## 外し方

- **A で入れた時**: 上の「完全に外す」の1行。ほかの動きは何も変わりません
- **B で入れた時**: `.claude\skills\seo-llmo-writer` フォルダを消すだけ
- **C で入れた時**: 貼った指示を消すだけ

## 安全について

中身は文章(Markdown)だけです。プログラム・自動で動く仕掛け(フック)・外部への通信は入っていません。

## 中身

```
skills/seo-llmo-writer/SKILL.md   … 指示書の本体(これ1枚で動く)
references/sources.md             … 参考にした公開リポジトリと研究の一覧
.claude-plugin/                   … Claude Code の /plugin で入れ外しするための設定
```

## 出典

公開リポジトリ(claude-seo・BlogPilot・llmopt・llm-docs-builder ほか)と、GEO の研究(KDD 2024)の考え方を、日本語の記事向けにまとめ直した物です。コードは含みません。詳しくは `references/sources.md`。

## 更新の記録

- v1.2.0(2026-10-27): 直す・書く時に、画像1枚ずつの説明文(キャプション)を必ず出すようにした。中身が分からない画像は本人に聞く
- v1.1.0(2026-10-24): Claude Code の /plugin で入れ外しできる形にした

作者: 遊牧民(yubokumin28) / クロコ🐊相談会で配布(2026-10-24)
