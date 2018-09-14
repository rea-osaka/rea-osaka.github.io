---
layout: single
title: "anacondaのインストール"
permalink: /works/howto/anaconda/install/
toc: true
toc_label: "目次"
---

## Anaconda


![anaconda](/assets/images/htanaconda/toppage001.png){: .align-center}
[https://www.anaconda.com](https://www.anaconda.com)
{: .text-center}

Anacondaは、主にPythonの環境構築を簡単にしてくれるディストリビューションです。

Anacondaがインストールするファイル数は非常に多いので、空きディスクスペースが最低限3GB必要です。
また、インストール作業時間も少しかかるので、インストールは時間に余裕がある時に行う事をお勧めします。


## セットアップファイルのダウンロード

トップページの右上、緑の「Downloads」ボタンをクリックして、
ダウンロードページへ行きます。

切り替わったページで「Windows」と書かれている部分をクリックします。
![anaconda](/assets/images/htanaconda/download001.png){: .align-center}

Windows Installerと書かれていることを確認し、
Python 3.6versionと書かれている方の「Download」ボタンをクリックし、
セットアップファイルを保存します。

![anaconda](/assets/images/htanaconda/download002.png){: .align-center}


## インストール


ダウンロードされたセットアップファイル「anaconda3-5.2.0-Windows-x86_64.exe」をダブルクリックします。（ファイル名の数字はバージョンで時期により異なります）

![anaconda](/assets/images/htanaconda/anacondasetupfile001.png){: .align-center}


### 1. セットアップのスタート

![anaconda](/assets/images/htanaconda/install001.png){: .align-center}

「next」をクリックします

### 2. ライセンスへの同意

![anaconda](/assets/images/htanaconda/install002.png){: .align-center}

同意文書に目を通して「I agree」をクリックします


### 3. インストールタイプの選択

![anaconda](/assets/images/htanaconda/install003.png){: .align-center}

現在のユーザーのみが使えるようにインストールします。
「Just me」にチェックが入っていることを確認して、「next」をクリックします。

現在のユーザーのみにインストールすると、管理者権限がなくてもインストールが行えます。
また、Anaconda環境はユーザー環境下で整備されるのみなので、システム全体の環境に影響を与えません。
Anacondaでもこのタイプのインストールを推奨しています。

### 4. インストール先の指定
![anaconda](/assets/images/htanaconda/install004.png){: .align-center}

既に適当な場所が入力されているはずなので、そのまま「next」をクリック


### 5. その他のインストールオプションの指定
![anaconda](/assets/images/htanaconda/install005.png){: .align-center}

 - Add Anaconda to my PATH enviroment variable

     チェックが**外れている**事を確認します。

     このチェックを外しておけば、同じパソコンに他のPython等をインストールしていても、混乱せずに独立して環境を整備できます。
     環境変数PATHについての知識がないままanaconda環境をPATHに混入させると、同名の実行ファイルのどれがどのタイミングで実行されるか把握できないので、色々な場面で思い通りに行かない現象に出くわす可能性が高くなります。
     パソコンに詳しくない方は必ず、チェックを外してください。


 - Register Anaconda as my default Phthon3.6

     どちらでも構いませんが、分からなければチェックを外しておきます。

上記の通りチェックボックスを確認したら、「Install」をクリックしましょう


### 6. インストールがはじまります。
![anaconda](/assets/images/htanaconda/install006.png){: .align-center}

anacondaでは、沢山のファイルがインストールされるので暫く待ちましょう。


### 7. インストールの完了
![anaconda](/assets/images/htanaconda/install007.png){: .align-center}

ファイルのインストール作業が完了した旨の画面が出たら、「next」をクリックします。


### 8. Visual Studio Codeの宣伝
![anaconda](/assets/images/htanaconda/install008.png){: .align-center}

マイクロソフトのVisual Studio Codeというエディタをインストール出来ますというオプション画面です。
「Skip」をクリックしてインストールせずに先に進みます。

このVS Codeというエディタは評判が良いので興味のある方は、別途調べてみてください。
ただ、ここでいきなりインストールする必要はありません。
インストールしたい場合は、マイクロソフト等の一時配布先で、ゆっくりとインストールしましょう。


### 9. インストール作業の完了 
![anaconda](/assets/images/htanaconda/install009.png){: .align-center}

「Finish」をクリックすれば完了です。

その際、チェックボックスにチェックが入っていると、Anacondaの説明サイトがブラウザで開かれます。


## Anaconda Promptを使ってアップデート

インストール作業が完了すると、Windowsのスタートメニューに「Anaconda3」ディレクトリが出来ているので開きます。


![anaconda](/assets/images/htanaconda/start001.png){: .align-center}


幾つかのアプリケーションがありますが、「Anaconda Prompt」をクリックして起動します。

![anaconda](/assets/images/htanaconda/a_prompt001.png){: .align-center}

プロンプトはコマンドを受け付けるアプリです。
カーソルが点滅して、コマンド入力受付中であることを示しています。

Anacondaシステムを最新の状態にするために、プロンプトに次のコマンドを入力します。

```
conda update conda
```

実際のプロンプト画面は次のようになります。

![anaconda](/assets/images/htanaconda/a_prompt002.png){: .align-center}

コマンドを書き込んだら、リターンキーを押してコマンドを実行します。

現在の環境が最新かどうか、調べてくれるのでしばらく待ちましょう。

もし、アップデートが必要な場合、次のような返答待ち画面になります。

```
Proceed([y]/n)?
```

そこにｙを入力してリターンキーを押しましょう。アップデートが開始されます。


![anaconda](/assets/images/htanaconda/a_prompt003.png){: .align-center}

暫く待っていると、アップデート作業が完了して、プロンプトが戻ってきます。


![anaconda](/assets/images/htanaconda/a_prompt004.png){: .align-center}


もし、アップデートの必要が無い場合は、

```
# All requested packages already installed.
```
とメッセージが出て、プロンプトに戻るので、何もする必要はありません。

これで、Anacondaのインストール作業は終了です。

プロンプトに以下のコマンドを入力することで、プロンプトを終了できます。

```
exit
```


