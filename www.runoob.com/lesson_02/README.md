React使用JSX来替代常规的JavaScript。JSX是一个看起来像XML的JavaScript的语法扩展，我们不需要一定使用JSX，但它有以下优点：
- JSX执行更快，因为它编译为JavaScript代码后进行了优化
- 它是类型安全的，在编译过程中能够发现错误
- 使用JSX编写模块更加简单快速

#### 使用JSX
JSX看起来类似HTML：
```javascript
ReactDOM.render(
    <h1>Hello,world!</h1>,
    document.getElementById('example')
)
```

#### 独立文件
新建一个helloworld_react.js文件，代码如下
```javascript
ReactDOM.render(
	<h1>Hello world</h1>,
	document.getElementById('example')
)
```
然后在HTML文件中引入该JS文件[index.html](www.runoob.com/lesson_02/index.html)
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8"/>
		<title>Hello React!</title>
		<script src="https://cdn.bootcss.com/react/15.4.2/react.min.js"></script>
		<script src="https://cdn.bootcss.com/react/15.4.2/react-dom.min.js"></script>
		<script src="https://cdn.bootcss.com/babel-standalone/6.22.1/babel.min.js"></script>
		<script type="text/babel" src="helloworld_react.js"></script>
	</head>
	<body>
		<div id="example"></div>
	</body>
</html>
```
#### Javascript表达式
```javascript
ReactDOM.
```