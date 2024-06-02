# JavaScript
* 特性
  * 面向对象。不区分对象类型。通过原型机制继承，任何对象的属性和方法均可以被动态添加。
  * 变量类型不需要提前声明 (动态类型)。
  * 不能直接自动写入硬盘。
* 程序结构
```
(function () {
  "use strict";
  function greetMe(yourName) {
    alert("Hello " + yourName);
  }
  greetMe("World");
})();
``` 
# 声明
* var：声明一个变量，可选初始化一个值。
* let：声明一个块作用域的局部变量，可选初始化一个值。
* const：声明一个块作用域的只读常量。
## 变量名规则
必须以字母、下划线（_）或者美元符号（$）开头；后续的字符也可以是数字（0-9）。因为JavaScript语言是区分大小写的，所以字母可以是从“A”到“Z”的大写字母和从“a”到“z”的小写字母。
## 变量初始值
* 用 var 或 let 语句声明的变量，如果没有赋初始值，则其值为 undefined。
如果访问一个未声明的变量会导致抛出 ReferenceError 异常。
* 你可以使用 undefined 来判断一个变量是否已赋值。`letName === undefined`
* undefined 值在布尔类型环境中会被当作 false 。
* 数值类型环境中 undefined 值会被转换为 NaN。
* 空值 null 在数值类型环境中会被当作 0 来对待，而布尔类型环境中会被当作 false。
## 全局变量
在网页中，全局对象是 window ，所以你可以用形如 window.variable 的语法来设置和访问全局变量。
## 转义字符
| 字符 | 意思 |
| - | - |
| `\0` | Null 字节 |
| `\b` | 退格符 |
| `\f` | 换页符 |
| `\n` | 换行符 |
| `\r` | 回车符 |
| `\t` | Tab (制表符) |
| `\v` | 垂直制表符 |
| `\'` | 单引号 |
| `\"` | 双引号 |
| `\\` | 反斜杠字符（\） |
| `\XXX` | 由从 0 到 377 最多三位八进制数XXX表示的 Latin-1 字符。例如，\251 是版权符号的八进制序列。 |
| `\xXX` | 由从 00 和 FF 的两位十六进制数字 XX 表示的 Latin-1 字符。例如，\ xA9 是版权符号的十六进制序列。号 |
| `\uXXXX` | 由四位十六进制数字 XXXX 表示的 Unicode 字符。例如，\ u00A9 是版权符号的 Unicode 序列。见Unicode escape sequences (Unicode 转义字符). |
| `\u*{XXXXX}*` | Unicode 代码点 (code point) 转义字符。例如，\u{2F804} 相当于 Unicode 转义字符 \uD87E\uDC04 的简写。 |
***
# 循环
## for...in与for...of
```
let arr = [3, 5, 7];
arr.foo = "hello";
for (let i in arr) {
  console.log(i); // 输出 "0", "1", "2", "foo"
}
for (let i of arr) {
  console.log(i); // 输出 "3", "5", "7"
}
// 注意 for...of 的输出没有出现 "hello"
```