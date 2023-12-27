# Printing Pattern Using Loops


This article shows the solution of hackerrank challenges.

<!--more-->

Print a pattern of numbers from **1** to **_n_** as shown below. Each of the numbers is separated by a single space. 
```
                            4 4 4 4 4 4 4  
                            4 3 3 3 3 3 4   
                            4 3 2 2 2 3 4   
                            4 3 2 1 2 3 4   
                            4 3 2 2 2 3 4   
                            4 3 3 3 3 3 4   
                            4 4 4 4 4 4 4   

```

**Input Format**
The input will contain a single integer **_n_**.

**Constraint**
\\(1 \leq n \leq 100\\)

**Sample Input 0**
```
2
```

**Sample Output 0**
```
2 2 2
2 1 2
2 2 2
```

**Sample Input 1**
```
5
```

**Sample Output 1**
```
5 5 5 5 5 5 5 5 5 
5 4 4 4 4 4 4 4 5 
5 4 3 3 3 3 3 4 5 
5 4 3 2 2 2 3 4 5 
5 4 3 2 1 2 3 4 5 
5 4 3 2 2 2 3 4 5 
5 4 3 3 3 3 3 4 5 
5 4 4 4 4 4 4 4 5 
5 5 5 5 5 5 5 5 5
```

**Sample Input 2**

```
7
```

**Sample Output 2**
```
7 7 7 7 7 7 7 7 7 7 7 7 7 
7 6 6 6 6 6 6 6 6 6 6 6 7 
7 6 5 5 5 5 5 5 5 5 5 6 7 
7 6 5 4 4 4 4 4 4 4 5 6 7 
7 6 5 4 3 3 3 3 3 4 5 6 7 
7 6 5 4 3 2 2 2 3 4 5 6 7 
7 6 5 4 3 2 1 2 3 4 5 6 7 
7 6 5 4 3 2 2 2 3 4 5 6 7 
7 6 5 4 3 3 3 3 3 4 5 6 7 
7 6 5 4 4 4 4 4 4 4 5 6 7 
7 6 5 5 5 5 5 5 5 5 5 6 7 
7 6 6 6 6 6 6 6 6 6 6 6 7 
7 7 7 7 7 7 7 7 7 7 7 7 7 
```

# Solution: 

```c
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int arr[10000][10000];
int n;

void init()
{
    for (int i = 0; i < 2*n-1;i++)
    {
        for (int j = 0; j < 2*n-1;j++)
        {
            arr[i][j] = -1;
        }
    }
}

void changerow(int row)
{
    for (int c = row;c < (2*n - 1 - row);c++)
    {
        if (arr[row][c] == -1)
        {
            arr[row][c] = n - row;
            arr[2*n - 1 - row - 1][c] = n - row;
        }
    }
}

void changecol(int col)
{
    for (int r = col;r < (2*n -1 - col);r++)
    {
        if (arr[r][col] == -1)
        {
            arr[r][col] = n - col;
            arr[r][2*n - 1 - col - 1] = n - col;       
        }
    }   
}

void solution()
{
    for (int i = 0;i< 2*n -1;i++)
    {
        for (int j = 0; j < 2*n - 1;j++)
        {
            printf("%d ", arr[i][j]);
        }
        printf("\n");
    }
}
int main() 
{
    scanf("%d", &n);
  	// Complete the code to print the pattern.
    init();
    for (int i = 0; i < n;i++)
    {
        changerow(i);
        changecol(i);
    }
    solution();
    return 0;
}
```
