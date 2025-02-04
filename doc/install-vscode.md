<h1>インストール手順（Visual Studio Code）</h1>

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [1. ソフトウェアのインストール](#1-ソフトウェアのインストール)
  - [1.1. インストーラの実行](#11-インストーラの実行)
  - [1.2. ユーザー設定（settings.json）](#12-ユーザー設定settingsjson)
  - [1.3. 拡張機能](#13-拡張機能)
- [2. 小伝馬町](#2-小伝馬町)
  - [2.1. キーボードショートカット コマンド markdown.extension.togglePreviewToSide を削除](#21-キーボードショートカット-コマンド-markdownextensiontogglepreviewtoside-を削除)
  - [2.2. html 出力時にサイドバー TOC を有効化](#22-html-出力時にサイドバー-toc-を有効化)
  - [2.3. Markdown TOC で日本語がダメぽ問題](#23-markdown-toc-で日本語がダメぽ問題)
  - [2.4. autoRenumber](#24-autorenumber)

<!-- /code_chunk_output -->

# 1. ソフトウェアのインストール

## 1.1. インストーラの実行

「Microsoft Visual Studio Code セットアップ」の「使用許諾契約書の同意」が表示されるので、「同意する(A)」のチェックをオンにして「次(N) >」ボタンをクリックする。

![install-vscode_20191217_060509](img/install-vscode_20191217_060509.png)

「Microsoft Visual Studio Code セットアップ」の「インストール先の指定」が表示されるので、各項目に以下の値を入力して「次(N) >」ボタンをクリックする。

![install-vscode_20191217_060521](img/install-vscode_20191217_060521.png)

| 項番 | 項目           | 値              |
| :--: | :------------- | :-------------- |
|  1   | インストール先 | C:\opt\vscode\  |

「既存のフォルダー」が表示されるので、「はい(Y)」ボタンをクリックする。

![install-vscode_20191217_060536](img/install-vscode_20191217_060536.png)

「Microsoft Visual Studio Code セットアップ」の「プログラムグループの指定」が表示されるので、「次(N) >」ボタンをクリックする。

![install-vscode_20191217_060548](img/install-vscode_20191217_060548.png)

「Microsoft Visual Studio Code セットアップ」の「追加タスクの選択」が表示されるので、各項目に以下の値を入力して「次(N) >」ボタンをクリックする。

![install-vscode_20191217_060645](img/install-vscode_20191217_060645.png)

| 項番 | 項目                                                                                       | 値                   |
| :--: | :----------------------------------------------------------------------------------------- | :------------------- |
|  1   | デスクトップ上にアイコンを作成する(D)                                                      | チェックをオフにする |
|  2   | エクスプローラーのファイル コンテキスト メニューに \[Code を開く] アクションを追加する     | チェックをオンにする |
|  3   | エクスプローラーのディレクトリ コンテキスト メニューに \[Code を開く] アクションを追加する | チェックをオンにする |
|  4   | サポートされているファイルの種類のエディターとして、Code を登録する                        | チェックをオフにする |
|  5   | PATH への追加（再起動後に使用可能）                                                        | チェックをオンにする |

「Microsoft Visual Studio Code セットアップ」の「インストール準備完了」が表示されるので、「インストール(I)」ボタンをクリックする。

![install-vscode_20191217_060700](img/install-vscode_20191217_060700.png)

「Microsoft Visual Studio Code セットアップ」の「Microsoft Visual Studio Code セットアップウィザードの完了」が表示されるので、「完了(F)」ボタンをクリックする。

![install-vscode_20191217_060716](img/install-vscode_20191217_060716.png)

## 1.2. ユーザー設定（settings.json）

※2019/12/30 時点

```json
{
  // diffEditor
  "diffEditor.renderSideBySide": false,
  // Editor
  "editor.colorDecorators": false,
  "editor.detectIndentation": false,
  "editor.fontFamily": "MeiryoKe_Console, Consolas, 'Courier New', monospace",
  "editor.formatOnPaste": true,
  "editor.formatOnSave": true,
  "editor.formatOnType": true,
  "editor.insertSpaces": true,
  "editor.lineNumbers": "on",
  "editor.minimap.renderCharacters": false,
  "editor.minimap.showSlider": "always",
  "editor.multiCursorModifier": "ctrlCmd",
  "editor.renderControlCharacters": true,
  "editor.renderIndentGuides": true,
  "editor.renderLineHighlight": "all",
  "editor.renderWhitespace": "all",
  "editor.rulers": [200],
  "editor.snippetSuggestions": "top",
  "editor.tabSize": 2,
  "editor.wordWrap": "on",
  // Emmet
  "emmet.showSuggestionsAsSnippets": true,
  "emmet.triggerExpansionOnTab": true,
  "emmet.variables": {
    "lang": "ja"
  },
  // Explorer
  "explorer.confirmDelete": false,
  // Files
  "files.associations": {
    ".*lintrc": "json"
  },
  "files.autoGuessEncoding": false,
  "files.encoding": "utf8",
  "files.eol": "\n",
  "files.exclude": {
    "**/*.map": true,
    "**/node_modules": true
  },
  "files.insertFinalNewline": true,
  "files.trimFinalNewlines": true,
  "files.trimTrailingWhitespace": true,
  "[markdown]": {
    "editor.quickSuggestions": true,
    "files.trimTrailingWhitespace": false
  },
  // Git
  "git.autofetch": true,
  "git.path": "C:\\opt\\git\\cmd\\git.exe",
  // HTML
  "html.format.contentUnformatted": "pre, code, textarea, title, h1, h2, h3, h4, h5, h6, p",
  "html.format.extraLiners": "",
  "html.format.unformatted": null,
  "html.format.wrapLineLength": 0,
  // Markdown
  "markdown.extension.orderedList.autoRenumber": false,
  "markdown.extension.orderedList.marker": "one",
  "markdown.extension.syntax.decorations": false,
  "markdown.extension.tableFormatter.enabled": false,
  "markdown.preview.breaks": true,
  "markdown.preview.fontFamily": "MeiryoKe_Console, Consolas, 'Courier New', monospace",
  "markdown.preview.fontSize": 14,
  // Markdown Preview Enhanced
  "markdown-preview-enhanced.enableExtendedTableSyntax": true,
  "markdown-preview-enhanced.enableScriptExecution": true,
  "markdown-preview-enhanced.previewTheme": "github-light.css",
  "markdown-preview-enhanced.singlePreview": true,
  // markdown-index
  "markdownIndex.indexBase": "#",
  // markdownlint
  "markdownlint.config": {
    "default": true,
    "MD013": {
      "line_length": 400
    },
    "MD025": false,
    "MD033": {
      "allowed_elements": ["h1", "span"]
    },
    "MD041": false
  },
  // Paste Images
  "pasteImage.defaultName": "${currentFileNameWithoutExt}_YMMDD_HHmmss",
  "pasteImage.insertPattern": "![${imageFileNameWithoutExt}](${imageFilePath})",
  "pasteImage.path": "${currentFileDir}\\img",
  // Search
  "search.exclude": {
    "**/tmp": true
  },
  // Window
  "window.openFoldersInNewWindow": "on",
  "window.title": "${activeEditorMedium}${separator}${rootName}",
  // Workbench
  "workbench.editor.labelFormat": "short",
  "workbench.editor.tabSizing": "shrink",
  "workbench.startupEditor": "none"
}
```

## 1.3. 拡張機能

※2019/12/30 時点

| 項番 | 名前                                          | バージョン |
| :--: | --------------------------------------------- | ---------- |
|  1   | Japanese Language Pack for Visual Studio Code | 1.41.2     |
|  2   | Markdown All in One                           | 2.6.1      |
|  3   | Markdown Checkbox                             | 1.6.0      |
|  4   | Markdown Preview Enhanced                     | 0.5.0      |
|  5   | markdown-index                                | 0.0.9      |
|  6   | markdownlint                                  | 0.32.0     |
|  7   | Paste Image                                   | 1.0.4      |
|  8   | PlantUML                                      | 2.13.5     |
|  9   | Prettier - Code formatter                     | 3.14.0     |

# 2. 小伝馬町

## 2.1. キーボードショートカット コマンド markdown.extension.togglePreviewToSide を削除

Markdown All in One はプレビュー表示のショートカットをオーバーライドします。

これは、`ctrl+k v` でプレビュー表示のトグル（開く,閉じるの切り替え）を行うためですが、Markdown Preview Enhanced（MPE）と競合するため無効にします。

ちなみに、有効状態だと MPE のプレビューではなく、デフォルトのプレビューが表示されます。

1. VS Code のメインメニューから、ファイル ＞ 基本設定 ＞ キーボードショートカットを開きます。
1. `ctrl+k v` で検索し、コマンド `markdown.extension.togglePreviewToSide` を右クリックしキーバインドを削除します。

## 2.2. html 出力時にサイドバー TOC を有効化

以前はデフォルトで有効でしたが、セキュリティの関係上デフォルトで無効になっています（ver.0.3.5 以降）。

有効にするには、ユーザー設定で`markdown-preview-enhanced.enableScriptExecution`を`true`にします。

有効にすると、html 出力時にサイドバーメニュー（目次）が生成されます。

ちなみにメニューボタンが左下に表示されるのですが、好みでないので左上にカスタマイズしています。

1. ctrl+shift+p を押し、 Markdown Preview Enhanced: Customize Css を開きます
1. 以下を最終行の後に追加

```less
// サイドバーTOCを左上にする
.md-sidebar-toc.md-sidebar-toc {
  padding-top: 40px;
}

#sidebar-toc-btn {
  bottom: unset;
  top: 8px;
}
```

## 2.3. Markdown TOC で日本語がダメぽ問題

結論、Auto Markdown TOC を使おう。

[Atom の markdown-toc でタイトルが日本語の場合に動かない場合の対処 - 山ｐの楽しいお勉強生活](http://yamap55.hatenablog.com/entry/2018/04/21/004258)

[GitHub Tips: Markdown に対して目次を作る方法 · sakura-editor/sakura Wiki · GitHub](https://github.com/sakura-editor/sakura/wiki/GitHub-Tips:-Markdown-%E3%81%AB%E5%AF%BE%E3%81%97%E3%81%A6%E7%9B%AE%E6%AC%A1%E3%82%92%E4%BD%9C%E3%82%8B%E6%96%B9%E6%B3%95)

_2019/12/29 追記_
Markdown Preview Enhanced で TOC が挿入できる（かつ、保存時に自動更新できる）ため、Markdown TOC も Auto Markdown TOC もいらん説。というか、いらん。

## 2.4. autoRenumber
