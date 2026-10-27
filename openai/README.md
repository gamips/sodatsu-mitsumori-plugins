# 育つ見積

育つ見積（Sodatsu Mitsumori）のRemote MCPを接続するプラグインです。見積書・請求書などの作成・編集、PDFや共有URLの取得、品目マスターや設定の操作に対応しています。

Install this plugin in your AI client to use the included skills with Sodatsu Mitsumori. Connect to `https://app.sodatsu-mitsumori.net/api/mcp` and complete OAuth authentication. If you already have a connection to this endpoint, reuse it to avoid duplicate connections. After installation, check that your AI client recognizes the plugin and its skills. Requests use your connected AI client for model inference. The plugin package connects to the existing service; it does not include the private MCP server.

## 利用条件

Freeでは、MCP経由の新規書類保存は累計5件までです。削除や再接続で件数は回復しません。有料プランは育つ見積の利用条件に従います。接続先AIの契約は別途必要です。

最新の操作仕様は、接続後に `get_agent_instructions` から取得します。

- [使い方](https://sodatsu-mitsumori.net/features/external-ai-mcp/)
- [サポート](https://sodatsu-mitsumori.net/aboutus/)
- [個人情報保護方針](https://sodatsu-mitsumori.net/privacy/)
- [利用規約](https://sodatsu-mitsumori.net/terms/)

## ライセンス

接続設定、スキル、メタデータ、文書はMITライセンスです。製品名とロゴは対象外です。非公開サーバーのソースコードは含まず、本ライセンスの対象にも含めません。詳細は `LICENSE` と `NOTICE` を参照してください。
