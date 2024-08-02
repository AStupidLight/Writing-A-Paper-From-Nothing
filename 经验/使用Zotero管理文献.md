Zotero的基础使用在这之前我已经简单学习过，不在此记录。

# 为什么我们需要管理文献？

搜索文献管理，大多数的内容都是：如何使用文献管理软件。但是却不去说明这么样去使用软件管理文献的目的是什么，我们希望利用其达成什么目标。

## 统一格式管理

从网络上下载的文献pdf，很多命名都是不统一的。我们此时需要一个统一的格式来记录这种一个文献重要的信息，让我们可以一目了然地知道这个文章的作者主题、作者、刊物名称等重要信息。Zotero通过自动识别DOI号来自动完成这件事。

## 自定义的论文层次体系

我们需要对浩如烟海的论文有一个自己的管理体系，其实就是文件夹树的设计。

有人将文献分类成精读和略读。如果只需要略读，那么利用碎片化的时间自然可以快速地读。也可以将其分为每个不同的研究领域和方法。

但是事实上，除了文件夹树的形式储存，Zotero本身还提供了基于标签的储存方式。对于一些文章我们本身就可以为其标定一系列的特征标签，以供查阅。

## 整理文献之间的关联

包括文章与文章之间的关联和笔记之间的关联。

## 自动生成引用

这或许对写学位论文用处比较大。反而不会对期刊论文有太多要求。

# 使用Zotero的技巧

## 标签

文献很多时候会自带标签，但是这些标签没有任何意义，建议全部删除。

可以为标签设置自己想要的颜色。除了其中的方法等等，我们还可以使用重要程度为其打标签。这样可以通过标签的方式直接来筛选重要的论文。

## 如何导出一篇文章的所有引文

在web of science中找到你想要的那个文献。拉到下面选择cited preferences。右边view as set of results。之后就可以按照普通的导出方式选择export，所有结果，导出为ris文件。最后在zotero当中导入。



使用zotero reference插件

[Releases · MuiseDestiny/zotero-reference (github.com)](https://github.com/MuiseDestiny/zotero-reference/releases)

## 搜索源添加sci-hub

首选项——高级——设置编辑器——extensions.zotero.findPDFs.resolvers

输入：

{

"name":"Sci-Hub",

"method":"GET",

"url":"https://sci-hub.ren/{doi}",

"mode":"html",

"selector":"#pdf",

"attribute":"src",

"automatic":true

}

# 使用时的一些问题

## 中文论文不自动获取信息怎么办

需要使用一个插件：

[Releases · l0o0/jasminum (github.com)](https://github.com/l0o0/jasminum/releases)

