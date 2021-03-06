---
title: "GO-Globalの機能"
linkTitle: ""
weight: 02
type: "docs"
---


- **ネットワークおよびウェブへのアクセス:** GO-Globalでは、ネットワークまたはWebアクセスを介して、GO-GlobalホストからWindowsアプリケーションへのアクセスを提供しております。
- **クロスプラットフォームの互換性:** GO-Globalでは、事実上すべてのクライアントプラットフォームからWindowsアプリケーションにアクセスすることができます。アプリケーションは、Mac、Windows、Linuxなどのデスクトップコンピュータ、およびiOSやAndroidのモバイルデバイスから実行することができます。GO-Globalを通じて配備されたWindowsベースのアプリケーションは、クライアントプラットフォームに関係なく、Windowsオペレーティングシステム上で実行されているかのような外観、操作感、機能を有しています。
- **クライアントファイルへのアクセス:** GO-Globalは、ハードディスクおよびマッピングされたネットワークドライブを含むクライアントドライブのシームレスな統合をサポートしています。これにより、ユーザはクライアントコンピュータに保存されているファイルにアクセスし、ローカルにファイルを保存することができます。
- **ホストの監視:** GO-Globalでは、個々のGO-Globalホストのリアルタイム監視、個々のクライアントとプロセスの制御、個々のユーザのログアウトおよびシャットダウンを提供しています。kitASPが開発した<GO-Global拡張パック>を利用することで、Webでユーザやセッションの監視を行うことも可能になります。
- **セッションシャドウイング:** セッションシャドウイング機能により、複数のユーザが単一のセッションとそのアプリケーションを表示して制御することができます。この機能により、ヘルプデスクの担当者やシステム管理者は、ユーザの問題のトラブルシューティングやデバッグを支援することができます。セッションシャドウイングは、ライブコラボレーションにも使用できます。
- **ロードバランシング:** ロードバランシングは、複数のGO-Globalホストにユーザセッションを分散します。ロードバランシングが有効な場合、ユーザはロードバランシングされたホストのいずれかで実行されている切断されたセッションに再接続することができます(※1)。
- **セッションの再接続:** セッションの再接続を有効にすると、GO-Globalはクライアント接続なしでサーバ上のクライアントセッションを維持します。ユーザがサーバから故意に切断した場合、またはネットワークの問題によりクライアントの接続が失われた場合、管理者が指定した期間、ユーザのセッションおよびアプリケーションはサーバ上で実行されたままになります。クライアントのホストへの接続が切断された場合、クライアントは自動的にホストへの再接続を試みます。
- **パフォーマンスカウンタ:** パフォーマンスカウンタをWindowsパフォーマンスモニタに追加して、アクティブなセッション数とサーバに接続されているクライアント数を追跡することができます。GO-Globalホストのパフォーマンスカウンタを使用すると、管理者はGO-Globalホストへのネットワークアクセスを持つすべてのマシンからサーバのアクティビティを監視することができます。
- **プロキシトンネリング:** プロキシトンネリングにより、ユーザはプロキシサーバを介してインターネット上のGO-Globalホストに接続することができます。
- **グループポリシーのサポート:** Microsoftのグループポリシーとその拡張機能を使用して、管理者はレジストリベースのポリシーの管理、スクリプトの割り当て、フォルダのリダイレクト、アプリケーションの管理、セキュリティオプションの指定を行うことができます。
- **SSLセキュリティ:** GO-Globalでは、GO-Globalのクライアントとサーバ間の通信方法としてSSL(Secure Socket Layer)をサポートしております。
- **タイムゾーンリダイレクト:** このオプションでは、GO-Globalホストで選択されているタイムゾーンに関係なく、クライアントコンピュータのタイムゾーンでGO-Globalセッションを実行することができます。
- **下位互換性のあるクライアントとホスト:** クライアントとサーバのメジャーバージョンとマイナバージョンが一致していても、リビジョン(サービスパック)またはビルド番号が一致しない場合でも、クライアントがGO-Globalホストに接続できるようになります。
- **クライアント印刷:** ユーザは、GO-Globalホスト上で実行されているアプリケーションからクライアントアクセス可能なプリンタに印刷することができます。GO-Globalのユニバーサルプリンタドライバは、ほぼすべてのプリンタを自動的にサポートしています。高度なプリンタ固有の機能については、管理者は、ネイティブプリンタドライバを使用するようにGO-Globalホストを設定することができます。
- **動的なディスプレイのサイズ変更:** ユーザが別のデバイスからセッションに再接続した場合、またはクライアントデバイスの解像度を変更した場合、GO-Globalはセッションのデスクトップのサイズを自動的に調整します。
- **高解像度ディスプレイのサポート:** GO-Globalは高解像度ディスプレイをサポートしています。GO-GlobalクライアントをWindowsで実行する場合、GO-GlobalはクライアントコンピュータのDPI(DPI Per Inch)設定を自動的に使用します。クライアントをWindows以外のオペレーティングシステムで実行する場合、GO-Globalはホスト上のコントロールパネルのディスプレイアプレットでユーザに指定されたDPI設定を使用します。
- **クライアントサウンド:** GO-Globalホストは、GO-Globalセッションで実行されているアプリケーションからWindowsクライアントに音声出力をストリーム配信します。
- **クライアントのシリアルポートとパラレルポート:** GO-Globalでは、ホスト上で実行されているアプリケーションがクライアントマシンのシリアルポートとパラレルポートにアクセスすることができます。この機能はWindowsクライアントでのみサポートされています。
- **モバイルアプリのツールバーエディタ:** 管理者は、Windowsアプリケーションがモバイルデバイスからアクセスされた際に、GO-Globalモバイルアプリの下部に表示されるカスタムツールバーボタンとメニューを作成することができます。カスタムツールバーは、iPad、iPhone、Androidタブレットなどのモバイルデバイスからアクセスする際のWindowsアプリケーションの操作性を大幅に向上させます。
- **Mobile Sense:** GO-GlobalのMobile Sense技術により、Windowsアプリケーションはモバイルアプリケーションのように動作します。たとえば、フォーカスがあるアプリケーションウィンドウは、ユーザのデバイスの画面に合わせて自動的にサイズが調整され、Windowsアプリケーションがテキスト入力を受信できるようになると、キーボードが自動的に開きます。
- **Windows互換性保証:** Windows互換性保証では、更新プログラムがGO-Globalと互換性があることをGraphOnが確認するまで、管理者はWindows更新プログラムのインストールを自動的に延期することができます。この機能をサポートするために、GraphOnはマイクロソフトのWindowsUpdateサービスを継続的に監視し、新しいアップデートがないかどうかを確認しています。Microsoftが1つまたは複数のWindowsアップデートをリリースすると、GO-Globalは、新しくリリースされたWindowsアップデートがGO-Globalと互換性があることをGraphOnが確認するまで、影響を受けるGO-GlobalホストへのすべてのWindowsアップデートのインストールを一時停止します。更新プログラムに互換性がない場合、GO-Globalは、GO-GlobalがすべてのWindows更新プログラムのリリースと互換性のある更新プログラムを自動的にダウンロードしてインストールするまで、影響を受けるホストへのすべてのWindows更新プログラムのインストールを停止します。このプロセスにより、Windows互換性保証により非互換性のリスクを最小限に抑え、管理者はGO-GlobalホストでのWindowsアップデートの管理の負担を軽減することができます。
- **ライセンスの概要:** Admin Consoleのタブには、ホストで利用可能なGO-Globalのライセンスが一覧表示され、各ライセンスの製品コード、シート数、メンテナンスの有効期限、およびステータスが表示されます。また、GO-Globalは、ライセンスの有効期限が近づいている場合や期限を超えた場合に管理者に通知します(※2)。 
- **クラウドライセンス:** クラウドライセンスでは、GO-GlobalのFlexeraベースのライセンスファイルに代わるシンプルで可用性の高いライセンスを提供しております。クラウドライセンスでは、ライセンスサーバ、製品コード、ライセンスファイルの再発行、再ホスト、アップグレードの必要がありません。代わりに、管理者はホストのアクティベーションウィザードを実行し、GraphOnアカウントにサインインして、そのホストで使用するライセンスを選択するだけです。管理者はいつでもライセンスからホストを追加したり削除したりできます。ライセンスの同時使用ユーザ数を増やすには、ライセンスの追加シートを購入するだけです。新しく購入したシートは、ライセンスを使用するように設定されたホストに自動的に追加されます。クラウドライセンスは永続的またはサブスクリプションで、オンプレミスおよびクラウドベースのGO-Globalホストの両方で使用できます(※2)。
- **サードパーティのロードバランサーとのセッション再接続のサポート:** サードパーティのロードバランサーを介してGO-Globalホストのクラスタに接続するユーザは、セッションを一時停止および再開し、ネットワークが中断した後にセッションに再接続できます。ユーザがサードパーティのロードバランサを介してホストに接続し、その後切断された場合、ロードバランサがユーザのセッションが実行されているホストにユーザを接続できなくても、GO-Globalは自動的にユーザをホストに再接続します。たとえば、ホストAで実行中のセッションを持つユーザが切断された場合、ユーザのGO-Global AppControllerは、ロードバランサを介してホストAへの再接続を自動的に試行します。ロードバランサがホストBへの接続をルーティングする場合、ホストBはホストAへの接続を開き、GO-Global AppControllerとホストAの間でデータを中継します。この機能は、AppControllerが実行されている場合にのみサポートされます。ユーザがAppControllerを閉じるか、Program Windowの[Disconnect]オプションを介してホストから明示的に切断した場合、ロードバランサがユーザの後続の接続をユーザのホスト以外のホストにルーティングすると、ユーザは実行中のセッションに再接続できなくなります。(※1)
- **GO-Global Web App:** JavaScriptおよびHTML5で開発されたGO-Global Web Appは、インストール不要のクライアントで、ユーザはWindows、Mac、およびLinuxコンピュータ上の一般的なWebブラウザからWindowsアプリケーションを実行することができます。Webアプリでは、ローカルアプリケーションとリモートアプリケーション間のコピーアンドペースト、クライアント側のパスワードキャッシング、およびGO-GlobalのプレビューPDFプリンタを使用したローカルプリンタへの印刷をサポートしています。
- **GO-Global AppController：** GO-Global Appは、AppControllerと呼ばれるブランド化されていないカスタマイズ可能なアプリケーションとして再設計されました。AppControllerは、GO-Globalのネイティブクライアントとブラウザアドオンの機能を、コンピュータのデスクトップ、モバイルデバイス、またはWebブラウザから起動できる単一のアプリケーションに結合します。AppControllerは簡単なインストールを提供し、顧客自身の企業ブランドでパーソナライズできます(※2)。
- **強力な暗号化ウィザード：** Admin Consoleを使用して、管理者はGO-Globalホストの信頼できるSSL証明書を生成でき、サードパーティの認証局から証明書を購入することなく強力な暗号化とSSL/TLSセキュリティを有効にできます(※2)。
- **2要素認証：** 2要素認証は、ユーザ名とパスワードに加えて、ユーザがスマートフォンの認証アプリから6桁のコードを入力することをオプションで要求することにより、セキュリティの追加レイヤーを提供します(※2)。
- **ビデオサポート：** ビデオサポートが有効になっている場合、GO-Globalセッションで実行されているアプリケーションおよびWebブラウザは、ビデオコンテンツをGO-Globalクライアントにリダイレクトします(※2)。
- **URLリダイレクト：** この機能により、GO-Globalユーザは、ホストのデフォルトブラウザではなく、ユーザのクライアントのデフォルトブラウザで開くWebリンクをクリックできます。これにより、ユーザはGO-Globalセッションで実行されているWebコンテンツおよびビデオに効率的にアクセスできます(※2)。
- **ファイルオープンリダイレクト：** ファイルオープンリダイレクトは、エンドユーザがクライアントで実行されているアプリケーションでホスト上のファイルを開くことができるようにすることで、エンドユーザのワークフローを合理化します。管理者は、特定のファイルタイプ(PDF、TXT、DOCXなど)の機能を有効にして、このタイプのファイルがOutlookなどのホストアプリケーションから開かれると、AutoCADやExcelなどのアプリケーションのクライアントにリダイレクトされて開かれます(※2)。
- **エンドユーザのブランド化：** 管理者は、Admin Consoleのブランド化ダイアログを使用して、Program Window、サインインダイアログ、およびAppControllerインストールページで、GraphOnのGO-Globalブランドを独自の会社名と画像に置き換えることができます(※2)。

(※1) KitASPでサポートしていない機能になります。KitASPが開発した<GO-Global拡張パック>を利用することで、Webを利用した負荷分散処理を行うことも可能になります。<br>
(※2) GO-Global 6.1で追加された機能になります。





