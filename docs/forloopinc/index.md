# For Loop in C

A challenges Hackerrank and its solution.

<!--more-->
**Objective**

In this challenge, you will learn the usage of the for loop, which is a programming language statement which allows code to be executed until a terminal condition is met. They can even repeat forever if the terminal condition is never met.

The syntax for the ```for``` loop is:
```
for ( <expression_1> ; <expression_2> ; <expression_3> )
    <statement>
```

- expression_1 is used for intializing variables which are generally used for controlling the terminating flag for the loop.

- expression_2 is used to check for the terminating condition. If this evaluates to false, then the loop is terminated.

- expression_3 is generally used to update the flags/variables.

The following loop initializes **_i_** to 0, tests that **_i_** is less than 10, and increments **_i_** at every iteration. It will execute 10 times. 
```
for(int i = 0; i < 10; i++) {
    ...
}
```

**Task**

For each integer **_n_** in the interval **[a,b]** (given as input) :

- If \\(1 \leq n \leq 9\\), then print the English representation of it in lowercase. That is "one" for  **1**, "two" for **2**, and so on.
- Else if \\(n > 9\\) and it is an even number, then print "even".
- Else if \\(n > 9\\) and it is an odd number, then print "odd".

**Input Format**

The first line contains an integer, **_a_**.
The seond line contains an integer, **_b_**.

**Constraints**
\\(1 \leq a \leq b \leq 10^6\\)

**Output Format**

Print the appropriate English representation,```even```, or ```odd```, based on the conditions described in the 'task' section.

**Note:** \\([a,b] = {x \in \Zeta | a \leq x \leq b} = {a, a + 1, ... , b}\\)

**Sample Input**
```
8
11
```

**Sample Output**
```
eight
nine
even
odd
```

# Solution: 

```c
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>



int main() 
{
    int a, b;
    scanf("%d\n%d", &a, &b);
  	// Complete the code.
    for (int i = a; i <= b;i++){
        if (i == 1){
            printf("one");
        }
        else if (i == 2){
            printf("two");
        }
        else if (i == 3){
            printf("three");
        }else if (i == 4){
            printf("four");
        }else if (i == 5){
            printf("five");
        }else if (i == 6){
            printf("six");
        }else if (i == 7){
            printf("seven");
        }else if (i == 8){
            printf("eight");
        }else if (i == 9){
            printf("nine");
        }
        if (i>=1 && i<=9){
            printf("\n");
        }
    }
    for (int i = 10; i <= b;i++){
        if (i%2==0){
            printf("even");
        }else{
            printf("odd");
        }
    printf("\n");
    }
    return 0;
}


```


