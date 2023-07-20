+++
authors = ["Trần Minh Tuấn"]
title = "Cấu hình của các phương trình toán học"
date = "2023-07-10"
description = "Hướng dẫn nhanh về sử dụng KaTeX"
math ="true"
tags = [
    "hugo",
    "markdown",
    "css",
    "html",
]
categories = [
    "Cú pháp",
    "Bản trình diễn chủ đề",
]
series = ["Bản trình diễn chủ đề"]
+++

Trong một dự án Hugo, các ký hiệu toán học có thể được sử dụng với sự trợ giúp của các thư viện JavaScript của bên thứ ba.

<!--more-->

Trong ví dụ này, chúng ta sẽ sử dụng [KaTeX](https://katex.org/).

-   Tạo một phần mẫu trong `/layouts/partials/math.html`
-   Bên trong, sử dụng [Auto-render Extension](https://katex.org/docs/autorender.html) hoặc phục vụ các tập lệnh cục bộ.
-   Bao gồm một phần trong các mẫu của bạn như sau:

```bash
{{ if or .Params.math .Site.Params.math }}
{{ partial "math.html" . }}
{{ end }}
```

-   Để bật KaTex trên toàn cầu, hãy đặt tham số `math` thành `true` trong cấu hình dự án
-   Để bật KaTex trên các trang cụ thể, hãy bao gồm tham số `math: true` trong tệp nội dung

**Nota:** Sử dụng tài liệu tham khảo trực tuyến [Supported TeX Functions](https://katex.org/docs/supported.html) làm cơ sở để tạo ra các kí hiệu toán học.

{{< math.inline >}}
{{ if or .Page.Params.math .Site.Params.math }}

<!-- KaTeX -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/katex.min.css" integrity="sha384-zB1R0rpPzHqg7Kpt0Aljp8JPLqbXI3bhnPWROx27a9N0Ll6ZP/+DiW/UqRcLbRjq" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/katex.min.js" integrity="sha384-y23I5Q6l+B6vatafAwxRu/0oK/79VlbSz7Q9aiSZUvyWYIYsd+qj+o24G5ZU2zJz" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/contrib/auto-render.min.js" integrity="sha384-kWPLUVMOks5AQFrykwIup5lo0m3iMkkHrD0uJ4H5cjeGihAutqP0yW0J6dpFiVkI" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
{{ end }}
{{</ math.inline >}}

### Examples

{{< math.inline >}}

<p>
Ký hiệu nội tuyến: \(\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…\)
</p>
{{</ math.inline >}}

Ký hiệu khối:

$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } }
$$
