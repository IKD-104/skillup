---
layout: default
title: github使ってソースをあげてみる
---
# github使ってソースをあげてみる

STEP1で今まで作ってきたファイルを管理してみましょう。
サンプルコードやこのWebサイトのソース管理をするため[GitHub](https://github.com/)を使ってみます。
GitHubではGitというバージョン管理システムを用いて進めます。

### githubアカウント作成

[アカウントを作成](https://github.com/join)にアクセスし、個人のアカウントを作成しましょう。
すでにアカウントをお持ちの方は既存のアカウントを使っていただいてOKです。


### リポジトリ作成

github上で、リポジトリを作成します。レポジトリというのはアプリケーションのソースやデータの格納場所のことです。
上のタブの `Repositories` からレポジトリ一覧ページに進み、 `New` ボタンを押し、名前をつけて新しいレポジトリを作成します。ここでは、仮に「onlineskillup_step1」としてみます。

https://github.com/<ユーザ名>/onlineskillup_step1  
このようなURLのページが出来上がっているはずです。
中身はまだ空ですが、こちらが作成したレポジトリになります。


### ソースコードをあげる

上で作成したレポジトリにソースコードをあげます。この行為を「プッシュ」と言います。

コマンドラインで次のコマンドを叩き、プッシュしてみてください。
```
# 作成したソースコードがあるフォルダに移動
cd <フォルダ>

# gitの初期化を行う
git init

# レポジトリの登録
git remote add origin https://github.com/<githubユーザ名>/onlineskillup_step1.git

# ユーザの登録
git config --local user.name <ユーザ名>
git config --local user.email <メールアドレス>

# 変更を確定させる
git add .
git commit -m "first commit"

# 変更をプッシュする(パスワードが聞かれたら、githubの登録時のパスワードを入力)
git push -u origin master
```

ブラウザでレポジトリに移動し、ファイルがあがっていることを確認してください。


### 詳しく

#### Gitについて

Gitを使うことでファイルの編集を履歴として保存することができ、プログラムの変更を確認したり復活させたりすることができます。
また複数人で1つのプログラムを編集して開発する際にもよく使われています。

Gitについては[GitBook](http://git-scm.com/book/ja)に詳しく書かれているので参考になります。
Chapter1でGitの基本やインストール、Capter2で基本コマンドについて書かれています。

GitクライアントとしてはGitBookにも書かれている[Git for Windows](https://git-for-windows.github.io/)があります。
他にも[GitHub Windows](https://windows.github.com/)や[SourceTree](http://www.sourcetreeapp.com/)といったクライアントが主に使われています。
どのクライアントも同じGitの作業はできます。

#### Githubについて

GithubはGitというバージョン管理ツールを用いたプロジェクトを複数人で共有するためのツールです。GitとGithubの違いをはっきりさせておくと理解が捗るかもしれません。
Githubについては[GitHub入門](http://www.slideshare.net/hideaki_honda/gitgithub-16508298)が参考になります。

***  

**[課題]gitを使いこなしてみよう**  
gitは開発をスムーズにするための機能がたくさんあります。余裕があれば、Gitの基礎から学ぶことのできる[入門サイト](http://www.backlog.jp/git-guide/)やGitのコマンドを説明してくれる[チュートリアル](https://www.atlassian.com/ja/git/tutorial)などが公開されていますので、色々なコマンドを使ってみて、gitによるバージョン管理に慣れてみましょう。


