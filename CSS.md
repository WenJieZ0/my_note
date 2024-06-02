# 语法
## 选择器
1. 类型：`h1 {}`
2. 类：`.box {}`
3. ID：`#box {}`
4. 标签属性：`a[title] {}`当a类型存在title属性时生效
5. 特定属性：`a[href="https://example.com"] {}`当a类型存在href属性且为该值时生效
6. 伪类、伪元素:
    [查看所有伪类，伪元素](https://www.w3school.com.cn/css/css_pseudo_classes.asp)
   * 伪类，用来样式化一个元素的特定状态。
    ```
    a:hover {
    }
    ```
    意为当鼠标指针悬浮到一个a元素上的时候生效。
    * 伪元素，选择一个元素的某个部分而不是元素自己。
    ```
    p::first-line {
    }
    ```
    意为当内容为p元素的第一行时生效。
7. 运算器组合选择：
    最后一组选择器可以将其他选择器组合起来，更复杂的选择素。
    ```
    article > p {
    }
    ```
    用运算符`>`选择了`<article>`元素的初代子元素`<p>`。
***