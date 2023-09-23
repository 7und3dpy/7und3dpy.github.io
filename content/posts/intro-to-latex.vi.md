+++
authors = ["Trần Minh Tuấn"]
title = "Giới thiệu về LATEX"
date = "2023-07-24"
description = "Bài viết mẫu hiển thị cú pháp Latex cơ bản."
tags = [
    "latex"
]
categories = [
    "study"
]
series = ["Latex"]
aliases = ["migrate-from-jekyl"]
+++


# 1. LaTeX là gì?
![](https://i.stack.imgur.com/t5VF4.png)

LaTeX là ngôn ngữ định dạng (document markup language) cho phép người dùng có thể soạn thảo tài liệu chất lượng cao cùng cấu trúc văn bản thống nhất và đồng bộ. LaTeX thường được sử dụng bởi sinh viên, giảng viên lẫn các nhà nghiên cứu về khoa học & kỹ thuật, cũng như một số lĩnh vực khác.

Tiền thân của LaTeX là TeX - ngôn ngữ định dạng do Donald Knuth phát minh nhưng rất khó sử dụng. Sau đó, LaTeX được phát minh bởi Leslie Lamport dựa trên TeX với nhiều cải tiến và trở nên phổ biến cho đến hiện nay.

Điểm đặc trưng của LaTeX nằm ở việc khuyến khích người dùng tập trung vào xây dựng nội dung và máy tính sẽ đảm nhiệm việc định dạng[1].


# 2. Tìm hiểu về LaTeX
## 2.1. Lợi ích từ LaTeX
- LaTeX có tính thống nhất: khoảng cách dòng, kích cỡ chữ, màu sắc, cách trình bày,... giúp bạn linh hoạt khi chuyển đổi đến văn bản khác.
- Tự động hoá nhiều thao tác: đánh số chương, xây dựng tiêu đề, tạo bảng, hình ảnh, tham chiếu,...
- Trích dẫn tài liệu tham khảo một cách tự động và nhất quán với hình thức trình bày gọn gàng.
- LaTex giúp bạn dễ dàng trình bày các công thức toán học ví dụ:
$$E = \frac{mc^2}{\sqrt{1-\frac{v^2}{c^2}}}$$
- LaTeX dễ làm việc với dự án lớn: Việc định dạng cả trăm, cả ngàn trang trong một file **.tex** với dung lượng không hề cao sẽ giúp bạn quản lý văn bản dễ dàng.
- LaTeX hiện có phần lớn packages giúp người dùng thực hiện nhiều công đoạn khác như thêm chú thích, vẽ sơ đồ, tạo bảng,... 
- LaTeX còn có những packages chuyên dụng phục vụ mục đích viết bài báo khoa học, trình chiếu lẫn thực hiện bảng tính.  

![](https://i.stack.imgur.com/ecqMl.jpg)
***Ảnh 01:*** *Một trong những lợi ích LaTeX mang lại trong việc định dạng văn bản dễ dàng*

## 2.2. Một số nhược điểm của LaTeX
- Cần thời gian để xây dựng cấu trúc chung cho tài liệu. Chẳng hạn như xây dựng format cho các bài báo khoa học.
- Soạn thảo trên LaTeX sẽ có chút tương đồng với việc lập trình - điều đó khiến bạn dễ tốn thời gian nếu gặp những lỗi nhỏ nhặt.
- Cần thời gian để học và sử dụng thành thạo LaTeX.

## 2.3. Một số Editor có thể tham khảo ở LaTeX
- MiKTeX (Bundle) (Windows)
- **Overleaf (Collaborative Online Editor)**
- Mactex (Bundle) (Mac)
- Texlive (Bundle) (Linux)
- Lyx (Bundle & Editor) (Windows, Mac, Linux)
- Texmaker (Windows, Mac, Linux)

Ở bài viết này, chúng ta sẽ tiến hành tìm hiểu chi tiết cách sử dụng LaTeX qua Editor Overleaf. Để bắt đầu, bạn có thể truy cập Overleaf ngay tại [đây](https://www.overleaf.com/). 

![](https://www.filepicker.io/api/file/ykJ4U4oRxXjmiuTyJ0QL)
***Ảnh 02:*** *Môi trường soạn thảo LaTeX trên Overleaf* 

# 3. Tìm hiểu về Overleaf
## 3.1. Điểm nổi bật của Overleaf
![](https://images.ctfassets.net/nrgyaltdicpt/5doLOtX69is0i6WIiY4um/6cc9be15c75155e7b93cd4823b742e44/overleaf_wide_colour_green_bg.png)

Overleaf là công cụ soạn thảo LaTeX miễn phí mang tính chất cộng tác trên nền web. Overleaf có nhiều tính năng khác biệt vốn nổi bật và thực sự hữu ích cho bất kỳ ai cần viết nhiều lẫn thực hiện cùng nhiều đối tượng.

Trong bài viết này, **nếu sử bạn không hề thông thạo LaTeX** hãy tham khảo một số cú pháp cơ bản về LaTeX tại [đây](https://www.overleaf.com/learn/latex/Free_online_introduction_to_LaTeX_(part_1)). Sau đó, Mình sẽ cung cấp đến bạn một chuẩn cơ bản khi thực hiện soạn thảo văn bản với LaTeX. Đừng ngần ngại copy các đoạn LaTeX code và chỉnh sửa lại để làm quen dần các bạn nhé!

## 3.2. Tạo project LaTeX trên Overleaf

**Và hơn hết, Mình vẫn khuyến khích bạn học cách sử dụng LaTeX**. LaTeX hoàn toàn không khó học và có nguồn thông tin, hướng dẫn gần như vô tận trên Internet về cách sử dụng LaTeX. Bạn sẽ không cần biết sâu về LaTeX (tuy nhiên một số lệnh và cách sử dụng vẫn sẽ cần thiết), và bạn sẽ có một hệ thống tuyệt vời để tự động hoá việc tổ chức bài viết của mình. 

Hãy tìm hiểu cùng Mình qua các bước sau.

## Bước 1 - Đăng ký tài khoản trên Overleaf
Để sử dụng Overleaf, bạn sẽ cần tạo tài khoản. Bạn có thể truy cập và đăng ký tại [đây](https://www.overleaf.com/register?source=post_page-----6599268c095f----------------------).

## Bước 2 - Tạo project mới sau khi đăng ký tài khoản trên Overleaf

![](https://www.filepicker.io/api/file/tJTSxbxOTdywD4SYmbrW)

1. Khi bạn đăng nhập, bạn sẽ thấy một hộp có tên là **New Project**. Nhấp vào hộp thoại này để bắt đầu tạo dự án. Một dự án trong Overleaf là một thư mục chứa một số tệp khác nhau.
2. Nếu bạn nhận được một URL trong email của bạn từ một người có tài liệu và bạn được yêu cầu nhấp vào URL để đến tài liệu, thì bạn đã có một tài liệu để làm việc, vì vậy chỉ cần đăng nhập sẽ dẫn bạn đến tài liệu đó.
3. Khi bạn nhấp vào **New Project**, bạn sẽ thấy một số mẫu tiêu chuẩn mà Overleaf đã thực hiện cho bạn như **Sample Project**. Tuy nhiên, chúng ta nên bắt đầu với **Blank Project** để tìm hiểu tổng quan hơn về các thao tác LaTeX trên Overleaf.

![](https://i.imgur.com/8Nccg2x.png?1)
***Ảnh 03***: *Môi trường soạn thảo cơ bản trên Overleaf* 

Hãy tiến hành nhìn từ trái sang phải:
1. Ở góc trên cùng bạn sẽ thấy dòng chữ **Menu** - tại đây chứa các chức năng như Download project, copy project, đếm số lượng chữ/ tiêu đề, liên kết với Git/Dropbox hay một số thao tác Setting chuyên sâu.
![](https://i.imgur.com/81fvwmk.png?1)
2. Cũng ở bên trái, bạn sẽ thấy một bảng điều khiển trông giống như một trình quản lý tệp tin ở bên trái. Theo mặc định, ta sẽ lựa chọn compile file **main.tex**. Bạn có thể upload thêm các tài liệu văn bản hoặc hình ảnh. Bên cạnh nó, gần một nửa màn hình là một bảng hiển thị tài liệu LaTeX với 2 tuỳ chọn là **Source** hoặc **Rich Text**. 
3. Nửa bên phải của màn hình sẽ hiển thị kết quả xuất khi xuất ra định dạng PDF. Tài liệu chủ yếu sẽ được compile và hiển thị tự động. Bạn có thể lựa chọn **Recompile** để có thể tự cập nhật nếu cần kiểm tra khi thực hiện tài liệu. Ở **Recompile**, bạn cũng có thể lựa chọn giữa việc bật/ tắt chế độ compile tự động, tốc độ compile nhanh (sẽ lưu dạng bản nháp)/ bình thường hay kiểm tra cú pháp trước khi compile.
![](https://i.imgur.com/igRmUCh.png?1)
4. Button tiếp theo bạn cần quan tâm chính là nút **Download PDF** - icon trắng thứ 2 nhìn từ **Recompile**. Button này sẽ giúp bạn lưu tài liệu về dạng Pdf nhanh chóng.
5. Ở góc trên cùng bên phải, bạn sẽ thấy button **Share** - bạn có thể lựa chọn **Turn on link sharing** để bất kỳ ai có link sẽ truy cập tham khảo và chỉnh sửa tài liệu. Còn nếu đây là tài liệu riêng tư, bạn có thể lựa chọn mời thủ công từng người dùng cộng tác qua email.
6. Bên cạnh button **Share** bạn sẽ thấy button **Submit** - button này sẽ giúp bạn submit trực tiếp tài liệu thực hiện đến các hội nghị, tạp chí khoa học uy tín. Đây cũng là một trong những tính năng độc đáo từ **Overleaf**.
7. Với button **History** bên cạnh button **Share**, đây là chức năng giúp bạn xem lại Lịch sử thực hiện chỉnh sửa tài liệu soạn thảo - phù hợp với nhu cầu back-up tài liệu.
![](https://i.imgur.com/gkxJClb.png?1)
8. Ở button cuối cùng **Chat** - đây là nơi để bạn liên lạc cùng những thành viên cộng tác. Điều đó sẽ giúp bạn tập trung ở Overleaf thay vì phải lựa chọn công cụ thứ 3 nếu phát sinh nhu cầu trao đổi nhóm.

### 3.2.1. Về File Manager Panel trong Overleaf
**Overleaf** cung cấp cho bạn một trình quản lý tệp tin giúp bạn có thể lưu trữ các tệp mà bạn sẽ sử dụng trong quá trình soạn thảo của mình. Đây có thể là tài liệu văn bản hoặc hình ảnh (nhớ chỉ tải lên tài liệu PDF, hình ảnh hoặc văn bản). Bạn cũng có thể tạo các thư mục mới nơi bạn có thể lưu trữ các tệp của mình. 

**Lưu ý**: Nếu project của bạn bạn có nhiều hình ảnh, bạn có thể tạo các thư mục riêng để giữ hình ảnh của mình.

Và trong hướng dẫn này, ta sẽ làm việc với file **main.tex** được tạo sẵn.

### 3.2.2. Tìm hiểu về Centre Panel

Hãy hình dung đây là khu vực thực hiện công việc soạn thảo chính. Centre Panel sẽ cung cấp cho bạn tất cả các công cụ và một số ràng buộc phục vụ mục đích soạn thảo.

Các mục menu ở đây không bao gồm các nút để chèn hình ảnh, bảng và trích dẫn. Qua đó, bạn phải sử dụng mã LaTeX. Và để hình dung rõ hơn, ta hãy tiến hành thiết kế Workflow cho file **main.tex**.

### 3.2.3. Một số lưu ý khi thực hiện soạn thảo ở LaTeX

Nhìn chung, các tài liệu học thuật như tài liệu nghiên cứu, bài báo khoa học,... luôn có một số cấu trúc phổ biến bao gồm:

- **Metadata**: Nơi bạn cung cấp tiêu đề, thông tin tác giả, thời gian và một số thông tin cơ bản khác. Trong LaTeX, bạn có thể hình dung đây là **Lời mở đầu**. Trong Overleaf, chúng ta đặt phần mở đầu ở đầu file **main.tex**. Ta sẽ khám phá chi tiết hơn khi chọn tính năng **Source** để hiển thị tài liệu.

- **Table and figures**: Phần lớn nhiều tài liệu học thuật sẽ chứa thông tin dưới dạng bảng và hình. Nếu bạn có nhiều bảng và số liệu, bạn nên đặt các số liệu và bảng trong các tệp riêng biệt có với các tên đơn cử **fig.tex** và **frames.tex**. Bằng cách đó, bạn có thể tham khảo chúng từ trong tài liệu hoặc bạn có thể sao chép và dán mã của bảng và số liệu từ các tài liệu đó vào phần cụ thể của tài liệu mà bạn đang viết.

- **Citiation**: Dân gian có câu "Nói có sách, mách có chứng". Việc sử dụng tài liệu tham khảo và trích dẫn chúng sẽ thể hiện sự tôn trọng của ta đến tác giả đã viết lẫn sử dụng tinh tế những tri thức được công nhận nhằm chứng minh cho luận điểm của mình.  

## 4. Xây dựng văn bản đầu tiên trên Overleaf

Bạn có thể vào Overleaf project của Mình, copy đoạn code này và paste vào link Overleaf của bạn nhé: https://www.overleaf.com/read/yhkrqpqdhcbj
**Note quan trọng**: Hãy lựa chọn compiler là XeLaTeX nếu muốn thử nghiệm các đoạn code trên nhé.
![](https://i.imgur.com/HbvTcYq.png?1)

### 4.1. Về phần khai báo giới thiệu - gồm tiêu đề bài viết lẫn các packages LaTeX cần thiết

Đầu tiên, ta sẽ lựa chọn loại document phù hợp. Ví dụ ở đây Ad lựa chọn loại document phù hợp để viết bài báo khoa học với cỡ giấy A4. 
```
\documentclass[a4paper]{article}
```
Liệt kê các packages sử dụng khi soạn thảo. Ở code block sau Ad có nhiều dấu **%** - mỗi khi ta liệt kê chúng ở đầu dòng nào thì dòng đó sẽ trở thành ghi chú. Với các ghi chú, chúng sẽ chỉ hiển thị ở cửa sổ soạn thảo và không xuất hiện ở file Pdf được xuất sau cùng.
```
% Packages này giúp chúng ta gõ tiếng Việt trên LaTeX
\usepackage[utf8]{inputenc}
% Packages này giúp chúng ta chèn hình ảnh vào LaTeX
\usepackage{graphicx}
% Đây là đường dẫn đến folder hình ảnh Ad đã tạo
\graphicspath{ {./images/} }
```

Tiếp theo, ta sẽ liệt kê tiêu đề bài viết, tên tác giả và ngày thực hiện tại đây. Bạn có thể tiến hành thay đổi các giá trị bên dưới.
```
\title{A Sample Document}
\author{Mình}
\date{\today}
```
### 4.2. Xây dựng nội dung trọng tâm
Qua đó, chúng ta đã kết thúc phần khai báo giới thiệu. Ta sẽ đến với phần quan trọng trong quá trình soạn thảo file LaTeX. Đầu tiên, bạn hãy luôn nhớ cú pháp sau:

```
% Dòng code này như một cánh cửa để ta tiến hành bắt đầu xây dựng tài liệu
\begin{document}

% Qua các thông tin giới thiệu được liệt kê, ta sẽ khai báo chúng tại đây
\maketitle
% \newpage là lệnh dễ dàng giúp bạn chuyển sang trang mới - Ad liệt kê ở đây vì thông thường một báo cáo chuẩn sẽ luôn dành hẳn một trang để làm trang bìa. 
\newpage

% ... Các dòng code khác bạn có thể tham khảo thêm ở link Overleaf Ad đã để sẵn nhé.

% Dòng code này dùng để kết thúc tài liệu, nếu thiếu dòng code này tài liệu sẽ báo lỗi
\end{document}
```
### 4.3. Xây dựng chương và mục lục tự động

Ta sẽ tiến hành tạo mục lục theo cú pháp sau:
```
\tableofcontents
\newpage
```

Để khai báo các Chương, ta khai báo với dạng \section, \subsection và một điểm đặc biệt ở LaTeX là chúng sẽ tự động cập nhật vào mục lục. 

```
\section{Chương 1}
\subsection{Chương con của chương 1}
% nếu muốn tiếp tục khai báo chương con, ta lại tiếp tục \subsubsection , \subsubsubsection , ...
```

Với các chương được thêm vào, mục lục sẽ được cập nhật tự động như thế này:
![](https://i.imgur.com/q2yW1dP.png?1)

### 4.4. Thêm hình ảnh trong Overleaf

Để thêm hình ảnh, bạn hãy thực hiện theo các bước: 
- Add hình ảnh lên project Overleaf, bạn có thể tạo thêm thư mục để dễ quản lý. Chẳng hạn như ảnh bên dưới, Ad tạo folder **images** để chứa tất cả hình ảnh.
![](https://i.imgur.com/R3e14Tm.png?1)
- Sử dụng đoạn code sau để add ảnh vào LaTeX nhé!
```
% Đây là cách tiếp cận đơn giản nhất trong việc add ảnh vào LaTeX
% Để chỉnh sửa chi tiết hơn, bạn hãy đọc thêm tài liệu LaTeX
\begin{figure}[ht]
\includegraphics[width=\textwidth]{name_of_the_file}
\end{figure}
```

### 4.5. Thêm table trong Overleaf

Xây dựng table mẫu, bạn có thể vào link: http://www.tablesgenerator.com/ để tạo table và copy đoạn code LaTeX ở website vào file.

### 4.6. Xây dựng danh mục tài liệu tham khảo và trích dẫn trong Overleaf
Ta sẽ xây dựng danh mục tài liệu tham khảo đơn giản qua các dòng code sau:
```
\begin{thebibliography}{2}
\bibitem{doc1}
Tên tác giả, \emph{Tài liệu 1}. Nơi xuất bản.
\bibitem{doc2}
Tên tác giả, \emph{Tài liệu 2}. Nơi xuất bản.
\end{thebibliography}
```

Qua các danh mục tài liệu tham khảo, ta có thể tiến hành trích dẫn qua lệnh **\cite{tên tài liệu được liệt kê ở \bibitem}**

## 5. Tổng kết

Mỗi công cụ soạn thảo luôn có những ưu và nhược điểm nhất định. Tuy nhiên, nếu bạn định hướng theo lĩnh vực nghiên cứu hay dự kiến thực hiện các bài báo khoa học trong tương lai thì LaTeX sẽ là lựa chọn phù hợp dành cho bạn. 

Cùng với đó, Overleaf cũng sẽ là một trợ thủ đắc lực với một trình soạn thảo online và giúp bạn kết nối soạn thảo cùng những thành viên trong dự án. 

**Mình Team**

## **Nguồn tham khảo**: 

[1] [Khoá học LateX online](https://www.overleaf.com/learn/latex/Free_online_introduction_to_LaTeX_(part_1)) được biên soạn bởi [Tiến sĩ Dr John Lees-Miller](https://www.overleaf.com/ourteam) và trình bày ban đầu tại Đại học Bristol.
<br>
[2] [How to use Overleaf to Write your papers](https://medium.com/thoughts-philosophy-writing/how-to-use-overleaf-to-write-your-papers-part-i-basic-minimalist-setup-6599268c095f) - Arindam Basu.