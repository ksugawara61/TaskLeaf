# TaskLeaf

Ruby on Railsで構築したタスク管理用のWebサイトです。

## 環境

| 項目 | バージョン |
| :--- | :--- |
| Ruby | 2.5.1 |
| Ruby on Rails | 5.2.3 |

## セットアップ

* ``bundle install``

```
$ bundle install --path vendor/bundle
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
