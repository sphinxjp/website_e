===========================
Make document more powerful
===========================

Sphinx has various kind of markups. By using these, you can make
document easily viewable and useful.

Inline markup
======================

There are some simple markups.

.. code-block:: rst

   *emphasis(italics)*

   **strong emphasis (boldface)**

   ``code samples``

   `Text with hyper-link <http://python.org>`_

Code block
==============

ライセンス文の表記や、ソースファイルなどをドキュメント中で表現する、コードブロックがあります。コロンは前の段落の末尾に付けることもできます。また、ブロックの前後には空行を入れてください。

.. code-block:: rst

   ::

      This document is a fiction. 
      登場する人物、企業名は架空のものです。

ソースコードを入れる場合には、言語名を指定することで、コードハイライトが行えるディレクティブがあります。Pygmentsというライブラリを利用しているため、日常使われるプログラミング言語やマークアップなどはかなり網羅しています。

.. code-block:: rst

   .. code-block:: python

      import this

List
======

There are bullet lists, enumerated list, difinition lists.

.. code-block:: rst

   * 宇都宮市
   * 那須塩原市
   * 真岡市

   1. まさし
   2. みんみん
   #. 夢餃子(#を使うと、自動で数字が割り当てられます)

   餃子
      宇都宮の名物として有名。餃子の像もある。静岡の浜松がライバル。
   ジャズ
      宇都宮はジャズの町としても売り出し中。
      楽器メーカーを多数抱える静岡の浜松がライバル
   焼きそば
      知る人ぞ知る宇都宮の名物。専門店多数。なぜかビニール袋で持ち帰る。


Table
========

There are some ways to make table.

Most complicated way
----------------------------

縦横のセルの連結も表現できます。

.. code-block:: rst

   +---------------------+
   |栃木県内の勉強会     |
   +========+============+
   |宇都宮  |集合知勉強会|
   +        +------------+
   |        |Objective-C |
   +--------+------------+
   |西那須野|とちぎRuby  |
   +--------+------------+


Second complicated way
--------------------------

.. code-block:: rst

   =========== ==================================
   勉強会で使う本
   ----------------------------------------------
   言語        本の名前
   =========== ==================================
   Ruby        dRubyによる分散・Webプログラミング
   Python      集合知プログラミング
   Objective-C 詳解Objective-C 2.0
   =========== ==================================

これ以外にもディレクティブを使った方法がいくつかあります。詳細は :ref:`directives` を参照してください。

Directives
==============

Sphinxが利用しているreStructuredTextのもっとも特徴的な機能がディレクティブです。Pythonを利用して新しいディレクティブを作ることもでき、Sphinxの拡張性の高さの源となっています。

ディレクティブの種類は多岐に渡っていて、すべてを詳解するのは難しいので、ここでは3つだけ詳解します。

すべてのディレクティブは次のような構造をしています。

.. code-block:: rst

   .. Directive-name:: Option
      :arguments: 
      :パラメータ付き引数: parameters

      contents

ディレクティブの種類によって、オプションや引数、コンテンツが指定できるかが異なります。

Images
--------

Use ``image`` directive to insert image files.


.. code-block:: rst

   .. image:: fighting_dogs.png

Index
----------

``index`` ディレクティブを設定していくと、索引を作ることができます。階層を持つ索引も表現できます。このディレクティブをセクションタイトル、表、画像などの前に置くことで、それらの要素に対してのリンクが作成されます。

``pair`` と ``triple`` による複数エントリー作成が強力なので、これを使うと、効率よく情報量の豊富な索引を生成できます。

.. code-block:: rst

   .. index:: ベルモール

   .. index::
      pair: 遊園地; 那須ハイランドパーク

   .. index:
      triple: うさぎや; チャット; お菓子

これをビルドすると、6つの索引のエントリーが作成されます。

最初のディレクティブは「ベルモール」という項目が1つだけ作られます。

次のディレクティブは、「遊園地→那須ハイランドパーク」と、「那須ハイランドパーク→遊園地」という、階層を持つエントリーが2つ作られます。

3つめのディレクティブは、「うさぎや→チャット,お菓子」「チャット→うさぎや,お菓子」「お菓子→チャット,お菓子」という3組のエントリーが作られます。

Note
--------

Note and Warning directives create note and warning, as you know.

.. code-block:: rst

   .. note::
      This is Node

   .. warning::
      This is Warning!!

これ以外にも様々な種類のディレクティブがあります。ドキュメントなどを参照して、さまざまな種類のディレクティブを使ってみてください。
