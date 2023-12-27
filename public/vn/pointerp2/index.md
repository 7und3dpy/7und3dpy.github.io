# Giải ngố Pointer (Phần 2)


This article shows the concept of Pointer and how it works P2.

<!--more-->


Mục đích của việc xác định _**loại**_ biến mà một con trỏ trỏ tới là gì?

```c    
         int *ptr;
```    

Một trong những lý do đó là, khi ptr "trỏ" tới một số nguyên, nếu chúng ta viết:

```c    
        *ptr = 2;
```    

 trình biên dịch biết cần sao chép bao nhiêu byte vào vị trí bộ nhớ được trỏ bởi con trỏ **ptr**. Nếu **ptr** được khai báo để trỏ tới một số nguyên, 4 byte sẽ được sao chép. Tương tự cho các kiểu số thực như floats và doubles, số byte tương ứng sẽ được sao chép. Tuy nhiên, việc xác định loại mà con trỏ trỏ tới còn cho phép trình biên dịch hiểu mã một cách thú vị hơn. Ví dụ, giả sử chúng ta có một khối trong bộ nhớ gồm mười số nguyên liên tiếp nhau. Tức là, 40 byte bộ nhớ được dành để chứa 10 số nguyên.

Bây giờ, giả sử con trỏ nguyên **ptr** của chúng ta trỏ tới số nguyên đầu tiên này. Ngoài ra, giả sử số nguyên đó nằm ở vị trí bộ nhớ 100 (decimal). Điều gì xảy ra khi chúng ta viết:

    
        ptr + 1;
     
    

Bởi vì trình biên dịch "biết" rằng đây là một con trỏ (tức giá trị của nó là một địa chỉ) và rằng nó trỏ tới một số nguyên (địa chỉ hiện tại của nó, 100, là địa chỉ của một số nguyên), nó sẽ thêm 4 vào **ptr** thay vì 1, để con trỏ "trỏ tới" **số nguyên** **kế tiếp**, tại vị trí bộ nhớ 104. Tương tự, nếu **ptr** được khai báo là một con trỏ tới kiểu short, nó sẽ thêm 2 vào thay vì 1. Cùng như vậy, với các kiểu dữ liệu khác như floats, doubles, hoặc cả kiểu dữ liệu được người dùng xác định như cấu trúc, cách thức này vẫn áp dụng. Điều này rõ ràng không phải là loại "cộng" mà chúng ta thường nghĩ đến. Trong ngôn ngữ C, nó được gọi là "cộng pointer" (pointer arithmetic), một thuật ngữ chúng ta sẽ quay lại sau này.

Tương tự, vì **++ptr** và **ptr++** đều tương đương với **ptr + 1** (tuy nhiên điểm trong chương trình mà **ptr** được tăng có thể khác nhau), việc tăng một con trỏ bằng toán tử ++, cả tiền tố và hậu tố, sẽ tăng địa chỉ mà nó lưu trữ một lượng bằng sizeof(type), trong đó "type" là loại đối tượng được trỏ tới (tức 4 byte cho một số nguyên).

Vì một khối gồm 10 số nguyên nằm liên tiếp nhau trong bộ nhớ, theo định nghĩa, là một mảng các số nguyên, điều này mang lại mối quan hệ thú vị giữa mảng và con trỏ.

Xét ví dụ sau:

```c    
        int my_array[] = {1,23,17,4,-5,100}; 
```    

Ở đây, chúng ta có một mảng chứa 6 số nguyên. Chúng ta truy cập từng số nguyên trong mảng này thông qua chỉ mục của mảng **my\_array**, i.e. sử dụng **my\_array\[0\]** đến **my\_array\[5\]**. Nhưng, chúng ta cũng có thể truy cập vào chúng bằng con trỏ như sau:

```c    
        int *ptr;
        ptr = &my_array[0];       /* point our pointer at the first
                                     integer in our array */ 
```    

Sau đó, chúng ta có thể in ra mảng của chúng ta bằng cách sử dụng notation của mảng hoặc bằng cách gián tiếp thông qua con trỏ. Đoạn code sau minh họa điều này:

```c  
    -----------  Program 2.1  -----------------------------------
    
    /* Program 2.1 from PTRTUT10.HTM   6/13/97 */
    
    #include <stdio.h>
    
    int my_array[] = {1,23,17,4,-5,100};
    int *ptr;
    
    int main(void)
    {
        int i;
        ptr = &my_array[0];     /* point our pointer to the first
                                          element of the array */
        printf("\n\n");
        for (i = 0; i < 6; i++)
        {
          printf("my_array[%d] = %d   ",i,my_array[i]);   /*<-- A */
          printf("ptr + %d = %d\n",i, *(ptr + i));        /*<-- B */
        }
        return 0;
    }
```    

Hãy biên dịch và chạy chương trình trên và lưu ý kỹ dòng A và B và rằng chương trình in ra các giá trị giống nhau trong cả hai trường hợp. Cũng lưu ý cách chúng ta giải tham chiếu con trỏ trong dòng B, tức là chúng ta đã thêm i vào nó trước khi giải tham chiếu con trỏ mới. Thay đổi dòng B thành:

```c    
        printf("ptr + %d = %d\n",i, *ptr++);
```    

và chạy lại... sau đó thay đổi thành:

```c    
        printf("ptr + %d = %d\n",i, *(++ptr));
````    

và chạy một lần nữa. Mỗi lần hãy cố gắng dự đoán kết quả và xem kỹ kết quả thực tế.

Trong ngôn ngữ C, tiêu chuẩn quy định rằng bất kỳ nơi nào chúng ta có thể sử dụng **&var\_name\[0\]** thì chúng ta có thể thay thế bằng **var\_name**.

```c    
        ptr = &my_array[0];
```    

chúng ta có thể viết:

```c    
        ptr = my_array;
```    

để đạt được cùng một kết quả.

Điều này khiến nhiều tài liệu khẳng định rằng tên của một mảng là một con trỏ. Tôi thích nghĩ về nó như "tên của mảng là địa chỉ của phần tử đầu tiên trong mảng". Nhiều người mới học (bao gồm cả tôi khi mới học) có xu hướng bị nhầm lẫn khi nghĩ về nó là một con trỏ. Ví dụ, trong khi chúng ta có thể viết

```c
        ptr = my_array;
```    

thì chúng ta không thể viết

```c    
        my_array = ptr;
```    

Lý do là trong khi **ptr** là một biến, **my\_array** là một hằng số. Nghĩa là, sau khi vị trí mà phần tử đầu tiên của **my\_array** sẽ được lưu trữ không thể thay đổi sau khi **my\_array\[\]** đã được khai báo.

Trước đây khi thảo luận về thuật ngữ "lvalue", tôi đã trích dẫn K&R-2 nơi nó nói:

> "An _**object**_ is a named region of storage; an _**lvalue**_ is an expression referring to an object."

Điều này đặt ra một vấn đề thú vị. Vì **my\_array** là một vùng lưu trữ có tên, tại sao **my\_array** trong câu lệnh gán trên không phải là một lvalue? Để giải quyết vấn đề này, một số người gọi **my\_array** là một "lvalue không thể sửa đổi".

Thay đổi chương trình ví dụ trên bằng cách thay

```c   
        ptr = &my_array[0];
```    

bằng

```c    
        ptr = my_array;
```    

và chạy lại để xác nhận kết quả giống nhau.

Bây giờ, hãy đi sâu hơn một chút vào sự khác biệt giữa tên **ptr** và **my\_array** Một số tác giả sẽ gọi tên một mảng là một con trỏ _**hằng số**_. Ý nghĩa của _**hằng số**_ ở đây là gì? Như chúng ta đã thấy, khi chúng ta khai báo một biến, chúng ta dành một chỗ trong bộ nhớ để chứa giá trị của kiểu tương ứng. Sau khi điều này được thực hiện, tên biến có thể được hiểu theo một trong hai cách. Khi được sử dụng ở phía trái của toán tử gán, trình biên dịch hiểu nó là vị trí bộ nhớ để di chuyển giá trị từ phía bên phải của toán tử gán. Nhưng khi được sử dụng ở phía bên phải của toán tử gán, tên biến được hiểu là nội dung được lưu trữ tại địa chỉ bộ nhớ đó dành để chứa giá trị của biến.

Với điều đó trong đầu, giờ chúng ta hãy xem xét các hằng số đơn giản nhất, như:

```c    
        int i, k;
        i = 2;
```    

Ở đây, trong khi **i** là một biến và nó chiếm một chỗ trong phần dữ liệu của bộ nhớ, **2** là một hằng số và, như vậy, thay vì dành một chỗ trong đoạn dữ liệu, nó được nhúng trực tiếp vào đoạn mã lệnh của bộ nhớ. Tức là, trong khi việc viết điều gì đó như **k = i;** nói với trình biên dịch tạo ra mã sẽ xem địa chỉ bộ nhớ của **&i** để xác định giá trị để di chuyển sang **k**, việc tạo ra mã bằng **i = 2;** chỉ đơn giản đưa ra số **2** in the code and there is no referencing of the data segment. trong mã và không có việc trích dẫn đến phân đoạn dữ liệu. Tức là cả **k** and **i** đều là các đối tượng, nhưng **2** không phải là một đối tượng.

Tương tự, trong ví dụ trên, vì **my\_array** là một hằng số, sau khi trình biên dịch xác định địa chỉ cho mảng này để lưu trữ, nó "biết" địa chỉ của **my\_array\[0\]** và khi nhìn thấy:

```c    
        ptr = my_array;
```    

nó chỉ sử dụng địa chỉ này như là một hằng số trong phân đoạn mã và không có việc trích dẫn đến phân đoạn dữ liệu ngoài việc này.

Điều này có thể là một nơi tốt để giải thích thêm về việc sử dụng biểu thức **(void \*)** trong Chương trình 1.1 của Chương 1. Như chúng ta đã thấy, chúng ta có thể có các con trỏ của các kiểu khác nhau. Cho đến nay, chúng ta đã thảo luận về con trỏ tới số nguyên và con trỏ tới ký tự. Trong các chương tiếp theo, chúng ta sẽ tìm hiểu về con trỏ tới cấu trúc và thậm chí con trỏ tới con trỏ.

Chúng ta cũng đã biết rằng trên các hệ thống khác nhau, kích thước của một con trỏ có thể thay đổi. Hơn nữa, kích thước của một con trỏ cũng có thể thay đổi tuỳ thuộc vào kiểu dữ liệu của đối tượng mà nó trỏ tới. Do đó, tương tự như số nguyên mà bạn có thể gặp vấn đề khi cố gắng gán một số nguyên dài cho biến của loại số nguyên ngắn, bạn cũng có thể gặp vấn đề khi cố gắng gán các giá trị của các con trỏ khác nhau cho các biến con trỏ khác nhau.

Để giảm thiểu vấn đề này, ngôn ngữ C cung cấp một con trỏ của kiểu void. Chúng ta có thể khai báo một con trỏ như sau:

```c    
    void *vptr;
```    

Một con trỏ void có thể coi là một con trỏ "chung chung". Ví dụ, trong khi C không cho phép so sánh một con trỏ kiểu số nguyên với một con trỏ kiểu ký tự, ví dụ, bạn có thể so sánh cả hai với một con trỏ void. Tất nhiên, giống như các biến khác, các phép ép kiểu có thể được sử dụng để chuyển từ một kiểu con trỏ sang kiểu khác trong các trường hợp phù hợp. Trong Chương trình 1.1 của Chương 1, tôi ép kiểu các con trỏ số nguyên thành con trỏ void để làm cho chúng tương thích với trình chỉ thị chuyển đổi %p. Trong các chương sau, các ép kiểu khác sẽ được thực hiện với lý do được định nghĩa trong đó.

Vâng, đó là nhiều khái niệm kỹ thuật phải tiếp thu và tôi không mong chúng ta có thể hiểu tất cả ngay lần đọc đầu. Đến lúc này và thực hiện thực nghiệm, bạn sẽ muốn trở lại và đọc lại hai chương đầu tiên. Nhưng bây giờ, hãy tiếp tục vào mối quan hệ giữa con trỏ, mảng các ký tự và chuỗi.

<!--[Chapter 3: Pointers and Strings](ch3x.md)

[Back to Table of Contents](pointers.md)-->

