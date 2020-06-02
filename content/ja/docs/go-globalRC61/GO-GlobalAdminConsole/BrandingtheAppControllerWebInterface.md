# GO-Globlal AppController Web Interfaceのブランディング

AppControllerは、コンピュータのデスクトップ、モバイルデバイス、またはWebブラウザから起動できる、ブランド化されていないカスタマイズ可能なアプリケーションです。AppControllerは、顧客の名前とロゴでブランド化できます。

### AppControllerのブランディング

1. Admin Consoleから、[Tools | Branding] をクリックします。
2. AppControllerタブをクリックします。
3. 次のいずれかをパーソナライズします。
* Company Name
* Product Name
* Installer Name
4. AppControllerがブラウザウィンドウ内で実行されるときのデスクトップの色を選択するには、色のRGB値を10進形式で入力します。白のデフォルト色は10進数で16777215です。たとえば、背景色を青に変更するには、16711680と入力します。背景色を緑に変更するには、65280と入力します。背景色を赤に変更するには、255と入力します。
5. 新しいProduct Logoを参照するには、[browse]ボタンをクリックします。次の形式.jpg.、jpeg、.pngがサポートされています。
6. [Clear all to restore defaults] ボタンをクリックして、元のテキストと画像に戻します。
7. [OK] をクリックします。

![4-20-1](/img/4-20-1.png) 

ブランディングオプションは、group = "Branding"の下のC：\ ProgramData \ GraphOn \ GO-Global \ HostProperties.xmlファイルに保存されます。 画像はC：\ ProgramData \ GraphOn \ GO-Global \ imagesに保存されます。
relay serverまたはセッションマネージャを使用すると、クラスタ内のすべてのホストで設定の変更が自動的に行われます。relay serverまたはセッションマネージャを使用しない場合、ブランドオプションをコンピューター間で手動でコピーできます。詳細については、「ホスト間での構成設定の手動コピー」を参照してください。