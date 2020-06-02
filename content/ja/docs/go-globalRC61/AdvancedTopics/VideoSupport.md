---
title: "ビデオサポート"
linkTitle: ""
weight: 26
type: "docs"
---

ビデオサポートが有効になっている場合、GO-Globalセッションで実行されているアプリケーションおよびWebブラウザは、ビデオコンテンツをGO-Globalクライアントにリダイレクトします。ビデオサポートはデフォルトで無効になっています。

管理者は、DefaultWorkspaceProperties.xmlのH264VideoプロパティID値を編集することにより、ビデオサポートを有効にできます。デフォルトでは、H264Videoプロパティは0に設定されており、ショートカットに追加されたコマンドライン引数や、ログオンHTMLページを開くハイパーリンクに関係なく、ビデオのサポートが無効になります。H264Videoを1に設定すると、コマンドライン引数に関係なくビデオサポートが有効になります。H264Videoが2に設定されている場合、ショートカットに-videoが追加されるか、ハイパーリンクにvideo = 1が追加されない限り、ビデオは無効になります。H264Videoが3に設定されている場合、ショートカットに-novideoが追加されているか、ハイパーリンクにvideo = 0が追加されていない限り、ビデオは有効です。

H264Videoプロパティが2に設定されている場合、ユーザはコマンドライン引数-videoをGO-Globalショートカットに追加することにより、ビデオサポートを有効にできます。たとえば、"C:\Program Files\GraphOn\AppController\AppController.exe" -h server1 -videoです。H264Videoプロパティが3に設定されている場合、ビデオサポートを無効にするには、ショートカットに-novideoを追加します。

### ビデオのサポートを有効/無効にする方法

1. Application Publishing Serviceを停止します。
2. DefaultWorkspaceProperties.xmlファイルをC:\ProgramData\GraphOn\GO-Globalディレクトリ内に配置してください。
3. WordpadでDefaultWorkspaceProperties.xmlを開き、次のセクションを探します。
</property> 
<property type="UINT32" group="Miscellaneous" id="H264Video">
<value>0</value> 
</property>
4. 0 を希望の値に置き換えます。(例：1、2、または3)
5. 編集した.xmlファイルを保存します。
6. Application Publishing Serviceを起動します。

ビデオサポートは、GO-Global AppControllerログオンページにvideo = 1またはvideo = 0を追加することで有効または無効にすることもできます。
例えば：
http://hostname/goglobal/?video=1は、H264Videoワークスペースプロパティが2に設定されている場合にビデオサポートを有効にします。
http://hostname/goglobal/?video=0は、H264Videoワークスペースプロパティが3に設定されている場合にビデオサポートを無効にします。

