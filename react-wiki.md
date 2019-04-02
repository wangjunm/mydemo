# React 教程

>React 是一个用于构建用户界面的 JAVASCRIPT 库。
>
>React主要用于构建UI，很多人认为 React 是 MVC 中的 V（视图）。
>
>React 起源于 Facebook 的内部项目，用来架设 Instagram 的网站，并于 2013 年 5 月开源。
>
>React 拥有较高的性能，代码逻辑非常简单，越来越多的人已开始关注和使用它。

# React 特点
>1.声明式设计 −React采用声明范式，可以轻松描述应用。
>
>2.高效 −React通过对DOM的模拟，最大限度地减少与DOM的交互。
>
>3.灵活 −React可以与已知的库或框架很好地配合。
>
>4.JSX − JSX 是 JavaScript 语法的扩展。React 开发不一定使用 JSX ，但我们建议使用它。
>
>5.组件 − 通过 React 构建组件，使得代码更加容易得到复用，能够很好的应用在大项目的开发中。
>
>6.单向响应的数据流 − React 实现了单向响应的数据流，从而减少了重复代码，这也是它为什么比传统数据绑定更简单。
# React 安装

## node 安裝

安装react 需要先搭建node环境。传送门->[Node.js 教程](http://www.runoob.com/nodejs/nodejs-tutorial.html)。

建议在 React 中使用 CommonJS 模块系统，比如 browserify 或 webpack，本教程使用 webpack。

国内使用 npm 速度很慢，你可以使用淘宝定制的 cnpm (gzip 压缩支持) 命令行工具代替默认的 npm:

```shell 
$ npm install -g cnpm --registry=https://registry.npm.taobao.org
$ npm config set registry https://registry.npm.taobao.org
```

这样就可以使用 cnpm 命令来安装模块了：
```shell 
$ cnpm install [name]
```


## 使用 create-react-app 快速构建 React 应用

create-react-app 是来自于 Facebook，通过该命令我们无需配置就能快速构建 React 开发环境。

create-react-app 自动创建的项目是基于 Webpack + ES6 。

执行以下命令创建项目：
```shell 
$ cnpm install -g create-react-app
$ create-react-app my-app
$ cd my-app/
$ npm start
```
在浏览器中打开 http://localhost:3000/ ，结果如下图所示：
# demo1
项目的目录结构如下：
```shell
my-app/
  README.md
  node_modules/
  package.json
  .gitignore
  public/
    favicon.ico
    index.html
    manifest.json
  src/
    App.css
    App.js
    App.test.js
    index.css
    index.js
    logo.svg
```
manifest.json 指定了开始页面 index.html，一切的开始都从这里开始，所以这个是代码执行的源头。

尝试修改 src/App.js 文件代码：
```js
import React, { Component } from 'react';
import logo from './logo.svg';
import './App.css';
 
class App extends Component {
  render() {
    return (
      <div className="App">
        <div className="App-header">
          <img src={logo} className="App-logo" alt="logo" />
          <h2>欢迎来到菜鸟教程</h2>
        </div>
        <p className="App-intro">
          你可以在 <code>src/App.js</code> 文件中修改。
        </p>
      </div>
    );
  }
}
 
export default App;
```
修改后，打开 http://localhost:3000/ （一般自动刷新），输出结果如下：
# demo2