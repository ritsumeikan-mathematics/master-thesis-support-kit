# LaTeX 執筆ガイド

本ディレクトリでは、修士論文執筆における LaTeX の導入から実践的な利用方法までを解説します。LaTeX は高品質な数式組版を可能にする標準的なツールですが、環境構築や特有の記法に慣れが必要です。

## 1. LaTeX とは
LaTeX（ラテフ / レイテック）は、論理構造に基づいた文書作成を行うための組版システムです。
- **数式の美しさ**: 数学・理系分野において世界標準の品質で数式を記述できます。
- **自動化**: 目次、図表番号、引用文献のリファレンスなどを自動的に管理します。
- **プレーンテキスト管理**: 執筆内容はテキストファイルとして保存されるため、Git 等による履歴管理と非常に相性が良いです。

## 2. 最も信頼できる情報源：TeX Wiki
LaTeX に関する疑問やエラーの解決には、日本のコミュニティによって維持されている **[TeX Wiki](https://texwiki.texjp.org/)** を参照することを強く推奨します。

- **[TeX Wiki トップページ](https://texwiki.texjp.org/)**: ほぼ全ての情報への入り口です。
- **[逆引き辞典](https://texwiki.texjp.org/?LaTeX%E5%85%A5%E9%96%80%2F%E3%83%AA%E3%83%95%E3%82%A1%E3%83%AC%E3%83%B3%E3%82%B9)**: 「〜したい」という目的からコマンドを探せます。
- **[パッケージリスト](https://texwiki.texjp.org/?LaTeX%E3%83%91%E3%83%83%E3%82%B1%E3%83%BC%E3%82%B8)**: 数学記号、図表、レイアウト調整に必要なパッケージの使い方が解説されています。

> [!TIP]
> Google検索等で古いブログ記事を参照すると、現在は推奨されない古い記法（例：`eqnarray`）が見つかることがあります。最新のベストプラクティスを確認する際は、まず TeX Wiki を確認する癖をつけましょう。

## 3. 基本的な数式と図のサンプル
数学系論文で頻用される基本的な構造です。
実際にコンパイル可能なテンプレートは **[samples/README.md](./samples/README.md)** を参照してください。

### 数式の記述
複数行の数式を揃える場合は `align` 環境（amsmathパッケージ）を使用します。

```latex
\begin{align}
    f(x) &= \int_{a}^{b} g(t) \, dt \label{eq:integral} \\
    \sum_{n=1}^{\infty} \frac{1}{n^2} &= \frac{\pi^2}{6}
\end{align}
式\eqref{eq:integral}は...
```

### 図の挿入
図を配置する際は `figure` 環境を使用し、必ず `label` を付けて本文から参照します。

```latex
\begin{figure}[htbp]
    \centering
    \includegraphics[width=0.8\textwidth]{figures/sample-plot.pdf}
    \caption{数値実験の結果}
    \label{fig:result}
\end{figure}
図\ref{fig:result}に示す通り...
```

---
---
[次ステップ]
- [日本語 LaTeX 環境の選択（エンジンの違い）](./latex-engines.md)
- [ローカル環境の構築（Windows/macOS）](./setup-local.md)
- [クラウド実行環境の利用と比較](./cloud-services.md)
