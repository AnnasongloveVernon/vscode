# js学习

## 字符串方法

str.indexOf('string'):返回该字符在字符串中首次出现的位置  
str.match('string'):在字符串化中执行对字母搜索，并显示匹配项(括号中可用字符串表达式)
str.replace("被替换字段","要替换的值")
str.toUpperCase() 转换成大写
str.tolowerCase() 转换成小写
str.split(',') 拆分字符串并存入数组

## 数字方法

浮点数的算术不是100%精确，但是可以通过乘一个数再同一个数解决
（5.123）.toFixed(2) 保留两位小数
（5.123）.toPrecision(2) 返回指定长度的数字

## 数组方法

判断是否是array
1.arr instanceof Array true
2.Array.isArray(arr)  true