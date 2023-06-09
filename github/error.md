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

強制的にプッシュする方法
```
git push -f -u origin master
```
リモートのorigin/masterにローカルのmasterをpush -fはforse, -uはupsteam「upstream（上流）ブランチを追跡する」
