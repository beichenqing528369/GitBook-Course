# 项目结构剖析



## Git目录结构

GitBook使用简单的目录结构。在 SUMMARY （即 SUMMARY.md 文件）中列出的所有 Markdown / Asciidoc 文件将被转换为 HTML。多语言书籍结构略有不同。


>一个基本的 GitBook 电子书结构通常如下：
> <ul> 
> <li>book.json</li>
> <li>README.md</li>
> <li>SUMMARY.md</li>
> <li>chapter-1</li>
> <ul>
> <li>README.md</li>
> <li>something.md</li>
> </ul>

> <li>chapter-2</li>
> <ul>
> <li>README.md</li>
> <li>something.md</li>
> </ul>
> </ul>






## GitBook 特殊文件的功能：

1. ```book.json``` 配置数据 (optional)
2. ```README.md``` 电子书的前言或简介 (required)
3. ```SUMMARY.md``` 电子书目录 (optional)
4. ```GLOSSARY.md``` 词汇/注释术语列表 (optional)


## 静态文件和图片
静态文件是在 SUMMARY.md 中未列出的文件。除非被忽略，否则所有静态文件都将复制到输出路径。

## 忽略文件和文件夹 

GitBook将读取 .gitignore，.bookignore 和 .ignore 文件，以获取要过滤的文件和文件夹。这些文件中的格式遵循 .gitignore 的规则

## 项目与子目录集成

对于软件项目，您可以使用子目录（如 docs/ ）来存储项目文档的图书。您可以配置根选项来指示 GitBook 可以找到该图书文件的文件夹：

> <ul> 
> <li>book.json</li>
> <li>docs/</li>
> <ul>
> <li>README.md</li>
> <li>SUMMARY.md</li>
> </ul>
> </ul>

## Summary

GitBook 使用 SUMMARY.md 文件来定义本书的章节和子章节的结构。 SUMMARY.md 文件用于生成本书的目录。SUMMARY.md 的格式是一个链接列表。链接的标题将作为章节的标题，链接的目标是该章节文件的路径。向父章节添加嵌套列表将创建子章节。

简单示例：

```

* [简介](README.md)
* [第一章 GitBook安装](chapter1/README.md)
* [第二章 GitBook使用](chapter2/README.md)
    * [本地项目制作](chapter2/section2.1.md)
    * [项目结构剖析](chapter2/section2.2.md)
* [第三章 GitBook官网介绍](chapter3/README.md)
    * [书籍主题](chapter3/section3.1.md)
    * [书籍设置](chapter3/section3.2.md)
    * [书籍在线制作](chapter3/section3.3.md)
    * [GitBook Editor 使用](chapter3/section3.4.md)
    * [域名绑定](chapter3/section3.5.md)
* [第四章 GitHub 集成](chapter4/README.md)
    * [GitHub关联](chapter4/section4.1.md)
    * [GitHub发布流程](chapter4/section4.2.md)
```

1. 每章都有一个专用页面（part#/README.md），并分为子章节。
2. 目录中的章节可以使用锚点指向文件的特定部分。


### 目录可以分为以标题或水平线 ---- 分隔的部分：
```
# Summary

* [简介](README.md)

## Part I
* [第一章 GitBook安装](chapter1/README.md)
* [第二章 GitBook使用](chapter2/README.md)
    * [本地项目制作](chapter2/section2.1.md)
    * [项目结构剖析](chapter2/section2.2.md)

## Part II
* [第三章 GitBook官网介绍](chapter3/README.md)
    * [书籍主题](chapter3/section3.1.md)
    * [书籍设置](chapter3/section3.2.md)
    * [书籍在线制作](chapter3/section3.3.md)
    * [GitBook Editor 使用](chapter3/section3.4.md)
    * [域名绑定](chapter3/section3.5.md)
* [第四章 GitHub 集成](chapter4/README.md)
    * [GitHub关联](chapter4/section4.1.md)
    * [GitHub发布流程](chapter4/section4.2.md)

-----
* [第五章 markDown语法](chapter5/README.md)


```


### Glossary
允许您指定要显示为注释的术语及其各自的定义。根据这些术语，GitBook 将自动构建索引并突出显示这些术语。GLOSSARY.md 的格式是 h2 标题的列表，以及描述段落

---



# Gitbook 配置

> 1. GitBook 允许您使用灵活的配置自定义您的电子书。
> 2. 这些选项在 book.json 文件中指定。对于不熟悉 JSON 语法的作者，您可以使用 JSONlint 等工具验证语法。


# 常规设置
<table>
<tbody>
    <tr>
        <th>变量</th><th>描述</th>
    </tr>
    <tr>
        <td><font color="Hotpink">root</font></td>
        <td><font color="Hotpink">包含所有图书文件的根文件夹的路径，除了 book.json</font></td>
    </tr>
    <tr>
        <td><font color="Pink">structure</font></td>
        <td><font color="pink">指定自述文件，摘要，词汇表等的路径，参考 Structure paragraph.</font></td>
    </tr>
     <tr>
        <td><font color="Pink">title</font></td>
        <td><font color="pink">您的书名，默认值是从 README 中提取出来的。在 GitBook.com 上，这个字段是预填的。</font></td>
    </tr>
     <tr>
        <td><font color="Pink">description</font></td>
        <td><font color="pink">您的书籍的描述，默认值是从 README 中提取出来的。在 GitBook.com 上，这个字段是预填的。</font></td>
    </tr>
     <tr>
        <td><font color="Pink">author</font></td>
        <td><font color="pink">作者名。在GitBook.com上，这个字段是预填的。</font></td>
    </tr>
     <tr>
        <td><font color="Pink">isbn</font></td>
        <td><font color="pink">国际标准书号 ISBN</font></td>
    </tr>
     <tr>
        <td><font color="Pink">language</font></td>
        <td><font color="pink">本书的语言类型 —— ISO code 。默认值是 en</font></td>
    </tr>
     <tr>
        <td><font color="Pink">direction</font></td>
        <td><font color="pink">文本阅读顺序。可以是 rtl （从右向左）或 ltr （从左向右），默认值依赖于 language 的值。</font></td>
    </tr>
     <tr>
        <td><font color="Pink">gitbook</font></td>
        <td><font color="pink">gitbook</font></td>
    </tr>
    
    
</table>



###详解

1. author： 作者姓名，在GitBook.com上，这个字段是预先填写的。
2. description: 电子书的描述，默认值是从 README 中提取出来的。在GitBook.com上，这个字段是预先填写的。
3. direction: 文本的方向。可以是 rtl 或 ltr，默认值取决于语言的值。
4. gitbook: 应该使用的GitBook版本。使用SemVer规范，接受类似于 >=3.0.0 的条件。
5. language: Gitbook使用的语言, 版本2.6.4中可选的语言如下：
6. links: 在左侧导航栏添加链接信息
7. root: 包含所有图书文件的根文件夹的路径， book.json 文件除外。
8. structure
9. styles: 自定义页面样式， 默认情况下各generator对应的css文件
10. title: 电子书的书名，默认值是从 README 中提取出来的。在 GitBook.com 上，这个字段是预先填写的。




## plugins
1. 插件及其配置在 book.json 中指定。有关详细信息。

2. 自 3.0.0 版本开始，GitBook 可以使用主题。有关详细信息，请参阅  [the theming section ](https://toolchain.gitbook.com/themes/)

Gitbook 默认带有 5 个插件：

1. highlight
2. search
3. sharing
4. font-settings
5. livereload

####添加插件
```
"plugins":
[
    "splitter"
]
```
####去除插件
```
"plugins": [
    "-search"
]

```


---
#structure

除了 root 属性之外，您可以指定 Readme，Summary，Glossary 和 Languages 的名称（而不是使用默认名称，如README.md）。这些文件必须在项目的根目录下（或 root 的根目录，如果你在 book.json 中配置了 root 属性）。不接受的路径，如：dir / MY_README.md。

```
structure.readme: Readme 文件名（默认值是  README.md ）
structure.summary:Summary 文件名（默认值是 SUMMARY.md ）
structure.glossary: Glossary 文件名（默认值是 GLOSSARY.md ）
structure.languages: Languages 文件名（默认值是 LANGS.md ）

```


## PDF配置
 book.json 中的一组选项来定制PDF输出：

> * pdf.pageNumbers      -    将页码添加到每个页面的底部（默认为 true）
> * pdf.fontSize    -     基本字体大小（默认是 12）
> * pdf.fontFamily   -    pdf.fontFamily
> * pdf.paperSize   -    页面尺寸，选项有： 'a0', 'a1', 'a2', 'a3', 'a4', 'a5', 'a6', 'b0', 'b1', 'b2', 'b3', 'b4', 'b5', 'b6', 'legal', 'letter' （默认值是 a4）
> * pdf.margin.top -  上边界（默认值是 56）
> * pdf.margin.bottom - 下边界（默认值是 56）
> * pdf.margin.right - 右边界（默认值是 62）
> * pdf.margin.left - 左边界（默认值是 62）


##生成电子书

GitBook 可以生成一个网站，但也可以输出内容作为电子书（ePub，Mobi，PDF）。

```
# Generate a PDF file
$ gitbook pdf ./ ./mybook.pdf
 
# Generate an ePub file
$ gitbook epub ./ ./mybook.epub
 
# Generate a Mobi file
$ gitbook mobi ./ ./mybook.mobi


```






