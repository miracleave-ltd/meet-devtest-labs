# Azure Dev Test Labsでテスト環境を構築してみる！

## 前提条件

以下の準備が必要です。

* Microsoft Azureアカウント（無料試用版でも可です）
* Visual Studio（**Windows**）
* Visual Studio for Mac（**Mac**）
* Git
* AzCopy
  * [Mac](https://aka.ms/downloadazcopy-v10-mac)
  * [Windows-64bit](https://aka.ms/downloadazcopy-v10-windows)
* 折れない心

## ざっくりとした流れ

1. Azure devtest labs作る
2. 匿名ユーザーでも招待出来るようにVM作成(windows server)
3. VMが出来たら，RDPで入る
4. `IIS`インストール
5. `.NET Core`ホスティングバンドルのインストール
6. サブネットにネットワークセキュリティグループ割当
7. ネットワークインターフェースとの関連付け
8. Visual StudioからVMにBlazorアプリのデプロイ
   MacはKuduで公開用のビルドファイルを手動アップ
9. ブラウザで動作確認
10. 作成したVMをスナップショット
11. AzCopy を使用して VHD ファイルをアップロード
