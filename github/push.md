# gitコマンド

## githubに挙げるまで
```
$ git init                                       # 現在いるディレクトリのgit設定ファイルを生成
$ git add ファイル名                              # 指定したファイルをインデックスに追加
$ git commit -m "コメント"                        # 変更履歴を保存
$ git remote add origin リポジトリURL             # リモートリポジトリのURLを登録
$ git push origin ブランチ名                      # リモートリポジトリにpush
```

## リモートリポジトリをローカルに持ってくる
```
$ git clone リポジトリURL
```

## リモートの変更をローカルに反映
```
$ git fetch origin                              #リモートリポジトリからローカルにあるリモートリポジトリのコピーに最新情報をダウンロード→ローカルに反映されているわけではない
$ git merge ブランチ名                           #ローカルブランチに反映する
$ git pull origin ブランチ名                     #fetchとmergeをまとめて実行
```

## 現状を把握するためのコマンド
```
$ git status                                   #add,commitに関するの確認
$ git diff                                     #ワークツリーとインデックスの差分確認
$ git reset HEAD^　　　　　　　　　　　　　　　 　#1つ前のコミットに戻る
$ git remote -v                             　 #現在の紐付き先の確認
```
## チーム開発で使うコマンド
```
git branch develop                           #developブランチの作成
git branch                                   #ブランチ一覧
git checkout develop                         #developブランチに移動
git checkout -b develop2                     #develop2ブランチを作成＆移動
```
## 機密情報などをpushしてしまった場合
GitHubからファイル本体だけでなくcommit履歴も削除し、強制pushを行うorリポジトリを作り直す
```
git reset --mixed ~~(commit_id)             #add,commitを取り消す
git reset HEAD^ 　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　#直前のadd,commitを取り消す
```
ここで "--soft" commitのみor "--hard"ファイル変更,add,comit全てを取り消すコマンドもある "git log" でコミットid確認しよう

## リモートリポを変えたい時
```
git remote set-url origin 変更後のssh
↓アカウント変えるなら以下のようになることも↓
git config --global user.name "Your Name"
git config --global user.email you@example.com
```

