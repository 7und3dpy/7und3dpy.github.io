# Giải ngố Pointer (Phần 1)

This article shows the concept of Pointer and how it works P1.

<!--more-->


Một trong những điều mà người mới bắt đầu học C cảm thấy khó khăn là khái niệm về con trỏ. Mục đích của hướng dẫn này là giới thiệu về con trỏ và cách sử dụng chúng cho những người mới bắt đầu. 

Tôi nhận thấy rằng lý do chính khiến những người mới bắt đầu gặp vấn đề với con trỏ là họ có cảm giác yếu hoặc rất ít về các biến, (vì chúng được sử dụng trong C). Vì vậy, chúng ta bắt đầu bằng việc thảo luận về các biến C nói chung. 

Biến trong chương trình là một cái gì đó có tên và giá trị của nó có thể khác nhau. Cách trình biên dịch và trình liên kết xử lý việc này là nó gán một khối bộ nhớ cụ thể trong máy tính để giữ giá trị của biến đó. Kích thước của khối đó phụ thuộc vào phạm vi mà biến được phép thay đổi. Ví dụ: trên PC 32 bit, kích thước của biến số nguyên là 4 byte. Trên các số nguyên PC 16 bit cũ hơn là 2 byte. Trong C, kích thước của loại biến chẳng hạn như số nguyên không nhất thiết phải giống nhau trên tất cả các loại máy. Hơn nữa, có nhiều loại biến số nguyên trong C. Chúng ta có số nguyên, số nguyên dài và số nguyên ngắn mà bạn có thể đọc trong bất kỳ văn bản cơ bản nào về C. Tài liệu này giả định việc sử dụng hệ thống 32 bit với số nguyên 4 byte .

Nếu bạn muốn biết kích thước của các loại số nguyên khác nhau trên hệ thống của mình, việc chạy đoạn mã sau sẽ cung cấp cho bạn thông tin đó.
```c
	#include <stdio.h>
	
	int main()  
	{  
		printf("size of a short is %d\\n", sizeof(short));  
		printf("size of a int is %d\\n", sizeof(int));  
		printf("size of a long is %d\\n", sizeof(long));  
	}
```

Khi khai báo một biến, chúng ta thông báo cho trình biên dịch hai thông tin: tên biến và loại biến. Ví dụ: chúng ta khai báo một biến kiểu số nguyên có tên **k** bằng cách viết:

```c
        int k; 
```   

Khi nhìn thấy phần "int" của câu lệnh này, trình biên dịch sẽ dành 4 byte bộ nhớ (trên PC) để giữ giá trị của số nguyên. Nó cũng thiết lập một bảng ký hiệu. Trong bảng đó, nó thêm ký hiệu **k** và địa chỉ tương đối trong bộ nhớ nơi 4 byte đó được đặt sang một bên.

Vì vậy, sau này nếu chúng ta viết:

```c    
        k = 2; 
```    

chúng ta hy vọng rằng, tại thời điểm chạy khi câu lệnh này được thực thi, giá trị 2 sẽ được đặt ở vị trí bộ nhớ dành riêng cho việc lưu trữ giá trị của **k**. Trong C, chúng ta gọi một biến như số nguyên **k** là một "đối tượng".

Theo một nghĩa nào đó, có hai "giá trị" gắn liền với đối tượng k. Một là giá trị của số nguyên được lưu trữ ở đó (2 trong ví dụ trên) và cái còn lại là "giá trị" của vị trí bộ nhớ, tức là địa chỉ của k. Một số văn bản đề cập đến hai giá trị này bằng danh pháp rvalue (right value, phát âm là "are value") và lvalue (left value, phát âm là "el value") tương ứng.

Trong một số ngôn ngữ, lvalue là giá trị được phép ở phía bên trái của toán tử gán '=' (tức là địa chỉ nơi kết quả đánh giá của phía bên phải kết thúc). Giá trị là giá trị nằm ở bên phải của câu lệnh gán, **2** ở trên. Giá trị không thể được sử dụng ở phía bên trái của câu lệnh gán. Như vậy: **2 = k**; Là bất hợp pháp.

Trên thực tế, định nghĩa "lvalue" ở trên đã được sửa đổi phần nào cho C. Theo K&R II (trang 197): [1]

> "An _**object**_ is a named region of storage; an _**lvalue**_ is an expression referring to an object."

Tuy nhiên, tại thời điểm này, định nghĩa được trích dẫn ban đầu ở trên là đủ. Khi chúng ta trở nên quen thuộc hơn với con trỏ, chúng ta sẽ đi sâu vào chi tiết hơn về điều này.

Được rồi, bây giờ hãy xem xét:
    
       int j, k; 
    
        k = 2; 
        j = 7;    <-- line 1 
        k = j;    <-- line 2 
    

Ở phần trên, trình biên dịch diễn giải **j** ở dòng 1 là địa chỉ của biến **j** (giá trị lvalue) và tạo mã để sao chép giá trị 7 vào địa chỉ đó. Tuy nhiên, ở dòng 2, **j** được hiểu là giá trị của nó (vì nó nằm ở phía bên phải của toán tử gán '='). Nghĩa là, ở đây **j** đề cập đến giá trị **được lưu** tại vị trí bộ nhớ dành riêng cho **j**, trong trường hợp này là 7. Vì vậy, số 7 được sao chép vào địa chỉ được chỉ định bởi lvalue của **k**.

Trong tất cả các ví dụ này, chúng tôi đang sử dụng số nguyên 4 byte nên tất cả việc sao chép giá trị từ vị trí lưu trữ này sang vị trí lưu trữ khác đều được thực hiện bằng cách sao chép 4 byte. Nếu chúng tôi sử dụng số nguyên hai byte thì chúng tôi sẽ sao chép 2 byte.

Bây giờ, giả sử rằng chúng ta có lý do muốn có một biến được thiết kế để chứa giá trị lvalue (một địa chỉ). Kích thước cần thiết để giữ giá trị như vậy tùy thuộc vào hệ thống. Trên các máy tính để bàn cũ hơn có tổng bộ nhớ là 64K, địa chỉ của bất kỳ điểm nào trong bộ nhớ có thể được chứa trong 2 byte. Máy tính có nhiều bộ nhớ hơn sẽ cần nhiều byte hơn để chứa địa chỉ. Kích thước thực tế được yêu cầu không quá quan trọng miễn là chúng ta có cách thông báo cho trình biên dịch rằng thứ chúng ta muốn lưu trữ là một địa chỉ.

Biến như vậy được gọi là __**biến con trỏ**__ (vì những lý do mà hy vọng sau này sẽ rõ ràng hơn). Trong C, khi định nghĩa một biến con trỏ, chúng ta làm như vậy bằng cách đặt trước tên của nó một dấu hoa thị. Trong C, chúng tôi cũng cung cấp cho con trỏ một loại, trong trường hợp này, đề cập đến loại dữ liệu được lưu trữ tại địa chỉ mà chúng tôi sẽ lưu trữ trong con trỏ của mình. Ví dụ, hãy xem xét việc khai báo biến:

```c
       int *ptr;
```    

**ptr** là tên biến của chúng ta (giống như **k** là tên biến số nguyên của chúng tôi). '\*' thông báo cho trình biên dịch rằng chúng ta muốn một biến con trỏ, tức là để dành bao nhiêu byte để lưu trữ một địa chỉ trong bộ nhớ. **int** nói rằng chúng ta dự định sử dụng biến con trỏ để lưu trữ địa chỉ của một số nguyên. Một con trỏ như vậy được gọi là "trỏ tới" một số nguyên. Tuy nhiên, lưu ý rằng khi chúng ta viết **int k;** chúng ta đã không cung cấp cho **k** một giá trị. Nếu định nghĩa này được thực hiện bên ngoài bất kỳ chức năng nào thì trình biên dịch tuân thủ ANSI sẽ khởi tạo nó về 0. Tương tự, **ptr** không có giá trị, tức là chúng ta chưa lưu địa chỉ vào đó trong khai báo trên. Trong trường hợp này, một lần nữa, nếu khai báo nằm ngoài bất kỳ hàm nào, nó sẽ được khởi tạo thành một giá trị được đảm bảo theo cách được đảm bảo không trỏ đến bất kỳ đối tượng hoặc hàm C nào. Con trỏ được khởi tạo theo cách này được gọi là con trỏ "null".

Mẫu bit thực tế được sử dụng cho con trỏ null có thể có hoặc không có giá trị bằng 0 vì nó phụ thuộc vào hệ thống cụ thể mà mã được phát triển trên đó. Để làm cho mã nguồn tương thích giữa các trình biên dịch khác nhau trên các hệ thống khác nhau, macro được sử dụng để biểu thị con trỏ null. Macro đó có tên NULL. Do đó, việc đặt giá trị của một con trỏ bằng macro NULL, như với câu lệnh gán chẳng hạn như ptr = NULL, đảm bảo rằng con trỏ đã trở thành con trỏ rỗng. Tương tự, giống như người ta có thể kiểm tra giá trị nguyên bằng 0, như trong **if(k == 0),** chúng ta có thể kiểm tra con trỏ null bằng cách sử dụng **if (ptr == NULL).**

Tuy nhiên, hãy quay lại việc sử dụng biến **ptr** mới của chúng ta. Giả sử bây giờ chúng ta muốn lưu trữ trong **ptr** địa chỉ của biến số nguyên **k**. Để làm điều này, chúng ta sử dụng toán tử **&** đơn nhất và viết:

```c   
        ptr = &k; 
```    

Những gì toán tử **&** thực hiện là truy xuất lvalue (địa chỉ) của **k**, mặc dù **k** nằm ở phía bên phải của toán tử gán '=' và sao chép giá trị đó vào nội dung của con trỏ ptr của chúng ta. Bây giờ, ptr được cho là "trỏ tới" **k**. Hãy kiên nhẫn với chúng tôi bây giờ, chỉ còn một nhà điều hành nữa mà chúng tôi cần thảo luận.

The "dereferencing operator" là dấu hoa thị và được sử dụng như sau:

```c    
        *ptr = 7; 
```    

sẽ sao chép 7 vào địa chỉ được trỏ bởi **ptr**. Do đó, nếu **ptr** "trỏ tới" (chứa địa chỉ của) **k**, câu lệnh trên sẽ đặt giá trị của **k** thành 7. Nghĩa là, khi chúng ta sử dụng '\*' theo cách này, chúng ta đang đề cập đến giá trị của cái mà ptr là trỏ tới chứ không phải giá trị của chính con trỏ.

Tương tự, chúng ta có thể viết:

```c    
     printf("%d\n",*ptr); 
```    

để in ra màn hình giá trị số nguyên được lưu trữ tại địa chỉ được trỏ bởi **ptr;**.

Một cách để xem tất cả những thứ này khớp với nhau như thế nào là chạy chương trình sau rồi xem lại mã và kết quả đầu ra một cách cẩn thận.
    
    ------------ Program 1.1 --------------------------------- 
```c    
    /* Program 1.1 from PTRTUT10.TXT   6/10/97 */
    
    #include <stdio.h>
    
    int j, k;
    int *ptr;
    
    int main(void)
    {
        j = 1;
        k = 2;
        ptr = &k;
        printf("\n");
        printf("j has the value %d and is stored at %p\n", j, (void *)&j);
        printf("k has the value %d and is stored at %p\n", k, (void *)&k);
        printf("ptr has the value %p and is stored at %p\n", ptr, (void *)&ptr);
        printf("The value of the integer pointed to by ptr is %d\n", *ptr);
    
        return 0;
    }
```    

Lưu ý: Chúng ta vẫn chưa thảo luận về những khía cạnh của C yêu cầu sử dụng biểu thức **(void \*)** được sử dụng ở đây. Hiện tại, hãy đưa nó vào mã thử nghiệm của bạn. Chúng tôi sẽ giải thích lý do đằng sau biểu hiện này ở chương sau.

* * *

To review:

*   Một biến được khai báo bằng cách đặt cho nó một kiểu và tên (ví dụ: **int k;**) 
*   Một biến con trỏ được khai báo bằng cách đặt cho nó một kiểu và một tên (ví dụ: **int \*ptr**), trong đó dấu hoa thị cho trình biên dịch biết rằng biến có tên **ptr** là một biến con trỏ và kiểu này cho trình biên dịch biết con trỏ trỏ tới kiểu gì (số nguyên trong trường hợp này).
*   Khi một biến được khai báo, chúng ta có thể lấy địa chỉ của nó bằng cách đặt trước tên của nó bằng toán tử **&** đơn nhất, như trong **&k**.
*   Chúng ta có thể "dereference" amột con trỏ, tức là tham chiếu đến giá trị của con trỏ mà nó trỏ tới, bằng cách sử dụng toán tử '\*' đơn nhất như trong ***ptr**.
*   "lvalue" của một biến là giá trị địa chỉ của nó, tức là nơi nó được lưu trong bộ nhớ. "rvalue" của một biến là giá trị được lưu trong biến đó (tại địa chỉ đó).
### References for Chapter 1:

1.  "The C Programming Language" 2nd Edition  
    B. Kernighan and D. Ritchie  
    Prentice Hall  
    ISBN 0-13-110362-8  
    
2. https://stackoverflow.com/questions/4318881/in-c-what-does-a-variable-declaration-with-two-asterisks-mean

3. https://beginnersbook.com/2014/01/c-pointer-to-pointer/

<!--[Chapter 2: Pointer Types and Arrays](ch2x.md)

[Back to Table of Contents](pointers.md)-->

