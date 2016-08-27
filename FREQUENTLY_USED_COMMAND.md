### よく使うコマンド一覧

直前のコミットを取り消す
```
$ git reset --soft HEAD^
```
 ローカルの修正をなかったことにする。
```
$ git checkout .
```
そのファイルの修正をなかったことにする。
```
$ git checkout <ファイル名>
```
直前のコミットのコメントを修正する。
```
$ git commit --amend
```
ブランチを切る。(そのままブランチをcheckout)
```
$ git checkout -b <ブランチ名>
```
リモートリポジトリにdevelopブランチがなかったら、追加される。
```
$ git push -u origin develop
```
```
$
```
