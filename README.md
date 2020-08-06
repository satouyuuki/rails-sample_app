### 使い方
本番のgem以外をインストール
```
$ bundle install --without production
```
データベースへのマイグレーションをかける
```
$ rails db:migrate
```
最後にテストをしてうまく言ってるか
```
$ rails test
```
テストが無事通ったらRailsサーバーを立てる
```
$ rails server
```
