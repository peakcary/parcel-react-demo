[Parcel](https://parceljs.org/)是一个新的打包工具，其特点是零配置、速度快。
### 1 新建目录

```js
mkdir parcel-react-demo
cd pracel-react-demo
```
### 2 初始化目录

```js
npm init -y
```

或

```js
yarn init -y
```

此时会创建package.json文件，文件内容

```
{
  "name": "parcel-react-demo",
  "version": "1.0.0",
  "main": "index.js",
  "author": "peak",
  "license": "MIT",
  "scripts": { 
    "test": "echo \"Error: no test specified\" && exit 1"
  }
}

```

### 3 添加 React

```js
npm install react react-dom --save
```
或
```js
yarn add react react-dom
```
package.json内容
```json
 
### 4 添加babel

新建.babelrc文件
```
touch .babelrc
```
输入内容
```
{
	"presets":["react"]
}
```

添加babel-preset-react:
```js
npm install babel-preset-react --D
```
或
```
yran add babel-preset-react -D
```

### 5 添加 Parcel

```js
npm install pracel-bundler --D
```
或
```js
yarn add pracel-bundler -D
```

### 6 新建index.html
内容
```html
<html>
	<body>
		<div id="root"></div>
		<script src="./index.js"></script>
	</body>
</html>
```

### 7 新建index.js
内容
```
import React from "react";
import ReactDOM from "react-dom";

const App = () => {
	return <h1>Hello Peak</h1>;
}

ReactDOM.render(<App />,document.getElementById("root"));
```

### 8 添加打包命令

package.json添加内容
```
"start":"parcel index.html"
```

### 9 完成

运行
```
npm start
```
或
```
yarn start
```
在浏览器打开http://localhost:1234

打包过程中会产生.cache和dist两个目录，如果是在git工程里面,可以新建.gitignort文件忽略这两个目录
```
.cache
dist
node_modules
```