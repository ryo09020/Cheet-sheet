# GitHubとの連携

- [1. GitHubの接続に必要な鍵の作成](#1-githubの接続に必要な鍵の作成)
- [2. 公開鍵をGitHubに登録](#2-公開鍵をgithubに登録)
- [3. GitHubとの接続確認](#3-githubとの接続確認)

## 1. GitHubの接続に必要な鍵の作成
```
username:~ $ ssh-keygen
```

 ターミナルに以上のコードを入力します。実行後に入力を求められますが、全て未入力で Enter キーを押してください。以上で公開鍵、秘密鍵を生成しました。
ちなみに
```
ls ~/.ssh
```
を打ち込むことで生成されたかの確認ができます。「id_rsa」(秘密鍵)と「id_rsa.pub」(公開鍵)が生成されていれば問題ありません。

## 2. 公開鍵をGitHubに登録
```
username:~ $cat ~/.ssh/id_rsa.pub
```
これを実行し、「ssh-rsa ~~~~~~~　」をコピーし、GitHubブラウザで右上の自分のアイコンから「Settings」を選択し、左側に表示されるメニューで SSH and GPG keys を選択し、New SSH key ボタンを選択。

その後,以下を設定しAdd SSH keyを選択

Title：どの PC の鍵かを区別します。分り易い名前を入力

Key type：[Authentication Key]を選択

Key：コピーした公開鍵の中身を貼り付ける

## 3. GitHubとの接続確認
```
username:~/environment $ ssh -T git@github.com
Hi username! You've successfully authenticated, but GitHub does not provide shell access.
```
2行目の記述がでできたら成功！！
