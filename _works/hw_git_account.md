---
layout: single
title: "GitHubアカウントの作り方"
permalink: /works/howto/github/account/
toc: true
toc_label: "目次"
---

## 1. GitHub
![GitHub](/assets/images/htgithub/top001.png)

[https://github.com](https://github.com/)

## 2. Sign Up フォームへの入力

トップページ右側に表示されるフォームに以下の必要事項を決めて入力します。

- ユーザー名
- メールアドレス
- パスワード


### 2-1. ユーザー名

ユーザー名はGitHub上で活動する時のあなたの名前になります。ISSUE等へのメッセージの書き込み等であなたを表すために、このユーザー名が表示されます。

また、GitHubのリポジトリは通常

```
UserName/RepositoryName
```
と表現されます。
また、GitHub上のユーザーリポジトリのURLも次のようにUserNameがそのまま使われます。


```
https://github.com/UserName/RepositoryName
```

ですから、**あなた自身を良く表していて、また、親しみの持てる**ユーザー名を付けましょう。

もし、ユーザー名をフォームに入力している時、入力枠の下側に赤い吹き出しで
「Username is already taken」
と表示され、入力枠の右端に赤いビックリマークが表示されてたら、そのユーザー名は既に使われているため登録することが出来ません。
後ろに数字を付ける等、別のユーザー名を検討してください。


![input form](/assets/images/htgithub/input001.png)

### 2-2. メールアドレス

この登録するメールアドレスは、GitHubからあなたに連絡を取るために使われます。
通常、このメールアドレスが勝手に公開されることはありません。

メールアドレス登録時の注意としては、GitHubで複数アカウントを作成しようとする時、ユーザー名が異なっていてもメールアドレスが同じ場合、アカウントは作成できません。

![input form](/assets/images/htgithub/input003.png)

上記のように既にメールアドレスが使われている警告メッセージがでるので、複数アカウント登録の際には別のメールアドレスを用意しましょう。


### 2-3. パスワード

また、パスワードは、７文字以上の英数文字で、アルファベットと数字の両方が必ず入っていなければなりません。

|パスワード例|正誤|理由|
|:---|:---|:---|
|aaabbbccc|✖|数字が無い|
|123456789|✖|アルファベットが無い|
|12ab34|✖|7文字未満|
|123abc456|○|有効なパスワード|


### 2-4. Creat account !!!

![input form](/assets/images/htgithub/input002.png)

緑の「Sign Up For GitHub」ボタンの下には、GitHubの利用規約とプライバシーポリシーのリンクがあり、
ボタンをクリックすることでこれらに同意することになるという文言が添えられています。
また、登録するメールアドレスにはGitHubからメールが届くことがある旨も説明されています。

それらに同意した上で緑の「Sign Up For GitHub」ボタンをクリックしましょう。
クリックすると、入力事項がＯＫであることが確認されて以下の様な画面になります。


![comfirm001](/assets/images/htgithub/comfirm001.png)

下の方にある緑の「Creat an account」ボタンをクリックしましょう。

## 3. プランの選択
次は利用プランを選択する画面になります。

![comfirm002](/assets/images/htgithub/comfirm002.png)

GitHubでは、公開リポジトリを利用する場合は、料金がかかりません。
もし、非公開のリポジトリ（有料）が必要になった場合は、いつでも切り変えられるので、初めは無料の公開リポジトリを選択しておけばＯＫです。

「Unlimited public repositories for free」の左にチェックが入っているのを確認して、
下の方にある緑の「Continue」ボタンをクリックしましょう。

## 4. アンケート

![question001](/assets/images/htgithub/question001.png)

幾つかのアンケートがあります。

適当に答えて「Submit」するか、よくわからなければ「skip this step」をクリックすればＯＫです。


## 5. メールアドレスでの本人確認 

アンケートに答えるかスキップすると、次のような画面になります。

![dashboard001](/assets/images/htgithub/dashboard001.png)

もしくは、画面の上に

> Please verify your email address to access all of GitHub's features.

> (GitHubの機能を全てを使うには、メールアドレスの確認をして下さい)

と書かれた、次のような画面になります。

![dashboard002](/assets/images/htgithub/dashboard002.png)

どちらにせよ、この画面が表示されているならば、
GitHubにあなたのアカウントがちゃんと作成され、
あなたは既にGitHubにサインインしている状態にあります。

しかし、最後に本人がこのアカウントを作成したことの最終確認作業が必要です。

### 5-1. GitHubからのメール

実は、「2. Sign Up フォームへの入力」を行うと、
登録したメールアドレスに以下のような確認メールが送られて来ているはずです。

![verifymail001](/assets/images/htgithub/verifymail001.png)

メール内の「Verify email address」と書かれているリンクをクリックすると、
GitHubがアカウント作成の確認を受け付けてくれます。

もし、「Verify email address」の部分がリンクになっていない場合、
「Paset the following link into your browser」と書かれている次の行の**URL**を
ブラウザに張り付けて直接そのURLリンクへ行ってください。


![welcomemail001](/assets/images/htgithub/welcomemail001.png)

確認作業が完了するとGitHubから上記のようなwelcomeメールが届きます。

以上で、GitHubへのアカウント作成作業は完了です。

### 5-2. メールの確認作業をしないと、、

もしかしたら、前述作業中に、メール着信に気が付いて、既に確認を行っていたかもしれません。
しかし、そうではない場合、このメールアドレスの確認作業をするまでは、ISSUE等への書き込みができません。

![verifyaccount001](/assets/images/htgithub/verifyaccount001.png)

上記のように、ISSUEの書き込み欄に

> You need to verify your email address before you can join conversation

> （議論に参加するにはメールアドレスの確認が必要です）

と表示されて、書き込みが出来ない場合は、まだメールアドレスの確認が終わっていません。
登録したメールアドレスのメールボックスを確認して、前述のGitHubからの確認メールに答えましょう。


## 6. GitHubへログインする

アカウントの作成作業が終わった後、

[https://github.com](https://github.com/)

というURLへアクセスした時、ログイン状態が保持されていれば、

![dashboard001](/assets/images/htgithub/dashboard001.png)

という感じの、自分のアカウントのダッシュボード画面になりますが、時間が経つなどしてログアウトした状態でアクセスすると

![GitHub](/assets/images/htgithub/top001.png)

というような、GitHubのトップページが表示されます。

ここで注意が必要です。

**このトップページからは、アカウントにログインできません。**


実は、トップページに表示されているフォームはアカウント作成のための入力フォームです。
ですから、既にアカウントを持っている場合、ここに自分のユーザー名等を入力して、「Sign up for GitHub」ボタンを押しても**ログインできません**。


### 6-1. Sign up と Sign in

ページをよく見てみると「Sign up」と「Sign in」という似た単語があることに気が付くはずです。
そして、このふたつの単語は似ているものの意味が全く違います。

「**Sign up**」とは、「アカウントを新規に作成して登録すること」です。
そして、「**Sign in**」が、「アカウントにログインすること」です。

この二つの単語に違いがあることさえ把握しておけば、GitHubのトップページを見た時に思い出すのでＯＫです。


**アカウントにログインするためには、「Sign in」しなければなりません。**


そのために、画面上部にある「Sign in」をクリックして Sign in 用のページに切り変えましょう。

![signinform](/assets/images/htgithub/signinform001.png)


切り替わったSign in ページは次の様になっているはずです。


![signinform](/assets/images/htgithub/signinform002.png)



### 6-2. ログインしよう

Sign in のページへ切り替えさえれすれば、ちゃんとログインできます。

上段のフォームへの入力は、ユーザー名、メールアドレスのどちらでも受け付けてくれます。
下段にパスワードを入力したら、緑の「Sign in」ボタンをクリックしましょう。


