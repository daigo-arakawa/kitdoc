---
title: "アプリケーションの管理"
linkTitle: ""
weight: 02
type: "docs"
---

Admin Consoleを使用すると、アプリケーションを公開して共有できます。

## アプリケーションのインストール

GO-Global を介して実行されるアプリケーションをインストールする場合、ベンダ提供の関連文書を参照して、適切なマルチユーザインストール方法を確認してください。ほとんどの場合、管理者アカウントでアプリケーションをインストールする必要がありますが、各アプリケーションによってインストール要件は異なります。またインストールは、マルチユーザ展開に関するMicrosoftのガイドラインに準拠する必要があります

>GO-Globalを介してアプリケーションを展開しても、各企業が無制限のアクセス権を取得することにはなりません。同時に実行できるアプリケーションの数に関しては、ベンダのライセンス供与規定に準拠する必要があります。

## アプリケーションの公開

アプリケーションはAdmin Consoleを使って公開されます。Admin Consoleを介してアプリケーションを公開するときに、アプリケーションの起動方法を制御する起動パラメータを指定できます。Interactive Quick Start Guideを実行するときは、プロンプトに従ってアプリケーションを公開してください。

### アプリケーションを公開する方法

1. [**All Hosts**]の一覧から、目的のホストを選択します。
2. [**Applications**]タブをクリックします。
3. [**Add**]ボタンをクリックします。
4. [**Location**]ボックスの横にある [**Browse**]ボタンをクリックして、アプリケーションの実行可能ファイルを見つけて選択します。
5. [**OK**]をクリックします。

![4-2-1](/img/4-2-1.png) 

デフォルトでは、ブラウズダイアログはPROGRAMDATA\Microsoft\Windows\Start Menu\Programsディレクトリに開きます。最初のアプリケーションを公開した後、ダイアログが最後に公開されたアプリケーションのディレクトリで開きます。

### アプリケーション名の変更

アプリケーションの .exeファイルを参照すると、そのファイル名が自動的に[Display Name]ボックス内に入力されます(アプリケーション名は Program Window に表示されます)。そのままデフォルトの表示名を使用することも、新しい名称を入力することも可能です。アプリケーションの表示名をスペースのみにすることはできません。また、バックスラッシュ(\)も使用できません。このフィールドは空欄のままにしないでください。

### アプリケーションアイコンの変更

アプリケーションのデフォルトアイコン以外のアイコンを選択する場合は、[]ボタンをクリックします。

### 起動状態の変更

[Startup State]セクションで、アプリケーションを最大化、最小化、通常モードのいずれで起動するかを選択します。デフォルトの起動状態は通常モードです。

### 開始ディレクトリの変更

アプリケーションの実行可能ファイルを参照した場合は、ディレクトリのパス名が自動的に[Start Directory]ボックスに表示されます。それ以外の場合は、アプリケーションを起動するディレクトリのフルパス名を入力します。

### コマンドラインオプションの指定

[Command-Line Options]ボックスで、アプリケーションの起動パラメータを指定できます。これらのパラメータは各アプリケーションに固有のものであるため、特定の起動パラメータについてはアプリケーションのドキュメントを参照してください。

## 公開アプリケーションへのリンクの共有

Admin Consoleの[Get Link]ボタンをクリックすると、選択したアプリケーションへのリンクをコピーしてユーザと共有し、そのアプリケーションにすばやくアクセスできます。

### アプリケーションリンクを共有する方法

1. インストールされている **アプリケーションのリスト**から、共有したいアプリケーションを選択します。
2. インストール済みアプリケーションのリストの右側にある[Get Link]ボタンをクリックします。
3. [Application Link]ダイアログで、[Copy]ボタンをクリックしてリンクをクリップボードにコピーします。
4. リンクを電子メールまたはインスタントメッセージに貼り付けて、ユーザと共有します。

![4-2-2](/img/4-2-2.png) 

>Admin Consoleがチュートリアルモードで実行されている場合、[Copy]ボタンをクリックすると、次のメッセージが表示されます。[Copy]をクリックしてこのリンクをクリップボードにコピーします。それを電子メールまたはインスタントメッセージに貼り付けて、ユーザと共有できます。

## ブラウザ外でのアプリケーションの実行

ユーザが公開アプリケーションへのリンクをクリックしてGO-Globalホストにサインインすると、アプリケーションが開き、Webブラウザの外部で実行されます。このデフォルト設定を無効にするには、[Run application outside the browser]のチェックを外します。これにより、パラメータ&embed = trueがURLに追加されます。このパラメータを追加してユーザがリンクをクリックすると、アプリケーションはユーザのWebブラウザ内で実行されます。

## ホストアドレスの編集

ホストアドレスは、GO-Global AppControllerまたはWeb Appがホストコンピュータへの接続に使用するアドレスを指定します。デフォルトでは、これはGO-Globalホストがインストールされているコンピュータの完全修飾ドメイン名です。クライアントが中継サーバまたはロードバランサを介してホストに接続する場合は、ホストアドレスを中継サーバまたはロードバランサの完全修飾ドメイン名に設定します。

### ホストアドレスを編集する方法

1. [Application Link]ダイアログで、[Host Address]ボックスにホストの完全修飾ドメイン名を入力します。アプリケーションリンクは自動的に更新されます。
2. [Copy]ボタンをクリックしてURLをコピーし、ユーザと共有します。

## Webサーバアドレスの編集

Webサーバアドレスは、GO-Global Web App、GO-Global AppController、それらをサポートするファイルをユーザのブラウザに提供するために使用されるWebサーバのアドレスを指定します。デフォルトのWebサーバアドレスはapps.graphon.comです。これは、GraphOnによってホストされているWebサーバのアドレスです。あなたがあなた自身のWebサーバを使うつもりならば、GO-Global WebコンポーネントをWebサーバにインストールし、WebサーバアドレスをあなたのWebサーバのアドレスに変更してください。たとえば、WebサーバがGO-Globalホストと同じコンピュータにインストールされている場合は、Webサーバアドレスとホストアドレスを同じアドレスに設定します。

### Webサーバのアドレスを編集する方法

1. [Application Link]ダイアログで、[Web Server Address]ボックスにWebサーバのアドレスを入力します。アプリケーションリンクは自動的に更新されます。
2. [Copy]ボタンをクリックしてURLをコピーし、ユーザと共有します。

>ユーザが内部ネットワークとパブリックネットワークの両方からホストにアクセスする場合、ホストとWebサーバは、[Host Address]フィールドと[Web Server Address]フィールドに指定されたアドレスを介して内部ネットワークとパブリックネットワークの両方からアクセスできる必要があります。これを実現するには、内部DNSエントリがホストアドレスとWebサーバアドレスをコンピュータの内部IPアドレスにマップし、パブリックDNSエントリがホストアドレスとWebサーバアドレスをこれらのコンピュータのパブリックIPアドレスにマップする必要があります。

## デフォルトリンクプロパティの設定

デフォルトのアプリケーションリンクプロパティを[Application Link]ダイアログボックスで指定したものに設定して、ホストアドレス、Webサーバアドレス、アプリケーションをブラウザの内部で実行するか外部で実行するかを含めることができます。これらのデフォルトのリンクプロパティは、新しいアプリケーションが公開されたときに適用されます。

### デフォルトのリンクプロパティを設定する方法

1. [Application Link]ダイアログで、[デフォルト設定]ボタンをクリックします。
2. [Yes]をクリックして確定します。

## アプリケーションの複製

アプリケーションの複製では、選択された登録済みアプリケーションの完全なコピーが作成されます。これは、同一のアプリケーションを異なるユーザやグループに対してさまざまな形で利用可能にする場合に便利です。たとえば、 [**Sign In**]ダイアログを表示しないコマンド行オプション付きの1つのバージョンのアプリケーションと、クライアントにサインインを要求するコマンド行オプションのない別のバージョンのアプリケーションを登録できます。アプリケーションを複製する場合には、新しい表示名を選択する必要があります。

### アプリケーションの複製方法

1. [**Installed Applications**]の一覧から複製するアプリケーションを選択します。
2. [Tools | Applications | Duplicate]の順にクリックします。

－または－

[Installed Applications]の一覧の右側にある [**Duplicate**]ボタンをクリックします。

## アプリケーション名の変更

アプリケーションに割り当てる表示名は、エンドユーザのProgram Windowに表示されます。アプリケーションの表示名は常時変更可能です。

### アプリケーションの表示名の変更方法

1. [Installed Applications]の一覧から名前を変更するアプリケーションを選択します。
2. [Tools | Applications | Rename]の順にクリックします。

－または－

　　[Installed Applications]の一覧の右側にある[**Rename**]ボタンをクリックします。
　　
3. [Rename Application]ダイアログの[New]ボックスに名前を入力します。

## アプリケーションのプロパティの編集

アプリケーションが公開されたら、いつでもアプリケーションのプロパティを編集できます。たとえば、アプリケーションのスタートアップ状態、実行可能ファイルの場所、アプリケーションを起動するフォルダの編集が可能です。

### アプリケーションのプロパティの編集方法

1. [**Applications**]タブをクリックします。
2. [**Installed Applications**]の一覧からアプリケーションを選択します。
3. [**Properties**]ボタンをクリックします。
4. 以下のいずれかの操作を行います
  - [**Executable Path**]ボックス内に、新しいパス名を入力します。
  - [**Start Directory**]ボックス内に、アプリケーションを起動するディレクトリのフルパス名を入力します。
  - [**Command-Line Options**]ボックス内に、そのアプリケーション用のスタートアップパラメータを入力します。
  - [**Display Name**]ボックス内に、そのアプリケーションの新しい表示名を入力します。
  - [**Startup State**]セクションで、そのアプリケーションの起動モード(Maximized、Minimized、Normal)を選択します。
  - [**Icon**]ボタンをクリックして、新しいアプリケーションアイコンを検索します。

![4-2-3](/img/4-2-3.png) 

## アプリケーションの削除

GO-Globalで展開したアプリケーションは、Admin Consoleで削除します。Admin Consoleでアプリケーションを削除しても、ホストからは削除されません。GO-Globalクライアントがそのアプリケーションにアクセスできなくなるだけです。

### アプリケーションの削除方法

1. [**Applications**]タブをクリックします。
2. [Installed Applications]の一覧から削除するアプリケーションを選択します。
3. [**Remove**]ボタンをクリックします。

－または－

　　[Tools | Applications | Remove]の順にクリックします。

Admin Consoleでインストール済みアプリケーションを削除する時に、あるユーザがそのアプリケーションを実行していた場合、そのユーザのセッションは中断されません。しかし、そのユーザがそのアプリケーションを終了すると、そのアプリケーションは利用不可能になり、Program Window内にアイコンは表示されません。

Admin Consoleへのアプリケーションの登録が完了すると、 [**Installed Applications**]の一覧にそのアプリケーション名とパス名が表示されます。カラムのタイトルをクリックすると、一覧内の項目を昇順または降順で並べ替えできます。Admin Console内の一覧はすべて、この方法で並べ替えできます。

ODBCデータソースを使用するアプリケーションを設定する場合は、GO-Globalクライアントがそのデータソースへアクセスできるよう、ODBCドライバをシステムDSNs(データソース名)として設定する必要があります。データソースに関する詳細情報は、Windows ODBC Data Source Administratorのオンラインヘルプを参照してください。

アクセス制限により、Admin ConsoleではUNCフォーマットで指定されたパス(例 : \Machine Name\Folder Name...)、またはマッピングされたネットワークドライブ上にあるパスの有効性を検証できません。公開された項目のExecutable PathまたはStart Directoryが、マッピングされたドライブを含むか、UNCパスで指定されている場合、Admin Consoleでは、それが有効であるか否かに関わらず、その指定パスを受け付けます。パスが無効な場合、またはクライアントユーザが指定された実行可能ファイルやフォルダへのアクセス権を持たない場合、公開された項目はProgram Windowに表示されません。その項目を選択して、 [**Properties**]ボタンをクリックします。そこで、その項目の[Executable Path]または [Start Directory]を更新します。その項目がアンインストールまたは新規の場所に移動されていると、Application Publishing Serviceが再開された後には、Admin Console内に表示されません。

Admin Consoleでは、UNCフォーマットで指定された、またはマッピングされたドライブにある任意の項目のパスに対するグループやユーザの設定は表示できません。これが当てはまる場合、任意のアプリケーションやファイルに対して、Cluster Managerの[Application Users/Groups]画面に「User/Group settings not available.(ユーザ/グループ設定は利用できません)」というメッセージが表示されます。

マッピングされたドライブ上に存在はしていてもGO-Globalでの利用ライセンスが供与されていない項目をAdmin Console内で公開すると、その項目のアイコンがProgram Windowに表示されます。しかし、ユーザはその項目をオープンすることはできず、起動するとエラーメッセージが表示されます。

>[Installed Applications]の一覧または[Application Users/Groups]の一覧内の項目上でマウスボタンを右クリックすると、最も頻繁に使用されるコマンドのショートカットメニューが表示されます。

## ユーザやグループに対するアプリケーション起動パラメータの割り当て

Admin Consoleでは、ネットワーク上またはローカルマシン上のユーザやグループに対するアプリケーションの実行方法を指定するパラメータの割り当てが可能です。ユーザやグループに対して設定されたパラメータは、ユーザやグループがそのアプリケーションを起動する度に適用されます。個人に対して設定されたアプリケーション起動パラメータは、グループやアプリケーションに対して設定されたパラメータより優先されます。クライアントがGO-Globalを介してアプリケーションを起動すると、Program Windowは、まず個別ユーザに対して割り当てられた起動パラメータを確認します。何もパラメータが割り当てられていない場合は、Program Windowがシステムから取得した順に、そのユーザが属するグループの一覧を確認します。または、Program Windowは、そのアプリケーションに割り当てられている一般的な起動パラメータを検索します。

>[**About GraphOn GO-Global**]ボックスで、ユーザが割り当てられているグループ、システムにおけるそのグループ一覧の順序を確認できます。

ユーザやグループ用のファイルアクセス許可は、サーバのWindows NTファイルシステム(NTFS)セキュリティ設定によって制御されます。ファイルアクセス許可は、Admin Consoleを通して設定することはできません。[Installed Applications]一覧からアプリケーションを選択すると、そのファイルやアプリケーション対してNTFSで指定されたユーザのアクセス許可が、[Application Users/Groups]一覧に表示されます。次に、特定のユーザやグループに対するアプリケーションのプロパティを編集できます。ファイルアクセス許可はNTFSで初期化されたドライブ上でのみ設定可能です。

### ユーザまたはグループに対するアプリケーション起動パラメータの割り当て方法

1. [**Applications**]タブをクリックします。
2. [**Installed Applications**]の一覧からアプリケーションを選択します。
3. [**Application Users/Groups**]の一覧からユーザまたはグループを選択します。
4. [**Properties**]ボタンをクリックします。
5. 以下のいずれかの操作を行います。
  - [**Start Directory**]ボックス内に、アプリケーションを起動するディレクトリ内のフル パス名を入力します。
  - [**Startup State**]セクションで、そのアプリケーションの起動モード (Maximized、Minimized、Normal) を選択します。
  - [**Command-Line Options**]ボックス内に、そのアプリケーションの起動時に使用するコマンド行引数を入力します。

![4-2-4](/img/4-2-4.png) 