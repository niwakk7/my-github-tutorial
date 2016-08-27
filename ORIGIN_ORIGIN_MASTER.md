## masterとorigin/masterについて(ついでにリモート追跡ブランチも)

#### gitには3つのブランチが存在する。
- ローカルブランチ(ローカルリポジトリ)
- リモート追跡ブランチ(ローカルリポジトリ)
- リモートブランチ(リモートリポジトリ)

#### よくあるmasterとorigin/masterで考えると、要点は以下。
- ローカルにはmasterとorigin/masterの2つのブランチが存在する。
- master はローカルの更新を見ている。
- origin/masterはリモート側の更新を見ている。
- git fetchを行った際に origin/masterは最新になるがmaster は更新されない。
- git merge origin/master を行うと master ← origin/masterへmerge される。

#### 図にするとこんな感じ。
![top-page](https://github.com/niwakk7/my-github-tutorial/blob/master/image/origin_origin_master_1.png)

#### リモート追跡ブランチ (develop) を作成するには以下のコマンドを実行。
```
$ git checkout -b develop origin/develop
```
というか、考えてみると。これはよく使うコマンドであった。新しい作業環境で開発リポジトリのmasterリポジトリをcloneしたあとにその他のブランチも持ってきたい。というか、持ってこないと話にならない。
そのときにいつも使うコマンドではないか！ようは、このコマンドで勝手にリモート追跡ブランチになっているということになる。
あえてリモート追跡ブランチを設定しよう、と思わなくてもよい。もちろん、このコマンドは、既にdevelopブランチがリモートリポジトリにあるときに成立する。

#### 追跡ブランチを確認したいときは、以下のコマンドを実行。
```
$ git branch vv
```


#### Reference
http://snowlong.hatenablog.com/entry/2015/03/12/212455  
http://qiita.com/uasi/items/69368c17c79e99aaddbf  
http://qiita.com/YusukeSuzuki@github/items/3bd5752783fd2c2f8805  
