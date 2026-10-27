# 育つ見積 プラグイン

育つ見積（Sodatsu Mitsumori）のRemote MCPに接続する配布パッケージです。接続設定と既存の33スキルを収録しています。

見積書・請求書などの作成・編集、PDFや共有URLの取得、品目マスターや設定の操作に対応します。接続先は `https://app.sodatsu-mitsumori.net/api/mcp` で、OAuth認証を使用します。既存の接続がある場合は、重複させずに再利用してください。

## パッケージ

| フォルダ | 形式 |
| --- | --- |
| `openai/` | Codex・ChatGPT向けAgent Plugins形式 |
| `claude/` | Claude向けプラグイン形式 |

[リリース](https://github.com/gamips/sodatsu-mitsumori-plugins/releases)から両形式のZIPを取得できます。現時点では導入・審査用のプレビューです。JSONと配布ファイルの検証は済んでいますが、実クライアントでの導入・OAuth・操作確認と公式ディレクトリへの申請はこれからです。

## Codexで試す

対応するCodex CLIでは、次のコマンドで配布元を追加できます。その後、対応するデスクトップアプリのプラグイン画面から導入・接続を行います。

```sh
codex plugin marketplace add gamips/sodatsu-mitsumori-plugins
```

クライアントやバージョンによる違いは、[OpenAIの導入手順](https://developers.openai.com/plugins/build/plugins#add-a-marketplace-from-the-cli)を確認してください。

## Claudeで試す

Claude Codeでは次のコマンドで配布元を追加し、プラグインを導入します。

```text
/plugin marketplace add gamips/sodatsu-mitsumori-plugins
/plugin install sodatsu-mitsumori@sodatsu-mitsumori-plugins
```

利用するClaudeアプリの対応状況は、[Claudeの配布ガイド](https://code.claude.com/docs/en/plugin-marketplaces)を確認してください。

## 利用とライセンス

育つ見積の利用条件と設定方法は、[MCPの使い方](https://sodatsu-mitsumori.net/features/external-ai-mcp/)を確認してください。導入後はプラグインとスキルが認識されることを実際のクライアントで確認してください。

接続設定、スキル、メタデータ、文書はMITライセンスです。製品名とロゴは対象外です。非公開サーバーのソースコードは含まず、本ライセンスの対象にも含めません。詳細は [LICENSE](LICENSE) と [NOTICE](NOTICE) を参照してください。

このリポジトリの公開は、各社の公式ディレクトリへの掲載を示すものではありません。
