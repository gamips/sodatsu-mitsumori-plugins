# 育つ見積 プラグイン

育つ見積（Sodatsu Mitsumori）のRemote MCPに接続する配布パッケージです。接続設定と34スキルを収録しています。

見積書・請求書などの作成・編集、PDFや共有URLの取得、取引先・品目マスターや設定の操作に対応します。接続先は `https://app.sodatsu-mitsumori.net/api/mcp` で、OAuth認証を使用します。既存の接続がある場合は、重複させずに再利用してください。

取引先は `sodatsu-partners` で検索・登録・編集・削除できます。既存の接続に取引先の権限がない場合は、OAuthで必要な権限を許可してください。

## パッケージ

| フォルダ | 形式 |
| --- | --- |
| `openai/` | Codex・ChatGPT向けAgent Plugins形式 |
| [`claude/`](claude/README.md) | Claude Code向けプラグインと導入ガイド |
| `antigravity/` | Antigravity向けプラグイン形式 |

[リリース一覧](https://github.com/gamips/sodatsu-mitsumori-plugins/releases)から、利用するクライアントに対応したZIPを取得できます。

## Codexで試す

プラグインに対応するCodex CLIでは、次のコマンドで配布元を追加し、プラグインを導入できます。導入後はMCP接続の認証状態を確認してください。

```sh
codex plugin marketplace add gamips/sodatsu-mitsumori-plugins
codex plugin add sodatsu-mitsumori@sodatsu-mitsumori-plugins
```

クライアントやバージョンによる違いは、[OpenAIの導入手順](https://developers.openai.com/plugins/build/plugins#add-a-marketplace-from-the-cli)を確認してください。

## Claude Codeで使う

Claude Codeから育つ見積に接続し、見積書・請求書などを作成できます。保存済みの書類の検索や、PDF・共有URLの取得にも使えます。株式会社ガミのGitHub配布元からインストールできます。

Claude Codeのセッションで次のコマンドを1行ずつ実行します。

```text
/plugin marketplace add gamips/sodatsu-mitsumori-plugins
/plugin install sodatsu-mitsumori@sodatsu-mitsumori-plugins
```

インストール後は `/mcp` で育つ見積のアカウントに接続します。認証の手順、依頼の例、更新方法は[Claude Code向けの使い方](claude/README.md)をご覧ください。

## Antigravityで試す

```sh
git clone https://github.com/gamips/sodatsu-mitsumori-plugins.git
agy plugin install ./sodatsu-mitsumori-plugins/antigravity
```

Antigravity向けパッケージは `agy plugin validate --strict` を通過しています。AntigravityからのOAuth接続は未確認です。

## 利用とライセンス

育つ見積の利用条件と設定方法は、[MCPの使い方](https://sodatsu-mitsumori.net/features/external-ai-mcp/)を確認してください。導入後はプラグインとスキルが認識されることを実際のクライアントで確認してください。

接続設定、スキル、メタデータ、文書はMITライセンスです。製品名とロゴは対象外です。非公開サーバーのソースコードは含まず、本ライセンスの対象にも含めません。詳細は [LICENSE](LICENSE) と [NOTICE](NOTICE) を参照してください。

このリポジトリの公開は、各社の公式ディレクトリへの掲載を示すものではありません。
