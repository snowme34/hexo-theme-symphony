# Symphony

A modified version of [Hexo](https://hexo.io) theme [Pure](https://github.com/cofess/hexo-theme-pure) and [Dawn](https://github.com/Ruffianjiang/hexo-theme-dawn).

[中文](README.cn.md)

[Preview](https://blog.snowme34.com/) | [iconfont](iconfont\demo.html)

[Preview of Pure](https://blog.cofess.com) | [Preview of Dawn](https://lossingdawn.top/)

Please read [documentation of Pure](https://github.com/cofess/hexo-theme-pure) for more details.

## Install theme

Execute the following command under your `hexo` folder.

```bash
git clone https://github.com/snowme34/hexo-theme-symphony.git themes/symphony
```
Then modify the property `theme` of the file `hexo/_config.yml`  to `theme: symphony`

After this modification, please make a copy of the `_config.yml.example` file called `_config.yml` and change the config accordingly.

The iconfont demo can be found [here](iconfont\demo.html). It is a html file included in the repo.

### Files for pre-designed pages

If the pages like `Categories` and `Tags` are used, please copy the `index` files under `[blog root]/symphony/_source` to the correspond folders inside `[blog root]/source`.

### Add images

Please add the necessary images to the corresponding path, like `donate` and `logo`.

Some of the path can be customized in the config files.

## Update theme

Execute the following command to update theme.

```bash
cd themes/symphony
git pull
```

## Modifications from original theme

### Fixed English translations

Please note the maintenance of Chinese version is not a focus in this repo.

In the original version, several places were hard-coded as Chinese, like titles and date. Some were hard-coded again as English and others are replaced with variables.

### Added new icons

Some additional icons, like Instagram, were added to the iconfont.

### Additional list in about-sidebar

A list called `Languages` are added to the about-sidebar, behaving same as the `Skills` sidebar.

### Footer

The [footer file](layout\_common) was changed accordingly.

### New variables for post

* disableDate

  Set `true` to disable the data displayed.

* disableWordcount

  Set `true` to disable the wordcount displayed.

### New behavior of post variable

sidebar - control the sidebar

`none`: Disable sidebar
`toc`: Display Catalogue sidebar (when variable `toc` is set `true`)
`custom`: Display customized sidebar, like the `About` page

Note: the behavior above was only tested when the sidebar is on the right side of the page.

### Disabled sticky bar for post

The bottom bar can only be seen at the end of the post, after comment part is enabled.

### Disabled comment number count

The comment number count displayed for the post was removed.

### Code block

The code block was modified. The modifications were heavily inspired by [material-x](https://github.com/xaoxuu/hexo-theme-material-x).

### Style

* Changed font and line-height

  Now use `Open Sans` and so on.

* Updated normalize.css

## Todo

* Add excerpt
* Fix the bug where the subcategories cannot be collapsed under `Categories` page
* Add a sidebar-toggle
* Add pink color theme
* Add a line beneath Titles of customized pages
* Add Telegram share support
* Test Google analytics
* Fix menu highlight bug

## Install plugin

### [hexo-wordcount](https://github.com/willin/hexo-wordcount)

```
npm install hexo-wordcount --save
```

### [hexo-generator-json-content](https://github.com/alexbruno/hexo-generator-json-content)

```
npm install hexo-generator-json-content --save
```

### [hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed)

```
npm install hexo-generator-feed --save
```

### [hexo-generator-sitemap](https://github.com/hexojs/hexo-generator-sitemap)

```
npm install hexo-generator-sitemap --save
```

### [hexo-generator-baidu-sitemap](https://github.com/coneycode/hexo-generator-baidu-sitemap)

```
npm install hexo-generator-baidu-sitemap --save
```

## Data files

Sometimes you may need to use some data in templates which is not directly available in your posts, or you want to reuse the data elsewhere. For such use cases, Hexo 3 introduced the new Data files. This feature loads YAML or JSON files in source/_data folder so you can use them in your site.

For example, add links.yml in source/_data folder.

### links data

add links.yml in source/_data folder.

The format of the link :

```
Name:
    link: http://example.com
    avatar: http://example.com/avatar.png
    desc: description
```

Add a number of links, we just need to repeat the format according to the above.

## Blog optimization

### [hexo-neat](https://github.com/rozbo/hexo-neat)

> auto Minify html、js、css and make it neat

```
npm install hexo-neat --save
```

You can configure this plugin in `_config.yml`.

```
# hexo-neat
neat_enable: true
neat_html:
  enable: true
  exclude:  
neat_css:
  enable: true
  exclude:
    - '*.min.css'
neat_js:
  enable: true
  mangle: true
  output:
  compress:
  exclude:
    - '*.min.js' 
```

### [hexo-baidu-url-submit](https://github.com/huiwang/hexo-baidu-url-submit)

```
npm install hexo-baidu-url-submit --save
```

### [hexo-translate-title](https://github.com/cometlj/hexo-translate-title)

> translate the chinese title of Hexo blog to english words automatially

```
npm install hexo-translate-title --save
```

You can configure this plugin in `_config.yml`.

```yml
translate_title:
  translate_way: google    #google | baidu | youdao
  youdao_api_key: XXX
  youdao_keyfrom: XXX
  is_need_proxy: true     #true | false
  proxy_url: http://localhost:8123
```

## Mathjax Support

### [hexo-renderer-markdown-it-plus](https://github.com/CHENXCHEN/hexo-renderer-markdown-it-plus)

install

```
npm un hexo-renderer-marked --save
npm i hexo-renderer-markdown-it-plus --save
```

You can configure this plugin in `_config.yml`.

```
markdown_it_plus:
  highlight: true
  html: true
  xhtmlOut: true
  breaks: true
  langPrefix:
  linkify: true
  typographer:
  quotes: “”‘’
  plugins:
    - plugin:
        name: markdown-it-katex
        enable: true
    - plugin:
        name: markdown-it-mark
        enable: false  
```

Article enable mathjax

```
title: Hello World
mathjax: true
```

