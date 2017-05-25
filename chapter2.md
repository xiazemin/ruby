# Ruby 模块（Module）

模块（Module）是一种把方法、类和常量组合在一起的方式。模块（Module）为您提供了两大好处。

模块提供了一个命名空间和避免名字冲突。

模块实现了 mixin 装置。

模块（Module）定义了一个命名空间，相当于一个沙盒，在里边您的方法和常量不会与其他地方的方法常量冲突。

模块类似与类，但有一下不同：

模块不能实例化

模块没有子类

模块只能被另一个模块定义

语法

module Identifier

statement1

statement2

...........

end

模块常量命名与类常量命名类似，以大写字母开头。方法定义看起来也相似：模块方法定义与类方法定义类似。

通过类方法，您可以在类方法名称前面放置模块名称和一个点号来调用模块方法，您可以使用模块名称和两个冒号来引用一个常量。

Ruby require 语句

require 语句类似于 C 和 C++ 中的 include 语句以及 Java 中的 import 语句。如果一个第三方的程序想要使用任何已定义的模块，则可以简单地使用 Ruby require 语句来加载模块文件：

语法

语法

require filename

在这里，文件扩展名 .rb 不是必需的。

实例

$LOAD\_PATH &lt;&lt; '.'

 

require 'trig.rb'

require 'moral'

 

y = Trig.sin\(Trig::PI/4\)

wrongdoing = Moral.sin\(Moral::VERY\_BAD\)

在这里，我们使用 $LOAD\_PATH &lt;&lt; '.' 让 Ruby 知道必须在当前目录中搜索被引用的文件。如果您不想使用 $LOAD\_PATH，那么您可以使用 require\_relative 来从一个相对目录引用文件。

注意：在这里，文件包含相同的函数名称。所以，这会在引用调用程序时导致代码模糊，但是模块避免了这种代码模糊，而且我们可以使用模块的名称调用适当的函数。

Ruby include 语句

您可以在类中嵌入模块。为了在类中嵌入模块，您可以在类中使用 include 语句：

