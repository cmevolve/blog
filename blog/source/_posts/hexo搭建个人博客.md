---
title: hexo搭建个人博客
date: 2019-05-26 11:15:15
categories: git
tags:
 - git
 - hexo
---

## 什么是Hexo ?
Hexo是一款基于Node.js的静态博客框架，依赖少易于安装使用，可以方便的生成静态网页托管在GitHub和Heroku上，是搭建博客的首选框架。

## 准备工作
### 相关资料
[Github 官网][1]
[Github Pages][2]
[Hexo 官网][3]
[Node.js 官网][4]
[Git 官网][5]


### 相关教程
[使用 GitHub 和 Hexo 搭建免费静态 Blog][6]
[简书 搭建个人博客][7]
[知乎][8]
[主题配置][9]

### 常用命令
依照上面的连接把准备工作做完了之后来使用下面命令开始博客之旅。

```js
npm install hexo -g #安装Hexo
npm update hexo -g #升级 
hexo init #初始化博客
命令简写
hexo n "我的博客" == hexo new "我的博客" #新建文章
hexo g == hexo generate #生成
hexo s == hexo server #启动服务预览
hexo d == hexo deploy #部署
hexo server #Hexo会监视文件变动并自动更新，无须重启服务器
hexo server -s #静态模式
hexo server -p 5000 #更改端口
hexo server -i 192.168.1.1 #自定义 IP
hexo clean #清除缓存，若是网页正常情况下可以忽略这条命令

```
### Markdown 格式

---
#### 添加标签
title: jQuery对表单的操作及更多应用
date: 2017-05-26 12:12:57
categories: 
- web前端
tags:
- jQuery
- 表格
- 表单验证
设置以后点击对应的标签均可连接到当前文章内。

#### 添加文章分类
title: jQuery对表单的操作及更多应用
date: 2017-05-26 12:12:57
categories: 
- web前端
如果在 web前端下方添加-xx 不会产生两个分类，会产生层级的分类，嵌套在上一级分类下。
#### 个性化定制
添加网易云音乐
打开网页版的网易云音乐，选择喜欢的音乐，点击生成外链播放器 复制外链的代码
修改 blog\themes\next\layout\_macro的sidebar.swig文件，添加刚刚复制的外链代码

设置背景
把你挑选的背景图片命名为：background.jpg，放在blog\themes\next\source\images里，在blog\themes\next\source\css\_custom文件的custom.styl首部添加：
```css
body {
  background:url(/images/background.jpg);
  background-attachment: fixed;
}
```
background-attachment: fixed;是固定背景图片。



  [1]: https://github.com/
  [2]: https://pages.github.com/
  [3]: https://hexo.io/zh-cn/
  [4]: https://nodejs.org/en/
  [5]: https://git-scm.com/
  [6]: https://wsgzao.github.io/post/hexo-guide/
  [7]: https://www.jianshu.com/p/f4dce0e76886
  [8]: https://zhuanlan.zhihu.com/p/26625249
  [9]: http://theme-next.iissnan.com/theme-settings.html