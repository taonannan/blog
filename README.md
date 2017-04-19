1.atam-cli 脚手架 学习到了怎么快速搭建网站 及 淘宝的移动端自适应页面 学习到了再750的设计图怎么快速制作 并且自动生成手机站访问的链接 以及browsersync调试移动端页面

脚手架的搭建

Adam(支持模版管理的项目初始化工具)

https://www.npmjs.com/package/adam-cli

安装adam

npm install -g adam-cli

添加模版

adam add https://github.com/amfe/activity-template.git

项目初始化

cd到项目路径，直接执行 adam 即可

adam init 项目 然后可以提交到gitHub上

安装依赖包，node_sass需要依靠淘宝镜像npm安装

SASS_BINARY_SITE=https://npm.taobao.org/mirrors/node-sass/ npm install

adam config

填入个人信息，每次添加模版的时候就不用输入长长的git地址了

Default gitlab group URL （http://gitlab.58corp.com/zhaoshaolong）

Gitlab/Github private token （eNGKyJ7Z6GyPVM4gfKF9

脚手架的使用说明

https://github.com/amfe/article/issues/17

运行项目 npm install npm run dev npm run build

a.活动下滑翻页运用了swiper插件

// 图片翻页

var swiper = new Swiper('.swiper-container', {
  direction: 'vertical',
  onSlideChangeEnd: function(swiper) {
      var arrow = document.getElementById("array");
      if (swiper.isEnd) {
          arrow.style.display = "none";
      } else {
          arrow.style.display = "block";
      }
  }
});

只需要配置 direction即可

b.运用了flex布局

flex-direction默认值为row 盒子横向布局 column为纵向布局

c.线性渐变代码

background: -webkit-gradient(linear, left top, left bottom, from(#e8ca89), to(#a88e5c));

2.怎样做移动端优化代码 减少无用的css

3.用到了在线雪碧图及图片压缩的好用逼格高的工具

https://tinypng.com/ 图片压缩

http://spritegen.website-performance.org/ 图片合并精灵

4.设置charles设置代理 调试移动端页面 、

设置代理的步骤：

1.选择proxy—ssl proxying settings

￼

2.勾选enable ssl proxying —— add

￼

3.填写host 和端口号

host为电脑的ip地址

port为端口号

￼

4.设置手机的代理 需同一个网络段

￼

这样就可以用代理测试啦啦啦

整个过程很nice 仅仅一个运营活动页面 学习到了这么多东西
