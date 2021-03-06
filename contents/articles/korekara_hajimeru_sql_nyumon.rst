.. article::
   :date: 2018-05-13
   :tags: sql


=========================
これからはじめる SQL 入門
=========================

`Jupyter本 <https://amzn.to/2KfiNmE>`_ の共著者である `池内さん <https://twitter.com/iktakahiro>`_ よりご恵贈いただきました。池内さんありがとうございます。

.. image:: http://image.gihyo.co.jp/assets/images/cover/2018/9784774196879.jpg
   :width: 50%
   :target: https://amzn.to/2wxP5Hr

誰に向けての本か
================

| タイトルのとおり、これからSQLを学びたいかたにとってはぴったりな内容です。
| 本書のはじめににも書かれておりますが、SQLは営業やマーケティング部門も扱うようになってきました。
| SQLを学ぶ上で専門用語がハードルとなりそうですが、本書では平易な表現で解説されており、ITになじみがないかたでも理解しやすい内容になっているのではないでしょうか。
| 
| すでにある程度SQLに通じているかたでも、基礎から復習したい場合にもよさそうです。私自身、SQLは少々触っていますが、SQL文を記述するに当たってのお作法など、学びになった点が随所にありました。
| 
| 本書はPostgreSQLを元にしていますが、他のRDBMSの場合についてもある程度触れているため、私のようなMySQLなどのユーザにとっても特に抵抗なく読める内容となっています。

環境構築
========

| SQLを学ぶに当たって、最初に乗り越えないといけない壁が環境構築です。プラットフォームやOSのバージョンなどによって導入手順がことなることがあるため、書籍で解説しようとすると非常に悩ましところですが、本書では仮想マシン(VirtualBos)を採用することで手順を統一化しています。
| 
| ほかにもDocker環境が準備されており、 `著者のGitHubリポジトリ <https://github.com/iktakahiro/sql-basic-book>`_ で導入方法が解説されています。
| 私は後者のDocker環境で導入しましたが、いくつかはまりどころがあったためフィードバックする予定です。 [#f1]_

本書の魅力
==========

さいごに本書を通読して、個人的に参考になった点を挙げてみます。読者によっては別な視点での学びがあると思います。SQLを学びたいかた、復習したいかたはぜひ本書を手にとって見てください。

SQL文のお作法
-------------

はじめの内は下記のようなSQLを書いてしまうことはままありますが、注意する点や推奨する書き方が解説されていたので参考になりました。

- 可読性の低下
- 意図しないクエリ
- 無駄なコスト

データ型の使い分け
------------------

データ型について紙面を割いて丁寧に解説されています。特にJSON型については知らなかったため、今後使ってみようと思いました。

複雑なクエリ
------------

本書の後半ではJOINやサブクエリなど、SQL文が複雑になってきます。使いこなせば便利なのはわかっているが、なかなか使いこなせないというケースはままありそうです。本書では長いSQL文を分割して実行し、解説されているため、いままで挫折した人も改めて挑戦してもよいのではないでしょうか。

.. [#f1] フィードバックしたものの内、クリティカルなものは即時修正していただきました。早速のご対応ありがとうございます。