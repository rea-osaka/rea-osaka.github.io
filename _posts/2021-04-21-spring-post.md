---
author: syunsuke
title: "春なので新しいこと"
---

まぁ、去年から今年にかけて、色々とややこしい時期なので、
このサイトくらい、前向きに、春なので新しいことを！！

## 久しぶりの更新

当委員会のサイトの久しぶりの更新です。

ずっと、Rに関する環境構築のページ内容が古くなっている事が気になっていたので修正しました。

データ分析の勉強を始める前後、Pythonを使ってプログラムを書いていて、
モジュール管理にanacondaが便利だったのと、
インタラクティブ作業において、
Jupyter Notebookが衝撃的に使い勝手が良かったので、
Rを勉強し始めた頃、そのまま、anacondaの中のRを使い始めました。
それで、このサイトのR環境構築でもanaconda経由のものを紹介していました。

しかし、僕自身、実際にRを使っていくと、
Jupyter Notebookと同等のノートのようなものを
RStudioでは何の設定もなしに使うことが出来ることがわかったり、
また、パッケージの管理についても、Rの場合にはpythonほど複雑ではないので、
ディストリビューションを使わないRそのもののパッケージ管理下においていても
ほとんど困ることが無いこともわかりました。

結局の所、Rを使う場合には、anaconda経由で管理をするよりも
Rネイティブの管理をRStudioを通じて行うほうが素直で楽でした。
また、近年のデータサイエンスブームのおかげか、
RStudio開発チームは活気があり、RStudio自体、更に頻繁に進化しています。
（もともと、RStudioという開発環境は、フリーで使えるものとして
最も優れていて、完成されているものの一つだと個人的に思います。）

というわけで、個人的には、R環境構築はRとRStudioがおすすめです。

## 新しいパッケージについて

retiパッケージは、
基本的に国土交通省が公表している不動産取引価格情報のcsvファイルを取り込む事と
種別類型、その他、地域等の選別を行うという、
R外のデータをRのデータにするという部分に特化しており、
それだけで、何かが得られるものではありません。

そのせいか、retiは、あまり人気がなさそうなので、
retiで取り込んだパッケージを集計してくれる`retiex`パッケージを作ってみました。

期間毎にデータをグループ分けし、それぞれのグループの要約統計量を計算してくれます。
また、その期間毎計算結果について、対前期間との比率や増減比、差を計算してくれる関数もあります。

また、最終的には、成果物としての出力があったほうが無いと、みんなの興味をひけないかな？と思い、
pdfへのレポート出力ができる`repoco`パッケージも試作しています。
こっちは、「レポートコレクション」として、
いくつものパターンを用意して、その中からそのデータに適したものを自分で選べるようにしたいなと思っていますが、
今は、土地建物一体取引の新築住宅に関するパターンだけがあります。

ただし、pdf出力するためには、TeXという一般の人はあまり使わないプログラムを使うことになり、
それをインストールする必要があるので、そのドキュメントも作りました。

プログラムからpdf出力できるというのは、Rで作業する際の大きなメリットの一つなので、
パソコンが嫌いじゃなければ、是非挑戦してみてほしいなと思っています。

## retiについて

retiでのファイル読み込みって、実は、結構時間がかかるんですよね。
僕自身、ある程度Rのコードを書くようになって、
改めてretiのコードを見直してみると、
見やすさのために代入を頻繁に使っているんですが、
データのコピーを沢山作っているのと同じなので、
この辺をなんとかしたら、もっと、読み込みが速くなるのかなぁ、、、なんて、思っています。



