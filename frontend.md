## Tree-Shaking
Tree-Shaking 只对 import 语句导入产生作用，对于 CommonJS 的 require 函数导入方式不产生作用，因为 Tree-Shaking 的工作方式是对代码进行静态分析，import 只能出现在代码的第一层，不能出现在 if 分支中，而且被导入的模块以字符串常量出现，所以 import 完全可以满足静态分析的需要；而 require 可以出现在 if 条件分支中，参数也可以是动态产生的字符串，所以只有在动态执行时才知道 require 函数如何执行，这样 Tree-Shaking也就爱莫能助了。

*Ref*：深入浅出R下JS P45
