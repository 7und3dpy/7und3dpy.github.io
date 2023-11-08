+++
authors = ["Trần Minh Tuấn"]
title = "HTML and CSS only tabs"
date = "2023-07-09"
description = "Sample article showcasing shortcodes for HTML/CSS only tabs"
tags = [
    "hugo",
    "markdown",
    "css",
    "html",
    "shortcodes",
]
categories = [
    "Cú pháp",
    "Bản trình diễn chủ đề",
]
series = ["Bản trình diễn chủ đề"]
aliases = ["migrate-from-jekyl"]
+++

## Shortcodes

Nội dung sau:

```markdown
{{</* tabgroup */>}}
{{</* tab name="Hello" */>}}
Hello World!
{{</* /tab */>}}

{{</* tab name="Goodbye" */>}}
Goodbye Everybody!
{{</* /tab */>}}
{{</* /tabgroup */>}}
```

Sẽ tạo ra:

{{< tabgroup >}}
{{< tab name="Hello" >}}
Hello World!
{{< /tab >}}

{{< tab name="Goodbye" >}}
Goodbye Everybody!
{{< /tab >}}
{{< /tabgroup >}}

## căn lề phải

Bạn cũng có thể căn chỉnh các tab sang bên phải:

```markdown
{{</* tabgroup align="right" */>}}
{{</* tab name="Hello" */>}}
Hello World!
{{</* /tab */>}}

{{</* tab name="Goodbye" */>}}
Goodbye Everybody!
{{</* /tab */>}}
{{</* /tabgroup */>}}
```

Thu được kết quả sau:

{{< tabgroup align="right" >}}
{{< tab name="Hello" >}}
Hello World!
{{< /tab >}}

{{< tab name="Goodbye" >}}
Goodbye Everybody!
{{< /tab >}}
{{< /tabgroup >}}

## Nội dung đánh dấu

Mọi nội dung Markdown hợp lệ đều có thể được sử dụng bên trong các tab:

````markdown
{{</* tabgroup align="right" style="code" */>}}
{{</* tab name="Ruby" */>}}

```ruby
puts 'Hello'
```

{{</* /tab */>}}
{{</* tab name="Python" */>}}

```python
print('Hello')
```

{{</* /tab */>}}
{{</* tab name="JavaScript" */>}}

```js
console.log("Hello");
```

{{</* /tab */>}}
{{</* /tabgroup */>}}
````

Vì vậy, bạn sẽ nhận được kết quả như sau:

{{< tabgroup align="right" style="code" >}}
{{< tab name="Ruby" >}}

```ruby
puts 'Hello'
```

{{< /tab >}}
{{< tab name="Python" >}}

```python
print('Hello')
```

{{< /tab >}}
{{< tab name="JavaScript" >}}

```js
console.log("Hello");
```

{{< /tab >}}
{{< /tabgroup >}}

Trong ví dụ này, `style="code"` làm cho kết quả dễ chịu hơn khi nội dung hoàn toàn là các khối mã.
