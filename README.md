
**webpack多入口文件打包策略**


1.首先，项目打包策略遵循以下几点原则：

2.选择合适的打包粒度，生成的单文件大小不要超过500KB
3.充分利用浏览器的并发请求，同时保证并发数不超过6
4.尽可能让浏览器命中304，频繁改动的业务代码不要与公共代码打包
5.避免加载太多用不到的代码，层级较深的页面进行异步加载

基于以上原则，我选择的打包策略如下：

1.第三方库如vue、jquery、bootstrap打包为一个文件
2.公共组件如弹窗、菜单等打包为一个文件
3.工具类、项目通用基类打包为一个文件
4.各个功能模块打包出自己的入口文件
5.各功能模块作用一个SPA，子页面进行异步加载


[项目链接](https://www.cnblogs.com/lvdabao/p/5944420.html)
