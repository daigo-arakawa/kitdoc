---
title: "ファイルオープンリダイレクト"
linkTitle: ""
weight: 27
type: "docs"
---

ファイルオープンリダイレクトは、クライアントドライブ機能を補完します。これにより、ユーザは、ホストで実行されているアプリケーションでクライアント上のファイルを開くことができます。ファイルオープンリダイレクトを使用すると、ユーザは、クライアントで実行されているアプリケーションで、ホストまたはクライアントにあるファイルを開くことができます。ホストファイルリダイレクトはデフォルトで有効になっており、AppControllerがWindowsで実行されている場合にのみサポートされます。
クライアントでファイルを開く **[Open files on client]** オプションを使用すると、クライアントで実行されているアプリケーションで、ホストまたはクライアントにあるファイルを開くことができます。たとえば、ユーザがGO-Global経由でアプリケーションを実行していて、アプリケーションでサポートされていないファイル形式を開いた場合、GO-Globalはファイルをユーザのコンピュータに自動的にダウンロードし、ファイル形式をサポートするユーザのコンピュータ上のアプリケーションを使用してファイルを開きます。
**[Open files on client]** オプションは、オーディオファイル、ビデオファイル、テキストファイル、PDF、およびMicrosoft Officeファイルに対してデフォルトで有効になっています。この機能は、AppControllerがWindowsで実行されている場合にのみサポートされます。

![7-27-1](/img/7-27-1.png)

### Open files on clientを無効にする方法

1. Admin Consolで、**[All Hosts]** のリストから目的のホストを選択します。
2. [Tools | Host Options] を順にクリックします。
3. **[Client Access]** タブをクリックします。
4. **[Open files on client]** を無効にします。
5. **[OK]** をクリックします。

クライアントでファイルを開くことは、Windowsエクスプローラや、Windowsの **[プログラムから開く]** 機能を介してファイルを開くアプリケーションではサポートされていません。ユーザがGO-Globalセッションでエクスプローラを実行し、ファイルを右クリックして[開く]を選択すると、ファイルの種類が[ファイルの種類]ダイアログで選択されている場合でも、ホスト上のアプリケーションでファイルが開きます。

## URLリダイレクション 

URLリダイレクションでは、GO-Globalのユーザがホストのデフォルトブラウザではなく、ユーザのクライアントのデフォルトブラウザで開くWebリンクをクリックすることができます。これにより、ユーザはGO-Globalセッションで実行されているWebコンテンツや動画に効率的にアクセスすることができます。URLリダイレクトはデフォルトで有効になっています。

![7-27-2](/img/7-27-2.png)

### URLリダイレクトを無効にする方法

1. Admin Consolで、**[All Hosts]** のリストから目的のホストを選択します。
2. [Tools | Host Options] を順にクリックします。
3. **[Client Access]** タブをクリックします。
4. **[File Types]** ボタンをクリックします。
5. **[URLs (web links)]** を無効にします。
6. **[OK]** をクリックします。