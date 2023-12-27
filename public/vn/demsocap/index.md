# Đếm số cặp


Cho một số dãy nguyên dương _a_ gồm **_N_** phần tử. Hãy đếm số cặp _(i,j)_ thỏa mãn: 
- \\(1 \leq i \leq j \leq N\\)
- \\(a_i^2 + a_j = X\\)

**Input format**
- Dòng đầu tiên gồm 2 số nguyên dương **_N, X_**
- Dòng thứ hai gồm **_N_** số nguyên dương _\\( a_1, a_2, a_3, ..., a_N\\)_

**Constraints**
- \\(2 \leq N \leq 500\\)

- \\(1 \leq X \leq 10^{18}\\)
- \\(1 \leq a_i \leq 10^6\\)

**Output format**

In ra số cặp _(i, j)_ thỏa mãn

**Sample Input 0**
```
10 12
3 3 3 3 3 3 3 3 3 3
```

**Sample Output 0**
```
55
```

**Sample Input 1**
```
5 1 
2 3 4 5 6
```

**Sample Output 1**
```
0
```


Hãy chú ý giá trị vì khả năng int chỉ đến 2^16 thôi tăng long long int lên 2^64 để giải quyết hết vấn đề

```c
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {

    /* Enter your code here. Read input from STDIN. Print output to STDOUT */    
    long long int N, X;
    long long int* arr;
    scanf("%lld %lld", &N, &X);
    arr = (long long int*)malloc(N * sizeof(long long int));
    for (int i =0; i < N; i++){
        scanf("%lld",(arr+i));
    }
    int cnt = 0;
    for (int i = 0; i < N ; i++){
        for (int j = i; j < N; j++){
            if (pow(*(arr+i),2) + *(arr+j) == X){
                cnt += 1;
                //printf("Pair found: %d, %d\n", arr[i], arr[j]);
            }
        }
    }
    printf("%d", cnt);
    free(arr);
    return 0;
}
```

