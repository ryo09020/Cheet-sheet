#gitコマンド

##githubに挙げるまで
```
$ git init                                       # 現在いるディレクトリのgit設定ファイルを生成
$ git add ファイル名                              # 指定したファイルをインデックスに追加
$ git commit -m "コメント"                        # 変更履歴を保存
$ git remote add origin リポジトリURL             # リモートリポジトリのURLを登録
$ git push origin ブランチ名                      # リモートリポジトリにpush
```

##リモートリポジトリをローカルに持ってくる
```
$ git clone リポジトリURL
```

##リモートの変更をローカルに反映
```
$git fetch origin                               #リモートリポジトリからローカルにあるリモートリポジトリのコピーに最新情報をダウンロード→ローカルに反映されているわけではない
$git merge ブランチ名                           #ローカルブランチに反映する
$git pull origin ブランチ名                     #fetchとmergeをまとめて実行
```

#現状を把握するためのコマンド
```
$git status                                   #add,commitに関するの確認
$git diff                                     #ワークツリーとインデックスの差分確認
$ git reset HEAD^　　　　　　　　　　　　　　　#1つ前のコミットに戻る
