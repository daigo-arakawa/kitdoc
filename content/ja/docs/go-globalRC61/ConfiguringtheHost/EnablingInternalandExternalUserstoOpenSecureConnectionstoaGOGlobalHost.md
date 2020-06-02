---
title: "社内外のユーザによるGO-Globalホストへのセキュアな接続を可能にする"
linkTitle: ""
weight: 08
type: "docs"
---


1. ホストとは別のコンピューターにWebコンポーネントをインストールします。(WebサーバとGO-Globalホストは、同じコンピュータ上の同じポートでリッスンすることはできません。）
2. Microsoft IISが実行されていないか、GO-Globalホスト上の接続を受け入れていないことを確認します。
3. [Hosts Options]ダイアログの[Security]タブの[Port]フィールドの値を443に変更します。

![2-8-1](/img/2-8-1.png)

4. ホストポートの設定を変更した後、ポートパラメータに433を付加してWebに追加します。ホストへの接続に使用されるリンクは例えば、http://hostname.graphon.com/goglobal/?host=hostname.graphon.com&port=443
5. [Hosts Options]の[Security]タブで、ホストとWebサーバのSSL証明書を取得します。Webサーバコンピュータのドメイン名とGO-Globalホストのドメイン名が同じであることを確認します。それ以外の場合、ブラウザは、WebサーバからダウンロードされたWebアプリがGO-GlobalホストへのWebSocket接続を開くのを防ぎます。
6. 外部DNSを構成して、ホストおよびWebサーバ証明書の共通名をホストおよびWebサーバコンピュータの外部IPアドレスに解決します。
7. ホストとWebの共通名を解決するように内部DNSを構成します。。