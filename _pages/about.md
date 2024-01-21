---
permalink: /
title: "academicpages is a ready-to-fork GitHub Pages template for academic personal websites"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

这是由 [academicpages 模板](https://github.com/academicpages/academicpages.github.io)提供支持并托管在 GitHub 页面上的网站的首页。[GitHub 页面](https://pages.github.com/)是一项免费服务，其中网站是根据 GitHub 存储库中存储的代码和数据构建和托管的，并在对存储库进行新提交时自动更新。该模板是从 Michael Rose 创建的 [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/) 分叉而来的，然后扩展到支持学者拥有的各种内容：出版物、讲座、教学、作品集、博客文章和动态生成的简历。您现在可以分叉[此存储库](https://github.com/academicpages/academicpages.github.io)，修改配置和 Markdown 文件，添加自己的 PDF 和其他内容，并免费拥有自己的网站，没有广告！此模板的旧版本为我自己的个人网站提供支持，该网站位于 [stuartgeiger.com](http://stuartgeiger.com/)，该网站使用此 [Github 存储库](https://github.com/staeiou/staeiou.github.io)。

## 数据驱动的个人网站

与许多其他基于 Jekyll 的 GitHub Pages 模板一样，academicpages 可让您将网站的内容与其形式分开。你网站的内容和元数据在结构化的Markdown文件中，而其他各种文件构成了主题，指定了如何将内容和元数据转换为HTML页面。您可以将这些不同的 Markdown （.md）、YAML （.yml）、HTML 和 CSS 文件保存在公共 GitHub 存储库中。每次提交更新并将其推送到存储库时，[GitHub](https://pages.github.com/) 页面服务都会基于这些文件创建静态 HTML 页面，这些文件免费托管在 GitHub 的服务器上。

动态内容管理系统（如 Wordpress）的许多功能都可以以这种方式实现，使用一小部分计算资源，并且对黑客攻击和 DDosing 的脆弱性要小得多。您还可以根据自己的喜好修改主题，而无需触及您网站的内容。如果你在 Jekyll/HTML/CSS 中损坏了某些东西无法修复，那么描述你的演讲、出版物等的 Markdown 文件是安全的。您可以回滚更改，甚至删除存储库并重新开始 - 只需确保保存 Markdown 文件即可！最后，您还可以编写脚本来处理网站上的结构化数据，例如[这个](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb)脚本，它分析有关演讲的页面中的元数据，以显示[您演讲的每个位置的地图](https://academicpages.github.io/talkmap.html)。

## 开始

1.  如果您没有 GitHub 帐户，请注册一个帐户并确认您的电子邮件（必填！
2.  通过单击右上角的“fork”按钮来分叉[此存储库](https://github.com/academicpages/academicpages.github.io)。
3.  转到存储库的设置（以“代码”开头的选项卡中最右边的项目应位于“取消监视”下方）。将存储库重命名为“\[您的 GitHub 用户名\].github.io”，这也将是您网站的 URL。
4.  设置站点范围的配置并创建内容和元数据（参见下文 -- 另请参阅[这组差异](http://archive.is/3TPas)，其中显示了为用户名为“getorg-testacct”的用户设置[示例站点](https://getorg-testacct.github.io/)而更改了哪些文件）
5.  将任何文件（如 PDF、.zip 文件等）上传到 files/ 目录。它们将显示在 https://\[你的 GitHub 用户名\].github.io/files/example.pdf。
6.  通过转到“GitHub 页面”部分中的存储库设置来检查状态

## 站点范围的配置

站点的主配置文件位于 [\_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml) 的基目录中，该目录定义侧边栏中的内容和其他站点范围的功能。您需要将默认变量替换为有关您自己和您站点的 github 存储库的变量。顶部菜单的配置文件位于 [\_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml) 中。例如，如果您没有作品集或博客文章，则可以从该 navigation.yml 文件中删除这些项目，以将其从标题中删除。

## 创建内容和元数据

对于网站内容，每种类型的内容都有一个 Markdown 文件，这些文件存储在 \_publications、\_talks、\_posts、\_teaching 或 \_pages 等目录中。例如，每个 talk 都是 [\_talks 目录中](https://github.com/academicpages/academicpages.github.io/tree/master/_talks)的 Markdown 文件。每个 Markdown 文件的顶部都是 YAML 中关于演讲的结构化数据，主题将解析这些数据以做很多很酷的事情。关于演讲的相同结构化数据用于生成 [Talks 页面上](https://academicpages.github.io/talks)的演讲列表、特定演讲的每个[单独](https://academicpages.github.io/talks/2012-03-01-talk-1)页面、[CV 页面](https://academicpages.github.io/cv)的演讲部分以及[您发表演讲的地点](https://academicpages.github.io/talkmap.html)地图（如果您运行此 [python 文件](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py)或 [Jupyter 笔记本](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb)，它会根据 \_talks 目录的内容为地图创建 HTML）。

**Markdown 生成器**

我还创建了[一组 Jupyter 笔记本](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator)，用于将包含有关演讲或演示文稿的结构化数据的 CSV 转换为单独的 Markdown 文件，这些文件将针对 academicpages 模板进行正确格式化。该目录中的示例 CSV 是我用于在 stuartgeiger.com 创建自己的个人网站的 CSV。我通常的工作流程是保留我的出版物和演讲的电子表格，然后在这些笔记本中运行代码以生成 Markdown 文件，然后提交并将它们推送到 GitHub 存储库。

许多人使用 git 客户端在本地计算机上创建文件，然后将它们推送到 GitHub 的服务器。如果你不熟悉 git，可以直接在 github.com 界面中直接编辑这些配置和 markdown 文件。导航到一个文件（如[此](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md)文件），然后单击内容预览右上角的铅笔图标（在“Raw |责备 |历史记录“按钮）。您可以通过单击铅笔图标右侧的垃圾桶图标来删除文件。您还可以通过导航到目录并单击“创建新文件”或“上传文件”按钮来创建新文件或上传文件。

示例：编辑演讲的 Markdown 文件[![编辑演讲的 Markdown 文件](https://github.com/a-strong-python/xiaoxiong.github.io/raw/master/images/editing-talk.png)](https://github.com/a-strong-python/xiaoxiong.github.io/blob/master/images/editing-talk.png)

## 更多信息

有关配置 academicpages 的更多信息[，请参阅指南](https://academicpages.github.io/markdown/)。[最小错误](https://mmistakes.github.io/minimal-mistakes/docs/configuration/)主题（此主题是从该主题派生而来的）的指南也可能有所帮助。
