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

\#!/usr/bin/ruby

\# -\*- coding: UTF-8 -\*-

def test

yield 5

puts "在 test 方法内"

yield 100

end

test {\|i\| puts "你在块 \#{i} 内"}

BEGIN 和 END 块

每个 Ruby 源文件可以声明当文件被加载时要运行的代码块（BEGIN 块），以及程序完成执行后要运行的代码块（END 块）。

实例

\#!/usr/bin/ruby

 

BEGIN { 

  \# BEGIN 代码块

  puts "BEGIN 代码块"

} 

 

END { 

  \# END 代码块

  puts "END 代码块"

}

  \# MAIN 代码块

puts "MAIN 代码块"

一个程序可以包含多个 BEGIN 和 END 块。BEGIN 块按照它们出现的顺序执行。END 块按照它们出现的相反顺序执行。当执行时，上面的程序输出以下结果：

