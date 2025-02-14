## Latex 常用基础命令

### 文本

- 设置字体

  ````
  \documentclass[11pt]{article} #字体11pt(默认值是10pt)
  \textbf{要加粗的字} #字体加粗
  \underline{要加下划线的字} #下划线
  \textit{要变为斜体的字} #斜体
  \textbf{\textit{加粗斜体的字}} 
  ````

- 设置纸张大小

  ````
  \documentclass[a4paper]{article} #a4paper,letterpaper
  ````

- 设置单双面

  ````
  \documentclass[twoside]{article} #oneside(artice, report默认值),twoside(book默认值)
  ````

- 标题与小标题

  ```
  \section # 一级标题
  \subsection # 二级标题
  \subsubsection # 三级标题
  ```

- 交叉引用

  ```
  \label{}
  \ref{}
  ```

  

#### 特殊符号

````
# % 如果要打出‘%’，要在前面加\
\%
````



### 标题/日期/作者

- 在\begin{document}之前输入标题

  ````
  \title{标题}\author{作者}\date{日期}
  ````

- 在\begin{document}之后输入标题

  ````
  \title{Your Paper}
  \author{You}
  \begin{document}
  \maketitle
  \end{document}
  ````

- 在\begin{document}之后另起一页输入标题

  ````
  \title{Your Paper}
  \author{You}
  \date{today}
  \begin{document}
  \begin{titlepage}
  \maketitle
  \end{titlepage}
  \end{document}
  ````

- 小标题及次级标题生成

  ````
  \section{Introduction} # 小标题section
  \subsection{Method} # 次级标题
  ````


### package

````
\usepackage{xeCJK} #在文档类型后加入如下包,同时在Menu中setting栏将编译器compiler切换为XeLaTeX,即可编译中文

\usepackage[english]{babel} # babel包表示多语言
````

### 换行/换页

- 利用空行切换至下一行；
- 在段尾添加如下代码，但不能形成段首缩进

  \newline或 \或\par 或 \hfill \break

- 换页添加代码

  \newpage


### 居中/左对齐/右对齐

- 内容全部居中/左对齐/右对齐

  ````
  \begin{center/flushleft/flushright}
  要居中/左/右的内容
  \end{center/flushleft/flushright}
  ````

- 部分左对齐

  ````
  \centering %小范围内(比如表格)居中后面部分内容
  \noindent  %本行左对齐不缩进
  ````


### 页边距

````
\usepackage{geometry}
\gemometry(a4paper,left=2.54cm,right=2.54cm,top=3.09cm,bottom=3.09cm) #%A4版上下为2.54厘米；左右为3.09厘米
````



### 空格

````
\quad #单格
\\quad #双格
````



### 表格

````
\multicolumn{2}{c}{内容} #合并两列内容

https://tablesgenerator.com/ # 辅助生成表格代码
````



### 网址

````
\cvsite{https://blog.csdn.net/m0_xxxxxxx} % Personal website
# 在短划线 '_' 前面加上 '\'
\cvsite{https://blog.csdn.net/m0\_xxxxxxx} % Personal website

````



### 公式

- 搜索相关工具 https://www.latexlive.com

````
# 所有字母都大写的变量名不能是斜体
\textrm{AHF}
\textrm{RH} RH的所有字母都要大写
````



### 反引号

````
# `
`lsmlon'
````



### 大约 波浪号

```
\textasciitilde
```



## 图片

- 统一设置图片路径

```
\graphicspath{{3_revised_paper_1/graphics/}}
# 在\begin{document}前
```



# Overleaf & Zotero

- [Zotero+ better bibtex+overleaf](https://blog.csdn.net/PLCET/article/details/130408777?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522169598354316800184122004%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=169598354316800184122004&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-130408777-null-null.142%5Ev94%5EchatsearchT3_1&utm_term=overleaf%20zotero&spm=1018.2226.3001.4187)
- 通过Zotero生成.lib的文件，导入到overleaf中。 常用的参考文献引用格式有Havard引用和IEEE引用，默认的引用格式是IEEE引用；

  - 首先在Zotero 中将需要的文献归类到一个目录中，右键Export collection，导出bibTex文件；
  - 在overleaf 中右键‘upload’，选择‘from Zotero’，

- 将bib文件上传到overleaf项目目录，进一步使用\cite插入文献即可；

  - overleaf会根据输入单词（通常是作者姓氏）自动搜索bib文件中的文献；

- 可以坚果云来实现多个电脑之间（包括跨操作系统）的文献同步；
- Zotero中安装Better BibTex插件

  - [Better BibTex教程](https://www.bilibili.com/read/cv16775542/)

    - 下载Better BibTex （xpi文件）
    - 从Zotero 安装Better BibTex： 在主菜单点击 Tools > Add-ons ，打开 add-ons manager
    - 打开xpi 文件即可安装

  - 修改key格式
  - pin key
  - refresh key in the Overleaf (zotero不会自动刷新 citation key)

    - Overleaf-refs_XXX.bib
    - key在overleaf中的更新可能没有反应，多点几次refresh就好了

# overleaf & vscode

- 安装Overleaf Workshop 插件

# 参考文献

- latex中的参考文献一般使用bibtex
- Bibtex style 有 [harvard](https://www.ctan.org/tex-archive/macros/latex/contrib/harvard/), [iopart-num](https://ctan.org/pkg/iopart-num). 

## 在文中

- 调整参考文献的顺序：在begin ducument之前写入

````
\usepackage[sort&compress]{natbib}
````

## 在文末

- 

```
\bibliographystyle{xxx.bst}
```

## Journal requirement

### Wiley AGU journal

### IOP

- IOP的模板没有提供可用的bst文件，需要自行下载

```
\item For the numerical (Vancouver) reference style we recommend that authors use 
 \verb"unsrt.bst"; this does not quite follow the style of published articles in our
 journals but this is not a problem.  Alternatively \verb"iopart-num.bst" created by Mark A Caprio
 produces a reference style that closely matches that in published articles.  The file is available from
\verb"http://ctan.org/tex-archive/biblio/bibtex/contrib/iopart-num/" .
\item For alphabetical (Harvard) style references we recommend that authors use the \verb"harvard.sty"
in conjunction with the \verb"jphysicsB.bst" BibTeX style file.  These, and accompanying documentation, can be downloaded
from \penalty-10000 \verb"http://www.ctan.org/tex-archive/macros/latex/contrib/harvard/".
Note that the \verb"jphysicsB.bst" bibliography style does not include article titles
in references to journal articles.
To include the titles of journal articles you can use the style \verb"dcu.bst" which is included
in the \verb"harvard.sty" package.  The output differs a little from the final journal reference
style, but all of the necessary information is present and the reference list will be formatted
into journal house style as part of the production process if your article is accepted for publication.
```

- \bibliographystyle{unsrt}
- \bibliographystyle{iopart-num}
- \bibliographystyle{jphysicsB}
- \bibliographystyle{dcu}

### Elsevier

- Elsevier的模板提供了三种：

  - Elsarticle-template-num.tex

  ```
  \documentclass[preprint,12pt]{elsarticle}
  \bibliographystyle{elsarticle-num}
  # 对应模板提供的elsarticle-num.bst文件
  ```

  

  - Elsarticle-template-num-names.tex

  ```
  \documentclass[preprint,12pt]{elsarticle}
  \bibliographystyle{elsarticle-num-names}
  # 对应模板提供的elsarticle-num-names.bst文件
  ```

  

  - Elsarticle-template-harv.tex

  ```
  \documentclass[preprint,12pt,authoryear]{elsarticle}
  \bibliographystyle{elsarticle-harv}
  # 对应模板提供的elsarticle-harv.bst文件
  ```


# Package

## [tcolorbox](https://github.com/T-F-S/tcolorbox)

- use color stack
  - 换页后字体颜色与上一页保持一致 [ref](https://github.com/T-F-S/tcolorbox/issues/202)

# Error

**error1**: 编译出来的参考文献序号都是[0]

**solved**: 在一开始加上：[ref](https://tex.stackexchange.com/questions/463556/all-the-citations-in-the-references-are-being-numbered-as-0-in-arxiv-while-upl)

```
\makeatletter
\let\blx@rerun@biber\relax
\makeatother
```

**note**: 这几行命令不是很好使，需要“删掉-刷新-加上-刷新”.如果刷新后还是[0]，试试把下面删掉再加上后重新编译

```
\bibliography{literature.bib}
```



**error2**: 编译的时候编译不出来，有很多红色的提示但是不确定哪里有问题、

**solve**: 拉到最后，点击‘Clear cached files’，再重新compile



**error3**：行序号不显示

```
\let\oldequation\equation
\let\oldendequation\endequation

\renewenvironment{equation}
{\linenomathNonumbers\oldequation}
{\oldendequation\endlinenomath}
```

**solved**: [ref](https://blog.csdn.net/qq_36674060/article/details/128721019?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522172044189616777224427115%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=172044189616777224427115&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v31_ecpm-3-128721019-null-null.142^v100^pc_search_result_base1&utm_term=latex%20lineno%20linenumbers&spm=1018.2226.3001.4187)
