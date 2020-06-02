---
title: "システム要件"
linkTitle: ""
weight: 04
type: "docs"
---

## GO-Globalホスト
- GO-Globalホストには、次の64ビットWindowsオペレーティングシステムのいずれかが必要です。
　**Windows Server 2019** - スタンダードとデータセンタ
　**Windows Server 2016** - スタンダードとデータセンタ
　**Windows Server 2012 R2** - スタンダードとデータセンタ
　**Windows 10 (バージョン1809以降)** - プロフェッショナルとエンタープライズ(マルチユーザ環境では、Windows Serverの利用を強く推奨します。)
- GO-Globalホストは、最新のWindowsアップデートがインストールされているコンピュータでサポートされています。
- インストールを実行するには、管理者がホストの管理者権限を持っている必要があり、ホストがネットワークプロトコルとしてTCP/IPを使用している必要があります。
- GO-Globalは、TCPパケットのためにGraphOnの登録ポート491をリッスンします。外部ファイアウォールやホスト上のソフトウェアファイアウォールをTCPポート491を許可するように設定してください。
- GO-GlobalはVMware ESXiおよびHyper-Vをサポートしています。
- GO-Globalは、Device Guard を有効にしているWindows Server 2016システムをサポートしていません。
- GO-Globalは、ドメインコントローラへのホストのインストールをサポートしていません。
- クライアントとホストの色深度は256以上である必要があります。1,600万以上を推奨します。
- GO-GlobalホストのメモリとCPUの要件は、公開されているアプリケーションとシステムにアクセスするユーザ数によって決まります。一般的に、GO-Globalホストは12 人のヘビーユーザ/500 MHz CPUと 25人のライトユーザ/500 MHz CPUをサポートすることができます。(「ヘビー」とは、1 つ以上の大規模なアプリケーションを継続的に実行しているユーザと定義されます。「ライト」とは、断続的なユーザ操作を伴う 1 つのアプリケーションを実行しているユーザと定義されます)。
- GO-Globalは最大500ミリ秒の往復遅延をサポートしています。
- GO-Globalでは、最低28.8kbpsのモデム速度が必要です。
- GO-Globalでは、ユーザのネットワーク帯域幅ごとに16kbpsを必要とします。

## GO-Global クライアント
GO-Globalは以下のクライアントプラットフォームをサポートしています。
- Windows 10（バージョン1809以降）ProfessionalとEnterprise（32 ビット/64 ビット）、Windows 7 Professional、Ultimate、Enterprise（32 ビット/64 ビット）。GO-Global は、最新のWindowsアップデートがインストールされたコンピュータでサポートされています。
- Mac OS X 10.13 以降
- Red Hat Enterprise Linux 7と8（64 ビット）、CentOS 7および8（64 ビット）、SUSE Linux Enterprise Desktop 15（64 ビット）、Ubuntu 18.04 LTSと19（64 ビット）
- iOS 11.0以降
- ARMプロセッサのAndroid 8.0以降

GO-Globalは以下のブラウザをサポートしています。
- Internet Explorer 11（32ビット）
- Mozilla Firefox 60以降
- Mac OS XでのApple Safari 11以降
- Google Chrome 67以降のWindows 7、Windows 10、Chromebookとの連携
- Microsoft Edge Chromium
