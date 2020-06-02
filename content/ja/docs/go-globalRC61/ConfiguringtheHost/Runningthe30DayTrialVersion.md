---
title: "Running the 30-Day Trial Version"
linkTitle: ""
weight: 07
type: "docs"
---

>本項目の設定は推奨設定ではございませんのでご注意ください。GO-Globalの評価を行う際にはきっとエイエスピー営業部までお問い合わせください。

GO-Global’s 30-day trial version can be downloaded from GraphOn’s website. The Activation Wizard runs during the GO-Global trial installation, and is accessible from the Start menu after installing the host. It configures the computer to use a GraphOn product license, then activates GO-Global on the computer. GO-Global can be activated on a computer with a trial license only once.

### To run the Activation Wizard
1. From the Start Menu, click GraphOn GO-Global | Activation Wizard.
2. When the Activation Wizard opens, follow the prompts. Sign in using your GraphOn account. Create an account if you do not have one. Then click the Sign in button. 

>GO-Global cloud trial licenses can only be used on computers that have direct access to the internet. If a computer does not have access to the internet (e.g., if it accesses the internet via a proxy server), the Activation Wizard will notify you that GO-Global is unable to communicate with GraphOn’s online license service. If you see this message, you can request an on-premises trial license as described below.
3. If applicable, select a GraphOn customer account.
4. Select the license you would like the computer to use. If there are no available licenses, click Start New Trial. Specify a description for the license, then click OK.
5. Click Accept to accept the GO-Global License Agreement.
6. Click Activate to enable GO-Global on this computer.

After installing GO-Global and running the Activation Wizard, you must restart the computer.

>If a license is grayed out, it is not an active license, and cannot be used.

## オンプレミスのトライアルライセンスを使用してGO-Globalをアクティブにする方法

インターネットに直接アクセスできないコンピュータの場合、またはクラウドのトライアルライセンスが確立できない場合、GraphOnはオンプレミスのFlexeraベースのトライアルライセンスを作成し、電子メールで送信します。オンプレミスライセンスを使用してGO-Globalを起動するには
1. コンピュータのホスト名とホストID（物理アドレス）を決定します。
a. [スタート | すべてのプログラム | アクセサリ | コマンドプロンプト] をクリックして、コマンドプロンプトウィンドウを開きます。
b. ipconfig /all と入力し、Enter キーを押します。
c. コンピュータのホスト名と物理アドレスを探します。
2. コンピュータのホスト名、ホストID(物理アドレス)、ユーザ数を明記してKitASPにメールを送信します。
3. KitASPからライセンスファイルが届いたら
a. .licファイルをc:\Program Files\GraphOn\GO-Global\Licensing ディレクトリにコピーしてください。
b. GO-Global License Manager Serviceを起動してください。
c. GO-Global Application Publishing Service を再起動します。

## 恒久的なオンプレミスライセンスのインストール

管理者は、現在クラウドやオンプレミスのトライアルライセンスを使用しているシステムに、オンプレミスの恒久的なライセンスをインストールすることができます。恒久的なライセンスの注文が入ると、GraphOnは注文を処理して新しいライセンスマスターを作成します。ライセンス情報は、注文リクエストに記載された連絡先にメールで送信されます。管理者はカスタマーポータルから製品コード、メールアドレス、ホスト名、ホストIDを入力してライセンスを有効化する必要があります。新しいライセンス(.lic)ファイルが添付ファイルとして電子メールで送信されます。ライセンス ID は、ライセンスファイルの名前のフォーマットに使用されます。(例: 8d73e4k.lic、8d73e4k はライセンス ID)。ライセンス ファイルの添付ファイルは、指定されたライセンスサーバにインストールする必要があります。

### 恒久的なのオンプレミスライセンスをインストールする方法
1. GO-Globalライセンスサーバ上のライセンスディレクトリ (例:C:\Program Files\GraphOn\GO-Global\Licensing\) からトライアルまたは無効になったライセンス (.lic) ファイルを削除してください。
2. 新しい.lic ファイルをGO-GlobalライセンスサーバーのLicensingディレクトリに移動する。
3. 必要に応じて、競合するライセンスマネージャーがある場合は、「SERVER」行のホストIDの後にポート番号を追加します。たとえば、以下のようになります。SERVER 2016ITL1 000C2931282E 27009 (これにより、ライセンスマネージャがポート27009を使用するように指示されます。)これ以外の変更を行うと、ライセンスが破損して無効になる可能性があることに注意してください。
4. GO-Globalライセンスサーバでサービスを開き、GO-Globalライセンスマネージャを再起動します。
5. ライセンス サーバーを使用しているすべての GO-Global ホストで: 
a. ホストで GO-Globalセッションが実行されていないことを確認します。
b. サービスを開き、GO-Global Application Publishing Serviceを再起動します。(これにより、すべてのユーザセッションが終了します)。

## ホスト以外のシステムにWebファイルをインストールする方法

GO-Global WebファイルをGO-Globalホスト以外のシステムにインストールすることができます。

### GO-Globalホスト以外のシステムにWebファイルをインストールする方法

1. 目的のWebサーバ上でホストインストーラを実行し、Webファイルをインストールすることを選択します。
2. Webサーバのlogon.html ページを編集し、ホスト名の代わりにGO-Globalホストのアドレスを挿入して、次のステートメントを追加します。

```
if (host.length == 0)
{
host="hostname";
}
```

## IIS Webサーバを使用して、既定のディレクトリ以外のディレクトリからWebファイルをホストする

Microsoft IIS Web Serverを使用して、既定のgoglobalディレクトリ以外のディレクトリからGO-Global Webファイルをホストすることができます。

### 既定のディレクトリ以外のディレクトリからWebファイルをホストする方法

1. Webサーバ上のc:\inetpub\wwwrootにディレクトリを作成し、それをあなたのユーザが表示するようにしたいものを呼び出します。例えば、C:\inetpub\wwwroot\Webのようなフォルダを作成します。
2. GO-GlobalホストからC:\Program files\GraphOn\GO-Global\Webディレクトリの内容を新しいディレクトリにコピーします。
3. IISマネージャを開き、[サイト | 既定のWebサイト]に移動します。[既定のWebサイト]を右クリックし、[仮想ディレクトリを追加]をクリックします。
4. 手順1で作成したディレクトリと同じエイリアスを指定し、物理パスを手順2でファイルをコピーしたディレクトリに指定します。例えば、c:\inetpub\wwwrootWebのようにします。
5. 新しい仮想ディレクトリをクリックします。次にMIMEタイプをダブルクリックします。
6. 追加をクリックします。File name extensionボックスに.memを入力します。[MIMEの種類]ボックスにapplication/octet-streamと入力します。次にOKをクリックします。
7. この仮想ディレクトリのデフォルトドキュメントとして logon.html を追加します。(詳細はIISでのデフォルトドキュメントの設定については、https://support.microsoft.com/enus/help/320051/how-to-configure-the-default-document-in-internet-information-servicesを参照してください)
8. IISの設定が正しいことを確認するには、ブラウザを開き、GO-Globalホストに接続するためのURLを入力します、例:http://hostname/web/logon.htmlもしくはhttps://hostname/web/logon.html (hostnameはあなたのGO-Globalホストの名前です。webはIISで作成した仮想ディレクトリの名前です。)

## Apache HTTPサーバを介したGO-Globalの実行

Apache HTTP Server 2.4 WebサービスがGO-Globalホストにインストールされている場合、ユーザはWebブラウザを使ってクライアントマシンから接続できます。

IISがインストールされている場合は、Apacheをダウンロードする前にWorld Wide Web発行サービスを停止して無効にする必要があります。[サービス]から、[World Wide Web発行サービス]を右クリックして[プロパティ]を選択します。[プロパティ]ダイアログで、[スタートアップの種類]ドロップダウンメニューから[無効]を選択し、[停止]ボタンをクリックします。OKをクリックしてください。

1. http://www.apachelounge.com/download/にアクセスして最新バージョンをダウンロードしてください。GraphOnによってテストされたバージョンはhttpd-2.4.29-Win64-VC15.zipでした。
2. C ++再配布可能なVisual Studio 2017をダウンロードしてインストールします。GraphOnによってテストされたバージョンは、次のリンクからダウンロードできます。https://aka.ms/vs/15/release/VC_redis.x64.exe
3. httpd-2.4.29-Win64-VC15.zipをC:\Apache24ディレクトリのGO-Globalホストに抽出します。
4.httpd.conf ファイルの DirectoryIndex ディレクティブに logon.html を追加します。例えばC:\Apache24conf\httpd.confをテキストエディタで開き、DirectoryIndex 行を編集してファイルを保存します。DirectoryIndex 行は以下のようになっているはずです。
```
<IfModule dir_module>
DirectoryIndex logon.html index.html
</IfModule>
```
5. [ スタート | すべてのプログラム | アクセサリー | コマンドプロンプト ]の順にクリックします。コマンドプロンプトを右クリックし、管理者として実行します。
6. [コマンドプロンプト]ウィンドウで、次のように入力します。
```
cd C:\Apache24\bin
httpd -k install
httpd -k start 
```
　　　　　まだ開いていない場合は、ファイアウォールでポート80を開く必要があります。SSLが実行されている場合は、ポート443が開いていることを確認してください。

6. C:\Apache24\binを開き、ApacheMonitor.exeを実行します。システムトレイからApache Monitorを開き、サービスが開始されたことを確認します。
7. C:\Apache24\htdocsを開き、goglobalという名前のディレクトリを作成します。
8. C:\Program files\GraphOn\GO-Global\Webの内容をC:\Apache24\htdocs\goglobalディレクトリにコピーします。
9. GO-Globalホスト上でブラウザを開き、http://localhost/goglobal/logon.html にアクセスしてセッションを開始します。

>GO-Globalのバージョン番号には、ソフトウェアのメジャーバージョン、マイナーバージョン、サービスパックバージョン、ビルド番号が含まれています。たとえば、バージョン6.1.2.37894では、6がメジャーバージョン、1がマイナーバージョン、2がサービスパックバージョン、そして37897がビルド番号です。
>
>GraphOnがGO-Globalへのメジャーアップグレードをリリースすると、メジャーバージョン番号が増えます。メジャーアップグレードには、通常、重要な新機能または変更された機能や機能、ユーザインターフェイスの変更、またはアーキテクチャの変更が含まれます。GraphOnがGO-Globalへのマイナーアップグレードをリリースすると、マイナーバージョン番号が増えます。マイナアップグレードには、一般的にマイナーな機能追加や変更、バグ修正とセキュリティ改善が含まれます。GraphOnがGO-GlobalにService Packをリリースすると、Service Packのバージョン番号が増えます。サービスパックには一般にバグ修正が含まれており、新しいプラットフォームのサポートとマイナーな機能強化が含まれている場合があります。ビルド番号はすべてのGO-Globalリリースで増加しています。ビルド番号だけが増えたリリースがパッチです。パッチには通常、セキュリティ上の問題、互換性の問題、および製品の問題に対する修正が含まれています。たとえば、パッチにはGO-Globalが最新リリースのMicrosoft Windows上で動作することを可能にする変更が含まれているかもしれません。