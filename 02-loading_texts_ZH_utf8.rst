加载文本
========

Unitex的一个主要功能是搜索文本表达式。要做到这一点，文本需要经过一系列处理使之成为规范化且无歧义的形式，以及拆分成句子的步骤。一旦这些操作被执行后，电子词典随即加载入文本中，从而可以通过许多语法使搜索文本更有效。

本章介绍了文本处理的几个步骤。

选择语言
--------

当你启动Unitex时，程序需要你选择操作的语言
(见图 [fig-language-selection])。
程序显示的语言既在系统目录里也在你的工作目录里。在你第一次使用某一种语言时，Unitex将系统目录下的该语言文件拷贝至你的工作目录，从而节约硬盘存储空间。

警告：如果你的工作目录里已经有了给定的语言，Unitex不会将系统数据复制至其中。因此，如果某次更新修改过资源文件或者字典，你需要自行拷贝该文件至你的工作目录，或者删除你工作目录下的该语言文件，让Unitex重新建立目录。

选择语言可以使Unitex找到对应的文件，例如字母表文件。
你可以在任何时候通过点击菜单栏“文本”中的“改变语言”来实现更换语言。
如果你更换了语言，程序会关闭所有和当前文本有关的窗口，如果它有的话。
当前的语言显示在标题栏的图像界面上。

.. figure:: resources/img/fig2-1.png
   :alt: [fig-language-selection]启动Unitex时的选择语言界面
   :width: 6.20000cm

   [fig-language-selection]启动Unitex时的选择语言界面

规范文本
--------

Unitex作用于Unicode编码的文本，而Unicode是全球文本编码的标准。
每个字符都其唯一的代码,从而可以不受操作系统和不同机器码限制地显示文本。Unitex
使用两个字节的编码表示方式，即Unicode 3.0标准,也称为Unicode
Little-Endian (详见 :raw-latex:`\cite{UNICODE}`).

进入Unitex的文本必须是Unicode格式。
如果你尝试加载非Unicode格式的文本，程序将会建议你转换
(见图 [auto-transcoding])。这个转换是根据当前语言而来的：如果你用法语工作，Unitex会转换你的文字 [1]_，通过假设它是用法语编码而成的。Unitex会默认建议你去替换原文件或是重命名原文件，在拓展名的开头加入
``.old``\ 。例如有一个ASCII文件\ ``biniou.txt``,
转换进程会复制这个ASCII文件并重命名为
``biniou.old.txt``\ ，或者用对应的Unicode来替换\ ``biniou.txt``\ 的内容。

.. figure:: resources/img/fig2-2.png
   :alt: [auto-transcoding]非Unicode文本的自动转换
   :width: 10.00000cm

   [auto-transcoding]非Unicode文本的自动转换

如果默认建议的编码不正确或者你想要不用，\ ``.old``\ 来重命名这个文件，你可以使用菜单栏中“编辑”下的“译码”。这个命令可以让你选择要转换文章的原始编码和目标编码
(见图 [transcoding]). 源代码默认和当前语言有关，而目标编码是 Unicode
Little-Endian。你可以通过选择任意源码和目标编码来改变这个选择。因此，你可以将你想要的数据转换成其他编码，比如你想做网页时使用UTF-8编码。“添加文件”按钮可以让你选择需要转换的文件。“移除文件”按钮能清空误选的文件列表。“译码”按钮将转换所有的文件。如果在处理文件时出现问题（比如给一个文件已经是Unicode了），程序会继续处理下一个文件。

.. figure:: resources/img/fig2-3.png
   :alt: [transcoding]文件转换
   :width: 12.00000cm

   [transcoding]文件转换

为了得到文本的正确形式，你可以同样使用文本处理就像Libre OpenOffice.org
(:raw-latex:`\cite{OpenOffice}`) 或者Microsoft
Word，以“Unicode文本”的形式保存你的文件。如果你用OpenOffice
Writer软件的话, 你应选择 “Coded Text (\*.txt)”格式
然后再激活的窗口上选择“Unicode”编码，如图 [OfficeWriter]所示。

.. figure:: resources/img/fig2-4.png
   :alt: [OfficeWriter]在OpenOffice Writer中以Unicode来储存文本
   :width: 12.50000cm

   [OfficeWriter]在OpenOffice Writer中以Unicode来储存文本

一台PC默认建议编码总是Unicode Little-Endian。它的编码不具有任何格式信息
(字体、颜色等)，因而它可以被Unitex使用。

通过菜单栏“信息”下的“偏好”内的“编码”标签，你可以将默认的编码改成
UTF16LE、 UTF16BE 或 UTF8。这个编码只对当前语言有效。

.. figure:: resources/img/fig2-5.png
   :alt: 对当前语言选择默认编码
   :width: 10.00000cm

   对当前语言选择默认编码

编辑文本
--------

通过菜单栏的“文件编辑”中的“打开”，你也可以使用Unitex的文本编辑器。这个编辑器有文本查找替换的功能，也内置了Unitex的字典。点击“搜索”按钮即可使用。你会看见窗口分成三个小部分。“搜索”部分与常用搜索操作相似。如果你将一篇文章拆分成句子，你可以在“搜索句子”这部分里使用句子编号来搜索。最后，“搜索字典”部分如图 [dictionary-search]所示，可以让你使用电子词典的有关操作。总的来说，即使词尾有变化，词形有变化或是符合语义学和语法学的编码都可以搜索。因此，如果你想要搜索所有带有“及物”（\ ``t``\ ）特征的动词，你只需要点击“语法学的编码”然后搜索“及物”（\ ``t``\ ）。你将会得到除了“及物”（\ ``t``\ ）这个词以外的所有的及物动词。

.. figure:: resources/img/fig2-6.png
   :alt: 在电子词典中搜索及物动词（\ ``t``\ ）[dictionary-search]
   :width: 15.00000cm

   在电子词典中搜索及物动词（\ ``t``\ ）[dictionary-search]

打开文本
--------

Unitex可以打开两种类型的文本文件。
具有\ ``.snt``\ 拓展名的文件是Unitex的预处理文本文件，可以被不同系统功能控制。具有\ ``.txt``\ 拓展名的文件是原始文件。你可以点击菜单栏“文本”中的“打开”来打开\ ``.txt``\ 文件。

.. figure:: resources/img/fig2-7.png
   :alt: 文本菜单
   :width: 14.00000cm

   文本菜单

.. figure:: resources/img/fig2-8.png
   :alt: 打开Unicode编码的文本
   :width: 13.00000cm

   打开Unicode编码的文本

文本的预处理
------------

一旦选好文本，Unitex就建议你进行预处理。预处理包含以下操作：分隔符的规范化，将文本拆分成句子，规范没有歧义的表达，将句子拆开，并加载字典。如果你拒绝对文本进行预处理，它将不会规范化，以及不能按语义分离，因此Unitex不能处理这些表达式。不过你总是可以自行点击菜单栏“文本”中的“预处理”来实现这个操作。

.. figure:: resources/img/fig2-9.png
   :alt: 预处理界面[fig-preprocessing-frame]
   :width: 15.00000cm

   预处理界面[fig-preprocessing-frame]

如果你选择预处理，Unitex会让你选择参数，见图 [fig-preprocessing-frame]。选项“Apply
FST2 in MERGE mode”用来把文本拆成句子。选项“Apply FST2 in REPLACE
mode”用来替换文本，尤其可以用作规范没有歧义的表达。选项“Apply All
default Dictionaries” 可以让你在DELA(Dictionnaires Electroniques du
LADL)格式的文本里运用字典。 选项“Analyse unknown words as free compound
words”用来在挪威语上，通过从词的简单形式的组合上进行正确分析词的自由组合形式。最后，选项“Construct
Text
Automaton”用来创建文本自动机。这个选项是默认关闭的，因为转换过长的文章需要占据大量内存和硬盘空间。构造文本自动机在第 [chap-text-automaton]章会详细介绍.

注意：如果你点击“Cancel but tokenize
text”,程序将所有的分隔符进行规范化并按语义分离；点击 “Cancel and close
text”可以取消操作。

规范分隔符
~~~~~~~~~~

标准的分隔符有空格，tab和回车。许多分隔符会连续出现，然而它对语言分析没有任何作用。我们通过以下几条方法来规范分隔符：

-  一系列的连续分隔符中包含至少一个回车，我们用一个回车即可来替代它们。

-  其余的连续分隔符，我们用一个空格来替换它们。

为了区分空格和回车，程序每步都会把它们储存下来，因为它们会在把文本分离成句子的过程中互相影响。规范
``mon_texte.txt``\ 后的结果与\ ``.txt``\ 处于同一目录下，且命名为\ ``mon_texte.snt``.

注意 : 当我们使用图形界面处理一篇文章时，一个叫

``mon_texte.snt`` 的目录在规范化后马上被创建。这个目录是文本目录，
包含了和这个文章所有有关的数据。

拆分成句子
~~~~~~~~~~

将文本拆成句子是预处理的重要一步，因为它决定了语言处理的单元。这个拆分用来给程序创造文本自动机。和我们想法相悖的是，搜索句子中的限制不是一个简单的问题。请考虑以下法语文本：

*La famille a appelé le Dr. Martin en urgence.*

*缩*\ 写词Dr后有个点，有个大写字母。如果把这个点当句号，而不是当成一个缩写标志的话，会产生错误。为了避免这种因加标点而产生的歧义现象，我们使用语法来判别句子结束的标志。图 [fig-example-sentence-splitting]
展示了一个用语法来拆分句子的例子。

.. figure:: resources/img/fig2-10.pdf
   :alt: 用语法拆分法语句子 [fig-example-sentence-splitting]
   :width: 15.00000cm

   用语法拆分法语句子 [fig-example-sentence-splitting]

当一条语法路径识别出这个序列或者当它产生句子分隔符 ``{S}``,
我们把这个标识符插入文章。比如，如图 [fig-example-sentence-splitting]
中的语法路径识别出这个序列中有问号和大写字母，于是在问号后插入 ``{S}``
标识符。如下文本所示：

*现在几点？八点。*

变成：

*现在几点？{S} 八点。*

语法标识符有以下几种特殊标记与准特殊标记：

-  ``<E>`` : 空词, 或epsilon。可以辨识出空序列 ;

-  ``<WORD>`` : 辨识出任意字母序列 ;

-  ``<LOWER>`` : 辨识出任意小写字母序列 ;

-  ``<UPPER>`` : 辨识出任意大写字母序列 ;

-  ``<FIRST>`` : 辨识出任意首字母大写序列 ;

-  ``<NB>`` : 辨识出任意相邻数字序列 (可辨出1234，而1 234则不行) ;

-  ``<PNC>`` : 辨识出标点符号 ; , ! ?
   还有西班牙语的问号和感叹号还有一些亚洲的标点符号 ;

-  <``^``> : 辨识出回车 ;

-  ``#`` : 禁止空格出现。

我们早期并未使用 ``<WORD>``, ``<LOWER>``, ``<UPPER>`` 和 ``<FIRST>``
而是用 ``<MOT>``, ``<MIN>``, ``<MAJ>`` 和 ``<PRE>``\ 。
现有的图标系统中仍然能使用这些标识符，但是它们现在贬值了。也就是说为了当前版本 [2]_的功能尽量避免去用它们,
防止增加没用的语言标识符的数量。

我们默认空格是出现在两个盒子之中的。但是我们可以增加\ ``#``\ 符号来禁止空格的出现。同时，如果你想强制出现空格，你需要加上\ ``" "``\ 。此外，大小写字母在字母表文件中定义过
(详见第 [chap-file-formats]章)。你可以参考第 [chap-grammars]章来得到更多图像的信息。语法上的细节，详见第
:raw-latex:`\cite{ameliorer-decoupage-en-phrases}`章。所用语法的名称
``Sentence.fst2`` 以及用法可以在该目录下获取 :

``/(répertoire personnel)/(langue)/Graphs/Preprocessing/Sentence``

这个语法用L’application de cette grammaire à un texte s’effectue grâce
au programme ``Fst2Txt``\ 程序来用
MERGE.模式处理文本。这个模式影响了语法处理后的输出结果。在这个模式下\ ``{S}``\ 会插入文本。程序需要一个\ ``.snt``\ 文件并修改它。

规范没有歧义的形式
~~~~~~~~~~~~~~~~~~

文本中的许多形式可以被规范化（比如说，法语中“*l’on*”可以替换成“*on*”)。你可以根据你的需要来替换这些形式。然而，你需要特别注意这种形式需要是没有歧义的。否则替换后的形式会没有意义

如果我们用“*à le-dit*”形式来替换这个“*audit*”, 在下句中：

*La cour a procédé à un audit des comptes de cette société.*

将会变成如下错误的句子 :

*La cour a procédé à un à le-dit des comptes de cette société.*

必须谨慎使用规范化，也需要注意空格。比如说，我们用“*ce*”替换“*c’*”，期间不增加空格，则下句：

*Est-ce que c’était toi ?*

将会变成如下错误的句子 :

*Est-ce que ce était toi ?*

可在规范化时用的符号与分割句子的语法中使用的符号一致。这个规范文法文件命名为
``Replace.fst2``\ 且在以下目录可被找到 :

``/(répertoire personnel)/(langue)/Graphs/Preprocessing/Replace``

和分割句子一致的是，这个语法也用\ ``Fst2Txt``\ 程序
,不过这次使用的是REPLACE模式，这个模式表示的是内部语法所生成的句子将会被外部产生的句子所替换。如 [fig-normalization-grammar]图所示的是一个规范英语动词的语法。

.. figure:: resources/img/fig2-11.pdf
   :alt: 规范英语动词的语法[fig-normalization-grammar]
   :height: 17.00000cm

   规范英语动词的语法[fig-normalization-grammar]

文本拆分成符号
~~~~~~~~~~~~~~

[tokenization]
一些语言，尤其是亚洲的语言中，会使用一些不同于西方语言的操作符。空格可能是禁止的，也可能是有条件的，或者必须的。为了更好处理这些特殊情况，Unitex在拆分文本上，对一个语言使用特定的方法。比如，法语就如下主要规则来处理：

主要分隔符可能是:

-  句子限制符 ``{S}``\ ；

-  停止标志 ``{STOP}``. 与\ ``{S}``\ 不同的是,
   ``{STOP}``\ 标志永远不会被语法识别，无论用什么方法。比如一份资料使用\ ``{STOP}``\ 来分割新闻，则程序不可能操作这一段；

-  一个语言标签 ``{aujourd'hui,.ADV}``;

-  一串相邻字母 (在字母表中定义的字母);

-  一个(只能有一个)字母非字母的符号，比如所有不再当前字母表文件中定义的字符；如果它是一个回车，则用空格代替。

对于其他语言来说，分隔符是一个字符一个字符处理的，除了\ ``{S}``\ 标志，\ ``{STOP}``\ 标志以及语言标记。这些简单的符号化是Unitex的基础功能，但是它限制了搜索操作的理想情况。

无论什么分割模式，文本中的回车总被空格取代。分割操作由 ``Tokenize``
来执行。这个程序会在存放文本的文件夹下新建许多文件 :

-  ``tokens.txt``\ 包含了在文本中按顺序搜索到的分隔符。

-  ``text.cod``\ 包含了一个整形数组。每个数字对应\ ``tokens.txt``\ 文件中符号在文中的索引;

-  ``tok_by_freq.txt``\ 包含了一个按使用频率来排序的分隔符表；

-  ``tok_by_alph.txt``\ 包含了一个按字母来排序的分隔符表；

-  ``stats.n`` 包含一些文本数据。

分割文章 :

*Un sou c’est un sou.*

返回这样的分隔符列表: *UN* 空格 *sou c ’ est un .*

你观察到标志化是一个较精细的操作(Un和un是两个不同的标志)，每个标志只出现了一次。把这些标记用0到5来编号,
这段文字用数字可以用下表表示：

+------------+--------+-----+---------+-----+---------+-----+--------+-----+---------+-------+----+----+
| 标记编号   | 0      | 1   | 2       | 1   | 3       | 1   | 4      | 1   | 2       | 5     |    |    |
+============+========+=====+=========+=====+=========+=====+========+=====+=========+=======+====+====+
| 对应语言   | *UN*   |     | *sou*   |     | *est*   |     | *UN*   |     | *sou*   | *.*   |    |    |
+------------+--------+-----+---------+-----+---------+-----+--------+-----+---------+-------+----+----+

Table: 文本\ *Un sou c’est un sou.*\ 的表示

详见第 [chap-file-formats]章.

.. figure:: resources/img/fig2-12.png
   :alt: Unités lexicales d’un texte anglais triées par fréquence
   :height: 10.00000cm

   Unités lexicales d’un texte anglais triées par fréquence

使用字典
~~~~~~~~

字典的应用由子字典中的原型组成。搜索发法语短语\ *Igor mange une pomme de
terre*\ 的结果如下：

::

    de,.DET+z1
    de,.PREP+z1
    de,.XI+z1
    mange,manger.V+z1:P1s:P3s:S1s:S3s:Y2s
    pomme,.A+z1:ms:fs:mp:fp
    pomme,.N+z1:fs
    pomme,pommer.V+z3:P1s:P3s:S1s:S3s:Y2s
    terre,.N+z1:fs
    terre,terrer.V+z1:P1s:P3s:S1s:S3s:Y2s
    une,.N+z1:fs
    une,un.DET+z1:fs

同时，程序识别出以下词组 :

::

    pomme de terre,.N+z1:fs

短语\ *Igor*\ 既不是法语单词，也不是法语词组，所以它被认为是生词。字典应用\ ``Dico``.程序来处理。三个文件(\ ``dlf``
储存单词, ``dlc`` 储存词组 ，以及\ ``err``
储存生词)将在文本目录下被新建。
我们把\ ``dlf``\ 文件及\ ``dlc``\ 文件成为字典文本。

一旦加载字典完毕后，Unitex会按顺序在一个窗口中显示单词、词组以及生词。图 [fig-Dico-application-results]显示了处理一篇英语文章的结果。

.. figure:: resources/img/fig2-13.png
   :alt: Résultats de l’application de dictionnaires sur un texte
   anglais[fig-Dico-application-results]
   :width: 12.00000cm

   Résultats de l’application de dictionnaires sur un texte
   anglais[fig-Dico-application-results]

通过点击菜单栏“文本”下的“添加语言资源...”按钮，我们同样可以不在预处理时运用字典。Unitex会显示一个窗口(见图
 [fig-Dico-configuration]) 供你选择可以应用的字典。

.. figure:: resources/img/fig2-14.png
   :alt: Paramétrage de l’application des
   dictionnaires[fig-Dico-configuration]
   :width: 10.00000cm

   Paramétrage de l’application des
   dictionnaires[fig-Dico-configuration]

“用户资源”列表会显示在用户目录\ ``(langue)/Dela``\ 下的所有\ ``.bin``\ 以及\ ``.fst2``\ 拓展名的字典。系统字典在“系统目录”下。<Ctrl+左键>可以让你同时使用多种字典。系统字典已经默认被安装。你可以选择用户字典以及系统字典的顺序通过上下箭头。(见图[fig-Dico-configuration])。“设置默认值”按钮可以让当前选择默认选项。如果你已经点击过了“应用所有默认字典”，这个选项也同样作用于预处理。
如果你右击字典名字，字典的介绍会随即显示，只要它存在。

Analyse des mots composés libres en néerlandais, allemand, norvégien et russe
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

[section-Norwegian-compound-words]
在有些语言比如挪威语中，词组可能含有他们的元素。比如，单词\ *aftenblad*\ 表示
*journal du soir*\ 是 *aften* (*soir*)和\ *blad*
(*journal*)的结合。\ ``PolyLex``
程序返回一个生词列表并且尝试分析有没有可能是一个组合词。如果能分析出至少一种可能性，程序就会分会一个列表并加入单词词典。

Ouverture d’un texte taggué
---------------------------

文本标记是大括号里的文本语法注释。比如说下句：

*I do not like the {square bracket,.N} sign! {S}*

这个标记可以防止歧义，并可以防止其他干扰。在我们这个例子中，我们不会把square
当成两个单词来认识。

然而，这些标记可能会影响预处理文章。不过用户可以通过点击菜单“文本”下的“打开含标签的文本”使文本的预处理不受影响，如图[preprocess-tagged-text]所示。

.. figure:: resources/img/fig2-15.png
   :alt: Prétraitement d’un texte taggué[preprocess-tagged-text]
   :width: 14.00000cm

   Prétraitement d’un texte taggué[preprocess-tagged-text]

.. [1]
   Unitex同时也会建议非Unicode Little-Endian的字典与图像进行自动转换。

.. [2]
   从3.1bêta版本起, 版本号4072，2015年10月2日
