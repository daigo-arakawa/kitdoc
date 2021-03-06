---
title: "アプリケーションの管理"
linkTitle: ""
weight: 02
type: "docs"
---

Admin Consoleを使用すると、アプリケーションを公開して共有できます。

## アプリケーションのインストール

GO-Global を介して実行されるアプリケーションをインストールする場合、ベンダ提供の関連文書を参照して、適切なマルチユーザインストール方法を確認してください。ほとんどの場合、管理者アカウントでアプリケーションをインストールする必要がありますが、各アプリケーションによってインストール要件は異なります。またインストールは、マルチユーザ展開に関するMicrosoftのガイドラインに準拠する必要があります

{{% alert title="参照" color="info" %}}
GO-Globalを介してアプリケーションを展開しても、各企業が無制限のアクセス権を取得することにはなりません。同時に実行できるアプリケーションの数に関しては、ベンダのライセンス供与規定に準拠する必要があります。
{{% /alert %}}

## アプリケーションの公開

アプリケーションはAdmin Consoleを使って公開されます。Admin Consoleを介してアプリケーションを公開するときに、アプリケーションの起動方法を制御する起動パラメータを指定できます。**Interactive Quick Start Guide** を実行するときは、プロンプトに従ってアプリケーションを公開してください。

### アプリケーションを公開する方法

1. **[All Hosts]** の一覧から、目的のホストを選択します。

![kit4-30-1](/img/kit4-30-1.png)

2. **[Applications]** タブをクリックします。
3. **[Add]** ボタンをクリックします。

![kit4-30-2](/img/kit4-30-2.png)

4. **[Location]** ボックスの横にある **[Browse]** ボタンをクリックして、アプリケーションの実行可能ファイルを見つけて選択します。

![kit4-30-3](/img/kit4-30-3.png)
![kit4-30-4](/img/kit4-30-4.png)

5. **[OK]** をクリックします。

![kit4-30-5](/img/kit4-30-5.png)<br>
![kit4-30-6](/img/kit4-30-6.png)

![4-2-1](/img/4-2-1.png) 

デフォルトでは、ブラウズダイアログは`PROGRAMDATA\Microsoft\Windows\Start Menu\Programs`ディレクトリに開きます。最初のアプリケーションを公開した後、ダイアログが最後に公開されたアプリケーションのディレクトリで開きます。

### アプリケーション名の変更

アプリケーションの .exeファイルを参照すると、そのファイル名が自動的に **[Name]** ボックス内に入力されます(アプリケーション名は Program Windowに表示されます)。そのままデフォルトの表示名を使用することも、新しい名称を入力することも可能です。アプリケーションの表示名をスペースのみにすることはできません。また、バックスラッシュ( \ )も使用できません。このフィールドは空欄のままにしないでください。

### アプリケーションアイコンの変更

アプリケーションのデフォルトアイコン以外のアイコンを選択する場合は、**[Icon]** ボタンをクリックします。

### 起動状態の変更

[Startup State]セクションで、アプリケーションを最大化、最小化、通常モードのいずれで起動するかを選択します。デフォルトの起動状態は通常モードです。

### 開始ディレクトリの変更

アプリケーションの実行可能ファイルを参照した場合は、ディレクトリのパス名が自動的に **[Start Directory]** ボックスに表示されます。それ以外の場合は、アプリケーションを起動するディレクトリのフルパス名を入力します。

### コマンドラインオプションの指定

**[Command-Line Options]** ボックスで、アプリケーションの起動パラメータを指定できます。これらのパラメータは各アプリケーションに固有のものであるため、特定の起動パラメータについてはアプリケーションのドキュメントを参照してください。

## 公開アプリケーションへのリンクの共有

Admin Consoleの **[Get Link]** ボタンをクリックすると、選択したアプリケーションへのリンクをコピーしてユーザと共有し、そのアプリケーションにすばやくアクセスできます。

### アプリケーションリンクを共有する方法

1. **Installed Applications** のリストから、共有したいアプリケーションを選択します。
2. インストール済みアプリケーションのリストの右側にある **[Get Link]** ボタンをクリックします。

![kit4-32-1](/img/kit4-32-1.png)
![kit4-32-2](/img/kit4-32-2.png)

3. **[Application Link]** ダイアログで、**[Copy]** ボタンをクリックしてリンクをクリップボードにコピーします。

![kit4-32-3](/img/kit4-32-3.png)

4. リンクを電子メールまたはインスタントメッセージに貼り付けて、ユーザと共有します。

![4-2-2](/img/4-2-2.png) 

{{% alert title="参照" color="info" %}}
Admin Consoleがチュートリアルモードで実行されている場合、**[Copy]** ボタンをクリックすると、次のメッセージが表示されます。**[Copy]** をクリックしてこのリンクをクリップボードにコピーします。それを電子メールまたはインスタントメッセージに貼り付けて、ユーザと共有できます。
{{% /alert %}}

## ブラウザ外でのアプリケーションの実行

ユーザが公開アプリケーションへのリンクをクリックしてGO-Globalホストにサインインすると、アプリケーションが開き、Webブラウザの外部で実行されます。このデフォルト設定を無効にするには、**[Run application outside the browser]** のチェックを外します。これにより、パラメータ **&embed=true** がURLに追加されます。このパラメータを追加してユーザがリンクをクリックすると、アプリケーションはユーザのWebブラウザ内で実行されます。

## ホストアドレスの編集

**ホストアドレス** は、GO-Global AppControllerまたはWeb Appがホストコンピュータへの接続に使用するアドレスを指定します。デフォルトでは、これはGO-Globalホストがインストールされているコンピュータの完全修飾ドメイン名です。クライアントがロードバランサ(GO-Global Relay Load Balancerやthird-party load balancerなど)を介してホストに接続する場合は、**ホストアドレス** を完全修飾ドメイン名に設定します。

### ホストアドレスを編集する方法

1. **[Application Link]** ダイアログで、**[Host Address]** ボックスにホストの完全修飾ドメイン名を入力します。アプリケーションリンクは自動的に更新されます。

![kit4-32-4](/img/kit4-32-4.png)
![kit4-32-5](/img/kit4-32-5.png)

2. **[Copy]** ボタンをクリックしてURLをコピーし、ユーザと共有します。

![kit4-32-6](/img/kit4-32-6.png)
![kit4-32-7](/img/kit4-32-7.png)

## Webサーバアドレスの編集

**Webサーバアドレス** は、GO-Global Web App、GO-Global AppController、それらをサポートするファイルをユーザのブラウザに提供するために使用されるWebサーバのアドレスを指定します。デフォルトのWebサーバアドレスは**apps.graphon.com** です。これは、GraphOnによってホストされているWebサーバのアドレスです。あなたがあなた自身のWebサーバを使うつもりならば、GO-Global WebコンポーネントをWebサーバにインストールし、**Webサーバアドレス** をあなたのWebサーバのアドレスに変更してください。たとえば、WebサーバがGO-Globalホストと同じコンピュータにインストールされている場合は、**Webサーバアドレス** と**ホストアドレス** を同じアドレスに設定します。

### Webサーバのアドレスを編集する方法

1. **[Application Link]** ダイアログで、**[Web Server Address]** ボックスにWebサーバのアドレスを入力します。アプリケーションリンクは自動的に更新されます。

![kit4-32-8](/img/kit4-32-8.png)
![kit4-32-9](/img/kit4-32-9.png)

2. **[Copy]** ボタンをクリックしてURLをコピーし、ユーザと共有します。

![kit4-32-10](/img/kit4-32-10.png)
![kit4-32-11](/img/kit4-32-11.png)

{{% alert title="参照" color="info" %}}
ユーザが内部ネットワークとパブリックネットワークの両方からホストにアクセスする場合、ホストとWebサーバは、**[Host Address]** フィールドと **[Web Server Address]** フィールドに指定されたアドレスを介して内部ネットワークとパブリックネットワークの両方からアクセスできる必要があります。これを実現するには、内部DNSエントリが **ホストアドレス** と **Webサーバアドレス** をコンピュータの内部IPアドレスにマップし、パブリックDNSエントリが **ホストアドレス** と **Webサーバアドレス** をこれらのコンピュータのパブリックIPアドレスにマップする必要があります。
{{% /alert %}}

## デフォルトリンクプロパティの設定

デフォルトのアプリケーションリンクプロパティを **[Application Link]** ダイアログボックスで指定したものに設定して、ホストアドレス、Webサーバアドレス、アプリケーションをブラウザの内部で実行するか外部で実行するかを含めることができます。これらのデフォルトのリンクプロパティは、新しいアプリケーションが公開されたときに適用されます。

### デフォルトのリンクプロパティを設定する方法

1. **[Application Link]** ダイアログで、 **[Set defaults]** ボタンをクリックします。

![kit4-32-12](/img/kit4-32-12.png)
![kit4-32-13](/img/kit4-32-13.png)

2. **[Yes]** をクリックして確定します。

![kit4-32-14](/img/kit4-32-14.png)
![kit4-32-15](/img/kit4-32-15.png)

## アプリケーションの複製

アプリケーションの複製では、選択された登録済みアプリケーションの完全なコピーが作成されます。これは、同一のアプリケーションを異なるユーザやグループに対してさまざまな形で利用可能にする場合に便利です。たとえば、 **[Sign In]** ダイアログを表示しないコマンド行オプション付きの1つのバージョンのアプリケーションと、クライアントにサインインを要求するコマンド行オプションのない別のバージョンのアプリケーションを登録できます。アプリケーションを複製する場合には、新しい表示名を選択する必要があります。

### アプリケーションの複製方法

1. **[Installed Applications]** の一覧から複製するアプリケーションを選択します。

![kit4-33-1](/img/kit4-33-1.png)
![kit4-33-2](/img/kit4-33-2.png)

2. [Tools | Applications | Duplicate]の順にクリックします。

![kit4-33-3](/img/kit4-33-3.png)
![kit4-33-4](/img/kit4-33-4.png)

－または－

[Installed Applications]の一覧の右側にある **[Duplicate]** ボタンをクリックします。

![kit4-33-5](/img/kit4-33-5.png)

## アプリケーション名の変更

アプリケーションに割り当てる表示名は、エンドユーザのProgram Windowに表示されます。アプリケーションの表示名は常時変更可能です。

### アプリケーションの表示名の変更方法

1. **[Installed Applications]** の一覧から名前を変更するアプリケーションを選択します。

![kit4-33-6](/img/kit4-33-6.png)
![kit4-33-7](/img/kit4-33-7.png)

2. [Tools | Applications | Rename]の順にクリックします。

![kit4-33-8](/img/kit4-33-8.png)
![kit4-33-9](/img/kit4-33-9.png)

－または－

[Installed Applications]の一覧の右側にある **[Rename]** ボタンをクリックします。<br>

![kit4-33-10](/img/kit4-33-10.png)

3. **[Rename Application]** ダイアログの **[New]** ボックスに名前を入力します。

![kit4-33-11](/img/kit4-33-11.png)
![kit4-33-12](/img/kit4-33-12.png)

## アプリケーションのプロパティの編集

アプリケーションが公開されたら、いつでもアプリケーションのプロパティを編集できます。たとえば、アプリケーションのスタートアップ状態、実行可能ファイルの場所、アプリケーションを起動するフォルダの編集が可能です。

### アプリケーションのプロパティの編集方法

1. **[Applications]** タブをクリックします。

![kit4-33-13](/img/kit4-33-13.png)

2. **[Installed Applications]** の一覧からアプリケーションを選択します。

![kit4-33-14](/img/kit4-33-14.png)

3. **[Properties]** ボタンをクリックします。

![kit4-33-15](/img/kit4-33-15.png)

4. 以下のいずれかの操作を行います
  - **[Executable Path]** ボックス内に、新しいパス名を入力します。
  - **[Start Directory]** ボックス内に、アプリケーションを起動するディレクトリのフルパス名を入力します。
  - **[Command-Line Options]** ボックス内に、そのアプリケーション用のスタートアップパラメータを入力します。
  - **[Display Name]** ボックス内に、そのアプリケーションの新しい表示名を入力します。
  - **[Startup State]** セクションで、そのアプリケーションの起動モード(Maximized、Minimized、Normal)を選択します。
  - **[Icon]** ボタンをクリックして、新しいアプリケーションアイコンを検索します。

![4-2-3](/img/4-2-3.png) 

## アプリケーションの削除

GO-Globalで展開したアプリケーションは、Admin Consoleで削除します。Admin Consoleでアプリケーションを削除しても、ホストからは削除されません。GO-Globalクライアントがそのアプリケーションにアクセスできなくなるだけです。

### アプリケーションの削除方法

1. **[Applications]** タブをクリックします。

![kit4-34-1](/img/kit4-34-1.png)

2. [Installed Applications]の一覧から削除するアプリケーションを選択します。

![kit4-34-2](/img/kit4-34-2.png)

3. **[Remove]** ボタンをクリックします。

![kit4-34-3](/img/kit4-34-3.png)
![kit4-34-4](/img/kit4-34-4.png)
![kit4-34-5](/img/kit4-34-5.png)

－または－

　　[Tools | Applications | Remove]の順にクリックします。

![kit4-34-6](/img/kit4-34-6.png)

Admin Consoleでインストール済みアプリケーションを削除する時に、あるユーザがそのアプリケーションを実行していた場合、そのユーザのセッションは中断されません。しかし、そのユーザがそのアプリケーションを終了すると、そのアプリケーションは利用不可能になり、Program Window内にアイコンは表示されません。

Admin Consoleへのアプリケーションの登録が完了すると、 **[Installed Applications]** の一覧にそのアプリケーション名とパス名が表示されます。カラムのタイトルをクリックすると、一覧内の項目を昇順または降順で並べ替えできます。Admin Console内の一覧はすべて、この方法で並べ替えできます。

ODBCデータソースを使用するアプリケーションを設定する場合は、GO-Globalクライアントがそのデータソースへアクセスできるよう、ODBCドライバをシステムDSNs(データソース名)として設定する必要があります。データソースに関する詳細情報は、Windows ODBC Data Source Administratorのオンラインヘルプを参照してください。

アクセス制限により、Admin ConsoleではUNCフォーマットで指定されたパス(例:\Machine Name\Folder Name...)、またはマッピングされたネットワークドライブ上にあるパスの有効性を検証できません。公開された項目の **Executable Path** または **Start Directory** が、マッピングされたドライブを含むか、UNCパスで指定されている場合、Admin Consoleでは、それが有効であるか否かに関わらず、その指定パスを受け付けます。パスが無効な場合、またはクライアントユーザが指定された実行可能ファイルやフォルダへのアクセス権を持たない場合、公開された項目はProgram Windowに表示されません。その項目を選択して、 **[Properties]** ボタンをクリックします。そこで、その項目の[Executable Path]または [Start Directory]を更新します。その項目がアンインストールまたは新規の場所に移動されていると、Application Publishing Serviceが再開された後には、Admin Console内に表示されません。

Admin Consoleでは、UNCフォーマットで指定された、またはマッピングされたドライブにある任意の項目のパスに対するグループやユーザの設定は表示できません。これが当てはまる場合、任意のアプリケーションやファイルに対して、Cluster Managerの[Application Users/Groups]画面に「User/Group settings not available.(ユーザ/グループ設定は利用できません)」というメッセージが表示されます。

マッピングされたドライブ上に存在はしていてもGO-Globalでの利用ライセンスが供与されていない項目をAdmin Console内で公開すると、その項目のアイコンがProgram Windowに表示されます。しかし、ユーザはその項目をオープンすることはできず、起動するとエラーメッセージが表示されます。

{{% alert title="参照" color="info" %}}
[Installed Applications]の一覧または[Application Users/Groups]の一覧内の項目上でマウスボタンを右クリックすると、最も頻繁に使用されるコマンドのショートカットメニューが表示されます。
{{% /alert %}}

## ユーザやグループに対するアプリケーション起動パラメータの割り当て

Admin Consoleでは、ネットワーク上またはローカルマシン上のユーザやグループに対するアプリケーションの実行方法を指定するパラメータの割り当てが可能です。ユーザやグループに対して設定されたパラメータは、ユーザやグループがそのアプリケーションを起動する度に適用されます。個人に対して設定されたアプリケーション起動パラメータは、グループやアプリケーションに対して設定されたパラメータより優先されます。クライアントがGO-Globalを介してアプリケーションを起動すると、Program Windowは、まず個別ユーザに対して割り当てられた起動パラメータを確認します。何もパラメータが割り当てられていない場合は、Program Windowがシステムから取得した順に、そのユーザが属するグループの一覧を確認します。または、Program Windowは、そのアプリケーションに割り当てられている一般的な起動パラメータを検索します。

{{% alert title="参照" color="info" %}}
**[About GraphOn GO-Global]** ボックスで、ユーザが割り当てられているグループ、システムにおけるそのグループ一覧の順序を確認できます。
{{% /alert %}}

ユーザやグループ用のファイルアクセス許可は、サーバのWindows NTファイルシステム(NTFS)セキュリティ設定によって制御されます。ファイルアクセス許可は、Admin Consoleを通して設定することはできません。[Installed Applications]一覧からアプリケーションを選択すると、そのファイルやアプリケーション対してNTFSで指定されたユーザのアクセス許可が、[Application Users/Groups]一覧に表示されます。次に、特定のユーザやグループに対するアプリケーションのプロパティを編集できます。ファイルアクセス許可はNTFSで初期化されたドライブ上でのみ設定可能です。

### ユーザまたはグループに対するアプリケーション起動パラメータの割り当て方法

1. **[Applications]** タブをクリックします。

![kit4-35-1](/img/kit4-35-1.png)

2. **[Installed Applications]** の一覧からアプリケーションを選択します。

![kit4-35-2](/img/kit4-35-2.png)

3. **[Application Users/Groups]** の一覧からユーザまたはグループを選択します。

![kit4-35-3](/img/kit4-35-3.png)

4. **[Properties]** ボタンをクリックします。

![kit4-35-4](/img/kit4-35-4.png)

5. 以下のいずれかの操作を行います。
  - **[Start Directory]** ボックス内に、アプリケーションを起動するディレクトリ内のフル パス名を入力します。
  - **[Startup State]** セクションで、そのアプリケーションの起動モード (Maximized、Minimized、Normal) を選択します。
  - **[Command-Line Options]** ボックス内に、そのアプリケーションの起動時に使用するコマンド行引数を入力します。

![4-2-4](/img/4-2-4.png) 

{{% alert title="情報" color="green" %}}
ユーザやグループごとにアプリケーションを公開、非公開にする設定はWindowsのOSレベルでアプリケーションのアクセス許可を行います。グループ単位で許可を行う場合は事前にユーザグループを作成して以下の情報を参照してください。<br>
KGTN 2010121602<br>
[GGW3.2.1/GGH4.X/GGH5.X] アプリケーションを利用できるユーザーを限定したい。<br>
KGTN 2016062301<br>
[GGH4.X-5.X] 特定ユーザーまたは特定クライアントに限り、アプリケーションを利用出来るようにする設定はあるのか？<br>
KGTN 2016081801<br>
[GGH5.X] 特定ユーザーに対してアプリケーションのアイコンを表示しない方法は？<br>
{{% /alert %}}

