语法规则
========

语法是代表大多数的语言现象的有效方式。第一部分介绍从形式上来说这些都是基于语法。然后，我们将看到如何建立和现在用Unitex的语法。

语法规范化
----------

上下文无关文法
~~~~~~~~~~~~~~

在Unitex语法是代数文法的变体，也被称为上下文无关文法。代数语法包括重写规则。这里是一个匹配任何数目的字符\ :math:`a`:语法。

:math:`S` :math:`aS`

:math:`S`

*非终端符号*
因为它们可以被重写。不能由规则重写符号称为\ *非终端符号*.成员权利规则非终端及终端的符号序列。Epsilon符号记为 
表示空词。在上面\ :math:`S`\ 语法是一个非终端符号和\ :math:` A `\ 终端。
:math:` S`\ 可以写成无论是在\ :math:` A `\ 随后\ :math:` S`\ 或一句空话。通过规则的应用程序的重写操作是被称作\ *分流*\ 。我们把一个语法识别的单词，如果有产生字推导的序列。非终端用作在第一分支的起始点被称作\ *公理*.

*aa*\ ，因为你可以通过执行以下分支得到关于\ :math:`S`\ 的公理：

公理 1: 改写成\ :math:`aS`\ 形式

:math:`aS`

公理 2: 把 :math:`S` 右边的成员改写成\ :math:`aS`

:math:`S` :math:`a` :math:`aaS`

公理 3: 把 :math:`S`\ 改写成

:math:`S` :math:`aS` :math:`aa` :math:`aa`

*一个语法的语言*\ 称为经其认可的所有单词。代数语法识别的语言被称为\ *代数语言*\ 或\ *上下文无关语言*.

广义的上下文无关文法
~~~~~~~~~~~~~~~~~~~~

扩展代数语法是代数语法，其中成员的权利规则是符号，不过正则表达式的多个序列。
因此，语法识别的\ :math:` A `\ 任何序列可以在单个规则的扩展语法被重写：

:math:`S` :math:`a*`

*递归转换* (*英文缩写RTN*) 或
*语法图*,用作一个用户友好的图形界面。事实上，规则的权利可以通过其名称是规则的左侧的图形来表示。

，Unitex文法是不完全广泛上下文无关文法，因为它们整合\ *转译*\ 的概念.这个概念，从有限自动机借来的，也就是说，语法可以产生输出。为了清楚起见，我们将使用语法术语或图形。当一个语法将产生的输出中，我们使用的术语\ *transducteur*,
在有限状态自动机的领域延伸的换能器的定义。

编辑图表
--------

创建图表
~~~~~~~~

要创建一个图表，请单击“FS图”菜单中的“新建” ([fig-fsgraph-menu]).

.. figure:: resources/img/fig5-1.png
   :alt: FS图菜单[fig-fsgraph-menu]
   :width: 13.00000cm

   FS图菜单[fig-fsgraph-menu]

，我们看到一个窗口出现在图 [fig-new-graph].

.. figure:: resources/img/fig5-2.png
   :alt: 空白图[fig-new-graph]
   :width: 14.50000cm

   空白图[fig-new-graph]

，必须转换为Unicode。转换方法是相同的，作为文字（见 [section-conversion-texte-unicode]).

箭头符号表示图表的\ *初始状态*\ 。由含有方形圆的初始符号是 *最终状态*
图表的最终状态。最后文法识别由路径从初始状态描述到最终状态序列。

，单击窗口中同时按下Ctrl键。
你会看到一个蓝色的方形象征产生的空的框（见图 [fig-box-creation]）.当创建一个框，后者被自动选择。

.. figure:: resources/img/fig5-3.png
   :alt: 创建框[fig-box-creation]
   :width: 14.50000cm

   创建框[fig-box-creation]

，窗口的顶部（图 [fig-box-creation]）.
该套装包含符号\ ``<E>``\ 它代表了空词。更换用符号本文\ ``I+you+he+she+it+we+they``\ ，然后按Enter键确认。你已经创建了一个包含七行一个对话框（见图 [fig-pronoun-box]).

.. figure:: resources/img/fig5-4.png
   :alt: 包含框
   :width: 14.50000cm

   包含框

``I+you+he+she+it+we+they``\ [fig-pronoun-box]

事实上，字符\ ``+``\ 作为分隔符。是因为它没有连接到任何其他的框显示为红色文本行。
经常使用的这种类型的框中插入一个图形注释。

，您必须创建一个框，与动词/
:math:`开始。框的文本是绿色的，并且可以包含空行。
这个框不能要么转型传入或传出过渡（见图~/ref{comment-box}).

\begin{figure}[!h]
\begin{center}
\includegraphics[width=12.5cm]{resources/img/fig5-4b.png}
\caption{包含注释的框\label{comment-box}}
\end{center}
\end{figure}
%\clearpage

\bigskip
\noindent为了一框连接到另一个，则必须点击开始框，然后在目标框。\index{Graphe!connexion des boîtes}\index{Boîtes!connexion}
如果已经有两个框之间的过渡，后者被去除。这是可能
在目标中执行，首先单击此相同的操作，然后按开始框，同时按下Shift键。
在我们的例子中，一旦连接到初始状态和图形的最终状态的方块中，
我们得到图~\ref{fig-pronoun-graph}:

\begin{figure}[!ht]
\begin{center}
\includegraphics[width=14.5cm]{resources/img/fig5-5.png}
\caption{英语代词的图形识别\label{fig-pronoun-graph}}
\end{center}
\end{figure}

\bigskip
\noindent注：如果您双击一个框，该框将连接到它本身（见图~\ref{fig-loop-box}）.要取消，再次框上的双击。
\bigskip
\begin{figure}[!h]
\begin{center}
\includegraphics[width=4.5cm]{resources/img/fig5-6.png}
\caption{Boîte reliée à elle-même\label{fig-loop-box}}
\end{center}
\end{figure}

\noindent点击“另存为...”，从“FSGraph”菜单来保存图。\index{Graphe!enregistrement}.默认情况下，Unitex提供了保存在子目录\verb+Graphs+的图形。\index{Répertoire!personnel de travail}你可以看到，如果图形通过检查图表标题的最后一个记录后改变包含文本 \verb+(Unsaved)+.

\bigskip
\noindent  一个图可能包含循环。环路可以环绕单框，如图.~ref{fig-loop-box}或更多，如图~\ref{multi-selection}所示。循环的内容将认识到任何数目的顺序次。我们可以对的次数设置限制，但仅用于围绕单个框的循环：参见~\ref{nb-repetitions}.

%%%%%%%%%%%%%%%%%%%%%%%
\bigskip
\noindent当改变一个图，我们可以证明，单击鼠标右键，右键菜单，可以执行最常见的操作〜（图~\ref{contextual-menu}）：

\bigskip
\begin{figure}[!h]
\begin{center}
\includegraphics[width=7.5cm]{resources/img/fig5-6b.png}
\caption{上下文菜单\label{contextual-menu}}
\end{center}
\end{figure}

\begin{itemize}
\item 创建一个框
\item 保存或打印当前图表或修改页面设置项目常用的菜单“工具”和“格式”“放大”是在菜单中也提供“FS图”\end{itemize}
如果选择了一个或多个方框，以下菜单变为可用，并且可以对这个组的框执行若干类型的操作。否则，他们是无用的，因此无效。\begin{itemize}
\item 关于所选框用输入变量的定义 \index{Variable!d'entrée}
或输出部分\index{Variable!de sortie}分隔符或形态模式所指的上下文的输出。这些操作也可以用图形窗口的编辑工具栏（见~\ref{toolbar-commands}）. 
\item 合并选定框
\item 在新图中导出选定框
\end{itemize}


%%%%%%%%%%%%%%%%%%%%%%%%


\subsection{子图}
\label{section-subgraphs}
\index{Graphe!appel à un sous-graphe}\index{\verb+:+}
要调用一个子图，由字符\verb+:+ 前面表示在一个框里他的名字。如果你在框中输入：

\medskip
\verb`\ alpha+:beta+gamma+:E:.grf\ :math:`

\medskip
\noindent你会得到类似于图~\ref{fig-subgraph-call}的框.

\begin{figure}[h]
\begin{center}
\includegraphics[width=6cm]{resources/img/fig5-7.png}
\caption{子图上绘制图表 \texttt{beta} et
\texttt{delta}\label{fig-subgraph-call}}
\end{center}
\end{figure}

\noindent您可以指定图形的全名
(\verb`\ E:.grf\ :math:`)或简单地不带路径的名称
 (\verb`\ beta\ :math:`);在这种情况下，子图被假定为在相同的目录中引用它的曲线图。这是不建议，因为它破坏了其便携使用使用绝对路径图的名字。如果您使用绝对图的名字来操作 \verb+E:\greek\delta.grf+ 图形编译器发出警告（见图〜\ref{fig-warning-absolute-graph-name}).

\begin{figure}[!h]
\begin{center}
\includegraphics[width=14.5cm]{resources/img/fig5-8.png}
\caption{对非便携式图形名称报错\label{fig-warning-absolute-graph-name}}
\end{center}
\end{figure}

\bigskip
\noindent为便携的同样的原因，建议使用\verb+\+或 \verb+/+作为图形名称的隔板。相反，它是使用器的\verb+:+好：无论你的工作系统。我们也可以看到在图
~\ref{fig-warning-absolute-graph-name}这就是分离器由图形编译器内部使用(\verb+E::greek:delta.grf+).

\bigskip
\noindent \textbf{投递目录}
\label{section-repository}

\bigskip
\noindent当一个人希望在` Y\ :math:`语法使用语法` X
:math:`，常见的做法是` X :math:`的所有图形复制的目录中`
Y\ :math:`的图是，这会有两个问题：

\begin{itemize}
  \item 在目录图形的数目很快就变得非常重要~;
  \item两个图不能有相同的名称。
\end{itemize}

\noindent 为了避免这种情况，可以存储在特定目录语法` X
:math:`，称为\textit{投递目录}.\index{Répertoire!dépôt de graphes}\index{Graphe!répertoire de dépôt}。这个目录是一种库，在那里你可以存储图形，然后使用\verb+::+而不是 \verb+:+。要使用这个机制，首先要在菜单中定义信息库目录“信息>首选项...>目录”（参见图\ref{directories}）.
选择在“图形库”目录。投递目录是适当的工作语言，所以你不必使用相同的目录多种语言。

\begin{figure}[!h]
\begin{center}
\includegraphics[width=8cm]{resources/img/fig5-10.png}
\caption{确认存放的目录\label{directories}}
\end{center}
\end{figure}

\bigskip
\noindent假设我们有一棵树，如图\ref{repository}.如果我们调用图\verb+DET+这是在子目录\verb+Johnson+，我们称作

% do not remove this line jump
\noindent \verb+::Det:Johnson:DET+
(见图\ref{repository-graph-call}\footnote{为了清楚起见，调用投递目录的图表显示在卡其色的背景，而不是灰色的。})。

\begin{figure}[!h]
\begin{center}
\includegraphics[width=3.9cm]{resources/img/fig5-11.png}
\caption{投递目录的例子\label{repository}}
\end{center}
\end{figure}

\begin{figure}[!h]
\begin{center}
\includegraphics[width=6.7cm]{resources/img/fig5-12.png}
\caption{调用投递目录的图\label{repository-graph-call}}
\end{center}
\end{figure}

\bigskip
\noindent提示：如果你想避免把你的图表复杂路径\verb+::Det:Johnson:DET+，您可以创建一个名为图\verb+DET+您将资料库根目录\verb+D:\repository\DET.grf+）。此图只包含对图形\verb+::Det:Johnson:DET+。然后，你可以把你的图形简单调用\verb+::DET+。这使1不和要有复杂的名称和2）修改投递目录的图表，而无需更改所有的图表。事实上，你只需要在投递目录的根更新图表。
\bigskip
\noindent调用子图显示在框由灰色背景（图~\ref{fig-subgraph-call}），或在卡其子图的情况下，行库目录看（图~\ref{repository-graph-call}）。如果该文件位于\verb++.grf子图未在指定的路径中，Unitex搜索文件\verb+.fst2+相同的名称。如果Unitex发现既不是\verb+.grf+ 也不\verb+.fst2+，调用缺少的图形出现在红色背景上的一条线。

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\begin{figure}[h!]
\begin{center}
\includegraphics[width=7cm]{resources/img/fig5-9.png}
\caption{缺少的子图显示为红色}
\end{center}
\end{figure}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\bigskip
\noindent在Windows中，您可以通过点击灰线，同时按下Alt键打开一个子图。在Linux上，使用<Alt +点击> \footnote被清除{如果您正在使用KDE，如果你用KDE的话，则<Alt +点击>}要打开一个子图，就其名字中间点击（中间的按钮），或使同时点击（左右按钮）。
%%%%%%%%%%%%%%%%%%%%

\bigskip
\noindent 图表由当前图形调用，调用当前图形可以通过点击第四组按钮中的第二和第三个按钮的工具栏上观看的图的列表（图~\ref{list-called-graphs}~; 也可见图~\ref{fig-toolbar}, 专栏~\ref{toolbar-commands}）.
在子图列表中：
\begin{itemize}
\item子图直接调用当前图形与简单的文件名显示
\item子图称为间接通过显示一个带箭头他们的名字之前，由当前图形称为图形之一
\item出现在图形由当前图形称为子图而不必连接，因此，未经处理的有其在橙色名
\item子图没有找到（拓展名既不是.grf也不.fst2）显示为红色。
\end{itemize}

\begin{figure}[!h]
\begin{center}
\includegraphics[width=15.2cm]{resources/img/fig5-12b.png}
\caption{显示所有已知图列表\label{list-called-graphs}}
\end{center}
\end{figure}


%%%%%%%%%%%%%%%%%%

\subsection{搬运框}
\index{Sélection multiple}\index{Boîtes!sélection}

您可以选择使用鼠标多框。只需点击和移动鼠标而不释放按钮。当您松开按钮时，受选择矩形的所有框将被选中，然后会出现在白色的蓝色背景（图 \ref{multi-selection}).

\begin{figure}[!ht]
\begin{center}
\includegraphics[width=10cm]{resources/img/fig5-13.png}
\caption{选择多个框\label{multi-selection}}
\end{center}
\end{figure}
%\vspace{-0.3cm}
%%%%%%%%%%%%%%%

\bigskip
\noindent 您可以选择多个框现在<CTRL>和<SHIFT>和点击每个框添加到选择。通过这种方式，可以选择多个框而不选择整个区域（图 \ref{multi-selection2}).

\begin{figure}[!ht]
\begin{center}
\includegraphics[width=10cm]{resources/img/fig5-13b.png}
\caption{选择选择框\label{multi-selection2}}
\end{center}
\end{figure}
%\vspace{-0.3cm}

%%%%%%%%%%%%%%
\bigskip
\noindent当选择框被选择后，您可以通过点击并没有释放按钮移动鼠标移动它们。要取消选择，单击图形中的空白区域;如果你点击一个框，所有的选择框将被连接到它。

\bigskip
\index{Sélection multiple!copier-coller}
\index{Copie}\index{Coller}
\noindent你可以让几框复制和粘贴，如图~\ref{copy-paste-multi-selection}.要做到这一点，选择它们，按<Ctrl+ C>或从“编辑”菜单中点击“复制”。你多现在在Unitex的剪贴板。然后，您可以通过按下<Ctrl+ V>或通过单击“粘贴”，从“编辑”菜单中粘贴此选择。

\begin{figure}[!h]
\begin{center}
\includegraphics[width=13cm]{resources/img/fig5-14.png}
\caption{复制并粘贴多个选择\label{copy-paste-multi-selection}}
\end{center}
\end{figure}

\bigskip
\noindent注意：您可以粘贴从它派生不同的图形多重选择。

\bigskip
\index{Graphe!suppression de boîtes}\index{Boîtes!suppression}
\noindent要删除框，选择删除它们所包含的文本（也就是说，在窗口顶部显示的字段中的文本），然后按Enter。

\bigskip
\noindent您不能删除初始状态或最终状态。

\subsection{输出}
\label{Transducers}\index{Transducteur}\index{\verb+/+}
这是可能的输出关联到一个框。为此，使用特殊字符\verb+/+。所有字符到它的权利将被视为输出的一部分。因此，文本\verb`\ one+two+three/number\ :math:`给出图框~\ref{fig-exemple-transduction}.

\begin{figure}[h]
\begin{center}
\includegraphics[width=4.5cm]{resources/img/fig5-15.png}
\caption{结果实例\label{fig-exemple-transduction}}
\end{center}
\end{figure}

\bigskip
\noindent要创建包含这个\verb+number+，并输出一个空框，我们写\verb+<E>/number+（例如〜：图中最右边的框~\ref{fig-using-variable}是空的，一个输出）。与框相关联的输出以粗体显示在下面。

%%%%%%%%%%%%%%
\bigskip
\noindent \textbf{权}
\index{Poids}

\noindent可以分配一个权重的换能器的框。因此，当一个序列由具有不同的输出几条路径识别
（歧义翻译器\index{Ambigu!transducteur}\index{Sortie d'un transducteur!ambiguïté}）只有一个最大权重路径将被保留。
经过一个“查找”，该协议将只承认曾经的序列，并输出（图~\ref{fig-weights-in-graphs}).

\begin{figure}[h!]
\begin{center}
\includegraphics[width=14.5cm]{resources/img/fig5-15b.png}
\caption{权重曲线\label{fig-weights-in-graphs}}
\end{center}
\end{figure}

\bigskip
\noindent权重是整数值。举一个权重为1的框中插入\verb+`\ 1\ :math:`+在出口，就如同\verb+<E>/`\ 1\ :math:`+.

\bigskip
\noindent路径的权重是在路径名中找到的最后重量。的重可以是零，但没有严格阴性。有重量的路径，甚至为零，具有优先于没有权重的特性。

\bigskip
\noindent 有了这些权重，我们可以定义识别相同序列的路径之间的优先权。不能设置两个序列，其中一个被包括在其他之间的优先级（见~\ref{section-configuration-recherche}）或重叠序列之间（见~\ref{section-priorite-gauche}).

\bigskip
\noindent权重是唯一的图内有效，而不是在子图或图表的调用者。

%%%%%%%%%%%%%

\subsection{输入变量}
\label{section-using-variables}
\index{Graphe!variables}\index{Variable!d'entrée}\index{\verb+$+$}
\index{Transducteur!avec variables}

有可能选择由输入变量的装置由一个语法识别的文本的部分。要输入变量\verb+var1+到语法的一部分关联，请使用带图标栏中图形上方的红色括号（第~\ref{toolbar-commands}章）一个或按钮或特殊符号\verb+`\ var1\ :math:`(+ 和
\verb+`\ var1\ :math:`)+。 （这些符号分别定义了区域店面的开头和结尾。建立一个包含\verb+`\ var1\ :math:`(+ 和 \verb+`\ var1\ :math:`)+，这些框不应该包含任何东西变量名，并且前面由 \verb+`\ +和右括号组成。然后将框连接到期望的区域语法）。
在图的曲线〜[fig-using-variable]，识别开头的号码，它被存储于命名为\ ``var1``\ ，接着\ ``dollar``
或是\ ``dollars``.

.. figure:: resources/img/fig5-16.png
   :alt: 输入变量的使用 ``var1``\ [fig-using-variable]
   :width: 13.50000cm

   输入变量的使用 ``var1``\ [fig-using-variable]

，大写或小写，并且数字和字符\ ``_`` 。
Unitex能区分是小写和大写字母之差。

，它可以在输出用的字符\ ``$``\ 在其名称中使用。图 [fig-date-grammar]的语法识别由一个月，一年的日期，并输出相同的日期，但在按年月顺序排列。

如果你想使用\ ``$``\ 字符输出在一个框中，我们必须设置它，如图〜[fig-using-variable].

.. figure:: resources/img/fig5-17.png
   :alt: 在日期的年份和月份反转[fig-date-grammar]
   :width: 14.50000cm

   在日期的年份和月份反转[fig-date-grammar]

，
新值将覆盖旧的。因此，如果该变量是在一个循环设置，只是在循环之后的变量的值取决于通过循环中的最后时间。

``Locate`` 和
``LocateTfst``\ 考虑到不确定的变量是空的。我们可以改变这种行为（见[section-advanced-search-options]）.此外，它是在图中可以查询一个变量，看它是否已经被初始化（第 [section-variables]章).

复制列表
~~~~~~~~

它可方便地进行复制黏贴，并从一个文本编辑器的邮框中的图表粘贴的词或短语的列表。为了避免必须每学期手动复制，Unitex提供的复制机制列表。要使用它，在你的文本编辑器中选择你的清单，使用<Ctrl+
C>或内置复制功能，你的编辑复制。然后创建图表在一个框里，并使用<Ctrl +
V键>或从“编辑”菜单中选择“粘贴”，将其粘贴到对话框。您将看到如图的窗口 [fig-setting-contexts-for-multiple-copy].

.. figure:: resources/img/fig5-18.png
   :alt: 选择一个列表的副本[fig-setting-contexts-for-multiple-copy]
   :width: 7.00000cm

   选择一个列表的副本[fig-setting-contexts-for-multiple-copy]

。默认情况下，这些设置都是空的。如下所示:

*eat*

*sleep*

*drink*

*play*

*read*

我们能看到如下框显示 [fig-multiple-copy].

.. figure:: resources/img/fig5-19.png
   :alt: 框通过复制列表具有加成上下文获得[fig-multiple-copy]
   :width: 6.70000cm

   框通过复制列表具有加成上下文获得[fig-multiple-copy]

特殊符号
~~~~~~~~

：

``" + : / < > # \``

表
 [tab-special-symbols]总结了这些符号Unitex的含义，以及，或如何在文本识别这些字符。

+------------+--------------------------------------------------------+---------------------+
| ``符号``   | ``意义``                                               | ``编码``            |
+============+========================================================+=====================+
| ``"``      | 双引号可以既不是Unitex解释序列，或在任何情况下变化。   | ``\"``              |
+------------+--------------------------------------------------------+---------------------+
| ``+``      | ``+`` 将框的不同行分开                                 | ``"+"``             |
+------------+--------------------------------------------------------+---------------------+
| ``:``      | ``:`` 引入一个子图                                     | ``":"`` or ``\:``   |
+------------+--------------------------------------------------------+---------------------+
| ``/``      | ``/`` 描述框的输出的最开头                             | ``\/``              |
+------------+--------------------------------------------------------+---------------------+
| ``<``      | ``<`` 在一些话的开头                                   | ``"<"`` or ``\<``   |
+------------+--------------------------------------------------------+---------------------+
| ``>``      | ``>`` 在一些话的结尾 ``">"`` or ``\>``                 |                     |
+------------+--------------------------------------------------------+---------------------+
| ``#``      | ``#`` 禁止空格                                         | ``"#"``             |
+------------+--------------------------------------------------------+---------------------+
| ``\``      | ``\`` 处理特殊字符                                     | ``\\``              |
+------------+--------------------------------------------------------+---------------------+

Table: 在图形编辑器的特殊符号的编码[tab-special-symbols]

工具栏功能
~~~~~~~~~~

[toolbar-commands]

工具栏上面的显示图标的图形包含快捷方式某些命令和可以操作使用“工具”图的框。此图标栏可以通过点击“粗”区域移动。它甚至可以从图分离，然后显示为单独的窗口（见图 [fig-toolbar]）.
在这种情况下，靠近窗口的事实替换工具栏到原来的位置。每个图都有自己的工具栏。

.. figure:: resources/img/fig5-20.png
   :alt: 工具栏[fig-toolbar]
   :width: 15.00000cm

   工具栏[fig-toolbar]

。以下五个操作对应于“复制”，“剪切”，“粘贴”，“重做”和“撤销”。

6个按钮对应编辑命令框。第一，在白色箭头的形状，对应于正常编辑框。其他5对应的工具。要使用工具，单击其图标：鼠标光标会改变形状，鼠标点击会再以特定的方式来解释。下面介绍的工具，从左至右依次为：

：代替点击创建一个空框; ：删除框，单击;
：此工具来选择一个或多个框以及或连接到另一个。不同于正常模式时，或同时移动鼠标指针显示将要创建的转换;
：此工具执行同前，但通过连接扭转所选框点击框;
：打开当您单击在一个框里相应的灰线一子图。

，图形上的〜右下方点击：点击次数将再次正常解释。

。下面的两个让你看到相关列表与当前图图表：

。如果一个文件位于拓展名\ ````.grf的同时它所包含的图形显示在一个窗口Unitex改变，一个弹出窗口会提示你重新加载。

，以另一图表或曲线图的另一个版本。一个新的窗口会出现（参见图 [Graph-DIFF]）包含两个图以指示所述类型的两个曲线图之间的差异的颜色：插入，删除，移动框和改变在绿色，分别，红色，紫色和黄色所示的框的内容。

.. figure:: resources/img/DIFF.png
   :alt: DIFF[Graph-DIFF]
   :width: 15.60000cm

   DIFF[Graph-DIFF]

最后六个按钮是快捷方式的变量，形态学方法或一个或多个选定框上下文的定义。如果选择一个或多个方框，这些按钮仅激活：

-  : 输入变量 (见第 [section-using-variables]章)

-  : 输出变量 (见第 [section-output-variables]章)

-  : 形态模式 (见第 [section-morphological-mode]章)

-  : 左侧内容(见第 [section-contexts]见第)

-  : 右侧内容 (见第 [section-contexts]见第)

-  : 右侧负内容 (见第 [section-contexts]见第)

显示选项
--------

在一个框里行进行排序
~~~~~~~~~~~~~~~~~~~~

您可以通过从子菜单中“工具”菜单中的“FS图”选择并单击“排序节点标签”框中的内容进行排序。此排序不使用\ ``SortTxt``\ 。这是一个基本的排序，根据在Unicode编码字符的顺序进行排序的方块的行。

缩放
~~~~

子菜单“缩放”，您可以选择在其中将在图表上显示的规模。

.. figure:: resources/img/fig5-21.png
   :alt: 子菜单缩放
   :width: 6.40000cm

   子菜单缩放

“适合屏幕”拉伸或收缩图形给它的屏幕大小。
“适合窗口”进行调整，使其在窗口中完全显示的图形。

抗锯齿
~~~~~~

抗混叠是避免了像素化效果的渲染效果。
您可以通过单击“格式”子菜单中激活这个效应“抗锯齿......”。图〜[fig-antialiasing]显示正常（上图），显示两个图，并应用了抗锯齿（下图）。

.. figure:: resources/img/fig5-22.png
   :alt: 抗锯齿实例[fig-antialiasing]
   :width: 13.50000cm

   抗锯齿实例[fig-antialiasing]

。我们建议，如果你的机器不是强大，最好不使用它。

对齐框
~~~~~~

以获得平滑的曲线图，它是对准框，水平和垂直方向是有用的。为此，选择框对齐，然后单击“对齐......”从子菜单中的“格式”菜单中的“FSGraph”或按<Ctrl+
M>。然后，您会看到如图 [fig-alignment-frame]窗口。

水平对齐选项有：

-  上: 框在最上面的框对齐;

-  中: 框都集中在同一轴线上;

-  下: 框在最低框对齐.

.. figure:: resources/img/fig5-23.png
   :alt: 调整窗口[fig-alignment-frame]
   :width: 6.60000cm

   调整窗口[fig-alignment-frame]

为垂直取向的可能是：

-  左: 框在最左边的方框内对齐;

-  中: 框都集中在同一轴线上;

-  右: 框与右边的框中对齐。

图 [fig-vertical-left-alignment]
展示出了对准的一个例子。该组框向右侧是被垂直排列在左侧的左框的副本。

.. figure:: resources/img/fig5-24.png
   :alt: 左垂直对齐的例子[fig-vertical-left-alignment]
   :width: 11.50000cm

   左垂直对齐的例子[fig-vertical-left-alignment]

“使用网格”，以显示在图形的背景的网格。这可以使用大约对齐框。

.. figure:: resources/img/fig5-25.png
   :alt: 使用网格的例子
   :width: 15.00000cm

   使用网格的例子

演示，字体和颜色
~~~~~~~~~~~~~~~~

您可以通过按下<Ctrl+
R>或点击从“格式”菜单中的“FSGraph”，这将导致的显示器的子菜单配置图的外观“介绍......”如图 [fig-graph-display-configuration].

.. figure:: resources/img/fig5-26.png
   :alt: 配置图形的外观[fig-graph-display-configuration]
   :width: 9.00000cm

   配置图形的外观[fig-graph-display-configuration]

字体设置为：

：在框中并在编辑框的内容文本框中使用的字体; ：用于显示框的事件字体。

：

-  背景：背景颜色;

-  前景：用于框的文字和图案色彩;

-  辅助节点：采用子图彩框;

-  选定的节点：选择使用时，画框的颜色;

-  如何节点：用于绘制未链接到任何其他框的颜色。

其他设置选项为：

-  日期：显示在曲线图的左下角当前日期;

-  文件名：显示在图的左下角的曲线图的名称;

-  路径：您可以在底角全路径图名的显示
   曲线图的左侧。此选项仅在“文件名”选项被选中的效果;

-  框架：绘制图形围绕一个框架;

-  从右到左：反转图形的播放方向（见例 [fig-right-to-left-graph]).

.. figure:: resources/img/fig5-27.png
   :alt: 从右读向左的图[fig-right-to-left-graph]
   :width: 14.50000cm

   从右读向左的图[fig-right-to-left-graph]

“默认”按钮，恢复默认设置。如果单击“确定”按钮，只有当前图形将在“信息”菜单中更改。首选项要更改语言的默认首选项，点击“首选项...”，然后选择“图形演示”选项卡。

Unitex的拓展图
--------------

一个文件中的曲线图
~~~~~~~~~~~~~~~~~~

要包含在文档中的图形，你必须做出一个图像。为此，第一种方法是将您的图形导出为图片格式〜：PNG，JPEG或SVG。要做到这一点，转到“FSGraph”菜单，单击“导出为图片”。然后选择文件类型。你会准备的图像被整合文档中或与图像编辑软件进行编辑。为了使图像更流畅，你可以让你想要的图形抗锯齿。
Contraitement
JPEG，PNG使用无损压缩质量，所以PNG总是给人比JPEG更好的结果。并且不同于PNG和JPEG，这是位图fomats，SVG是一个矢量格式，这往往提供了一个更好的结果。使用该软件Inkscape中，它也可以转换在EPS或PDF
SVG文件，与这些命令行：

::

    Inkscape -z -E graph.eps graph.svg

::

    Inkscape -z -A graph.pdf graph.svg

第二种方法是屏幕截图:

Windows操作系统下:

12键上的“打印屏幕”。在Windows的“附件”菜单启动\ ``Paint``\ 。按<Ctrl+
V>。
``Paint``\ 可以告诉你，在剪贴板中的图像太大，并询问您是否要放大图像。点击“Yes”。现在，您可以编辑画面的图像。选择您感兴趣的区域。要做到这一点，去选择模式通过点击虚线框是在窗口的左上角。现在，您可以用鼠标选择图像的区域。一旦你选择的区域，按<Ctrl+
C>。您的选择现在在剪贴板上，它会刚刚进入你的文件，并键入<Ctrl +
V>粘贴图像。

Linux操作系统下:

（如使用\ ``xv``\ ）。然后调整用图形编辑器（如\ ``TheGimp``\ ）你的形象，并粘贴图像文档中以同样的方式与Windows相同。

**矢量图**

如果你喜欢一个矢量图像，你可以把你的图形为SVG，可与软件一起使用，如Inkscape
(:raw-latex:`\cite{Inkscape}`).
它允许获得在文件可用的PostScript输出LaTeX.

打印图片
~~~~~~~~

您可以通过点击从“FS图”菜单打印出图“打印...”或 按下<Ctrl+ P>。

注意：您必须确保打印机的方向设置（纵向或横向）的图形的方向一致。

你可以通过点击菜单中的“FS图”“页面设置”设置您的打印首选项。您也可以打印通过点击打开所有图形“全部打印…”。
