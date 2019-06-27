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

* webpackのインストール

```
$ bin/rails webpacker:install
```

* JavaScriptパッケージのインストール

```
$ bin/yarn install
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

* プロセスを起動

```
$ bundle exec unicorn -c config/unicorn.rb -D
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

1. https://qiita.com/syou007/items/555062cc96dd0b08a610