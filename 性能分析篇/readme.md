# 性能分析

## 性能分析概念
火焰图
- 每一个小块表示函数在栈中的位置
- y轴表示调用栈，每一层表示一个调用函数，调用栈越深，火焰就越高
- 小块的长度表示该函数占用cpu的时间，或者是相对父函数占用cpu的比例，如果函数处在栈顶，且宽度很大，说明该函数存在性能问题

## cpuprofile记录
### 使用chrome://inpsect附加调试Nodejs脚本
1. 附加调试node
```console
# 本地进程附加
node --inspect app.js
node --inspect=9229 app.js
# 远程调试附加
node --inspect=ip:9229 app.js
```
2. 在浏览器输入chrome://inpsect，configration之后就可以附加上进程了
3. 附加到进程后，点击profiler，并点击start开始记录
4. 开始压力测试nodejsApi接口
5. 压测结束，点击stop停止记录，并将cpufile另存到本地
6. 打开chrome-devtools，找到performance后将存好的cpufile上传上去，即可看到效果
7. 分析改火焰图


## 问题
1. 火焰图中的会出现一段一段的空白段，请问这是什么？
![空白段](./images/cpublank.png)

## 工具
[speedscope](https://www.speedscope.app)

## 参考链接

[快速定位NodeJs线上问题 - 之火焰图篇](https://juejin.im/post/5d0346266fb9a07ead59f7a6)

[如何读懂火焰图](http://www.ruanyifeng.com/blog/2017/09/flame-graph.html)
