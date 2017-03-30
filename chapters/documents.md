文件篇
===

![Documents](http://toolbox.phodal.com/images/documents/documents.png)

Pandoc
---

> Pandoc是一個標記語言轉換工具，可實現不同標記語言間的格式轉換，堪稱該領域中的“瑞士軍刀”。

可以將 markdown、 reStructuredText、 textile、 HTML、 DocBook、 LaTeX、 MediaWiki markup、 TWiki markup、 OPML、 Emacs Org-Mode、 Txt2Tags、 Microsoft Word docx、 LibreOffice ODT、 EPUB、 Haddock markup

轉化為

XHTML、 HTML5、 以及HTML幻燈片Slidy， S5，或者DZSlides、Microsoft Word docx、 OpenOffice/LibreOffice ODT、 OpenDocument XML、EPUB、DocBook、 GNU TexInfo、 Groff man pages、LaTeX、 ConTeXt、 LaTeX Beamer slides、PDF via LaTeX、Markdown、 reStructuredText、 AsciiDoc、 MediaWiki markup、 Emacs Org-Mode、 Textile

上圖

![Pandoc](http://toolbox.phodal.com/images/documents/pandoc.png)

我最常用的就是：將md轉化為workd及pdf。我的畢業論文及之前的幾本電子書都是這麼做的，它是一個命令列工具，安裝方式：

 - Windows: choco install pandoc
 - Ubuntu/CentOS/OpenSUSE: apt-get intall pandoc 或者 yum install pandoc
 - Mac OS: brew install pandoc

使用方式如下：

      pandoc fullstack.md -o fullstack.docx

如果要轉為PDF，則需要另外的一個工具——LaTeX

Graphviz
---

> Graphviz （英文：Graph Visualization Software的縮寫）是一個由AT&T實驗室啟動的開源工具包，用於繪製DOT語言指令碼描述的圖形。它也提供了供其它軟體使用的庫。

簡單的來說，就是將程式碼轉換為圖形:

![Graphviz](http://toolbox.phodal.com/images/documents/graphviz-example.png)

它讓我最驚訝的是DOT語言，簡直是以我們平時的用法來定義的。上面的圖形的程式碼類似於這樣的：

    home->products->widgets

又是一個讓人驚呆的黑科技，這才是人類應該使用的語言。它可以支援PostScript，PDF，SVG，PNG等一系列的格式，用法

     dot -T png phodal.dot -o phodal.png

簡單、粗暴到沒有朋友。

ImageMagick
---

> ImageMagick (TM) 是一個免費的建立、編輯、合成圖片的軟體。它可以讀取、轉換、寫入多種格式的圖片。圖片切割、顏色替換、各種效果的應用，圖片的旋轉、組合，文字，直線，多邊形，橢圓，曲線，附加到圖片伸展旋轉。

來自重點：可以支援超過兩百多種格式。It can read and write images in a variety of formats (over 200) including PNG, JPEG, JPEG-2000, GIF, TIFF, DPX, EXR, WebP, Postscript, PDF, and SVG.

它提供了一個命令列工具叫：``convert``，這可以自由地轉換圖片的形式，如：

    convert image.jpg image.png

還可以加各種效果，如：

![ImageMagick](http://toolbox.phodal.com/images/documents/gausisan.jpg)

順便做個介紹：上面的這個人叫瑞典模特兒萊娜·瑟德貝里，是在刊於1972年11月號《花花公子》雜誌上的一張裸體插圖照片的一部分。**她的臉部與裸露的肩部已經變成了事實上的工業標準。**

又是一個簡單、粗暴到沒有朋友的工具。

TeX 和 Latex
---

TeX是由是一個由美國計算機教授高德納（Donald Ervin Knuth）編寫的功能強大的排版軟體。順便推薦一下他寫的一本書：《計算機程式設計藝術》。因為：

> 高德納最早開始自行編寫TEX的原因是當時十分粗糙的排版水平已經影響到他的鉅著《計算機程式設計藝術》的印刷質量。他以典型的黑客思維模式，最終決定自行編寫一個排版軟體：TEX。他原本以為他只需要半年時間，在1978年下半年就能完成，但最終他用了超過十年時間，直到1989年TEX才最終停止修改。

這直接讓我想起Martin Fowler在寫《領域特定語言》裡好像也是用DSL。Tex的最大優點是可以寫出下面的這本複雜的公式：

![formular](http://toolbox.phodal.com/images/documents/formular.jpg)

LaTeX 建立在 TeX 之上的工具，它在TeX的基礎上大大改善了易用性。對了，如果只是一般的用途的話，就沒有必要拿去裝逼了~。

它也是工作於命令列上的工具。

Jupyter Notebook
---

Jupyter Notebook使用瀏覽器作為介面，其前身是Ipython Notebook，Ipython3.0之後新建為Jupyter項目。它支援Markdown、Python語言互動、R語言互動、圖形顯示、執行時間分析、LaTex公式，對於互動程式設計、資料分析和資料視覺化非常有用。

![Jupyter](http://toolbox.phodal.com/images/documents/Jupyter.png)

**安裝（使用pip）**

    $ pip install jupyter

**執行**

    $ jupyter notebook

官網：[Jupyter](https://jupyter.org/)


Gitbook
---

Gitbook是一個命令列工具(node.js庫)，可以把你的Markdown檔案彙整合起來，生成一個靜態網站，也可以輸出為PDF等多種格式。

![gitbook](http://toolbox.phodal.com/images/documents/gitbook.jpg)

**安裝（使用npm）**

    $ npm install gitbook-cli -g

**使用**

    $ gitbook init ＃ 初始化書籍目錄
    $ gitbook serve ＃ 執行

官網：[Gitbook](https://www.gitbook.com/)
