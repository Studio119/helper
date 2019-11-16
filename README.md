# helper
开发系统中会遇到的一些问题的解决方案

# Case 0 - axios.helpers.normalizeHeaderName

在使用 axios 向服务器发送请求时，会遇到抛出错误
**`TypeError: "name.toUpperCase is not a function"`

此问题的产生原因为
参数传入该模块方法的时候，并未保证其类型为 string，
解决方案即先对 name 参数调用 toString() 方法。

开发过程中如若遇到此问题，
可使用此仓库的 **`./normalizeHeaderName.js`** 文件覆盖以下路径的同名文件：
**`.\node_modules\axios\lib\helpers\normalizeHeaderName.js`

