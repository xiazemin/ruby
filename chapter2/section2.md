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

使用 ensure 语句

有时候，无论是否抛出异常，您需要保证一些处理在代码块结束时完成。例如，您可能在进入时打开了一个文件，当您退出块时，您需要确保关闭文件。

ensure 子句做的就是这个。ensure 放在最后一个 rescue 子句后，并包含一个块终止时总是执行的代码块。它与块是否正常退出、是否抛出并处理异常、是否因一个未捕获的异常而终止，这些都没关系，ensure 块始终都会运行。

语法

begin 

   \#.. 过程

   \#.. 抛出异常

rescue 

   \#.. 处理错误 

ensure 

   \#.. 最后确保执行

   \#.. 这总是会执行

end

Catch 和 Throw

raise 和 rescue 的异常机制能在发生错误时放弃执行，有时候需要在正常处理时跳出一些深层嵌套的结构。此时 catch 和 throw 就派上用场了。

catch 定义了一个使用给定的名称（可以是 Symbol 或 String）作为标签的块。块会正常执行直到遇到一个 throw。



