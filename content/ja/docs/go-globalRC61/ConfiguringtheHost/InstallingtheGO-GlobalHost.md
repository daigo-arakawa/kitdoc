---
title: "GO-Globalホストのインストール"
linkTitle: ""
weight: 04
type: "docs"
---


GO-Globalは自己解凍型の実行ファイルとして提供され、gg-host.exeをダブルクリックすることでインストールできます。ホストセットアッププログラムを実行する際には、コンピュータの管理者グループのメンバであるアカウントにログインする必要があります。
既定では、GO-Globalホストセットアップは、コアホストコンポーネント、Webコンポーネント(ブラウザログオンのためにホストを設定するために必要なすべてのファイルを含む)、ライセンス コンポーネントのすべてをインストールします。[Customize]ボタンをクリックして、インストールしたくないコンポーネントのチェックを外すことで、インストールをカスタマイズすることができます。それ以外の場合は、[Install]ボタンをクリックします。GO-Globalを有効にするには、GO-Globalのライセンスファイルを既定のライセンスフォルダにコピーしてください。ライセンスサーバを使用するように GO-Globalを設定するには、中央ライセンスサーバーを使用するように GO-Globalを設定するを参照してください。
後でライセンスファイルをコピーする場合は、ファイルをコピーした後にGO-Global License Managerを再起動し、次に GO-Global Application Publishing Serviceを再起動する必要があります。

### GO-Global License Managerを再起動する方法
1. [コントロールパネル | 管理ツール | サービス]をクリックします。
2. サービスの一覧から [GO-Global License Manager]を選択します。
3. 右クリックして、[再起動]を選択します。

### GO-Global Application Publishing Serviceを再起動する方法
1. [コントロールパネル | 管理ツール | サービス]をクリックします。
2. サービスの一覧から [GO-Global Application Publishing Service]を選択します。
3. 右クリックして、[再起動]を選択します。

ホストをインストールしてコンピュータを再起動した後、Webブラウザを選択してGO-GlobalのInteractive Quick Start Guideを開きます。このガイドでは、Admin Consoleを通じてアプリケーションを公開する方法、アプリケーションへのリンクを共有する方法を説明しています。GO-Global AppControllerのログオンページにhelp=ac を追加することで、Interactive Quick Guideをいつでも開くことができます。たとえば、http://hostname/goglobal/?help=acのように設定します。

>ライセンスファイルの最小権限は以下の通りです。
Administrators: Full Control; Users: Read & Execute; SYSTEM: Full Control
以下のエラーメッセージがLogファイルに表示された場合、ライセンス・ファイルのパーミッションが正しくない可能性があります。
>
>`FlexLM code #-1; FlexLM text: Cannot find license file. The license files (or license server system network addresses) attempted are listed below. Use LM_LICENSE_FILE to use a different license file, or contact your software provider for a license file.)`

2つのGO-Globalライセンスを組み合わせる場合、または同じGO-Globalホストで2つの別々のライセンスを使用する場合、ライセンスファイルのホスト名は大文字と小文字が区別され、同一である必要があります。

GO-Globalホストの起動設定を設定する場合は、リストから[GO-Global Application Publishing Service]を選択し、[起動]ボタンをクリックします。GO-Globalホストに適用するオプションを選択します。