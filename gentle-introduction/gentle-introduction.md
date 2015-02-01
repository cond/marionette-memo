# Backbone.Marionette.js: A Gentle Introductionのメモ

## 基本的なスタイル(構成)

### モジュール分け

* データ(モデル、コレクション)は、Entityモジュールに置く
* 機能(サブアプリケーションと呼んでいる)ごとに、モジュールに分ける
  * 例えば、ユーザ一覧表示画面、ユーザ情報画面を、それぞれモジュールにする感じ

### 各画面(機能)の実装

## テクニック

* [テーブルの行のクリックで色(属性)が変わるようにする](#click_change_color)
* [テーブルの行を削除する際に、フェードアウト効果をつける](#fade_out)

## コミットごとのメモ

主なコミットごとに、ソースに注釈を記入してある。

https://github.com/cond/marionette-gentle-introduction/commits/master

### コンタクト先一覧を表示する

**テキスト**: "Structuring Code with Modules"の完了時点(p45)

**ソース**: [refactor app into modules](https://github.com/cond/marionette-gentle-introduction/commit/c2e8c43f38ba357417a828c09ec4152fcf723807)

コンタクト先3件(データは決め打ち)を画面に表示する。

* CollectionViewを使っている。

### CompositeViewを使って一覧を表示する

**テキスト**: "Using a CompositeView"の完了時点 (p49)

**ソース**: [display contacts list using a CompositeView](https://github.com/cond/marionette-gentle-introduction/commit/2b009b3893dcf3ad6c48ff6617b2d12475f8c669)

* CollectionViewの代わりに、CompositeViewを使うようにした
* HTML的には`<ul>`でなく、`<table>`を使って表示する

<a name="click_change_color"></a>
### テーブルの行をクリックするとハイライトをオン/オフする

**テキスト**: ”Using Events”の完了時点 (p51)

**ソース**: [toggle highlighting on clicked row](https://github.com/cond/marionette-gentle-introduction/commit/443967a2670e69bc1e2e9addb361c7c0d3e80568)

* テーブルの行をクリックすると、ハイライトがオン/オフされる。
* 実装は、ItemViewでclickイベントを拾って、warningクラスをトグルさせている。

<a name="fade_out"></a>
### データの削除機能を実装した

**テキスト**: "Animating the Removed ItemView"まで完了 (p61)

**ソース**: [removing a contact from the collection](https://github.com/cond/marionette-gentle-introduction/commit/2ad473c38c9f67328e24d6c866578791eacc0d9c)

* Deleteボタンをクリックすると、データを削除する。
* 削除の際に、フェードアウトのアニメーション効果を表示する。


### 個別レコード表示画面を実装した

**テキスト**: "Displaying Contacts in Dedicated Views" まで完了 (p68)

**ソース**: [display contact in dedicated view](https://github.com/cond/marionette-gentle-introduction/commit/c7322097ace71fee3047aaa341ceba274f36bfd3)

* 一覧画面で、Showボタンをクリックすると、そのレコードの内容が表示される
* 個別レコード表示画面のコントローラとビューは Showモジュールで定義している。
* このバージョンではルータを使っていないので、URLは変わらないままである。
