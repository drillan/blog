.. article::
   :date: 2017-09-03
   :tags: python, miyadaiku

ブログをリニューアルしました
-------------------------------

Miyadaiku に乗り換えた理由
==========================

これまでは静的サイトジェネレータとして `Pelican <http://docs.getpelican.com>`_ を使用していましたが `Miyadaiku <https://miyadaiku.github.io>`_ に乗り換えました。

Miyadaiku は Python 製の静的サイトジェネレータです。当初は ipynb ファイルが最初から扱える `Nikola <https://getnikola.com>`_ に乗り換える予定でしたが、下記のような理由で Miyadaiku を採用しました。

Jinja2 が使える
    Jinja2 は Python 製のテンプレートエンジンです。
    従来の静的サイトやブログでは記事の内容やテンプレートをベタ書きする必要がありました。
    共通部分をテンプレート化することで生産性が上がりそうです。 

Jupyter Notebook に対応
    コンテンツをreStructuredText, Markdown, HTML, YAMLなど、さまざまな形式で記述できます。
    Miyadaiku を使う一番の後押しとなったのは ipynb ファイルに対応したことが決め手となりました。
    元々、この機能はなかったのですが、私が作者の石本さんにお願いしたところ、早速実装していただきました。石本さん、ありがとうございます。
    Jupyter Notebook を記事にすると `こんな感じ <../notebooks/bokeh_sample.html>`_ になります

国産
    OSSの世界において、メイドインジャパンである必要はないと言われて喧しいですが、下記の点は私のような英語が不自由な者にとっては大変ありがたいです。

    * 日本語のドキュメントが最初から用意されている
    * 日本語で問い合わせやリクエストができる
    * マルチバイトの心配が少ない

Python 3.6以降に対応
    後発のツールということもあり、後方互換を気にしなくてよいというのは意外に大きな利点じゃないかと思っています。
    複数のバージョンに対応するには開発コストがかかるだけでなく、潜在的なバグを生むリスクが潜んでいます。
    ソースコードをチラ見したところ、Python 3.6以降でしか使えないような f-strings などが使われており、いい意味で開き直っていてコードリーディングも捗りそうです。

テーマが扱いやすい
    pip からテーマをインストールできます。Python ユーザにとって最も簡明な方法ではないでしょうか？
    Jinja2 を利用してテーマを継承できるため、カスタマイズも容易です。

ちなみに、石本さんが管理されている `python.jp <https://python.jp>`_ も Pelican から Miyadaiku ベースになっています。移行した理由については `ブログ <http://atsuoishimoto.hatenablog.com/entry/2017/08/09/133346>`_ に記載されているので、ご一読をおすすめします。

Miyadaiku の名前
================
| Miyadaiku の名前の由来は、Jinja2 (神社)を使うことから、Miyadaiku (宮大工)と命名されたのではないかなと思われます。
| モジュール名にも `muneage` (棟上げ)や `zichinsai` (地鎮祭)など、専門用語が散りばめられています。

Miyadaiku のテーマ
==========================
Miyadaiku はリリースされたばかりのパッケージということもあり、他の静的サイトジェネレータと比較してテーマが少ない状況です。特に、ブログに関してはテーマがデフォルトのものしかなく、ブログを新規に構築する際にはテーマをかなりいじることになりました。

テーマのバリエーションについては時間が解決すると思いまが、私が新規に実装した機能としてはSNSのシェアボタン[ [#f]_ ]などです。外に出せるようなテーマができたら `PyPI <https://pypi.python.org>`_ に登録する未来があるかもしれません。

.. [#f] まだちゃんと動作確認していないため、どなたかポチッと試していただけると助かります。