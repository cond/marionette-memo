# Backbone.Marionette.js: A Gentle Introductionのメモ

## 基本的なスタイル(構成)

### モジュール分け

* データ(モデル、コレクション)は、Entityモジュールに置く
* 機能(サブアプリケーションと呼んでいる)ごとに、モジュールに分ける
  * 例えば、ユーザ一覧表示画面、ユーザ情報画面を、それぞれモジュールにする感じ

### 各画面(機能)の実装



## コミットごとのメモ

コミットごとに、ソースに注釈を記入してある。

https://github.com/cond/marionette-gentle-introduction/commits/master

### コンタクト先一覧を表示する

**テキスト**: "Structuring Code with Modules"の完了時点(p45)

**ソース**: [refactor app into modules](https://github.com/cond/marionette-gentle-introduction/commit/c2e8c43f38ba357417a828c09ec4152fcf723807)

コンタクト先3件(データは決め打ち)を画面に表示する。

* CollectionViewを使っている。

