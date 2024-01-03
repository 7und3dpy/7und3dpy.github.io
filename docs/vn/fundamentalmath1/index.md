# Kiến thức toán cơ bản cho Data Science (phần 1)

Bài viết mẫu hiển thị các kiến thức cơ bản về toán.

<!--more-->




# Kiến thức toán cho lĩnh vực Data Science (Phần 1)

Để bắt đầu học Machine Learning hay Data Science, người học sẽ bị choáng ngợp bởi khối lượng kiến thức đồ sộ liên quan đến lĩnh vực Toán học. Đây cũng là điều hiển nhiên bởi Toán học luôn là nền tảng cho bất kỳ ngành Khoa học đương đại nào.

![](https://149695847.v2.pressablecdn.com/wp-content/uploads/2019/01/Data-science-without-mathematics.jpg)

Sự vững chắc về nền tảng toán học hình thành đằng sau các thuật toán sẽ tạo cho bạn một lợi thế không hề nhỏ so khi nghiên cứu và làm việc ở lĩnh vực Data Science. **Bởi hơn hết, doanh nghiệp luôn chỉ trả rất nhiều tiền cho công nghệ bên trong máy móc thay vì người vận hành vốn không có bất kỳ kiến thức chuyên sâu nào về chúng.** Bạn hiểu ý này chứ  ?

Để tìm hiểu chuyên sâu hơn ta có thể hình dung một quy trình khoa học phổ biến trong xử lý Âm thanh như sau:
  - Khai thác thông tin, tính chất vật lý của âm thanh và Mô hình hóa quá trình hình thành chúna
  - Xây dựng giả thuyết hình thành về chúng
  - Ước tính độ chất lượng của nguồn dữ liệu thu thập được
  - Định lượng sự không chắc chắn xung quanh dữ liệu và dự đoán
  - Xác định mẫu ẩn từ luồng thông tin
  - Khai thác và tìm hiểu giới hạn của một mô hình
  - Nghiên cứu bằng chứng toán học và logic trừu tượng đằng sau nó

Qua đó, ta có thể thấy bản chất của Data Science không gắn liền với một lĩnh vực hay một chủ đề cụ thể mà còn có thể xử lý rất nhiều vấn đề, hiện tượng đa dạng như Chuẩn đoán bệnh ung thư hay dự báo thời tiết.

# 1) Tìm hiểu về Biến, Hàm số, Phương trình và Đồ thị

Các lĩnh vực Toán học những điều cơ bản chúng ta vốn đọc học từ Trung học trở đi. Hãy cùng Ad tổng hợp một số nền tảng cơ bản này nhé:
- Hàm số logarit, hàm mũ, hàm số đa thức, số hữu tỉ
- Hình học và định lý cơ bản, kiến thức về lượng giác
- Số thực và số phức cùng những tính chất cơ bản
- Kiến thức về Chuỗi, tổng, bất đẳng thức
- Vẽ và biểu diễn đồ thị, kiến thức về tọa độ Descartes và toạ độ cực, đường conic

### Những kiến thức này vận dụng ra sao ?

Với những lập trình viên thì chúng ta đều đã tìm hiểu qua các thuật toán tìm kiếm và sắp xếp. Và nếu như bạn chưa biết đến thì Ad có thể giải thích như sau:
- Thuật toán tìm kiếm như việc bạn tìm kiếm số thứ tự của mình trong phòng thi trong danh sách. 
- Thuật toán sắp xếp đơn thuần là việc sắp xếp các phần tử trong danh sách theo thứ tự tăng và giảm dần. Và với lập trình cài đặt trên máy tính thì từng thuật toán sắp xếp khác nhau sẽ thực hiện trong các mốc thời gian khác nhau. Thuật toán thực hiện nhanh hay chậm còn phụ thuộc vào các yếu tố khác như kích thước bộ dữ liệu, độ phức tạp của thuật toán, ...

Qua đó, nếu Ad ứng dụng chúng để tối ưu việc tìm kiếm trên Cơ sở dữ liệu với hàng chục triệu phần tử thì sẽ không khó khăn khi chúng ta bắt gặp khái niệm "Binary Search". Tuy nhiên nếu muốn tối ưu chương trình thì ta không chỉ ngồi đó và áp source code có sẵn vào để test đúng không nào? ^^

Để một chương trình tìm kiếm được tối ưu, ta phải cần hiểu về khái niệm logarit lẫn sự lặp lại của phương trình. Qua việc tính toán trong thời gian chạy logarit, bạn có thể hình dung ra những không gian tìm kiếm phù hợp cho thuật toán nhằm xây dựng cấu trúc dữ liệu phù hợp.

Chính vì thế "Binary Search" luôn xuất hiện nhiều biến thể với hiệu suất ngày càng tăng.

Tham khảo Binary search Algorithm: https://en.wikipedia.org/wiki/Binary_search_algorithm

### Bạn có thể bổ sung kiến thức về Toán ở đâu ?

- Website Machine Learning cơ bản: https://machinelearningcoban.com/math/#luu-y-ve-ky-hieu
- Data Science Math Skills - Coursera: https://www.coursera.org/learn/datasciencemathskills
- Introduction to Algebra - edX: \
https://www.edx.org/course/introduction-algebra-schoolyourself-algebrax-1
- Algebra I - Khan Academy: https://www.khanacademy.org/math/algebra

### 2) Kiến thức về Thống kê (Statistics)

![](https://online.stat.psu.edu/statprogram/sites/statprogram/files/2018-08/statistics-review.jpg)

Cho tới nay, nhiều bạn thường cho rằng Thống kê chủ yếu thuộc về phạm trù Kinh tế. Nhưng có lẽ bạn sẽ bất ngờ thực sự vì chúng liên quan đến Data Science rất nhiều là đằng khác. 

Có thể nói nếu bạn đã theo lĩnh vực Data Science việc hiểu biết Lập trìn hay ngôn ngữ cũng chỉ là công cụ. Cái cốt lõi mà người học Data Science lẫn Machine Learning (Máy học) **phải nắm thật vững là Toán và Xác suất thống kê**.

Nếu nói theo một cách tán gẫu, ta còn có một công thức: 
**Data Science = Big Data + Statistics + Computer Science**

Và hiện nay thì Việt Nam chúng ta luôn đầy rẫy những vấn đề thực tế. Với chủ đề rộng lớn như vậy thì việc lập ra kế hoạch là vô cùng quan trọng để đảm bảo chúng ta luôn bao quát mọi thứ:
- Tóm tắt dữ liệu và thống kê mô tả, xu hướng trung tâm, phương sai, hiệp phương sai, tương quan
- Xác suất cơ bản: cơ bản, kỳ vọng, tính toán xác suất, định lý Bayes, xác suất có điều kiện
- Các hàm phân phối xác suất: thống nhất, bình thường, nhị thức, bình phương, định lý giới hạn trung tâm
- Lấy mẫu, đo lường, tạo số ngẫu nhiên
- Kiểm tra giả thuyết lẫn độ tin cậy, độ lỗi,...
- Hồi quy tuyến tính, kỹ thuật chính quy hoá

### Những kiến thức này vận dụng ra sao ?

Những kiến thức về Toán, Thống kê,... chính là điểm khác biệt trong Mindset của một Data Science. Nhiệm vụ của bạn chính là đặt câu hỏi và tìm hiểu thật kỹ vấn đề thực tế mình cần giải quyết. Một khi vấn đề được xác định thì đó là lúc bạn sẽ tiến hành thu thập dữ liệu và phân tích thật kỹ lưỡng không khác gì Sherlock Holmes.

Với kiến thức về Toán lẫn Thống kê, bạn có thể tự đặt ra những giả thuyết về dữ liệu mình đang xét hay phán đoán kết quả từ giải thuyết và không ngừng hình thành những câu hỏi mới nhằm phân tích dữ liệu thật chuẩn xác.

### Bạn có thể bổ sung kiến thức về Thống kê ở đâu ?

- Statistics and Probability in Data Science using Python - edX: \
https://courses.edx.org/courses/course-v1:UCSanDiegoX+DSE210x+3T2017/course/
- Data Science - D2Academics: https://d2academics.thinkific.com/courses/take/data-science/
- Statistics with R Specialization - Coursera: https://www.coursera.org/specializations/statistics
- Business Statistics and Analysis Specialization - Coursera: \
https://www.coursera.org/specializations/business-statistics-analysis
- (Sách tiếng Việt) Phân Tích Dữ Liệu Với R – Hỏi Và Đáp (Tái Bản 2018) - Nguyễn Văn Tuấn

Qua phần đầu của chủ đề **Kiến thức toán cho lĩnh vực Data Science**, mình mong rằng có thể cung cấp đến các bạn một chút hành trang trên con đường trở thành những Data Scientist thực thụ. Những kiến thức về Toán còn lại sẽ được Ad đề cập tại phần sau, hãy theo dõi mình để luôn cập nhật những bài post mới nhất các bạn nhé!



