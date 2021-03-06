# Ruby 方法

Ruby 方法与其他编程语言中的函数类似。Ruby 方法用于捆绑一个或多个重复的语句到一个单元中。

方法名应以小写字母开头。如果您以大写字母作为方法名的开头，Ruby 可能会把它当作常量，从而导致不正确地解析调用。

方法应在调用之前定义，否则 Ruby 会产生未定义的方法调用异常。

语法

def method\_name \[\( \[arg \[= default\]\]...\[, \* arg \[, &expr \]\]\)\]

expr..

end

从方法返回值

Ruby 中的每个方法默认都会返回一个值。这个返回的值是最后一个语句的值。例如：

实例

def test

i = 100

j = 10

k = 0

end

在调用这个方法时，将返回最后一个声明的变量 k。

Ruby return 语句

Ruby 中的 return 语句用于从 Ruby 方法中返回一个或多个值。

语法

return \[expr\[\`,' expr...\]\]

如果给出超过两个的表达式，包含这些值的数组将是返回值。如果未给出表达式，nil 将是返回值。

可变数量的参数

假设您声明了一个带有两个参数的方法，当您调用该方法时，您同时还需要传递两个参数。

但是，Ruby 允许您声明参数数量可变的方法。让我们看看下面的实例：

实例

\#!/usr/bin/ruby

\# -\*- coding: UTF-8 -\*-

 

def sample \(\*test\)

   puts "参数个数为 \#{test.length}"

   for i in 0...test.length

      puts "参数值为 \#{test\[i\]}"

   end

end

sample "Zara", "6", "F"

sample "Mac", "36", "M", "MCA"

