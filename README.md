# git差分ファイルアップロードツール、git up-fileコマンドのご案内

git-up-fileはコマンドラインからgit diffの差分ファイルを任意のディレクトリにアップロードするツールです。

## 使うための準備
git-up-fileとgit-up-file.confをPATHが貼られている場所に置いて利用できます。
または、適当なディレクトリに置いて、PATHを貼ってもOKです。

例）
下記の場所に置いて.bashrcの中でPATHを設定する場合。

* /D/sample-directory/git-up-file
* /D/sample-directory/git-up-file.conf

.bash_profileに以下の追加する。
```
export PATH=$PATH:/D/sample-directory/
```

### 設定ファイル

git-up-file.conf

UPしたいディレクトリが増えた場合はこの設定ファイルに追加してください。

## 使い方

```
$ git up-file <commit> <-option>
$ git up-file <commit> <commit> <-option>
```

## 利用例
```
$ git up-file HEAD -option
$ git up-file HEAD^ -option
$ git up-file origin/master..HEAD -tour
```
※<-option>は任意で設定可能
※<commit>はgit diffで利用できるものと同じ
[忘れやすい人のための git diff チートシート](http://qiita.com/shibukk/items/8c9362a5bd399b9c56be)

## 改訂履歴
* ver2: git移行によりelement配下のファイルをsvnディレクトリへUPする機能は廃止しました。