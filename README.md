此库是一个临时展示与修改库（fork过来后进行了修改，去除了一些重复性错误），利用github page托管静态网站，主要方便多人协同和初学修改，另外就经费与项目目的来看不太可能开服务器所以也不会用VPS，AWS等平台或者docker和Kubernetes这类工具，此外如果大家想自己搞一个网站（在已经有服务器的情况下）可以套模板或者教程利用我之前提到的平台和工具来便捷的部署，为之后的学习工作助力。

“编辑说明：1.网页具体内容在index.md里进行编辑，点击铅笔图标进入edit界面，注意一些标题中代码的中文编码问题，编辑结束后保存即commit changes，对于每次的修改如有必要写在提交时的summary里方便从action中查找记录回滚数据。
        2.网页大标题文件位于_config.yml文件中，我来修改即可。
        3.上传文件时，图片和其他文件统一上传至assets/css/中，命名要规范，不确定的问我，我最近会上传一个素材文件夹上去，不断补充。
        4.上传时注意，网页上传文件统一只能一次上传一个文件且不能上传文件夹，可以使用github desktop的图形化界面上传本地库或者使用git（命令行，用起来很简洁）来上传本地库解决文件夹问题。
        5.排版和文字编辑风格详见微信分享。
        6.此库是编辑库，最后初版完成后我会folk此库出一个新库作为最终展示，所以不要随意更改文件结构。”

“想自定义展示内容的话，主要会涉及以下几个文件：

_config.yml: 基础配置。
_layouts: 自定义布局。
_includes: 添加或修改可重用的组件。
assets: 加入自己的样式或脚本。
index.md, another-page.md: 修改或添加内容。”

“此外，我大概看了一下库的结构，每个文件夹注释如下：
文件夹github: 用于存放与GitHub相关的设置和文件。
_includes: 包含可重用的代码片段。
_layouts: 定义页面的基础结构。
_sass: 存放Sass样式文件。
assets: 包含所有静态文件，如图片、CSS、JavaScript等。
docs: 用于存放文档。
script: 存放自动化脚本。
.gitignore: Git忽略文件。
.rubocop.yml: RuboCop配置文件。
.travis.yml: Travis CI配置文件。
Gemfile: 列出Ruby依赖。
LICENSE: 开源许可证。
README.md: 项目说明。
_config.yml: Jekyll配置文件。
another-page.md, index.md: Markdown文件，网站内容。
jekyll-theme-cayman.gemspec: Ruby gem规格文件。”

最后说明一下，由于github page的网页编辑比较简单，且在已经有模板的情况下配合md可以使用自然语言来完成编写，所以如果无需整体结构变更和额外扩展就不需要以使用scss或者html为重点去改动。介于actions的修改日志可以配合多人在线修改，每次修改一定要记得注明summary。
