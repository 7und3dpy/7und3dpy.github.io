# Giới thiệu về Weka

Sample article demonstrating basic Markdown syntax and HTML element formatting.

<!--More-->
# Xây dựng mô hình Classification - Machine Learning cơ bản với Weka

![](https://datamahadev.com/wp-content/uploads/2020/09/Classification-in-Machine-Learning-datamahadev.com_.jpeg)

Đừng nghĩ Machine Learning chỉ dành cho những chuyên gia. Bởi nếu là một người học/ người dùng không chuyên với mong muốn tiếp cận Machine Learning thì Weka sẽ là một sự lựa chọn không tồi tý nào.

Weka là một tập hợp các thuật toán học máy cho các nhiệm vụ khai thác dữ liệu. Nó chứa các công cụ để chuẩn bị dữ liệu, phân loại, hồi quy, phân cụm, khai thác quy tắc kết hợp và trực quan hóa. 

Weka là phần mềm nguồn mở được cấp theo GNU General Public License. Sản phẩm được xây dựng bởi nhóm nghiên cứu Machine Learning thuộc Khoa Khoa học Máy tính của Đại học Wakaito, New Zealand.

Đặc biệt, Weka còn hỗ trợ việc học tập Deep Learning.

Bạn có thể khám phá thêm về Weka tại đây: https://www.cs.waikato.ac.nz/ml/weka/index.html

## Vì sao nên chọn Weka?

Một lợi ích lớn của việc sử dụng Weka là nó chứa số lượng lớn các thuật toán Machine Learning được hỗ trợ. Càng nhiều thuật toán càng giúp mình tìm hiểu tường tận về vấn đề của bản thân và dễ dàng so sánh các thuật toán với nhau.

Điển hình hơn hết là Weka đã có sẵn các thuật toán chúng ta tiếp cận Case Study Titanic một cách trực quan hơn. Ở đây ta sẽ tiếp cận với 3 thuật toán Classification cơ bản: K-Neighrest Neighbor, Naive Bayes & Decision Tree.

## Tìm hiểu về Case Study Titanic

![](https://media.nationalgeographic.org/assets/photos/000/273/27302.jpg)

Vào ngày 15 tháng 4 năm 1912, trong chuyến hành trình đầu tiên của mình, tàu Titanic đã chìm sau khi va chạm với một tảng băng trôi và lấy đi 1502 trong số 2224 hành khách lẫn phi hành đoàn. Thảm kịch giật gân này đã gây sốc cho cộng đồng quốc tế và dẫn đến các quy định an toàn tốt hơn cho tàu.

Mặc dù có một số yếu tố may mắn liên quan đến việc sống sót sau vụ chìm tàu, một số nhóm người có khả năng sống sót cao hơn những người khác, chẳng hạn như phụ nữ, trẻ em và giới thượng lưu.

Ở Case Study này, ta sẽ tiến thành phân tích về những loại người có khả năng sống sót. Cụ thể, ta sẽ sử dụng công cụ học máy để dự đoán hành khách nào sống sót sau thảm kịch.

Bạn có thể tham khảo thêm về Case Study này và lấy dữ liệu tại đây: https://www.kaggle.com/c/titanic/overview

#### **Input**
Từ dữ liệu gốc, mình sẽ tối giản chúng. Mình đã lọc ra vài thuộc tính quan trọng lẫn chỉnh sửa tên thuộc tính ảnh hưởng đến khả năng sống sót (**survived**) của hành khách trên tàu Titanic.   
Thuộc tính đầu vào của mình sẽ bao gồm: 

| Thuộc tính   |      Định nghĩa      | Giải thích |
|----------|:-------------:|------:|
| class | Loại vé - Ticket class. Có thể là vé hạng nhất, hạng hai,... | 1 = 1st, 2 = 2nd, 3 = 3rd |
| gender | Giới tính | Đã chuẩn hoá 0 - Nữ và 1 - Nam |
| age | Tuổi tác | 1 - adult và 0 - children |
| survived | Khả năng sống sót | 0 - không và 1 - Có |

Nếu muốn test thử bộ dữ liệu đã được chuẩn hoá từ mình, bạn có thể download tại đây: https://drive.google.com/file/d/13ycO_k8erbZrS-cxa-F8RlWlfitF57Kv/view?usp=sharing

#### **Output**: 
Dữ liệu đầu ra rất đơn giản đưa ra dự đoán về khả năng tử nạn của các hành khách còn lại dựa trên những yếu tố biết trước như tên, tuổi, giới tính, số người đi cùng, vị trí phòng v…v.
#### **Ý nghĩa**: 
Bài toán cho phép chúng ta có thể dựa vào đó để dự đoán khả năng sống sót của một người dựa trên một thảm họa từ đó có thể rút ra những kinh nghiệm trong các chuyến hành trình trong tương lai, Có thể là thiết kế lại tàu một cách an toàn hơn, dịch vụ chăm sóc, cảnh báo,...
#### **Phân tích**: 
Có thể dễ nhận thấy đây là một bài Two-Class Classification với kết quả đầu ra là **survived** hay không.

## How to use Weka?

Cá nhân mình nghĩ việc sử dụng Weka rất đơn giản, bạn chỉ việc cài đặt và chọn CSV file.
![](https://i.imgur.com/uYRi4yL.png)
Okay và tiếp đến các bạn chọn mục Classify:
![](https://i.imgur.com/koui4zN.png)
Ở Classifier, các bạn chọn thuật toán phù hợp mình muốn test. Mình sẽ test thử thuật toán K- Neighrest Neighbor đầu tiên.

Tiếp đến ở test option bạn có thể chọn:

- Use training set: Sử dụng toàn bộ dữ liệu để huấn luyện mô hình.
- Supplied test set: Bạn cung cấp thêm test set để kiểm tra mô hình.
- Cross-validation: Hay còn gọi là k-fold Cross validation. Phương pháp này phân chia dữ liệu thành k tập con có cùng kích thước. Tại mỗi vòng lặp sử dụng một tập con là tập thử nghiệm và các tập con còn lại là tập huấn luyện. Giá trị k thường là = 10. Ta có thể dùng một trong hai cách:
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; + Leave-one-out : k=số mẫu trong dữ liệu (dành cho tập dữ liệu nhỏ)
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; + Stratified cross-validation : dùng phương pháp lấy mẫu để các lớp trong từng tập con phân bố như trên toàn bộ dữ liệu.
- Percentage split: Chia dữ liệu thành training set, test set tuỳ vào % bạn muốn.

Tương tự ta tiếp tục với thuật toán Decision Tree ID3 và Naive Bayes.
![](https://i.imgur.com/Ixx08sl.png)
![](https://i.imgur.com/e87Sxzd.png)

Qua đó chúc mọi người có những trải nghiệm thú vị cùng Weka. Trước khi sử dụng cũng đừng quên cảm ơn khoa Khoa học Máy tính - Đại học Wakaito, New Zealand đã mang đến một sản phẩm tuyệt vời như thế này mọi người nhé!

## More information about Weka

- Chi tiết về tool (bao gồm link tải, tài liệu hướng dẫn và cả khoá học): \
https://www.cs.waikato.ac.nz/ml/weka/index.html
- Để add ID3 Decision Tree vào Weka: \
https://stackoverflow.com/questions/48888463/weka-3-8-package-installation-what-are-the-steps-to-add-id3
- Nếu các bạn không thấy KNN trong Lazy, hãy chọn IBk classifier
- Một bài viết mình thấy cũng thú vị cho bạn nào chưa rõ về đánh giá mô hình: https://ongxuanhong.wordpress.com/2015/08/25/danh-gia-mo-hinh-model-evaluation/
