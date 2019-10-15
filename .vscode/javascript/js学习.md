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

* 向数组添加元素 arr.push(elem)
* 删除数组最后一个元素 arr.pop()
* 将数组元素连接成一个字符串 arr.join(',')
* 连接两个数组 arr1.concat(arr2,arr3) 
* 在指定位置pos插入n元素 arr.splice(n,pos,elem[0],elem[1],...,elem[n])
* 将数组转化成字符串 arr.toString()
* 将新元素添加到数组的开头 arr.unshift(elem)
* 删除数组的第一个元素 arr.shift(elem)
* 选取数组中的元素 arr.slice(pos1,pos2) 返回从arr[pos1]到arr[pos2]之间的所有元素，包括pos1 不包括pos2

### 数组排序

* arr.sort() 字符串数组：首字母从a-z排序升序 再接着使用 arr.reverse() 将数组倒过来写 变成z-a降序
* 数字数组排序：升序 arr.sort(function(a,b){return a-b})
降序 arr.sort(function(a,b){return b-a})
* 数组的最值问题  
升序：第一项最小值
降序：第一项最大值
* 方法实现最值问题

```
    function myArrayMin(arr) {
        var len = arr.length;
        var min = Infinity;
        while (len--) {
            if (arr[len] < min) {
            min = arr[len];
            }
        }
        return min;
    }
    function myArrayMax(arr) {
        var len = arr.length;
        var max = -Infinity;
        while (len--) {
            if (arr[len] > min) {
            min = arr[len];
            }
        }
        return max;
    }
```

### 数组的迭代

* arr.forEach(function(value, index, array){}) 遍历循环
* arr.map(function(value,index,array){ return value*2 }) 数组的映射 对每一项做完操作形成新数组并返回
* arr.filter(function(value,index,array){ return value>18}) 过滤,返回return条件是真的项组成的数组
* arr.reduce(function(prev,cur,index,arr){
...
}, init)
作用：
1.求数组项之和  

var sum = arr.reduce(function (prev, cur) {
    return prev + cur;
},0)

2.求数组项最大值  

var max = arr.reduce(function (prev, cur) {
    return Math.max(prev,cur);
})

3.数组去重  

var newArr = arr.reduce(function (prev, cur) {
    prev.indexOf(cur) === -1 && prev.push(cur);
    return prev;
},[])

* arr.reduceRight() 与arr.reduce的遍历顺序相反

* arr.every(function(value, index, array){return value>18})  检查所有数组值是否通过测试 返回值 true/false

* arr.some((value, index, array) {return value > 18;}) 检查某些数组值是否通过了测试。 返回值 true/false

* arr.indexOf(string) IE8及以下不支持 返回第一个匹配的值的索引值

* arr.lastIndexOf(string) IE8及以下不支持 返回最后一个匹配的值的索引值

* arr.find(function(value, index, array){return value>18}) 返回满足条件第一个值

* arr.findIndex(function(value,index,array){return value>18}) 返回满足条件的第一个值的索引值

## JavaScript 错误处理

* try...catch...

``` utf-8
try {
  adddlert("欢迎您，亲爱的用户！");
}
catch(err) {
  document.getElementById("demo").innerHTML = err.message;
}
```

## 对象

* 删除对象的属性 delete obj.property
