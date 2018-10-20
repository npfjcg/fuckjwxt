fuckjwxt
===

解决弱智教务系统不支持 IE11 或非 IE 浏览器的问题。

至今他们仍然没有正式使用新版的、可以支持手机访问的教务系统。

有关研究过程和技术细节，可参阅[这篇文章](https://vjudge1.github.io/2015/05/29/let-jiao-wu-xi-tong-support-linux/)。

本篇说明原文来自洋神的 GitHub 仓库，由 Yukino Shiratama 修改完善。

# 安装

## IE 11

IE 11 可以使用兼容性视图，无需此项目。具体操作方法是，按 F12，在开发人员工具里找到“仿真”，然后将浏览器版本设置为旧一些的。

如果不想开兼容性视图，请说服教务处赶快改代码。
** 实际上上学期已经在进行新版教务系统的测试了，然而迟迟不上线 **

## Edge

除了中间人攻击，目前没想到什么好办法，除非你能说服教务处赶快改代码。

** 要不然还是建议点击左上角三个点，然后"用 Internet Explorer 打开"来的好，只要回到 IE 11 的步骤就行了 **

## Firefox 和 Chrome

有一个插件叫做 gooreplace，虽说是用来替换谷歌资源的（因为外国网站喜欢用 Google CDN，而 Google CDN 正好被墙了，所以很多外国网站都进不去），不过也可以用在教务系统身上。

首先安装 gooreplace 插件，然后点击“自定义规则”，添加以下两个规则：

原始 URL                                | 目的 URL
----------------------------------------|-----------------------------------
http://jwxt.upc.edu.cn/jwxt/js/core.js  | https://upclinux.github.io/fuckjwxt/js/core.js
http://211.87.177.1/jwxt/js/core.js     | https://upclinux.github.io/fuckjwxt/js/core.js

提醒:

手机端的 Chrome 无法安装插件，所以。。。除非你用的是毛子开发的 Yandex 浏览器

## Safari

目前没找到合适插件。有一个叫 Browser Tools for CN 的插件据说支持 Safari，但是无法下载。

## Opera

貌似没有人用……

## Android/iOS/WP 

很不幸，除非你会中间人攻击，或者能够说服教务处赶紧改代码。

** 似乎新版教务系统能支持手机端直接访问，但是他们咕咕咕了 **

# 已知问题

1. “任务栏”不能切换窗口。
2. 由于教务系统脚本本身的错误（夹在服务器端页面中，无法干预），“查看全校课表”等功能无法使用。
3. Chrome 和 Opera 不支持一切会弹出“对话框”的操作，例如选课。
