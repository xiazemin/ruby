# Ruby变量

变量是持有可被任何程序使用的任何数据的存储位置。

Ruby 支持五种类型的变量。

一般小写字母、下划线开头：变量（Variable）。

$开头：全局变量（Global variable）。

@开头：实例变量（Instance variable）。

@@开头：类变量（Class variable）类变量被共享在整个继承链中

大写字母开头：常数（Constant）。

在 Ruby 中，您可以通过在变量或常量前面放置 \# 字符，来访问任何变量或常量的值。

Ruby 伪变量

它们是特殊的变量，有着局部变量的外观，但行为却像常量。您不能给这些变量赋任何值。

self: 当前方法的接收器对象。

true: 代表 true 的值。

false: 代表 false 的值。

nil: 代表 undefined 的值。

\_\_FILE\_\_: 当前源文件的名称。

\_\_LINE\_\_: 当前行在源文件中的编号。

