# Hướng dẫn cú pháp Markdown



Bài viết này là một ví dụ cơ bản để hiển thị cú pháp Markdown được sử dụng trong các tệp nội dung của Hugo. Nó cũng cho thấy cách mỗi phần tử HTML cơ bản được tạo kiểu bằng CSS với chủ đề Hugo.

<!--more-->

## Tiêu đề

Các phần tử HTML sau `<h1>`-`<h6>` đại diện cho 6 cấp độ tiêu đề của phần. `<h1>` là dành cho các phần cấp cao nhất trong khi `<h6>` là dành cho cấp thấp nhất.

# H1

## H2

### H3

#### H4

##### H5

###### H6

## Đoạn văn

Xerum, người mà tôi có thể giải thích ai đang đau đớn. Và khi tôi đến với bạn, khi tôi tràn ngập niềm vui, tôi đau đớn, hoặc tôi được sinh ra, hoặc tôi là một kẻ ngốc, vì người đã làm tôi đau đớn với niềm vui của tôi, là chuyên gia về mọi thứ, hoặc những gì anh ta đã xé nát và rách nát, và ý chí của anh ta bị xé nát, như thể anh ta đáng được chở che, anh ta có đi đến trái tim và làm theo những điều giống nhau không? Tại sao lỗ chân lông lại nhô lên, khi nó được đặt ở một nơi không biết ý muốn của chuột hay vạn vật? Tôi sẽ im lặng. Đối với tất cả những gì tôi là, trái tim tôi bị xáo trộn theo cách này hay cách khác, và tôi xé chúng ra và làm khô chúng, để tôi có thể giết chúng hoặc ném chúng đi. Anh ta ghét sự thật, mà làn sóng veliamenim là nguyên nhân và bản thân khuôn mặt, bạn đang ở trong tình huống đau đớn của phiên bản.

Là nó đi du lịch? Bởi vì trong chuyện của mỗi người có một số điều bạn ghét hoặc bạn ghét, bạn sẽ ăn để không để sự khôn ngoan của mình che giấu sự thật rằng trái tim và trái tim hoặc điều đó thật buồn cười.

## Trích dẫn

Thành phần trích dẫn đại diện cho nội dung được trích dẫn từ một nguồn khác, tùy chọn có nguồn được chứa trong một phần tử `footer` hoặc `cite`, và cũng tùy chọn với thông tin in dòng như ghi chú và viết tắt.

#### Trích dẫn không có nguồn

> Sau đó, để đúc andaepu, kiến ​​​​thức được cung cấp sẽ được cắt giảm tương ứng.
> **Lưu ý** rằng bạn có thể sử dụng cú pháp Markdown trong một trích dẫn.

#### Trích dẫn có nguồn

> Không giao tiếp bằng cách chia sẻ bộ nhớ, hãy chia sẻ bộ nhớ bằng cách giao tiếp.<br>
> — <cite>Rob Pike[^1]</cite>

## Bảng

Bảng không phải là một phần cốt lõi của thông số kỹ thuật Markdown, nhưng Hugo hỗ trợ chúng.

| Tên | Tuổi |
|---|---|
| Bob   | 27    |
| Alice | 23    |

#### Bảng với Markdown trong dòng

| Italics | Bold | Code |
|---|---|---|
| _italics_ | **bold** | `code` |

## Khối mã

#### Khối mã với dấu ngoặc đơn

```html
<!DOCTYPE html>
<html lang="vi">
    <head>
        <meta charset="utf-8" />
        <title>Ví dụ về HTML5</title>
    </head>
    <body>
        <p>Kiểm tra</p>
    </body>
</html>
```

#### Khối mã với bốn khoảng trắng

```html
    <!doctype html>
    <html lang="en">
    <head>
      <meta charset="utf-8">
      <title>Example HTML5 Document</title>
    </head>
    <body>
      <p>Test</p>
    </body>
    </html>
```

#### Khối mã với shortcode highlight nội bộ của Hugo

{{< highlight html >}}

<!doctype html>
<html lang="pt-br">
<head>
  <meta charset="utf-8">
  <title>Ví dụ về HTML5</title>
</head>
<body>
  <p>Kiểm tra</p>
</body>
</html>
{{< /highlight >}}

## Loại danh sách

#### Danh sách được sắp xếp

1. Mục đầu tiên
2. Mục thứ hai
3. Mục thứ ba

#### Danh sách không được sắp xếp

-   Một mục
-   Một mục khác
-   Một số mặt hàng khác

#### Danh sách lồng nhau

-   Trái cây
    -   Rác
    -   Quả cam
    -   Chuối
-   Các sản phẩm từ sữa
    -   sữa
    -   Phô mai

#### Chú thích

Đánh dấu[^2] ở cuối[^3] của văn bản này[^4].

## Các yếu tố khác — abbr, sub, sup, kbd, mark

<abbr title="Định dạng trao đổi đồ hoạ">GIF</abbr> là định dạng ảnh bitmap.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Nhấn <kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Xoá</kbd></kbd> để đóng.

Hầu hết <mark>kỳ nhông</mark> là loài sống về đêm và săn côn trùng, sâu và các sinh vật nhỏ khác.

[^1]: Đoạn trích trên được lấy từ [màn trình diễn](https://www.youtube.com/watch?v=PAAkCSZUG1c) của Rob Pike trong Gopherfest, ngày 18 tháng 11 năm 2015.
[^2]: Chú thích cuối trang.
[^3]: Một cái khác ở đây.
[^4]: Hay nhỉ?

