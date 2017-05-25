# Ruby 语法

让我们编写一个简单的 Ruby 程序。所有的 Ruby 文件扩展名都是 .rb。所以，把下面的源代码放在 test.rb 文件中。

实例

\#!/usr/bin/ruby -w

puts "Hello, Ruby!";

运行实例 »

在这里，假设您的 /usr/bin 目录下已经有可用的 Ruby 解释器。现在，尝试运行这个程序，如下所示：

$ ruby test.rb

Ruby 程序中的行尾

Ruby 把分号和换行符解释为语句的结尾。但是，如果 Ruby 在行尾遇到运算符，比如 +、- 或反斜杠，它们表示一个语句的延续。

Ruby 标识符

标识符是变量、常量和方法的名称。Ruby 标识符是大小写敏感的。这意味着 Ram 和 RAM 在 Ruby 中是两个不同的标识符。

Ruby 标识符的名称可以包含字母、数字和下划线字符（ \_ ）。

Ruby 中的 Here Document

"Here Document" 是指建立多行字符串。在 &lt;&lt; 之后，您可以指定一个字符串或标识符来终止字符串，且当前行之后直到终止符为止的所有行是字符串的值。

如果终止符用引号括起，引号的类型决定了面向行的字符串类型。请注意&lt;&lt; 和终止符之间必须没有空格。

下面是不同的实例：

实例

\#!/usr/bin/ruby -w

\# -\*- coding : utf-8 -\*-

 

print &lt;&lt;EOF

    这是第一种方式创建here document 。

    多行字符串。

EOF

 

