

## 介绍

1.  转到存储库的设置（以“代码”开头的选项卡中最右边的项目应位于“取消监视”下方）。将存储库重命名为“\[您的 GitHub 用户名\].github.io”，这也将是您网站的 URL。
2.  设置站点范围的配置并创建内容和元数据（参见下文 -- 另请参阅[这组差异](http://archive.is/3TPas)，其中显示了为用户名为“getorg-testacct”的用户设置[示例站点](https://getorg-testacct.github.io/)而更改了哪些文件）
3.  将任何文件（如 PDF、.zip 文件等）上传到 files/ 目录。它们将显示在 https://\[你的 GitHub 用户名\].github.io/files/example.pdf。
4.  通过转到“GitHub 页面”部分中的存储库设置来检查状态
5.  （可选）使用文件夹中的 Jupyter 笔记本或 python 脚本从 TSV 文件生成用于发布和讨论的 Markdown 文件。`markdown_generator`

更多信息，请访问 [https://academicpages.github.io/](https://academicpages.github.io/)

## 在本地运行（不在 GitHub Pages 上运行，在您自己的计算机上提供服务）

1.  克隆存储库并进行更新，如上所述
2.  确保你已经安装了 ruby-dev、bundler 和 nodejs：`sudo apt install ruby-dev ruby-bundler nodejs`
3.  Run 清理目录（无需运行`bundle clean``--force`)
4.  运行以安装 ruby 依赖项。如果出现错误，请删除 Gemfile.lock，然后重试。`bundle install`
5.  运行以生成 HTML 并从本地服务器提供它将在更改时自动重建和刷新页面。`bundle exec jekyll liveserve``localhost:4000`

## 更新日志 -- 错误修复和增强功能

像学术页面这样的现成模板主题存在一个后勤问题，这使得获得错误修复和核心主题的更新有点棘手。如果你分叉这个存储库，自定义它，然后再次拉取，你可能会遇到合并冲突。如果要保存各种.yml配置文件和 Markdown 文件，可以删除存储库并重新分叉。或者您可以手动修补。

为了支持这一点，对底层代码的所有更改都显示为带有“代码更改”标记的已关闭问题 -- [在此处](https://github.com/academicpages/academicpages.github.io/issues?q=is%3Aclosed%20is%3Aissue%20label%3A%22code%20change%22%20)获取列表。每个问题线程都包含一个链接到单个提交或多个提交之间的差异的注释，因此那些拥有分叉存储库的人可以轻松识别他们需要修补的内容。
