# Ruby 数据类型

Ruby支持的数据类型包括基本的Number、String、Ranges、Symbols，以及true、false和nil这几个特殊值，同时还有两种重要的数据结构——Array和Hash。

您可以使用序列 \#{ expr } 替换任意 Ruby 表达式的值为一个字符串。在这里，expr 可以是任意的 Ruby 表达式。

实例

\#!/usr/bin/ruby -w

puts "相乘 : \#{24\*60\*60}";

这将产生以下结果：

相乘 : 86400

数组

数组字面量通过\[\]中以逗号分隔定义，且支持range定义。

（1）数组通过\[\]索引访问

（2）通过赋值操作插入、删除、替换元素

（3）通过+，－号进行合并和删除元素，且集合做为新集合出现

（4）通过&lt;&lt;号向原数据追加元素

（5）通过\*号重复数组元素

（6）通过｜和&符号做并集和交集操作（注意顺序）

实例

\#!/usr/bin/ruby

ary = \[ "fred", 10, 3.14, "This is a string", "last element", \]

ary.each do \|i\|

```
puts i
```

end

尝试一下 »

这将产生以下结果：

fred

10

3.14

This is a string

last element

如需了解更多有关 Ruby 数组的细节，请查看 Ruby 数组（Array）。

哈希类型

Ruby 哈希是在大括号内放置一系列键/值对，键和值之间使用逗号和序列 =&gt; 分隔。尾部的逗号会被忽略。

实例

实例

\#!/usr/bin/ruby

hsh = colors = { "red" =&gt; 0xf00, "green" =&gt; 0x0f0, "blue" =&gt; 0x00f }

hsh.each do \|key, value\|

```
print key, " is ", value, "\n"
```

end

范围类型

一个范围表示一个区间。

范围是通过设置一个开始值和一个结束值来表示。范围可使用 s..e 和 s...e 来构造，或者通过 Range.new 来构造。

使用 .. 构造的范围从开始值运行到结束值（包含结束值）。使用 ... 构造的范围从开始值运行到结束值（不包含结束值）。当作为一个迭代器使用时，范围会返回序列中的每个值。

范围 \(1..5\) 意味着它包含值 1, 2, 3, 4, 5，范围 \(1...5\) 意味着它包含值 1, 2, 3, 4 。

实例

\#!/usr/bin/ruby

 

\(10..15\).each do \|n\|

    print n, ' '

end



