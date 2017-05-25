# Ruby异常

在 begin/end 块中附上可能抛出异常的代码，并使用 rescue 子句告诉 Ruby 完美要处理的异常类型。

语法

begin \#开始

raise.. \#抛出异常

rescue \[ExceptionType = StandardException\] \#捕获指定类型的异常 缺省值是StandardException

$! \#表示异常信息

$@ \#表示异常出现的代码位置

else \#其余异常

..

ensure \#不管有没有异常，进入该代码块

end \#结束

使用 raise 语句

您可以使用 raise 语句抛出异常。下面的方法在调用时抛出异常。它的第二个消息将被输出。

语法

raise 

 

或

 

raise "Error Message" 

 

或

 

raise ExceptionType, "Error Message"

