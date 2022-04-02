# Rollup.js

## 简介

### Overview（概述）

Rollup是一个JavaScript模块打包工具，它可以将小段代码编译成大段复杂的代码，像lib或是应用程序。它使用新的标准化模式对模块进行打包，而不是与过去相同的打包方案，如CommonJS和AMD。ES模块可以让你更简单的实现按需加载，更自由的引用你喜欢的lib中独有的函数。Rollup可以让按需加载在你打包时直接实现。

### Installation （安装）

```bash
npm i -g rollup
```
这是在全局安装rollup打包工具，如果你只想在项目中使用rollup打包工具，可以参考 Install Rollup Loacally。

### Quick Start （快速开始）

Rollup不仅可以使用命令行接口配合配置文件使用，也可以使用它的JavaScript API。可以执行`rollup --help`去查看可用的配置以及参数。

下面命令均以`main.js`为项目打包时的入口，以`bundle.js`为打包结果输出的出口。

对于浏览器：

```bash
# compile to a <script> containing a self-executing function ('iife')
rollup main.js -file budle.js --format iife
```

对于Node.js：

```bash
# compile to a CommonJS module ('cjs')
rollup main.js --file bundle.js --format cjs
```

对于浏览器和Node.js：

```bash
# UMD format requires a bundle name
rollup main.js --file bundle.js --format umd --name 'myBundle'
```