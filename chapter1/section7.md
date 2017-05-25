# Ruby块

块由大量的代码组成。

您需要给块取个名称。

块中的代码总是包含在大括号 {} 内。

块总是从与其具有相同名称的函数调用。这意味着如果您的块名称为 test，那么您要使用函数 test 来调用这个块。

您可以使用 yield 语句来调用块。

语法

block\_name{

statement1

statement2

..........

}

yield 语句

让我们看一个 yield 语句的实例：

实例

\#!/usr/bin/ruby

\# -\*- coding: UTF-8 -\*-

def test

puts "在 test 方法内"

yield

puts "你又回到了 test 方法内"

yield

end

test {puts "你在块内"}

以上实例运行结果为：

在 test 方法内

你在块内

你又回到了 test 方法内

你在块内



