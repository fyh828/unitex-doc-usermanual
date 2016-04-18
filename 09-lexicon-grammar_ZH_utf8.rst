语法和词汇
==========

词典 -
语法表是表示语言的元素的句法属性的一个紧凑的方式。能够通过一个参数化机构自动构建从这些表中的本地文法，图表。

。第二部分介绍了参数化图形和从语法词汇表生成图形自动机制。

语法词汇表
----------

语法词汇已被Maurice Gross和他的团队开发了一种方法LADL
(:raw-latex:`\cite{L}`, :raw-latex:`\cite{BGL}`,
:raw-latex:`\cite{methodes-en-syntaxe}`, :raw-latex:`\cite{GL}`,
:raw-latex:`\cite{gross1994}`, :raw-latex:`\cite{gross1994b}`,
:raw-latex:`\cite{gross1991}`, :raw-latex:`\cite{gross1986}`,
:raw-latex:`\cite{gross1984}`, :raw-latex:`\cite{gross1984b}`,
:raw-latex:`\cite{gross1983}`, :raw-latex:`\cite{gross1982}`,
:raw-latex:`\cite{gross1978}`, :raw-latex:`\cite{leclere2005}`,
:raw-latex:`\cite{salkoff2004}`)
主要原则是每个动词几乎单一的语法属性。因此，这些性能必须系统描述的，因为它是不可能预测动词的精确的行为。这些系统的描述是通过矩阵，其中的行对应的动词，和列语法属性表示。所考虑的特性是正式性能如由动词允许添加和所述不同的转换，这动词可经历（被动，名词，外位等）的数量和性质。矩阵通常也称为表，是二进制：一个符号\ ``+``\ 如果动词检查属性，标志\ ``-``\ 出现在一个行的交叉点和属性的列，否则用。有关更多信息，语法属性看\ http://infolingu.univ-mlv.fr\ ，其中词汇，语法表都可以免费下载。

(:raw-latex:`\cite{these-annie}`),表语(:raw-latex:`\cite{les-nominalisations}`,:raw-latex:`\cite{les-predicats-nominaux}`,
:raw-latex:`\cite{giry1978}`, :raw-latex:`\cite{gross1976}`,
:raw-latex:`\cite{ranchhod2001}`), adverbes
(:raw-latex:`\cite{syntaxe-de-ladverbe}`,
:raw-latex:`\cite{grammaire-des-adverbes}`), ou les expressions figées,
dans de nombreuses langues
(:raw-latex:`\cite{lexique-grammaire-allemand2}`,
:raw-latex:`\cite{lexique-grammaire-italien2}`,
:raw-latex:`\cite{lexique-grammaire-italien}`,
:raw-latex:`\cite{lexique-grammaire-coreen2}`,
:raw-latex:`\cite{lexique-grammaire-coreen}`,
:raw-latex:`\cite{lexique-grammaire-malgache}`,
:raw-latex:`\cite{lexique-grammaire-espagnol}`,
:raw-latex:`\cite{lexique-grammaire-allemand}`,
:raw-latex:`\cite{lexique-grammaire-hongrois}`,
:raw-latex:`\cite{ranchhod1996}`, :raw-latex:`\cite{ranchhod1991}`,
:raw-latex:`\cite{gross1986b}`).

图 [fig-table-32NM]显示语法词汇的列表。此表涉及动词承认数字的补充。

.. figure:: resources/img/fig8-1.png
   :alt: Table de lexique-grammaire 32NM[fig-table-32NM]
   :width: 15.00000cm

   Table de lexique-grammaire 32NM[fig-table-32NM]

Conversion d’une table en graphes
---------------------------------

Principe des graphes paramétrés
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

变换的图表是由图机构的装置
设置。其原理是：我们建立一个描述可能的结构图。此图通过变量引用表列。然后对表中，该曲线图，其中，变量根据位于对应的列的交叉点，并经处理的线的单元中的内容置换的副本中的每一行生成。如果表格单元格中包含的标志\ ``+``\ 相应的变量由\ ``>``\ 取代。如果单元格包含符号\ ``-``,含有相应变量的框被删除，同时删除这个框的路径。在所有其他情况下，该变量修改为被替换的单元的内容。

表的格式
~~~~~~~~

词汇，语法表使用电子表格程序通常编码比如OpenOffice.org Calc
(:raw-latex:`\cite{OpenOffice}`).要使用Unitex，该表必须在Unicode文本使用以下约定编码：列必须在标签和行由回车符分隔。

.org
Calc的表，保存文本文件(拓展名为\ ``.csv``)。然后该程序通过提供类似图 [fig-csv-export].窗口设置备份。选择编码“Unicode”，选择制表符分隔列，不指定文字分隔符。

.. figure:: resources/img/fig8-2.png
   :alt: 使用OpenOffice.org Calc的备份配置表[fig-csv-export]
   :width: 12.00000cm

   使用OpenOffice.org Calc的备份配置表[fig-csv-export]

，Unitex跳过第一行，考虑给予列的标题。因此，您必须确保列的标题正好占据一行。如果没有标题行，表中的第一行会被忽略，并且有几个头线，它们将来自第二线条被解释表。

图的参数
~~~~~~~~

参数化曲线是显示在参照表语法词汇的列中的变量的曲线图。通常使用这种机制与语法图，但没有什么会阻止建立参数化图形，或预处理标准。

``@``\ 其次是用大写字母列名（列的编号从\ ``A``).

例子： ``@C``\ 参照该表的第三列。

``+`` 或 ``-``\ 代替， ``-``\ 标记对应于通过这个变量去除的方式。
有可能通过字符前述执行反向操作
``@``\ 一个感叹号。在这种情况下，这是当变量是指标志\ ``+``\ 路径被删除。如果变量返回或标志既不是\ ``+``\ ，也不是
``-``,它是由格子中的替换内容。

``@%``
，这是由在表中的行号代替。它的值是每行不同的事实允许使用容易地表征的线。这个变量不会受到感叹号的在左边。

图 [fig-reference-graph]给出了示例参数化的曲线图，旨在被应用到如图 [fig-table-31H]词库的无关文法表中的31H表。

.. figure:: resources/img/fig8-3.png
   :alt: 图的参数的实例[fig-reference-graph]
   :width: 15.00000cm

   图的参数的实例[fig-reference-graph]

.. figure:: resources/img/fig8-4.png
   :alt: 词汇语法31H表[fig-table-31H]
   :width: 15.00000cm

   词汇语法31H表[fig-table-31H]

自动生成图像
~~~~~~~~~~~~

从参数化图形和表格生成图表，它必须首先通过点击菜单中的“词汇，语法”打开表“打开...”（参见 [fig-lexicon-grammar-menu]）。该表必须已转换为Unicode文本。

.. figure:: resources/img/fig8-5.png
   :alt: Menu “Lexicon-Grammar”[fig-lexicon-grammar-menu]
   :width: 12.00000cm

   Menu “Lexicon-Grammar”[fig-lexicon-grammar-menu]

（见图 [fig-table-display]）选定的表格显示在一个窗口。如果它不显示在屏幕上，它可以被其他窗口Unitex被隐藏。

.. figure:: resources/img/fig8-6.png
   :alt: Displaying a table[fig-table-display]
   :width: 15.00000cm

   Displaying a table[fig-table-display]

要自动生成一个参数化图形图表，请点击“编译到GRF...”，从“词汇，语法”菜单。出现如图[fig-configuration-graph-generation]。

.. figure:: resources/img/fig8-7.png
   :alt: 确认自动生成图像[fig-configuration-graph-generation]
   :width: 9.00000cm

   确认自动生成图像[fig-configuration-graph-generation]

“参考图形（在GRF格式）”，然后设置为使用图的名称。在“结果GRF语法”中，指定将要生成的主图的名称。主图表是利用已生成的所有图的曲线图。通过搜索这个图形文字，你会同时应用和所有生成的图表。

设置“子图名”让你指定要生成的图的名称。可以肯定，所有的图形都会有不同的名称，建议使用变量\ ``@%``\ ，这个变量将被替换为通过它的数字每个输入，以确保所有的图表都不同的名称。例如，如果填充的名称帧“``TestGraph.grf``”，并且如果子图被命名为“``TestGraph_@%.grf``”，从16产生的子图16线将被命名为“``TestGraph_0016.grf``”。

图[fig-archaiser]
和图[fig-badauder]表明通过施加图的参数化曲线产生两个图 [fig-reference-graph]在表31H.

图 [fig-main-graph]显示获得的主要图。

.. figure:: resources/img/fig8-8.png
   :alt: 对于动词生成的图表 ``archaiser``\ [fig-archaiser]
   :width: 15.00000cm

   对于动词生成的图表 ``archaiser``\ [fig-archaiser]

.. figure:: resources/img/fig8-9.png
   :alt: 对于动词生成的图表 ``badauder``\ [fig-badauder]
   :width: 15.00000cm

   对于动词生成的图表 ``badauder``\ [fig-badauder]

.. figure:: resources/img/fig8-10.png
   :alt: 主图调用所有生成的图[fig-main-graph]
   :width: 10.00000cm

   主图调用所有生成的图[fig-main-graph]
