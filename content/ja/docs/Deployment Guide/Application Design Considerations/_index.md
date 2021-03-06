---
title: "アプリケーション設計の検討事項"
linkTitle: ""
weight: 02
type: "docs"
---

## 検討事項

標準のWindowsサーバ環境とGO-Globalホスト環境の重要な違いは、これらの環境で動作するアプリケーションの設計です。集中ホスト環境では、アプリケーションはその環境で動作するように特別に設計されています。GO-Globalを利用すると、WindowsベースのPC用に設計されたアプリケーションは、GO-Globalホスト環境用に明示的に開発する必要なく動作します。今日のWindowsサーバ上で動作するアプリケーションは、変更なしでGO-Globalホスト上で動作します。

これは、複数のユーザが共通のWindowsサーバーシステムを同時に共有することの影響を考慮するときに重要です。異なるユーザが自分のローカルハードウェアリソース(CPU、メモリ、ディスクなど)とローカルソフトウェアリソース(レジストリ設定、設定ファイル、ダイナミックリンクライブラリなど)を使用してアプリケーションを実行する代わりに、GO-Globalホスト環境のユーザは共有します。同じハードウェアリソースとソフトウェアリソース、たとえば、GO-Globalホスト環境で2人のユーザが同じアプリケーションを実行している場合、そのアプリケーションの2つのコピーが同じシステムで起動され、それぞれ異なるユーザコンテキストで動作します。これらすべては、オペレーティングシステムによって舞台裏で管理されています。

ただし、複数のユーザに共通のシステム内の同じ一連のアプリケーションにアクセスさせると、多くの競合領域が生じる可能性があります。これらの分野は次のとおりです。

- **マルチユーザによるCPU時間の競合** GO-Globalホスト環境では、各ユーザは自分のアプリケーション環境を持ち、そのユーザが利用できるアプリケーションは何でも実行できます。ただし、すべてのユーザによって実行されるすべてのアプリケーションは、サーバマシン上で利用可能な中央CPUリソースについて競合しています。1人のユーザが不十分に書かれた、CPU集中型のアプリケーションを実行すると、そのサーバ上の他のユーザはかなりのパフォーマンス低下を経験する可能性があります。
- **マルチユーザによるディスクアクセスを求めて競合** これは、従来のクライアント/サーバネットワーク接続を使用してユーザがディスクアクセスを競合する方法と似ています。GO-Globalホスト環境では、ユーザはアプリケーションや関連するアプリケーションファイルへのアクセスだけでなく、サーバオペレーティングシステムのディスクアクセスについても競合するため、入出力の要求がより厳しくなります。たとえば、複数のユーザが同時に異なるダイナミックリンクライブラリ(DLL)を呼び出したり、実メモリ領域と仮想メモリ領域を交換したりすることがあります。
- **マルチユーザによるランダムアクセスメモリ(RAM)の競合** 各ユーザは独立したセッションを持っています。このセッションは、ユーザが自由に使用できるように、メモリを大量に消費するすべてのアプリケーションで満たすことができます。できる限り多くのアプリケーションを開こうとするユーザもいれば、より保守的なアプローチを取って必要なアプリケーションだけを実行するユーザもいます。それにもかかわらず、すべてのユーザのニーズは、サーバメモリリソースの同じコアセットから満たされています。
- **マルチユーザによるネットワークアクセスの競合** 他の分散処理環境と同様に、ネットワークはデスクトップとサーバ間の通信のためのパイプラインを提供します。GO-Globalホスト環境では、すべてのデスクトップアクティビティのグラフィカル出力とマウス/キーボード入力がデスクトップとサーバ間のネットワークリンクを介して流れるため、ネットワークアクセスの必要性は従来の分散型クライアント/サーバアーキテクチャよりも重要です。サーバへのネットワーク接続が機能していないと、GO-Globalクライアントはまったく機能できません。
- **マルチユーザによるサーバ側のハードウェアコンポーネントを求めて競合** CD-ROM、ディスクドライブ、シリアルポート、パラレルポートなどのハードウェアコンポーネントは、通常クライアントベースではなくサーバベースです。したがって、ユーザがサーバ側のハードウェアコンポーネントにアクセスしようとすると、他のユーザが同じような要求をして競合する可能性があります。これらの伝統的に非共有のコンポーネントを共有することは、ユーザにとっても、これらのコンポーネントにアクセスするアプリケーションにとっても、新たな考慮事項を生み出します。
- **マルチユーザによるグローバルWindowsオブジェクトとリソースへのアクセスの競合** GO-Globalホスト環境では、ユーザはWindowsサーバの個々のコピーを実行しません。コアコンポーネントのいくつかは複製されていますが、残りのコンポーネントはGO-Globalユーザ間で共有されています。そのため、ユーザはレジストリ、ページングファイル、システムサービス、その他のグローバルオブジェクトおよびリソースへのアクセスを競合します。

これらの競合点の多くは、GO-Globalホストシステムのサイズをクライアントの要求を処理するのに十分なCPU、メモリ、ディスクリソースでサイジングすることで軽減できます。たとえば、マルチプロセッサ構成では、CPUの可用性を最大限に高めることができます。追加の物理メモリを取り付けることで、メモリの可用性を最大限に高めることができます。最後に、複数のSCSIチャネルを構成し、オペレーティングシステムとアプリケーションの負荷を異なる物理ドライブに分散させることで、ディスクアクセスのパフォーマンスを最大限に引き出すことができます。GO-Globalホストを正しく設定することは、最適なアプリケーションパフォーマンスを得るための重要な要素です。

## 重要なパフォーマンス要因
- あなたのアプリケーションを知っている
アプリケーションを知っているためには、次の質問をする必要があるかもしれません。どのくらいのメモリが必要ですか？ユーザがアプリケーションのメモリをどれだけ共有できるかアプリケーションはどのように画面を更新しますか？それは多くのユーザ入力を必要としますか？許容できる性能とは何ですか？
- あなたのユーザを知っている
ユーザを知っているためには、次の質問をする必要があります。ユーザはアプリケーションを開いたままにしますか？ユーザはいつログオンしますか？ユーザは1日を通してログオンしたままですか？ログオンは1日を通して均等に分散されていますか？それとも、ほとんどのログオンはその日の特定の時間に行われていますか？
- あなたのネットワークを知る
GO-Globalはユーザにアプリケーションセッションを提供するため、ネットワーク通信は非常に重要です。まれにネットワークの速度が低下しても、許容できないパフォーマンスがユーザにもたらされる可能性があります。あなたのネットワークを知ることは次の質問を含むかもしれません：あなたのユーザはどれくらい速くタイプしますか？アプリケーションはグラフィックを多用しますか。クライアントワークステーションの典型的なディスプレイ解像度は何ですか？アプリケーションを実行しているユーザに必要なネットワーク帯域幅はいくつですか？

