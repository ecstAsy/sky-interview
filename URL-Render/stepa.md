<h3 align='center'>从浏览器接收url到开启网络请求线程</h3>

* 浏览器进程/线程模型，JS的运行机制

  - Browser进程：浏览器的主进程（负责协调、主控），只有一个
  - 第三方插件进程：每种类型的插件对应一个进程，仅当使用该插件时才创建
  - GPU进程：最多一个，用于3D绘制
  - 浏览器渲染进程（内核）：默认每个Tab页面一个进程，互不影响，控制页面渲染，脚本执行，事件处理等（有时候会优化，如多个空白tab会合并成一个进程） 