# ローカル環境の構築 (Windows/macOS)

自身の PC に LaTeX 環境を構築することで、オフラインでの執筆や、クラウドサービスの制限（コンパイル時間やファイルサイズ）を受けない自由な執筆が可能になります。

## 1. インストール

OS ごとに推奨されるディストリビューションが異なります。非常に容量が大きいため（約 5GB〜）、安定したネットワーク環境で実行してください。

### Windows: TeX Live
1.  **[TeX Live 公式サイト](https://texwiki.texjp.org/?TeX%20Live)** (TeX Wiki) から `install-tl-windows.exe` をダウンロードします。
2.  インストーラーを実行し、「Simple Install」または「Advanced Install」を選択します。
    - **Advanced Install** を選び、スキームを「small」にして必要なものだけ入れることも可能ですが、初心者には「full」（デフォルト）を推奨します。

### macOS: MacTeX
1.  **[MacTeX 公式サイト](https://tug.org/mactex/)** から `MacTeX.pkg` をダウンロードして実行します。
2.  Homebrew を利用している場合は、以下のコマンドでもインストール可能です。
    ```bash
    brew install --cask mactex
    ```

---

## 2. エディタの設定 (VS Code)
エディタには **Visual Studio Code (VS Code)** と拡張機能 **LaTeX Workshop** の組み合わせを推奨します。

### 導入手順
1.  VS Code の拡張機能マーケットプレイスで `LaTeX Workshop` をインストールします。
2.  プロジェクトのルート（またはユーザー設定）に以下の設定を追加します。これにより、保存時に自動で LuaLaTeX によるビルドが走ります。

### 設定テンプレート (`.vscode/settings.json`)
以下の内容をコピーして、プロジェクトフォルダ内の `.vscode/settings.json` に保存してください。

```json
{
    "latex-workshop.latex.recipes": [
        {
            "name": "lualatex",
            "tools": ["lualatex"]
        }
    ],
    "latex-workshop.latex.tools": [
        {
            "name": "lualatex",
            "command": "lualatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOC%"
            ]
        }
    ],
    "latex-workshop.latex.autoBuild.run": "onSave",
    "latex-workshop.view.pdf.viewer": "tab"
}
```

---

## 3. 動作確認
1.  適当なフォルダに `test.tex` を作成し、以下の内容を記述します。
    ```latex
    \documentclass{ltjsarticle}
    \begin{document}
    こんにちは、LaTeX。 $E=mc^2$
    \end{document}
    ```
2.  ファイルを保存（Ctrl+S / Cmd+S）し、右側に PDF が表示されれば成功です。

> [!NOTE]
> ローカル環境のメンテナンス（パッケージの更新）には、Windows なら `TeX Live Manager (tlshell)`、macOS なら `TeX Live Utility` を定期的に実行することをお勧めします。

---
[次ステップ]
- [クラウド実行環境の利用と比較](./cloud-services.md)
- [実践的なサンプルコード集](./samples/README.md)
- [Git/GitHub によるバージョン管理の概要（オプション）](./github-integration.md)

