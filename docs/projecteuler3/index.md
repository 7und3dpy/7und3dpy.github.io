# Project Euler 3: Largest prime factor



The prime factor of $13195$ are $5, 7, 13$ and $29$

<!--more-->

What is the largest prime factor of a given number $N$ ?

**Input Format**

First line contains $T$, the number of test cases. This is followed by $T$ lines each containing an integer $N$

**Constraints**
- $1 \leq T \leq 10$
- $10 \leq N \leq 10^12$

**Output format**

For each test case, display the larget prime factor of $N$

**Sample Input 0**
```
2
10
17
```

**Sample Output 0**

```
5
17
```

**Explaination 0**
- Prime factors of $10$ are ${2,5}$, largest is $5$
- Prime factor of $17$ is $17$ itself, hence largest is $17$

**Solution**

```c

```

**Explaination**

Thuật toán $\mathcal{O}(\sqrt{N})$

Phương pháp cơ bản ở đây là duyệt dãy số nguyên tố: 
\\[P = \{2,3,5,7,11,17,...\}\\]

để tìm ước số nguyên tố của $N$. Thông thường phương pháp như vậy rất tốn kém bộ nhớ, thường sử dụng [Sàng Eratosthenes](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes). Do đó, ta sẽ duyệt qua một dãy $Q[1,2,...,] = \{q_1,q_2,...\}$ dễ sinh hơn dãy $P$ sao cho $P \subseteq Q$ ($Q$ có thể chứa hợp số)
\\[Q[1,2,...] = \{2,3,5,7,11,13,17,19, 23, 25, 29, 31, 35, 37, 41...\} \hspace{1cm} (1)\\]

Ngoại trừ 2 dãy số đầu tiên, dãy $Q$ có khoảng cách giữa hai số liền kề nhau thay đổi liên tục giữa 2 và 4. Mã giả như sau: 


