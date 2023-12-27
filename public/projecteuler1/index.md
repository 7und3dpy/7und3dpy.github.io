# Project Euler 1: Multiples of 3 and 5


This problem is a programming version of [Problem 1](https://projecteuler.net/problem=1) from [projecteuler.net](https://projecteuler.net/)

<!--more-->

If we list all the natural numbers below $10$ that are multiples of $3$ or $5$ , we get $3$, $5$, $6$ and $9$. The sum of these multiples is $23$. Find the sum of all the multiples of $3$ or $5$ below $N$.

**Input Format**
First line contains $T$ that denotes the number of test cases. This is followed by $T$ lines, each containing an integer, $N$.

**Constraints**
- \\(1 \leq T \leq 10^5\\)
- \\(1 \leq N \leq 10^9 \\)

**Output Format**
For each test case, print an integer that denotes the sum of all the multiples of $3$ or $5$ below $N$

**Sample Input 0**
```
2
10
100
```

**Sample Output 0**
```
23
2318
```

**Explaination 0**

For $N=10$, if we list all the natural numbers below $10$ that are multiples of $3$ or $5$, we get $3$, $5$, $6$ and $9$. The sum of these multiples is $23$. 

Similarly for $N = 100$, we get $2318$

**Code**
```C
#include <math.h>
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <assert.h>
#include <limits.h>
#include <stdbool.h>

int main(){
    int t; 
    scanf("%d",&t);
    for(int a0 = 0; a0 < t; a0++){
        int n; 
        scanf("%d",&n);
        int sum_1 = 0 , sum_2 = 0;
        for (int num_ = 3; num_ < n; num_++){ //num_ mean the number that are multiples of 3 or 5 
            if (num_ % 3 == 0 || num_ % 5 == 0){ 
                if (num_ % 15 == 0){ 
                    sum_2 += num_;
                }
                printf("%d\n", num_);
                sum_1 += num_;
            }
        }
        printf("%d\n", sum_1 - sum_2);
    }
    return 0;
}
```

```python
import math
import os
import random
import re
import sys

if __name__ == '__main__':
    t = int(input().strip())

    for t_itr in range(t):
        n = int(input())
        n1 = (n - 1)//3
        n2 = (n - 1)//5
        n3 = (n - 1)//15  
        print(3*n1*(n1+1)//2 + 5*n2*(n2+1)//2 - 15*n3*(n3+1)//2) 
```

**Explaination**
Let takes an example $N = 10$

There are some integers that satisfy the conditional problem like 3, 5, 6 and 9

Takes as a sum: $3 + 6 + 9 = 3(1 + 2 + 3)$ which equal to this sum formula $3 \times frac{n(n + 1)}{2}$ where $n$ is the total number satisfying this condition

$n$ can computed by get the input number then substract $1$ and divide the multiply of number that satisfied the problem to get the quotient

Since 15 is both the multiplies of 3 and 5 there is a redundancy, so that we need to substract total sum of the multiply of 15
