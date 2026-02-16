# 修士論文支援キット

修士論文の執筆と研究活動を一通りサポートするための **AI プロンプト集 ＋ LaTeX 環境ガイド** のセットです。

## 目的と位置づけ

修士課程の学生が、学術的誠実性を保ちながら効率的に高品質な論文を仕上げることを支援するためのリソース集です。

具体的には：

- **論文執筆プロセスの効率化**：繰り返し作業や形式的なタスクを補助
- **論理性・学術的妥当性のセルフチェック**：AI を「問いかけの相手」として活用
- **LaTeX 環境構築の支援**：モダンな日本語 LaTeX 環境のセットアップとサンプル提供
- **研究倫理とツール利用の指針提示**：AI や既存ツールを適切に使うためのガイドライン

**注意**: 提供されるのはあくまで「補助ツール・プロンプト」であり、内容の正確性や学位授与は保証しません。

## ディレクトリ構成

### `ai-prompts/`

修士論文の各フェーズで使える AI プロンプトのコレクションです。

- **想定用途**：
  - 執筆済み文章の論理検証
  - 説明の補足・深化案の生成
  - 数式画像や箇条書きの LaTeX 変換
  - 公聴会（修士論文発表）での質問シミュレーションと回答評価

- **利用前の注意**：[`ai-prompts/README.md`](./ai-prompts/README.md) を事前に読み、AI 利用の前提・注意点を確認してください。

**主なファイル**：
- `01_master_thesis_ai_usage_principles.md` - AI 利用の基本原則
- `02_master_thesis_analysis_templates.md` - 論理分析・検証プロンプト
- `03_master_thesis_latex_conversion.md` - LaTeX 変換プロンプト
- `04_master_thesis_explanation_expansion.md` - 説明補足・深化プロンプト
- `05_master_thesis_public_hearing_support.md` - 公聴会支援プロンプト

### `latex-guide/`

モダンな LaTeX 執筆環境の構築ガイドとサンプル群です。

- **推奨エンジン**：LuaLaTeX による現代的な日本語環境
- **環境選択肢**：
  - Windows/macOS 上のローカル環境
  - Prism・CloudLaTeX 等のクラウド環境

**主な内容**：
- [`latex-guide/README.md`](./latex-guide/README.md) - 導入ガイドと信頼できる情報源へのリンク
- `beamer-presentation-from-thesis.md` - 修士論文から Beamer で20分発表スライドを作るガイド
- `beamer-thesis-presentation.tex` - Beamer 発表用サンプルテンプレート
- 数学論文用の最小テンプレート

## 使い方

1. **AI プロンプトを使う場合**：
   - [`ai-prompts/01_master_thesis_ai_usage_principles.md`](./ai-prompts/01_master_thesis_ai_usage_principles.md) を最初に読む
   - 目的に合ったテンプレートを選び、プレースホルダ（`[...]`）を埋めて使用

2. **LaTeX 環境を構築する場合**：
   - [`latex-guide/README.md`](./latex-guide/README.md) を読み、自分に合った環境を選択
   - サンプルファイルを参考に執筆環境を整備

3. **公聴会の準備をする場合**：
   - [`ai-prompts/05_master_thesis_public_hearing_support.md`](./ai-prompts/05_master_thesis_public_hearing_support.md) を使用
   - 発表構成の改善、想定質問のシミュレーション、回答案の評価が可能

## 今後の拡張予定

以下のコンテンツを追加予定です：

- [ ] 修士論文用 LaTeX テンプレート
- [ ] Python 等によるデータ解析・可視化スクリプト集
- [ ] 図表作成ガイドライン
- [ ] BibTeX を用いた引用文献管理のベストプラクティス
- [ ] 先行研究調査のための検索クエリ生成テンプレート
- [ ] 英語論文執筆支援プロンプト

## ライセンスと免責事項

- このリポジトリの内容は教育目的で提供されています
- 内容の正確性や完全性は保証されません
- 各自の責任において利用してください
- 所属機関のガイドラインや指導教員の方針を優先してください

## 貢献

改善提案や追加コンテンツのアイデアがあれば、Issue や Pull Request でお知らせください。

---

**関連リンク**：
- [TeX Wiki](https://texwiki.texjp.org/)
- [LaTeX 入門 (TeX Wiki)](https://texwiki.texjp.org/?LaTeX%E5%85%A5%E9%96%80)
