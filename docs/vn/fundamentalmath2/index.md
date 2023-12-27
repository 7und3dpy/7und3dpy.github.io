# Kiến thức toán cơ bản cho Data Science (phần 2)


# Kiến thức toán cho lĩnh vực Data Science (Phần 2)

## 3) Đại số tuyến tính

![](http://kisonecat.com/teaching/2014/math2568/logo.png)

Bạn có bao giờ thắc mắc khi lướt Facebook và nhận được gợi ý kết bạn hay việc Netflix luôn gợi ý các phim phù hợp với sở thích bản thân mình. Đó được gọi là **Recommend System** với các thuật toán được triển khai trong quá trình thu thập, phân tích dữ liệu về thông tin, xu hướng người dùng để đưa ra các gợi ý phù hợp cho người dùng trên hệ thống.

Tại đây, kiến thức Đại số tuyến tính sẽ được áp dụng giúp chúng ta hiểu chuyên sâu hơn cách thuật toán học máy hoạt động trên luồng dữ liệu. Từ đó các Data Scientist sẽ dễ dàng phân tích, xử lý insight trong dữ liệu một cách chi tiết nhất.

Hãy cùng mình tìm hiểu những kiến thức cơ bản về Đại số tuyến tính cần có nào:
- Các tính chất cơ bản của ma trận và vector: phép nhân vô hướng, biến đổi tuyến tính, chuyển vị, liên hợp, ...
- Quy tắc nhân ma trận và các thuật toán khác nhau, nghịch đảo ma trận
- Các Ma trận đặc biệt: ma trận vuông, ý tưởng về ma trận thưa thớt và dày đặc, vector đơn vị, ma trận đối xứng, ma trận đơn vị,...
- Mô hình phân tích ma trận thành nhân tử (Matrix Factorization) / phân tích LU, loại bỏ Gaussian / Gauss-Jordan, giải hệ phương trình tuyến tính Ax = b
- Cơ sở không gian vector, tính trực giao, bình phương tuyến tính nhỏ nhất
- Vector riêng & giá trị riêng trong ma trận, chéo hoá ma trận, phương pháp Singular Value Decomposition (SVD)

#### Kiến thức này được ứng dụng ra sao?

Tất cả các thuật toán neural network đều sử dụng các kỹ thuật đại số tuyến tính để biểu diễn và xử lý các cấu trúc mạng lẫn huấn luyện dữ liệu. Kiến thức Đại số tuyến tính còn ứng dụng trong xử lý ảnh hay các thao tác, biểu diễn dữ liệu thực tế.

#### Tôi có thể học chúng từ đâu?

- Linear algebra: foundations to frontiers - edX: \
https://courses.edx.org/courses/course-v1:UTAustinX+UT.5.05x+2T2017/course/
- Mathematics for Machine Learning: Linear Algebra - Coursera: \
https://www.coursera.org/learn/linear-algebra-machine-learning
- Python cho Đại số Tuyến tính - Machine learning Cơ bản: \
https://fundaml.com/course/5990a766cdc6e32b3b4d0666/intro
- Kiến thức về Đại số Tuyến tính cũng được đề cập kết hợp quiz + assignment để kiếm tra kiến thức tại Week một khoá Machine Learning - Coursera: \
https://www.coursera.org/learn/machine-learning

## 4) Giải tích (Calculus)

![](https://i.udemycdn.com/course/750x422/34273_f5de_8.jpg)

Giải tích chắc hẳn là một trong những môn học đại cương khá "ám ảnh" đối với sinh viên khối Khoa học - Kỹ thuật lẫn Kinh tế. Nhưng bất luận thực trạng sinh viên sợ hãi môn học ra sao thì Giải tích vẫn xuất hiện tất yếu trong Machine Learning lẫn Data Science.

Giải tích hình thành nên các giải pháp phân tích tưởng chừng cơ bản như Hồi quy tuyến tính (Linear Regression). Mà hơn hết, khi xây dựng một mô hình thuật toán máy học để phân tích và dự đoán giả thuyết dữ liệu thì Giải tích sẽ đóng vai trò quan trọng trong quy trình tìm độ lỗi cực tiểu cho mô hình và tối ưu hoá độ chính xác của mô hình.

Đây là một môn học khó nhưng sẽ cực kỳ giá trị nếu bạn được trang bị kiến thức Giải tích trên con đường trở thành Data Scientist. Hãy cùng Ad tìm hiểu những kiến thức cơ bản cần nắm nào:
- Kiến thức về Hàm số một biến, giới hạn, liên tục, khác biệt
- Các định lý về giá trị trung bình (Mean value theorems), các dạng không xác định, quy tắc L'Hospital
- Tính cực đại và cực tiểu của hàm số
- Quy tắc nhân (Product rule), Quy tắc dây chuyền (Chain rule)
- Chuỗi Taylor, khái niệm tổng hợp / tích hợp chuỗi vô hạn
- Các định lý giá trị cơ bản và trung bình của phép tính tích phân, đánh giá tích phân xác định và không xác định
- Hàm Gamma và hàm Beta
- Kiến thức về Hàm số nhiều biến, giới hạn, liên tục, đạo hàm riêng
- Khái niệm cơ bản của phương trình vi phân 

#### Tôi sẽ sử dụng kiến thức này ở đâu?

Bạn đã bao giờ từ hỏi thuật toán Logistic Regression thực hiện như thế nào? Phải chăng là chúng sử dụng phương pháp mang tên "Gradient Descent" để tìm hiểu hàm mất mát tối thiểu. Để hiểu cách thức hoạt động của nó, bạn cần nắm các khái niệm về độ dốc, đạo hàm, giới hạn hàm số lẫn quy tắc chuỗi.

Tham khảo thuật toán Logistic Regression: \
https://machinelearningcoban.com/2017/01/27/logisticregression/

#### Tôi có thể bổ sung kiến thức Giải tích ở đâu ?
- Pre-university calculus - edX: https://www.edx.org/course/pre-university-calculus
- Calculus I - Khan Academy: https://www.khanacademy.org/math/calculus-1
- Mathematics for machine learning: Multivariable calculus - Coursera: \
https://www.coursera.org/learn/multivariate-calculus-machine-learning

## 5) Toán rời rạc (Discrete Math)

![](http://www.discrete-math-hub.com/just_a_graph.small.png)

Data Science hiện nay được thực hiện với sự trợ giúp của các hệ thống tính toán và Toán rời rạc là trung tâm của các hệ thống ấy.

Toán rời rạc sẽ bao gồm các khái niệm quan trọng đối với việc sử dụng hàng ngày các thuật toán và cấu trúc dữ liệu trong những project phân tích:
- Tìm hiểu về phép đếm, tổ hợp,...
- Nắm những kỹ thuật chứng minh cơ bản
- Khái niệm cơ bản của logic quy nạp, suy diễn và mệnh đề
- Hiểu được Cấu trúc dữ liệu cơ bản: ngăn xếp, hàng đợi, đồ thị, mảng, bảng băm, cây
- Những niệm cơ bản của Đồ thị và ứng dụng
- Hệ thức truy hồi

#### Tôi có thể bổ sung kiến thức này ở đâu ?

Ví dụ khi phân tích về bài toán hành vi người dùng mạng xã hội, dữ liệu có thể được mô phỏng như các thuộc tính của biểu đồ và ta cần nghiên cứu thuật toán nhanh nhất để tìm kiếm lẫn duyệt qua từng điểm đồ thị. Và việc học cấu trúc rời rạc sẽ giúp bạn tìm hiểu độ phức tạp của thuật toán ở những không gian và thời gian khác nhau. Từ đó sẽ giúp bạn chọn lựa thuật toán phù hợp để giải quyết vấn đề của mình.

#### Tôi có thể học Toán rời rạc ở đâu?

- Introduction to Discrete Mathematics for Computer Science Specialization - Coursera: https://www.coursera.org/specializations/discrete-mathematics
- Master discrete mathematics: sets, math logic, and more - Coursera: \
https://www.udemy.com/master-discrete-mathematics/
- Introduction to Mathematical Thinking - Coursera: \
https://www.coursera.org/learn/mathematical-thinking


# Tổng kết

Để trở thành một DS quả là một quá trình dài để học tập, rèn luyện tri thức lẫn mindset dúng không nào. Qua đó, ta có thể thấy từ bài toán đến ứng dụng thực tiễn luôn là một thử thách lớn và lại càng gắn liền với trách nhiệm nếu bạn phụ trách cho Doanh nghiệp. Bởi nguy hiểm vẫn là việc "Sai một ly đi một dặm" dẫn đến một rủi ro không hề nhỏ.

Hãy không ngừng đặt ra những câu hỏi và cố gắng vận dụng tri thức tìm ra lời giải phù hợp lẫn tối ưu nhất. Trong giai đoạn Hội nhập của Việt Nam hiện nay, cơ hội vẫn luôn trong tầm tay bạn khi và chỉ khi bản thân luôn nỗ lực hết mình.


