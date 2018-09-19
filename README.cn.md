# Symphony

基于 Hexo 主题 [Pure](https://github.com/cofess/hexo-theme-pure) 和 [Dawn](https://github.com/Ruffianjiang/hexo-theme-dawn) 修改的主题 Symphony | [iconfont](iconfont/demo.html)

[Preview of Pure](https://blog.cofess.com) | [Preview of Dawn](https://lossingdawn.top/)

详情请见 [Pure](https://github.com/cofess/hexo-theme-pure).

## 改动

### 删除 repo 内个人化的主题配置

请手动创建 `_config.yml`.

### 英文翻译

请注意本 repo 不包括中文版的维护。

翻译了几处原版本 hard coded 的中文。

### 添加新的图标

在原有的基础上添加了几个图标，详情请见 [iconfont](iconfont/demo.html)

此为一个 repo 内的 html 文件，请 clone 之后本地打开。

### 关于页面侧边栏

添加新的列表，`Languages`

### 页脚

根据实际情况修改了页脚

### 添加新的页面变量

* disableDate

  禁用日期显示

* disableWordcount

  禁用字数统计显示

* copyright

  启用页尾版权内容


### 侧边栏变量

sidebar

`none`: 禁用侧边栏
`toc`: 使用文章目录作为侧边栏
`custom`: 自定义，如关于页面

### 禁用粘滞底部条

底部条只会在页面末尾显示

### 禁用评论统计数

Post 不会显示评论统计数

### 代码块

更改代码块样式。参考 [material-x](https://github.com/xaoxuu/hexo-theme-material-x).

### 样式

* 修改了字体和行间距

* 更新了 normalize.css

## Todo

* Add excerpt
* Fix the bug where the subcategories cannot be collapsed under `Categories` page
* Add a sidebar-toggle
* Add pink color theme
* Add a line beneath Titles of customized pages
* Add Telegram share support
* Test Google analytics
* Fix menu highlight bug
* Update based on original repo
  * [fork list](https://github.com/snowme34/hexo-theme-symphony/network/members)
* Add demo page for iconfont
  * After a lot of preparation
