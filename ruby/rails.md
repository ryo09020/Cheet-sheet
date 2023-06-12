## Railsアプリケーションの作成

- Appのひな形の作成
```
rails new アプリ名
```

- controller作成
```
rails g controller コントローラ名(複数形&小文字)
```

- controller作成と同時にアクション、必要なviewとRouting作成方法
```
rails g controller コントローラ名　アクション名たち
```

- model作成
```
rails g model   モデル名(単数形&1文字目大文字)
rails db:migrate　　　　　　　　　　　　　　　  　　　　　　 #テーブル作成
```




## routingの書き方
下の2行は同じ意味
```
HTTPメソッド 'URL' => 'コントローラ#アクション'
get 'homes/top' => 'homes#top'
get 'homes/top'
```

## 　git clone してからアプリを立ち上げるまで
```
bundle install
yarn add @babel/plugin-proposal-private-methods @babel/plugin-proposal-private-property-in-object
rails db:migrate RAILS_ENV=test
```



## ミスったら集

```
rm -rf アプリ名　　　                                  #アプリ削除
```
```
rails d controller コントローラ名　　                        #コントローラ削除
```
```
rails g migration Addカラム名Toテーブル名 カラム名:型名      #カラム追加
→rails g migration AddNameToUsers name:string

rails g migration Removeカラム名Fromテーブル名 カラム名:型名 #カラム削除
```
```
rails routes                                                #routing確認
```
```
rails db:migrate:status                                     #現状どこまでmigratefileが読み込まれているか確認できる
```
```
rails db:migrate:reset                                     #現状のDBの環境を破棄し、新しくmigratefileからDBの作成
```
```
$ rails db:rollback                                      # 最新のmigrationファイルのstatusをupからdownに変更
$ rails db:rollback STEP=〇　←戻したいファイルの個数    #いくつかのmigrationファイルをまとめてdownにしたいとき
$ rails db:migration:down VERSTION= ◯◯ ← MigrationID  ## 特定のmigrationファイル一つのみdownにしたいとき
```
