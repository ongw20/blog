## Tree-Shaking
Tree-Shaking 只对 import 语句导入产生作用，对于 CommonJS 的 require 函数导入方式不产生作用，因为 Tree-Shaking 的工作方式是对代码进行静态分析，import 只能出现在代码的第一层，不能出现在 if 分支中，而且被导入的模块以字符串常量出现，所以 import 完全可以满足静态分析的需要；而 require 可以出现在 if 条件分支中，参数也可以是动态产生的字符串，所以只有在动态执行时才知道 require 函数如何执行，这样 Tree-Shaking也就爱莫能助了。

*Ref*：深入浅出RxJS P45

## script 标签
直接写在 `html` 中 `script` 标签中的 js 代码会阻塞整个页面，包括html结构中他上面的内容。  
`<script src="..."></script>`不会阻塞他之前内容的渲染，但等他下载执行完后他后面的内容才会渲染。  
异步创建 `script` 不会阻塞页面渲染。

`script` 标签 `onload` 在 js 文件加载并执行完毕后调用。

`webpack` 将多个符合 `CommonJS` 规范的模块打包成一个 js 文件，供浏览器执行。异步加载可通过动态创建 `script` 标签实现。

## CRP
即 关键渲染路径 (Critical Rendering Path)  
关键渲染路径是浏览器将 HTML CSS JavaScript 转换为在屏幕上呈现的像素内容所经历的一系列步骤。
