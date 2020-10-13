# 5.1. Macの場合

**Visual Studio for Mac**では**Azure VM**へWebデプロイの機能が追いついていないため，別の対応方法を記載しています．<br>
Windiowsは全てVisual Studioで完結しますが，Macは少し違う手法を取ります．

プロジェクトの新規作成を選択します．

![](img/52_m.png)

**Blazor Server**を選択します．

![](img/53_m.png)

認証なしでOKです．

![](img/54_m.png)

プロジェクト名や場所は任意なので，好きな名称を入力してください．

![](img/55_m.png)

プロジェクトが作成されたらソリューションで**右クリック->公開->フォルダに公開**を選択してください．

![](img/56_m.png)

公開先のフォルダを選択します．<br>デフォルトのまま変更していないですが，任意です．

![](img/57_m.png)

作成したプロジェクト内まで移動し，Finderを開きます．

![](img/58_m.png)

以下のフォルダを**Windows Server**へアタッチして，コピーしていきます．
![](img/59_m.png)


VMに接続するときに使用した`.rdp`ファイルを**Microsoft Remote Desktop**へドラッグ&ドロップします．

![](img/60_1_m.png)

パネルを右クリックし，**Edit**を選択，**Folders**のタブを選択し，**Redirect folders**にチェックを付けます．<br>
**[+]** ボタンをクリックして，Visual Studioで公開先で選択したフォルダを指定し，VMから誤ってファイルが削除されないように**Read-only**にチェックを付けます．
![](img/60_m.png)

再び**Windows Server**に戻り，**Server Maneger**から**IIS Manager**を選択します．
![](img/65_m.png)

**Default Web Site**で**右クリック->Explore**を選択します．

![](img/63_m.png) 

ファイルエクスプローラーが開きますので，このフォルダへファイルをアップロードしていきます。
![](img/63_1.png)

更にファイルエクスプローラーを開き，Macの**Microsoft Remote Desktop**で設定したフォルダがアタッチされているのでダブルクリックして移動します．<br>※Macが見えない場合は**Microsoft Remote Desktop**を閉じて再度繋ぎ直してみてください．

![](img/61_m.png)

上記手順で開いたMacのファイルを全てコピーします．

![](img/64_m.png)

これでデプロイが完了です．
早速Webページを開いてみましょう．

![](img/66_m.png)

Blazor Serverで作成されたページが表示されました．<br>Macの場合は少し面倒ですが，デプロイ時は上記の手順を再度繰り返せばOKです．
