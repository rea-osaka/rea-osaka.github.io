---
layout: single
title: "良く使うパッケージのインストール"
permalink: /works/howto/r/packageinstall/
toc: true
toc_label: "目次"
---

RStudioを使ってＲパッケージをインストールします。

インターネットにつながっている環境で、以下の手順を行ってください。


## 1. RStudioを起動してPackagesペインをみつける

RStudioの画面は、幾つかの区画に分かれています。


そして、その区画の上部をよく見てもらうと、どの区画にも、
内容を切り替えることが出来る「タブ」が並んでいるのをみつけることが出来るはずです。

![rpacageinst](/assets/images/htr/rpackage_inst001.png){: .align-center}

ここで、右下の区画に注目して下さい。
「File」「Plots」「Packages」「Help」「Viewer」と並んでいるはずです。
そこを、クリックするとそれぞれの内容に切り替わるので、順番にクリックして試してみましょう。

さて、今回使うのは「Packages」です。PackagesタブをクリックしてPackagesを開けば、パッケージインストールの準備が完了です。
![rpacageinst](/assets/images/htr/rpackage_inst002.png){: .align-center}


## 2. Packagesペイン

Packagesには、既にインストールされているパッケージの一覧が表示されています。

![rpacageinst](/assets/images/htr/rpackage_inst003.png){: .align-center}

青くなっているパッケージ名をクリックするとそのパッケージのヘルプに切り替わります。
良く見ると上部のタブが「Help」に切り替わっているはずです。慌てず、
**元に戻りたい時は「Packages」タブをクリック**しましょう。

さて、タブの下をよく見てもらうと「Install」「Update」という項目が並んでいるのを見つけられるはずです。
![rpacageinst](/assets/images/htr/rpackage_inst004.png){: .align-center}

## 3. Install Packages ダイアログ

先にみた「Install」と書かれている部分にカーソルを持っていくと、カーソルが指で指し示すマークに変わるので、クリックしましょう。
「Install Packages」ダイアログが開きます。

ダイアログの真ん中辺りに「Packages(separate multiple with space or comma)」と書かれていいて、その下に入力フォームがあります。
この入力フォームに、インストールしたいパッケージ名を書き込み、下の「Install」と書かれているボタンを押すと、パッケージのインストールが出来ます。

![rpacageinst](/assets/images/htr/rpackage_inst005.png){: .align-center}

まずは、試しに入力フォームに`tidyverse`と書き込んでみましょう。

入力フォームに`tidyverse`と書けたら、下の「Install」ボタンを押してください。
RStudioの左側の区画である「Console」に、以下のコマンドが自動的に入力されて実行されます。

```R
> install.packages("tidyverse")
```

コマンドが実行されると、Console上にインストールに関する色々な情報が出力がされます。
出力の内容は、英語ですが、インターネットを通じて、パッケージをダウンロードし、適切な場所にインストールする進捗状況が示されています。

一つのパッケージを指定したとしても、デフォルトでは、関連して必要となる他のパッケージも自動でインストールしてくれるので、
インストール作業が完了するまでには少し時間が掛かります。特に`tidyverse`を初めてインストールする時には関連パッケージが何十個もインストールされ、大きなファイルの展開などもされるため、数分待つことになるかもしれません。

インストール作業が完了したら、プロンプト（入力待ちのカーソル）に戻ってくるので、それまでおとなしく待ちましょう。

![rpacageinst](/assets/images/htr/rpackage_inst006.png){: .align-center}

Ｒの解説書を読んでいると、「もし、まだ○○のパッケージをインストールしていないなら、インストールしましょう」という記述がよく出てきます。

必要とされるパッケージが、既にインストールされているかどうかの確認は、Packagesペインの一覧で行うことが出来ます。
一覧に表示されていれば、あなたのパソコンに既にインストールされています。
また、タブの下の段の右端にある検索フォームを活用することも出来ます。

良く分からない時は、重複してインストールしてしまって構いません。


## 4. よく使うパッケージのインストール

小委員会で発表しているRスクリプトや研修の時に事前にインストールしておいてもらいたいパッケージを列挙しておきます。
前項のやり方に従って、インストールしてみてください。

- tidyverse
- sf
- data.table
- devtools

## 5. GitHubで公開されているパッケージのインストール

Rのパッケージには、**CRAN**(シーラン)と呼ばれる、Rの公式プログラム配布場所から入手ができるものと、
GitHub等の**CRAN以外**の場所から入手出来るものがあります。

先にRStudioのインストール機能を使って、インストールできるパッケージはCRANから入手できるパッケージのみです。

次は、GitHubで公開されているパッケージをインストールする方法を紹介します。
当小委員会では、[Ｒパッケージ「reti」](https://github.com/rea-osaka/reti)
(**R**eal **E**state **T**ransaction-price **I**nfomation data)を
GitHub上で開発して公開しているので、これをインストールします。

GitHub上のパッケージをインストールするためには、コンソールのプロンプトにコマンドを打ち込んで実行します。
RStudioの左側のコンソール区画にある、プロンプトに次のコマンドを打ち込みます。

```R
> devtools::install_github("rea-osaka/reti")
```







