可以直接使用BootCDN的React CDN库
```html
<script src="https://cdn.bootcss.com/react/15.4.2/react.min.js"></script>
<script src="https://cdn.bootcss.com/react/15.4.2/react-dom.min.js"></script>
<script src="https://cdn.bootcss.com/babel-standalone/6.22.1/babel.min.js"></script>
```
#### 使用案例
```html

<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Hello React!</title>
    <script src="https://cdn.bootcss.com/react/15.4.2/react.min.js"></script>
    <script src="https://cdn.bootcss.com/react/15.4.2/react-dom.min.js"></script>
    <script src="https://cdn.bootcss.com/babel-standalone/6.22.1/babel.min.js"></script>
  </head>
  <body>
    <div id="example"></div>
    <script type="text/babel">
      ReactDOM.render(
        <h1>Hello, world!</h1>,
        document.getElementById('example')
      );
    </script>
  </body>
</html>
```
#### 实例解析
引入了三个库：react.min.js、react-dom.min.js和babel.min.js
- react.min.js - React的核心库
- react-dom.min.js - 提供与DOM相关的功能
- babel.min.js - Babel可以将ES6代码转化为ES5的代码，这样可以在目前不支持ES6的浏览器上执行React代码。Babel内嵌了对JSX的支持。
```javascript
ReactDOM.render(
    <h1>Hello world!</h1>,
    document.getElementById('example')
);
```
以上代码将一个h1标题，插入到id="exmaple"节点中

**注意**:
***如果我们需要使用JSX，则<script>标签中的type属性要设置为text/babel***

#### 通过npm使用React
如果国内使用npm比较慢，可以使用淘宝定制的cnpm命令行工具替换默认的npm:
> $ npm install -g cnpm --registry=https://registry.npm.taobao.org
> 
> $ npm config set registry https://registry.npm.taobao.org 

这样就可以通过cnpm命令来安装模块了
> $ cnpm install [name]

#### 使用create-react-app快速构建React开发环境
create-react-app来源于Facebook，通过该命令能够快速构建React开发环境

create-react-app自动创建项目是基于Webpack+ES6，执行如下命令创建项目：
> $ cnpm install -g create-react-app
>
> $ create-react-ap my-app
> 
> $ cd my-app
> $
> $ npm start

在浏览器中打开http://localhost:3000/，结果如下
![http://www.runoob.com/wp-content/uploads/2016/02/0FBC219D-EFF6-4F0D-BB9D-2A97BD177770.jpg](http://www.runoob.com/wp-content/uploads/2016/02/0FBC219D-EFF6-4F0D-BB9D-2A97BD177770.jpg)
尝试修改 src/App.js 文件代码：
```javascript
import React, { Component } from 'react';
import logo from './logo.svg';
import './App.css';

class App extends Component {
  render() {
    return (
      <div className="App">
        <header className="App-header">
          <img src={logo} className="App-logo" alt="logo" />
          <h1 className="App-title">Welcome to React</h1>
		  <h2>欢迎来到菜鸟教程</h2>
        </header>
        <p className="App-intro">
          To get started, edit <code>src/App.js</code> and save to reload.
        </p>
      </div>
    );
  }
}

export default App;

```
修改后，打开http://localhost:3000/ 结果如下
![https://www.runoob.com/wp-content/uploads/2016/02/629B9FC4-7FD7-42A4-BBA0-B108B3F83BD9.jpg](https://www.runoob.com/wp-content/uploads/2016/02/629B9FC4-7FD7-42A4-BBA0-B108B3F83BD9.jpg)