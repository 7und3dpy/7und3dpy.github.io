+++
authors = ["Trần Minh Tuấn"]
title = "Hỗ trợ biểu tượng cảm xúc"
date = "2023-07-07"
description = "Hướng dẫn sử dụng biểu tượng cảm xúc với Hugo"
tags = [
    "hugo",
    "markdown",
    "emoji",
]
categories = [
    "Cú pháp",
    "Bản trình diễn chủ đề",
]
series = ["Bản trình diễn chủ đề"]
+++

Biểu tượng cảm xúc có thể được kích hoạt trong dự án Hugo theo nhiều cách.

<!--more-->

Chức năng [`emojify`](https://gohugo.io/functions/emojify/) có thể được gọi trực tiếp trong các mẫu hoặc với [Inline Shortcodes](https://gohugo.io/templates/shortcode-templates/#inline-shortcodes).

Để bật biểu tượng cảm xúc trên toàn cầu, hãy áp dụng `enableEmoji` với giá trị `true` đã [cài đặt](https://gohugo.io/getting-started/configuration/) từ trang web của bạn và sau đó bạn có thể thêm mã biểu tượng cảm xúc trực tiếp vào tệp nội dung. Ví dụ:

<p><span class="nowrap"><span class="emojify">🙈</span> <code>:see_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙉</span> <code>:hear_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙊</span> <code>:speak_no_evil:</code></span></p>
<br>

Ô [Emoji cheat sheet](http://www.emoji-cheat-sheet.com/) là một tài liệu tham khảo hữu ích để xác định mã biểu tượng cảm xúc.

---

**Nota:** Các bước trước kích hoạt chuỗi biểu tượng cảm xúc và ký tự Chuẩn Unicode trong Hugo, tuy nhiên, việc hiển thị các nét tượng trưng này phụ thuộc vào trình duyệt và nền tảng được sử dụng. Để chọn kiểu biểu tượng cảm xúc, bạn có thể sử dụng phông chữ biểu tượng cảm xúc của bên thứ ba hoặc danh sách phông chữ. Ví dụ:

{{< highlight html >}}
.emoji {
font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
}
{{< /highlight >}}

{{< css.inline >}}

<style>
.emojify {
	font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
	font-size: 2rem;
	vertical-align: middle;
}
@media screen and (max-width:650px) {
  .nowrap {
    display: block;
    margin: 25px 0;
  }
}
</style>

{{< /css.inline >}}
