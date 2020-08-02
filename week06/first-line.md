#为什么 first-letter 可以设置 float 之类的，而 first-line 不行呢？

::first-line 匹配到的第一行字符长度取决于很多因素，比如元素宽度和文字大小。

宽度变小或者文字变大后，第一行后面的字符会流到第二行。

如果 ::first-line 可以设置 float，第一行的文字就会形成单独一块，脱离当前文档流。

当遇到元素宽度变化和文字大小变化时，无法与第二行字符自由联动。

而 first-letter 是单独的一个确定性字符，就不存在这样的状况了。



参考资料：https://www.w3.org/TR/2019/WD-css-pseudo-4-20190225/#first-text-line

