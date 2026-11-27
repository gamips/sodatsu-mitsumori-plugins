# 育つ見積 for Claude Code

Claude Codeから「育つ見積」に接続し、見積書・請求書・納品書・発注書を作成・編集できます。保存済みの書類を探す、見積書をもとに請求書を作る、PDFや共有URLを取得するといった作業も、Claude Codeに頼めます。取引先や登録品目の確認にも対応しています。

株式会社ガミがGitHubで配布しています。ご利用にはClaude Codeと育つ見積のアカウントが必要です。

## インストールする

Claude Codeを起動し、セッション内で次のコマンドを1行ずつ実行します。GitHubの配布元から直接インストールできるため、ZIPのダウンロードは不要です。

```text
/plugin marketplace add gamips/sodatsu-mitsumori-plugins
/plugin install sodatsu-mitsumori@sodatsu-mitsumori-plugins
```

インストール先を聞かれたら、利用したい範囲を選びます。読み込みを求められた場合は `/reload-plugins` を実行するか、Claude Codeを再起動します。

## 育つ見積に接続する

1. Claude Codeで `/mcp` を開き、名前に `sodatsu-mitsumori` が含まれる接続を選びます。
2. `Authenticate` を選ぶとブラウザが開きます。使いたい育つ見積のアカウントでログインし、画面に表示される権限を確認して接続を許可します。
3. Claude Codeに戻り、`/mcp` で育つ見積が接続済みになったことを確認します。

## Claude Codeで頼む

最初は「育つ見積に保存している最近の見積書を5件見せて」と頼むと、書類を変更せずに接続を確認できます。

| やりたいこと | 依頼の例 |
| --- | --- |
| 見積書を作る | 株式会社サンプル宛てに、現地調査を1式、税抜30,000円で見積書にして。保存する前に内容を見せて。 |
| 見積書から請求書を作る | 見積番号○○の見積書をもとに請求書を作って。発行前に内容を確認したい。 |
| PDFを取得する | 見積番号○○のPDFを取得して。 |

同じ件名の書類が複数ある場合は、書類番号や取引先名を添えると指定しやすくなります。

## アップデートする

ターミナルで次のコマンドを順に実行します。開いているセッションには `/reload-plugins` で反映できます。

```sh
claude plugin marketplace update sodatsu-mitsumori-plugins
claude plugin update sodatsu-mitsumori@sodatsu-mitsumori-plugins
```

## 利用条件とサポート

育つ見積のFreeプランでは、MCP経由で新規保存できる書類は累計5件です。書類の削除や再接続で残り件数は戻りません。Claude Codeには、別途Claude側の利用条件が適用されます。

- [育つ見積の外部AI連携](https://sodatsu-mitsumori.net/features/external-ai-mcp/)
- [サポート](https://sodatsu-mitsumori.net/aboutus/)
- [個人情報保護方針](https://sodatsu-mitsumori.net/privacy/)・[利用規約](https://sodatsu-mitsumori.net/terms/)
- [Claude Codeのインストールガイド](https://code.claude.com/docs/en/plugins/install)・[MCP接続ガイド](https://code.claude.com/docs/en/mcp)

接続設定、スキル、メタデータ、文書はMITライセンスです。製品名とロゴは対象外です。詳細は [LICENSE](LICENSE) と [NOTICE](NOTICE) をご覧ください。
