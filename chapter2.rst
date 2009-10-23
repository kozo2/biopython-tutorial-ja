.. image:: biopython.jpg

.. Overview

.. index::
   single: Biopython; 2章 クイックスタート

2章 クイックスタート
====

.. This section is designed to get you started quickly with Biopython, and to give a general overview of what is available and how to use it. All of the examples in this section assume that you have some general working knowledge of Python, and that you have successfully installed Biopython on your system. If you think you need to brush up on your Python, the main Python web site provides quite a bit of free documentation to get started with (http://www.python.org/doc/).

この節はBiopythonをすばやく始め、何ができるかや、どのように使うかを全体的につかむためのものです。この節の例はあなたがPythonの一般的な知識を持っていること、そしてBiopythonのインストールに成功していることを仮定しています。もしあなたがPythonについて学び直す必要があるなら、Pythonのメインウェブサイトでは問題を解決するためのフリーなドキュメントがたくさん提供されています(http://www.python.org/doc/)。

.. Since much biological work on the computer involves connecting with databases on the internet, some of the examples will also require a working internet connection in order to run.

多くのバイオインフォマティクス作業はインターネット上のデータベースとつなぐ作業を含みます。またいくつかの例は実行にネット接続が必要となるでしょう。

.. Now that that is all out of the way, let’s get into what we can do with Biopython.

それではBiopythonでできることを身につけてみましょう。

.. index::
   pair: 全体像; biopython

2.1 Biopythonパッケージの全体像
---------------------------------

.. As mentioned in the introduction, Biopython is a set of libraries to provide the ability to deal with “things” of interest to biologists working on the computer. In general this means that you will need to have at least some programming experience (in Python, of course!) or at least an interest in learning to program. Biopython’s job is to make your job easier as a programmer by supplying reusable libraries so that you can focus on answering your specific question of interest, instead of focusing on the internals of parsing a particular file format (of course, if you want to help by writing a parser that doesn’t exist and contributing it to Biopython, please go ahead!). So Biopython’s job is to make you happy!

イントロで述べたように、Biopythonは計算機を用いて仕事する生物学者にとって興味深そうなことを処理するためのライブラリです。これはあなたがいくらかのプログラミング経験(もちろんPythonにおいてです!)もしくはプログラムを学ぶことにすくなくとも興味がある必要があることを意味します。Biopythonの仕事は、特定のファイルフォーマットの内部を気にすることなく(もちろんあなたがBiopythonに無いパーサーを書くことでBiopythonを助け、貢献してくれるならどうぞ!)あなたにとって興味がある問題に答えることができるように再利用可能なライブラリを提供することでプログラマとしてのあなたの仕事をより簡単にすることです。Biopythonの仕事はあなたを幸せにすることなのです!

.. One thing to note about Biopython is that it often provides multiple ways of “doing the same thing.” Things have improved in recent releases, but this can still be frustrating as in Python there should ideally be one right way to do something. However, this can also be a real benefit because it gives you lots of flexibility and control over the libraries. The tutorial helps to show you the common or easy ways to do things so that you can just make things work. To learn more about the alternative possibilities, look in the Cookbook (Chapter 14, this has some cools tricks and tips), the Advanced section (Chapter 16), the built in “docstrings” (via the Python help command, or the API documentation) or ultimately the code itself.

Biopythonについて注意すべきことの一つは"同じことをする"方法をしばしば複数提供しているということです。最近のリリースにおいては改善していますが、このことは何かをする正しい方法はひとつであるべきというPythonの思想においていらだたしいことです。しかしながら、これは実に利点ともなり得ます、なぜならそれは柔軟性とライブラリのコントロールを与えてくれるからです。さらなる可能性について学ぶには、クックブック(14章、ここにはいくつかのこつやヒントがあります)、より進んだ節(16章)、ビルトインの"docstrings"(Pythonのヘルプコマンドもしくは\ `APIのドキュメンテーション <http://biopython.org/DIST/docs/api/>`_\)、最終的にはコードそのものを見てください。

.. index::
   pair: 全体像; biopython

2.2 配列でお仕事
---------------------------------

.. Disputably (of course!), the central object in bioinformatics is the sequence. Thus, we’ll start with a quick introduction to the Biopython mechanisms for dealing with sequences, the Seq object, which we’ll discuss in more detail in Chapter 3.

議論の余地はあるかもしれませんが、バイオインフォマティクスにおける中心課題は配列です。それ故、私達はBiopythonの配列を扱う機能で手短なイントロを始めたいと思います。それはSeqオブジェクトというもので3章でより詳しく議論します。

.. Most of the time when we think about sequences we have in my mind a string of letters like ‘AGTACACTGGT’. You can create such Seq object with this sequence as follows - the “>>>” represents the Python prompt followed by what you would type in:
