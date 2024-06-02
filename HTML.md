# HTML
## HTML页面的结构
```
<!doctype html>
<html lang="zh-CN">
  <head>
    <meta charset="utf-8" />
    <title>我的测试站点</title>
  </head>
  <body>
    <p>这是我的页面</p>
  </body>
</html>
```
1. `<!DOCTYPE html>`: 声明文档类型。能自动检查书写错误。
2. `<head></head>`：这个元素是一个容器，它包含了所有你想包含在 HTML 页面中但不在 HTML 页面中显示的内容。这些内容包括你想在搜索结果中出现的关键字和页面描述、CSS 样式、字符集声明等等。以后的章节中会学到更多相关的内容。
3. `<meta charset="utf-8">`：这个元素代表了不能由其他 HTML 元相关元素表示的元数据，比如 `<base>、<link>、<script>、<style> 或 <title>。`charset 属性将你的文档的字符集设置为 UTF-8，其中包括绝大多数人类书面语言的大多数字符。有了这个设置，页面现在可以处理它可能包含的任何文本内容。没有理由不对它进行设置，它可以帮助避免以后的一些问题。
## 特殊字符引用
| 原意字符 | 等价字符 |
| - | - |
| `<` | `&lt;` |
| `>` | `&gt;` |
| `"` | `&quot;` |
| `'` | `&apos;` |
| `&` | `&amp;` |
## 为文档设定主语言
```
<html lang="zh-CN">
  …
</html>
```

***

