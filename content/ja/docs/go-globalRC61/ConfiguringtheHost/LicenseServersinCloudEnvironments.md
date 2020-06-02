# クラウド環境でのライセンスサーバー

GO-Globalライセンスファイルは、GO-Global License Manager Serviceが実行されているコンピュータのMACアドレスにバインドされます。Amazon Web Services (AWS) などのクラウド環境では、仮想コンピュータのMACアドレスが変更されることがあります。GO-Global License Manager Serviceを実行しているコンピュータのMAC アドレスが変更されると、サービスがライセンスをチェックアウトできなくなり、GO-Globalセッションの開始に失敗します。これを防ぐには、GO-Global License Manager Serviceを実行している仮想コンピューターに固定のMACアドレスを設定する必要があります。AWS環境では、固定のElastic IPアドレス(EIP)と固定のMACアドレスを持つElastic Network Interface(ENI)を作成し、GO-Global License Manager Serviceを実行している仮想コンピュータ(EC2 インスタンス)にENIをアタッチすることで、これを行うことができます。

### AWSでEIPとENIを作成し、EC2インスタンスにアタッチする方法
1. Elastic IP（EIP）を作成する。
EC2コンソールのナビゲーションペインから「ネットワークとセキュリティ」→「Elastic IPs」と進み、「Allocate new address」を選択します。
詳細については、AWS EIPのドキュメントを参照してください。
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html
2. Elastic Network Interface(ENI)を作成します。
2.1 EC2コンソールのナビゲーションペインで、ネットワークインターフェースを選択します。
2.2 Create Network Interfaceをクリックします。
2.3 説明を入力し、適切な可用性ゾーンからサブネットを選択します。
2.4 プライベートIPは自動割り当てのままにしておく。
2.5 ファイアウォールルールを含むセキュリティグループを選択します。
3. Elastic IP(EIP)をElastic Network Interface(ENI)に割り当てます。
3.1 EIPとENIを作成したら、「ネットワークインターフェース」→「アクション」→「IPアドレスの管理」と進みます。
3.2 手順1で作成したEIPをENIに割り当てます。
詳細については、AWS ENIのドキュメントを参照してください。
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html

>ENIをインスタンスに割り当てるには、ENIのサブネットがGO-Global License Managerサービスを実行しているAWSインスタンスと同じ可用性ゾーンにある必要があります。Availability Zoneのサブネットを使用するか、Amazon Virtual Private Cloud (VPC)を介してAvailability Zoneにカスタムサブネットを作成することができます。

4. GO-Global License Managerサービスを実行しているインスタンスにENIをアタッチします。
4.1 EC インスタンスから、GO-Global License Manager サービスを実行しているインスタンスを選択し、[アクション] > [ネットワーキング] > [ネットワーク インターフェイスの添付] を選択します。
4.2 手順 2 で作成した ENI を選択します。利用できない場合は、別のAWSインスタンスにアタッチされているか、インスタンスとは異なる可用性ゾーンに作成されている可能性があります。
