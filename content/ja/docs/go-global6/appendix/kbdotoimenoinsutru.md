+++
title = "キーボードとIMEの追加インストール"
description = ""
weight = 7
+++

# キーボードとIMEの追加インストール

クライアントがホストとは異なるキーボードやIMEを使用する前に、それらをサポートするためのファイルをGO-Global Hostにインストールする必要があります。ほとんどの場合、レイアウトはオペレーティングシステムのインストール中にコピーされますが、東アジア言語と右から左へ表記される言語はコピーされません。

### Windows Server 2016 が稼動するサーバにキーボード レイアウトをインストールする方法

1. スタートメニューから[コントロールパネル]をクリックします。
2. **[言語]**タブをクリックします。
3. 希望する言語(および該当する場合は地域の変更)を選択して、[追加]をクリックします。


追加のファイルがあなたのマシンにコピーされます。OSのインストールCDまたはネットワーク共有名を提供する必要があります。新しい言語のサポートは再起動後に利用可能になります。

### Windows Server 2008 が稼動するサーバにキーボード レイアウトをインストールする方法

1. スタート メニューから **[コントロールパネル]**をクリックします。
2. **[地域と言語のオプション]**アイコンをダブルクリックします。
3. **[キーボードと言語]**タブをクリックします。[**キーボードの変更**]をクリックします。
4. **[テキストサービスと入力言語]**ウィンドウで、 **[追加]**ボタンをクリックして目的の言語を追加します。 **[入力言語の追加]**ウィンドウのチェックボックスをクリックして言語を選択します。
5. ****
6. **[テキストサービスと入力言語]**ウィンドウの **[適用]**ボタンをクリックします。
7. ****

以下に、各GO-Globalクライアントがサポートするキーボードの一覧を示します。

**Linuxクライアント**は以下をサポートします。

| Linux  キーボード レイアウト名                                                                | Linux  キーボード レイアウト | Windows  入力言語       | Windows  キーボード レイアウト名 | Windows  キーボード レイアウト | キーボード マッピング ファイル * |
|-----------------------------------------------------------------------------------------------|------------------------------|-------------------------|----------------------------------|--------------------------------|----------------------------------|
| U.S. English                                                                                  | us                           | 英語(米国)              | US                               | 00000409                       | us.kbm                           |
| Japanese                                                                                      | jp                           | 日本語                  | 日本語 (106/109  キー)           | E0010411 (IME)                 | jp.kbm                           |
| French                                                                                        | fr                           | フランス語 (フランス)   | フランス語                       | 0000040C                       | fr.kbm                           |
| Belgian  (be-latin1)                                                                          | be                           | フランス語 (ベルギー)   | フランス語 (ベルギー)            | 0000080C                       | be.kbm                           |
| German、 German(Latin1)、 German (Latin1 w/ no  dead keys)                                    | de                           | ドイツ語 (ドイツ)       | ドイツ語                         | 00000407                       | de.kbm                           |
| Polish                                                                                        | pl                           | ポーランド語            | ポーランド語  (214)              | 00010415                       | pl.kbm                           |
| Brazilian (ABNT2)                                                                             | br                           | ポルトガル語 (ブラジル) | ポルトガル語 (ブラジルABNT2)     | 00010416                       | br.kbm                           |
| *  詳細については、下の「クライアントキーボードのマッピングファイル」の項を参照してください。 |                                                                

**Mac OS Xクライアント**は以下をサポートします。

| Mac OS X  キーボード  レイアウト名                                                            | Windows  入力言語     | Windows  キーボード レイアウト名 | Windows  キーボード レイアウト | キーボード マッピング ファイル * |
|-----------------------------------------------------------------------------------------------|-----------------------|----------------------------------|--------------------------------|----------------------------------|
| U.S. English                                                                                  | 英語(米国)            | US-International                 | 00020409                       | us.kbm                           |
| French                                                                                        | フランス語 (フランス) | US-International                 | 00020409                       | fr.kbm                           |
| German                                                                                        | ドイツ語 (ドイツ)     | US-International                 | 00020409                       | de.kbm                           |
| *  詳細については、下の「クライアントキーボードのマッピングファイル」の項を参照してください。 |   

>Mac OS XキーボードとWindowsキーボードの物理的な違いにより、Mac OS Xキーボードマッピングファイルでは、米国国際Windowsキーボードレイアウトを使用して、キーの大部分をWindowsアプリケーションに変換しています。

Windowsクライアント(ネイティブのWindowsクライアント、ActiveXコントロール、およびプラグインを含む)は、GO-Globalホストにドライバがあるすべてのキーボードをサポートします。

## クライアントキーボードマッピングファイル

GO-Globalは、LinuxおよびMac OS X上のキーボードマッピングファイルを使用して、適切なキーボードレイアウトがホストにロードされ、正しいキーコードが各キーを押して放すたびに送信されるようにします。キーボードマッピングファイルを使用すると、新しいキーボードマッピングファイルをクライアントにコピーするだけで、新しいキーボードのサポートを追加できます。キーボードマッピングファイルは、Linuxの/ etc / gg-client / kbdディレクトリとMacの/ etc / GO-Global / kbdディレクトリにインストールされています。キーボードマッピングファイルが見つからない場合は、us.kbmキーボードマッピングファイルの内部バージョンが使用されます。

これらのクライアントは、オペレーティングシステムから取得した情報に基づいてキーボードマッピングファイルを自動的に読み込むことができます。

キーボードマッピングファイルのインストール場所(デフォルトのルートパス)

| クライアント OS | ネイティブ インストール | Browser Plug-in  インストール | デフォルト レイアウト | レイアウトの取得                  |
|-----------------|-------------------------|-------------------------------|-----------------------|-----------------------------------|
| Linux           | /etc/ggw/kbd            | ~/.mozilla/ggw/kbd            | U.S. English          | 環境変数、または OSから自動で取得 |
| Mac OS X        | /etc/ggw/kbd            | /etc/ggw/kbd                  | U.S.                  | 環境変数、または OSから自動で取得 |

## GO-Globalで使用されるキーボード/ IME識別子

GO-Globalは、まとめてGO-Global Input Identifier(GGII)と呼ばれる2つの識別子を使用して、セッションのキーボード/IMEを指定します。最初のキーボードレイアウトです。これらは、WindowsオペレーティングシステムがキーボードドライバとIMEプログラムをロードするために使用する8桁の文字列識別子です。これらはロケールIDと似ていますが、最後の4桁は通常、キーボードでサポートされている言語の4桁のロケールIDと一致します。IMEを指定するキーボードレイアウトは、通常「E」で始まります。使用可能なキーボードレイアウトの一覧は、[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\ Keyboard\Layouts]キーの下のレジストリに表示されます。

GO-Globalが使用する2番目の識別子はレイアウトテキスト文字列です。これは、各キーボードレイアウトレジストリキーのレジストリ値です。これらの文字列は、入力言語を追加するときにキーボードレイアウト/IMEの下のドロップダウンボックスに表示されます。次の例では、最初のキーボードレイアウトGGIIは00000409、レイアウトテキストGGIIはUSです。2番目の例では、キーボードレイアウトGGIIがE0010411で、レイアウトテキストGGIIが日本語入力システム(MS-IME2002)です。

例：

```
HKEY_LOCAL_MACHINE \ SYSTEM \ CurrentControlSet \ Control \ Keyboard Layouts \ 00000409  
Layout File = KBDUS.DLL  
Layout Text  = US
```

```
HKEY_LOCAL_MACHINE \ SYSTEM \ CurrentControlSet \ Control \ Keyboard Layouts \ E0010411  
Ime File = name81.name  
Layout File = Kbdjpn.dll  
Layout Text = Japanese Input System（MS-IME2002）
```

| 環境変数          | 説明                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GGW_KBD_FILE      | 使用するマッピングファイルの完全修飾パスの指定に使用されます。指定すると、他のあらゆるファイル名パスの取得方法に優先します。例 : Linuxの場合 GGW_KBD_FILE=/home/someuser/KeyMappingFiles/MyCustomKeyMappingFile.kmfと指定すると、正しいファイルがロードされます。このファイルが見つからない場合は、us.kbm キーボードマッピングファイルの内部バージョンが使用されます。                                                                                                                                                                                                                                                                                                                                      |
| GGW_KBD_FILE_ROOT | キーボードマッピングファイルへのルートパス名の指定に使用されます。キーボードマッピングファイルを含むkbdディレクトリは、このディレクトリに置きます。例:Linuxの場合、GGW_KBD_FILE_ROOT=/home/someuserと指定すれば、/home/someuser/kbd/xxx.kbmファイルがロードされます。「xxx」は、次に説明するGGW_KBD_FILE_LAYOUT 環境変数から、または直接オペレーティングシステムから取得されたLAYOUTを示します。                                                                                                                                                                                                                                                                                                            |
| GGW_KBD_LAYOUT    | どのLAYOUT(またはファイル名のプレフィックス)を使用するかの指定に使用されます。このLAYOUT名に拡張子.kbmが付いたものがファイル名として使用されます。例:GGW_KBD_LAYOUT=MyCustomKeyMappingFile と指定すれば、/ect/ggw/kbd/MyCustomKeyMappingFile.kbmファイルがロードされます。上に説明したGGW_KBD_FILE_ROOTも使用されている場合は、/home/someuser/kbd/MyCustomKeyMappingFile.kbmファイルがロードされます。マッピングファイルへのルートパス名のサブディレクトリを、ここに含めることもできます。例:GGW_KBD_LAYOUT=thinclient/usと指定すれば、別のルートパスが指定されていないかぎり、/etc/ggw/kbd/thinclient/us.kbmファイルがロードされます。これは、オペレーティングシステムから自動取得したLAYOUTに優先します。 |

## クライアントキーボードオプションの設定

-kbショートカットパラメータまたは「キーボード」ハイパーリンクパラメータを使用して、セッションのキーボード/IMEを指定できます。これらは上記の両方のタイプのGGIIを取ります。Windowsコンピュータでは、-kbショートカットパラメータが指定されていない場合、GO-Globalは現在アクティブなキーボードレイアウトのレイアウトテキストを使用します。Linuxコンピュータでは、コマンドラインでレイアウトテキストが指定されていない場合、GO-Globalはレイアウトテキストをサーバに送信しません。

例：キーボードレイアウトを使用したWindowsショートカット

## レイアウトテキスト置換の指定

クライアントとサーバーのキーボードレイアウト名をマッピングするために、サーバー上でレイアウトテキストの置換を指定できます。それらを使用することができます：

1. 異なるバージョンのWindowsでのレイアウトテキスト名の違いを克服します。たとえば、Windows 2000のGO-Globalクライアントシステムの **日本語入力システム(MS-IME2000)**レイアウトテキストは、GO-Globalホストの **日本語入力システム(MS IME2002)**レイアウトテキストに置き換えることができます。
2. UNICODE名を持つキーボードレイアウトをANSI名に置き換えます。たとえば、ASCII HTMLページで「keyboard」アプレットパラメータを使用してUNICODE名でキーボードレイアウトを指定するときは、UNICODE名の代わりにASCII名を使用する必要があります。

キーボードレイアウトの置換は、[HKEY_LOCAL_MACHINE\SOFTWARE\GraphOn\GO-Global\System\ Keyboard\Layout\Substitutes]レジストリキーで指定されています。このキー内の各REG_SZ値はGGIIの名前を持ち、値はクライアント名の代わりに使用されるべきサーバからのレイアウトテキストの名前です。

## 代替レイアウトテキストの設定

クライアントからGGIIが指定されていない場合、または指定されたGGIIが有効なキーボードレイアウトをロードできない場合、GO-Globalホストはフォールバックメカニズムを使用してセッションに使用するキーボードレイアウトを決定します。代替レイアウトテキストは、有効なGGIIを渡すクライアントを除いて、サーバに接続しているすべてのクライアントによって使用されるキーボードレイアウトのレイアウトテキストです。アクティブなキーボードレイアウトがIMEの場合、代替レイアウトテキストはインストール中に自動的に設定されます。インストール後に、次のレジストリキーの下にある **Fallback Layout Text**の値を編集して変更することができます。

>中国語のGO-Globalホストに接続すると、ショートカットから[**サインイン**]ダイアログが、デフォルト言語として中国語を指定しているIMEバーと共に表示されます。Ctrl+スペースバーをクリックしても言語は切り替わりません。ユーザは手動で英語を選択するためにマウスポインタでIMEバーをクリックする必要があります。IMEバーを手動でクリックしないと、ユーザはユーザ名とパスワードを入力できません。

## 複数の入力ロケールの設定

**デフォルトユーザ**アカウントプロファイルは、異なる入力ロケールまたは複数の入力ロケール、あるいはその両方で構成できます。 GO-Globalホストにログオンする新規ユーザのアカウントロファイルは、 **デフォルトユーザ**アカウントの入力ロケールで自動的に設定されます。ユーザは、自分のアカウントプロファイルで定義されている任意の入力ロケールに切り替えることができます。

>移動ユーザプロファイルまたは既にGO-Globalホストに存在するプロファイルを持つユーザは、これらの新しい設定を受け取りません。これらのアカウントは手動で設定する必要があります。

例として、次の手順では英語のWindows Server 2016にドイツ語の入力ロケールをインストールして使用する方法について説明します。

1. **英語版のWindows Server 2016でドイツ語を有効にします。**
  1.1 入力ローカルを設定したいユーザアカウントでGO-Globalホストに対話的にサインインします。
  1.2 [スタート | コントロールパネル | 地域の言語オプション]をクリック
  1.3 **言語**タブをクリックします。
  1.4 ドイツ語を選択し、開くをクリックします。
  1.5 地域の変更としてDeutsch(Deutschland)を選択し、Addをクリックします。
2. **入力ロケールが正しくインストールおよび構成されていることを確認してください。**
  2.1 この対話型セッションで **メモ帳**を起動します。
  2.2 英語で数文字を入力してください。
  2.3 左Alt + Shiftを押します。
  2.4 数文字を入力して、それらがドイツ語で表示されることを確認します。

これで、ドイツ語の入力ロケールが、 **デフォルトユーザ**プロファイルと、ステップ1.1でシステムにログオンしたユーザに対して有効になります。

3.GO-Globalセッション中に入力ロケールを切り替えます。
    3.1 GO-Globalクライアントを起動し、手順1.1で使用したアカウントでサーバに接続します。
    3.2 メモ帳を起動します。
    3.3 英語で数文字を入力してください。
    3.4 左Alt + Shiftを押します。
    3.5 数文字を入力して、それらがドイツ語で表示されることを確認します。

>サインインダイアログが表示されているときは、ユーザは入力ロケールを切り替えることができません。 GO-Global **ホスト**のデフォルト言語の入力ロケールが使用されます。
>
>Windowsクライアントでは、サーバベースのアプリケーションの選択された入力ロケールは、クライアントコンピュータのシステムトレイに表示されません。