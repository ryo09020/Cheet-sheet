# Pythonの環境構築
## 前提
Homebrewのinstallが完了している
```
brew doctor      #Homebrewの確認
```
## 1. pyenvのインストール
```
brew install pyenv
echo 'eval "$(pyenv init --path)"' >> ~/.zprofile
echo 'eval "$(pyenv init -)"' >> ~/.zshrc
```
## 2. pyenvでpython.verを切り替える
インストール可能なバージョンの一覧を表示
```
pyenv install --list
```
pythonのバージョンインストール
```
pyenv install 3.11.3<versionを埋める>
```
インストールされているバージョンを見る
```
pyenv versions
```
最後にバージョンの切り替え
```
pyenv global 3.11.3
```

## シェル　bash→zsh
```
chsh -s /bin/zsh
echo $SHELL
```
