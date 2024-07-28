# gitのエラー集
## 1. ローカルのコミット履歴と、リモートのコミット履歴が同一でない
この時以下のエラーが出る。
```
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'github.com:~~~.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

```

### 解決方法1: 強制的にプッシュする方法(あまりお勧めしない)
```
git push -f -u origin master
```
リモートのorigin/masterにローカルのmasterをpush -fはforse, -uはupsteam「upstream（上流）ブランチを追跡する」
この方法だとリモートのコミットたちはローカルのコミットに上書きしてしまうのでリモートの変更も残してローカルのコードを反映したい時は以下のように行う。

### 解決方法2: ローカルとリモートのブランチをmergeすることで解決
```
git merge origin origin/main
```
このコードはリモートのmainブランチ情報をローカルのoriginにmergeさせようとするもの


この後にローカル行でマージエディターができるのでそこから必要なものを残していらない方を消す作業を行う。

最後にcommitしてpushすることを忘れないようにしましょう。

## 2. チーム開発においてのエラーたち
