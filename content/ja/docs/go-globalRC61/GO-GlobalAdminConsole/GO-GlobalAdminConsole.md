---
title: "GO-Global AdminConsole"
linkTitle: ""
weight: 01
type: "docs"
---
AdminConsoleでは、GO-Globalホストの管理、監視、GO-Globalホストへのクライアントアクセスの制御を行うことができます。AdminConsoleには、GO-Globalホストにサインインしているユーザのリストと、ユーザが実行しているアプリケーションが表示されます。AdminConsoleでは、アプリケーションの追加と削除、ユーザセッションの終了、ホスト上で実行されているプロセスの終了など、さまざまな管理タスクを実行できます。

### AdminConsoleにアクセスする方法
デスクトップ上のGO-Global Admin Consoleアイコンをダブルクリックします。もしくは

1. Windowsタスクバーの[スタート]ボタンをクリックします。
2. [GraphOn GO-Global｜AdminConsole］をクリックします。

AdminConsoleの左側のパネルには、Application Publishing Serviceを実行しているネットワーク上のホストの一覧が表示されます。デフォルトでは、Application Publishing Serviceには、自分のマシンで実行されているホストの情報が表示されます。他のホストに接続してホストの情報を表示するには、[GO-Global Hosts]の一覧からホスト名をクリックします。
ホストのアイコンに赤い X ![4-1-1](/img/4-1-1.png)が付いている場合、管理者はそのホストの管理者権限を持っていません。ホストのアイコンが赤×でグレー表示されている場合は、そのホストがApplication Publishing Serviceを実行していないか、オフになっています。いずれの場合も、管理者はAdminConsoleからそのホストにアクセスできません。AdminConsoleの左側パネルの［All Hosts]アイコンをクリックすると、ネットワーク上のすべてのアクティブなセッションのリストが表示されます。これにより、個々のホストに接続することなく、アクティブな GO-Globalセッションを表示することができます。また、特定のセッションのホストを検索するのにも便利です。
AdminConsoleからそのホストにアクセスするには、各GO-Globalホストの管理者グループに所属している必要があります。ホストの管理者権限がない場合、アプリケーションの追加やプロセスの終了などを行うことができません。

![4-1-2](/img/4-1-2.png)