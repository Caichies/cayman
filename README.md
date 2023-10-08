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

# The Cayman theme

[![.github/workflows/ci.yaml](https://github.com/pages-themes/cayman/actions/workflows/ci.yaml/badge.svg)](https://github.com/pages-themes/cayman/actions/workflows/ci.yaml) [![Gem Version](https://badge.fury.io/rb/jekyll-theme-cayman.svg)](https://badge.fury.io/rb/jekyll-theme-cayman)

*Cayman is a Jekyll theme for GitHub Pages. You can [preview the theme to see what it looks like](http://pages-themes.github.io/cayman), or even [use it today](#usage).*

![Thumbnail of Cayman](thumbnail.png)

## Usage

To use the Cayman theme:

1. Add the following to your site's `_config.yml`:

    ```yml
    remote_theme: pages-themes/cayman@v0.2.0
    plugins:
    - jekyll-remote-theme # add this line to the plugins list if you already have one
    ```

2. Optionally, if you'd like to preview your site on your computer, add the following to your site's `Gemfile`:

    ```ruby
    gem "github-pages", group: :jekyll_plugins
    ```

## Customizing

### Configuration variables

Cayman will respect the following variables, if set in your site's `_config.yml`:

```yml
title: [The title of your site]
description: [A short description of your site's purpose]
```

Additionally, you may choose to set the following optional variables:

```yml
show_downloads: ["true" or "false" (unquoted) to indicate whether to provide a download URL]
google_analytics: [Your Google Analytics tracking ID]
```

### Stylesheet

If you'd like to add your own custom styles:

1. Create a file called `/assets/css/style.scss` in your site
2. Add the following content to the top of the file, exactly as shown:
    ```scss
    ---
    ---

    @import "{{ site.theme }}";
    ```
3. Add any custom CSS (or Sass, including imports) you'd like immediately after the `@import` line

*Note: If you'd like to change the theme's Sass variables, you must set new values before the `@import` line in your stylesheet.*

### Layouts

If you'd like to change the theme's HTML layout:

1. For some changes such as a custom `favicon`, you can add custom files in your local `_includes` folder. The files [provided with the theme](https://github.com/pages-themes/cayman/tree/master/_includes) provide a starting point and are included by the [original layout template](https://github.com/pages-themes/cayman/blob/master/_layouts/default.html).
2. For more extensive changes, [copy the original template](https://github.com/pages-themes/cayman/blob/master/_layouts/default.html) from the theme's repository<br />(*Pro-tip: click "raw" to make copying easier*)
3. Create a file called `/_layouts/default.html` in your site
4. Paste the default layout content copied in the first step
5. Customize the layout as you'd like

### Customizing Google Analytics code

Google has released several iterations to their Google Analytics code over the years since this theme was first created. If you would like to take advantage of the latest code, paste it into `_includes/head-custom-google-analytics.html` in your Jekyll site.

### Overriding GitHub-generated URLs

Templates often rely on URLs supplied by GitHub such as links to your repository or links to download your project. If you'd like to override one or more default URLs:

1. Look at [the template source](https://github.com/pages-themes/cayman/blob/master/_layouts/default.html) to determine the name of the variable. It will be in the form of `{{ site.github.zip_url }}`.
2. Specify the URL that you'd like the template to use in your site's `_config.yml`. For example, if the variable was `site.github.url`, you'd add the following:
    ```yml
    github:
      zip_url: http://example.com/download.zip
      another_url: another value
    ```
3. When your site is built, Jekyll will use the URL you specified, rather than the default one provided by GitHub.

*Note: You must remove the `site.` prefix, and each variable name (after the `github.`) should be indent with two space below `github:`.*

For more information, see [the Jekyll variables documentation](https://jekyllrb.com/docs/variables/).

## Roadmap

See the [open issues](https://github.com/pages-themes/cayman/issues) for a list of proposed features (and known issues).

## Project philosophy

The Cayman theme is intended to make it quick and easy for GitHub Pages users to create their first (or 100th) website. The theme should meet the vast majority of users' needs out of the box, erring on the side of simplicity rather than flexibility, and provide users the opportunity to opt-in to additional complexity if they have specific needs or wish to further customize their experience (such as adding custom CSS or modifying the default layout). It should also look great, but that goes without saying.

## Contributing

Interested in contributing to Cayman? We'd love your help. Cayman is an open source project, built one contribution at a time by users like you. See [the CONTRIBUTING file](docs/CONTRIBUTING.md) for instructions on how to contribute.

### Previewing the theme locally

If you'd like to preview the theme locally (for example, in the process of proposing a change):

1. Clone down the theme's repository (`git clone https://github.com/pages-themes/cayman`)
2. `cd` into the theme's directory
3. Run `script/bootstrap` to install the necessary dependencies
4. Run `bundle exec jekyll serve` to start the preview server
5. Visit [`localhost:4000`](http://localhost:4000) in your browser to preview the theme

### Running tests

The theme contains a minimal test suite, to ensure a site with the theme would build successfully. To run the tests, simply run `script/cibuild`. You'll need to run `script/bootstrap` once before the test script will work.
