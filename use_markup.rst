===========================
Make document more powerful
===========================

..
  Sphinxには様々なマークアップがあります。これを利用すると、見やすく情報量の豊富なドキュメントを作ることができます。

Sphinx has various kind of markups. By using these, you can make
document easily viewable and useful.

Inline markup
======================

..
   太字、斜体、リテラルなどが利用できます。

There are some simple markups.

.. code-block:: rst

   *emphasis(italics)*

   **strong emphasis (boldface)**

   ``code samples``

   `Text with hyper-link <http://python.org>`_

Code block
==============

..
  ライセンス文の表記や、ソースファイルなどをドキュメント中で表現する、コードブロックがあります。コロンは前の段落の末尾に付けることもできます。また、ブロックの前後には空行を入れてください。


There is an Code block which describe licenses or source code in the
document. Colon can be add previous Paragraphs. Empty lines should be
inserted around code block.


.. code-block:: rst

   ::

      This document is a fiction. 
      All characters and companies in this document are fictional.


ソースコードを入れる場合には、言語名を指定することで、コードハイライトが行えるディレクティブがあります。Pygmentsというライブラリを利用しているため、日常使われるプログラミング言語やマークアップなどはかなり網羅しています。

.. code-block:: rst

   .. code-block:: python

      import this

List
======

There are bullet lists, enumerated list, difinition lists.

.. code-block:: rst

   * New York
   * San Francisco
   * San Jose

   1. Zushi Puzzle
   2. Sushi Zone
   #. Ushiwakamaru (#. for auto-numbering)

   Sushi
      Sushi is a Japanese food consisting of cooked vinegared rice (shari)
      combined with other ingredients (neta), usually raw fish or
      other seafood.
   Udon
      Udon is a type of thick wheat-flour noodle of Japanese cuisine.
   Japanese Curry
      Japanese Curry is one of the most popular dishes in Japan, where
      people eat it an average of 84 times a year.


Table
========

There are some ways to make table.

Most complicated way
----------------------------

Grid tables allow arbitrary cell contents (body elements), and both
row and column spans.

.. code-block:: rst

   +---------------------+
   |Tutorials            |
   +========+============+
   |Light   |Python      |
   +Weight  +------------+
   |        |Ruby        |
   +--------+------------+
   |Compile |Objective-C |
   +--------+------------+

Second complicated way
--------------------------

.. code-block:: rst

   =========== ==================================
   Books for Languages
   ----------------------------------------------
   Lang        Book title
   =========== ==================================
   Ruby        The dRuby Book
   Python      Programming Python
   Objective-C Programming in Objective-C
   =========== ==================================

..

  これ以外にもディレクティブを使った方法がいくつかあります。詳細は :ref:`directives` を参照してください。

There are some other ways using directives. See the :ref:`directives`
for more detail.



Directives
==============

Sphinxが利用しているreStructuredTextのもっとも特徴的な機能がディレクティブです。Pythonを利用して新しいディレクティブを作ることもでき、Sphinxの拡張性の高さの源となっています。

ディレクティブの種類は多岐に渡っていて、すべてを詳解するのは難しいので、ここでは3つだけ詳解します。

すべてのディレクティブは次のような構造をしています。

.. code-block:: rst

   .. Directive-name:: Option
      :arguments: 
      :arguments with parameter: parameters

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

