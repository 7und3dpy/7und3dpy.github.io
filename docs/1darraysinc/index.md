# 1D Arrays in C

This article shows the concept of Pointer and how it works P1.

<!--more-->

An array is a container object that holds a fixed number of values of a single type. To create an array in C, we can do int ```arr[n]```;. Here, arr, is a variable array which holds up to **10** integers. The above array is a static array that has memory allocated at compile time. A dynamic array can be created in C, using the malloc function and the memory is allocated on the heap at runtime. To create an integer array, **_arr_** of size **_n_** , ```int *arr = (int*)malloc(n * sizeof(int))```, where **_arr_** points to the base address of the array.Sample Output 1in. Iterate the array calculating the sum of all elements. Print the sum and free the memory where the array is stored.

While it is true that you can sum the elements as they are read, without first storing them to an array, but you will not get the experience working with an array. Efficiency will be required later. 

**Input Format**

The first line contains an integer, **n**.
The next line contains **n** space-separated integers.

**Constraints**

$1 \leq n \leq 1000$

$1 \leq a[i] \leq 1000$

**Output format**
Print the sum of the integers in the array.

**Sample input 0**
```
6
16 13 7 2 1 12 
```

**Sample output 0**
```
51
```

**Sample Input 1**
```
7
1 13 15 20 12 13 2 
```

**Sample Output 1**
```
76
```

# Solution: 

```c
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {

    /* Enter your code here. Read input from STDIN. Print output to STDOUT */    
    int n,s = 0;
    scanf("%d",&n);
    int *arr = (int*)malloc(n * sizeof(int));
    
    for (int i = 0; i <n; i++){
        scanf("%d",&arr[i]);
        s += arr[i];
    }
    printf("%d",s);
    return 0;
}
```

