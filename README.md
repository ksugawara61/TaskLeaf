# TaskLeaf

Ruby on Railsで構築したタスク管理用のWebサイトです。

## 環境

| 項目 | バージョン |
| :--- | :--- |
| Ruby | 2.5.1 |
| Ruby on Rails | 5.2.3 |
| Unicorn | 5.5.1 |

## セットアップ

* ``bundle install``

```
$ bundle install --path vendor/bundle
```

* JavaScriptパッケージのインストール

```
$ bin/yarn install
```

* Databaseの設定

```
$ RAILS_ENV=development bin/rake db:create db:migrate db:seed
```

## 実行コマンド

* 開発環境の実行

```
$ bin/rails s
```

* テストの実行

```
$ bundle exec rspec spec 
```

* アセットのプリコンパイル

```
$ bin/rails assets:precompile
```

### Unicorn関連

* プロセスを起動<br>
  ``-E`` オプションで実行環境を設定可能

```
$ bundle exec unicorn -c config/unicorn.rb -D -E development
```

* プロセスの停止

```
$ kill -QUIT `cat ./tmp/pids/unicorn.pid`
```

* プロセスの再起動

```
$ kill -HUP `cat ./tmp/pids/unicorn.pid`
```

* プロセスの緩やかな再起動

```
$ kill -USR2 `cat ./tmp/pids/unicorn.pid`
```

## 参考文献

1. 大塚隆弘、 依光奏江、 銭神裕宜、 櫻井達生、 松本拓也、 大場寧子、 小田井優、 小芝美由紀, 現場で使えるRuby on Rails 5 速習実践ガイド: 5.2対応, 2019.
2. Unicorn設定のまとめ - Qiita, https://qiita.com/syou007/items/555062cc96dd0b08a610, Online; accessed 27-June-2019.
