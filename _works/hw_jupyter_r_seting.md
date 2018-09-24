---
layout: single
title: "RをJupyter Notebookで使う"
permalink: /works/howto/r/jupyter_setting/
toc: true
toc_label: "目次"
---

## Anacondaを使って、Jupyter Notebookを使えるようにする

### (1) Anacondaをインストール

まず、Anacondaをインストールすることによって、Jupyter Notebookが使えるようになります。
Anacondaがインストールされていない場合は、
「[anacondaのインストール](/works/howto/anaconda/install/)」に従って、Anacondaをインストールしましょう。

Anacondaのインストールが完了したら、
windowsのスタートメニューから「Anaconda Prompt」を起動します。

そして、プロンプトに
```
jupyter notebook
```
と入力して、リターンキーを押しましょう。


![rgui](/assets/images/htr/jupinst001.png){: .align-center}

プロンプトに、幾つかのメッセージが表示され、その後すぐに既定のブラウザが起動してJupyterNoteブックの画面が表示されます。

![rgui](/assets/images/htr/jupinst002.png){: .align-center}

### (2) Jupyter Notebookの終了
Jupyter Notebookが起動することを確認出来たら、Jupyter Notebookを終了します。
Anaconda Promptをクリックしてフォーカスを移し、「Ctrl + c」（コントロールキーと「c」のキーを同時に押す）を２回押します。


## Jupyter Notebookで Rが使えるようにする。

初期状態のJupyter Notebookでは、「Python(パイソン)」という言語しか使えないので、[IRkernel](https://irkernel.github.io/installation/)というものを使ってＲ言語が使えるように整備します。

### (1) 必要なＲのパッケージのインストール

 R環境に以下のパッケージをインストールします。

  - repr
  - IRdisplay
  - evaluate
  - crayon
  - pbdZMQ
  - devtools
  - uuid
  - digest

 Rのパッケージのインストールについては、「[パッケージのインストール](/works/howto/r/packageinstall)」の手順によって、
 上記のパッケージをひとつづつインストールすことが出来ますが、
 沢山のパッケージをインストールする場合、作業が煩雑になります。
 
 そこで、ここではコマンドを使ってインストールする次の手順を試してみましょう。

Windowsのスタートメニューから「R x64」を選んでRguiを起動します。

![rgui](/assets/images/htr/startrgui001.png){: .align-center}

以下のコマンドをコピーします。行が長いので、横スクロールして右端までしっかり選択してからコピーするように注意しましょう。

 ```
install.packages(c('repr', 'IRdisplay', 'evaluate', 'crayon', 'pbdZMQ', 'devtools', 'uuid', 'digest'))
 ```

次に、これをR Consoleのプロンプトに貼り付けます。

![rgui](/assets/images/htr/jupinst003.png){: .align-center}

そしてリターンキーで、実行します。（もし、CRANのミラーサイトの一覧が表示された場合は、適当な場所（Tokyo等）を選択します）

インストール作業が表示され、しばらくすると完了してプロンプトが表示されます。

![rgui](/assets/images/htr/jupinst004.png){: .align-center}


続いて、R Consoleのプロンプトに以下のコマンドを入力して実行します。
（コピー＆ペーストで構いません）
```
devtools::install_github('IRkernel/IRkernel')
```

このコマンドは、パッケージを通常のCRANからではなく、GitHubからインストールするコマンドです。
パッケージの入手先が異なるだけで、パッケージをインストールしている作業に変わりは在りません。

![rgui](/assets/images/htr/jupinst005.png){: .align-center}

インストール作業が表示され、しばらくすると完了してプロンプトが表示されます。

必要なパッケージのインストールが終わったら、
一旦、R Consoleを終了してください。

### (2) JupyterにRを組み込む作業

今度は、Anacondaの環境下でR Colnsoleを起動して、作業する必要があるので
概略で、次の手順を実行します。

 * Anaconda Promptを立ち上げる
 * Anaconda PromptからRgui.exeを実行する
 * 立ち上がったRguiのRconsole内でコマンドを実行する


以上の手順を、次の通り実施していきましょう。

### Anaconda Promptを立ち上げる。

windowsのスタートメニューから「Anaconda Prompt」を立ち上げます


### Anaconda PromptからRgui.exeを実行する

Anaconda Promptから、Rgui.exeを実行するためには、Rgui.exeの場所を入力する必要があります。
そのために、以下の手順でRgui.exeの場所を探します。


まず、ウインドウズのスタートメニューから「R x64」を開いて、**右**クリックします。
![rgui](/assets/images/htr/startmenu001.png){: .align-center}

上記のようにメニューが展開されるので、「その他」＞「ファイルの場所を開く」とたどり、左クリックするとフォルダが開きます。

フォルダの中の「R x64」のショートカットファイルを**右**クリックし、
メニューから「ファイルの場所を開く」を左クリックします
![rgui](/assets/images/htr/r_position001.png){: .align-center}

すると、Rのインストールされているフォルダが開きます。

このフォルダの中に、「Rgui.exe」という実行ファイルを見つけることが出来るはずです。

みつけたら、その「Rgui.exe」をAnaconda Promptのwindow内にドラッグ&ドロップします。

![rgui](/assets/images/htr/r_position002.png){: .align-center}
そうすることで、Anacomda Promptのプロンプトに「Rgui.exe」の場所を書き込むことができます。

スクリーンショットのように、Rgui.exeの場所が書き込まれたら、そのままリターンキーを押して実行しましょう。
Rguiが立ち上がり、R Consoleが立ち上がります。



### 立ち上がったRguiのR Console内でコマンドを実行する
続いて、R Consoleのプロンプトに以下のコマンドを入力して実行します。

```
IRkernel::installspec()
```

Jupyterから分かる場所に、IRKernelというものがインストールされます。

![rgui](/assets/images/htr/jupinst006.png){: .align-center}

以上の作業を終えて、Jupyter Notebookを立ち上げると、Rのノートが使えるようになります。

