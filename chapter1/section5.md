# Ruby 注释



注释是在运行时会被忽略的 Ruby 代码内的注释行。单行注释以 \# 字符开始，直到该行结束，如下所示：

实例

\#!/usr/bin/ruby -w

 

\# 这是一个单行注释。

 

puts "Hello, Ruby!"



运行实例 »

当执行时，上面的程序会产生以下结果：

Hello, Ruby!

Ruby 多行注释

您可以使用 =begin 和 =end 语法注释多行，如下所示：

实例

\#!/usr/bin/ruby -w

 

puts "Hello, Ruby!"

 

=begin

这是一个多行注释。

可扩展至任意数量的行。

但 =begin 和 =end 只能出现在第一行和最后一行。 

=end

