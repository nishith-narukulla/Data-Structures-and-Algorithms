# Data Structures & Algorithms

## 5 steps to learn

- [x] Learn at least one Programming Language
- [x] Learn about Complexities
- [ ] Learn Data Structure and Algorithms
- [ ] Practice, practice and practice more
- [ ] Compete and become a pro

## Complexities
- these complexities decides whether the solution is efficient or not

### Time Complexity
- to measure the amount of time required to execute the code
- The time required for executing a code depends on
    - The number of operations performed in the program
    - The speed of the device
    - The speed of data transfer if being executed on an online platform
- modified def:
    - the rate of which the time taken increases w.r.t to inpust size
- in most of the cases it takes one second to complete 10e8 operations.

- **Big-O Notation (Ο)**
    - Big-O notation specifically describes the worst-case scenario
- **Omega Notation (Ω)**
    - Omega(Ω) notation specifically describes the best-case scenario
- **Theta Notation (θ)**
    - This notation represents the average complexity of an algorithm

![complexities](https://media.geeksforgeeks.org/wp-content/cdn-uploads/mypic.png)

### Space complexity
- the amount of space required to execute successfully the functionalities of the code
- basically extra space/Auxiliary space used by your code

## Patterns
- Learn patterns for better understanding of loops

- basically patterns were done by the nested loops
    - inner loop is for rows and
    - outer loop is for columns
- **step1:** count the no.of columns for outer loop
- **step2:** for inner loop focus on the columns and connect them somehow to the rows
- **step3:** print pattern inside inner loop
- **Step4(Optional):** observe symmetry

### Example patterns
#### **Pattern:1** 
```java
/*

* * * *
* * * *
* * * *
* * * *

@rows    --> 4
@columns --> 4
*/

for(int i=0; i<4;i++){
    for(int j=0;j<4;j++){
        System.out.print("* ");
    }
    System.out.println("\n");
}
```
```python
for i in range(4):
    for j in range(4):
        print("*", end=" ")
    print("\n")
```

#### **Pattern:2**
```java
/*

*
* *
* * *
* * * *
* * * * *

@rows    --> 5
@columns --> 1 to 5

*/

for(int i=0; i<5;i++){
    for(int j=0;j<=i;j++){
        System.out.print("* ");
    }
    System.out.println("\n");
}
```
```python
for i in range(5):
    for j in range(0,i+1):
        print("*", end=" ")
    print("\n")
```

#### **Pattern:3**
```java
/*

1
1 2
1 2 3
1 2 3 4
1 2 3 4 5

@rows    --> 5
@columns --> 1 to 5

*/

for(int i=0; i<5;i++){
    for(int j=0;j<=i;j++){
        System.out.print(j+1);
        System.out.print(" ");
    }
    System.out.println("\n");
}
```
```python
for i in range(5):
    for j in range(0,i+1):
        print(j+1, end=" ")
    print("\n")
```

#### **Pattern:4**
```java
/*

1
2 2
3 3 3
4 4 4 4
5 5 5 5 5

@rows    --> 5
@columns --> 1 to 5

*/

for(int i=0; i<5;i++){
    for(int j=0;j<=i;j++){
        System.out.print(i+1);
        System.out.print(" ");
    }
    System.out.println("\n");
}
```
```python
for i in range(5):
    for j in range(0,i+1):
        print(i+1,end=" ")
    print("\n")
```

#### **Pattern:5**
```java
/*

* * * * *
* * * *
* * *
* * 
*
@rows    --> 5
@columns --> 5 to 1
*/

for(int i=5; i>0;i--){
    for(int j=0;j<i;j++){
        System.out.print("*");
        System.out.print(" ");
    }
    System.out.println("\n");
}
```
```python
for i in range(0,5,-1):
    for j in range(0,i+1):
        print("*",end=" ")
    print("\n")
```

#### **Pattern:6**
```java
/*

1 2 3 4 5
1 2 3 4
1 2 3
1 2
1

@rows    --> 5
@columns --> 5 to 1

*/

for(int i=5; i>0;i--){
    for(int j=0;j<i;j++){
        System.out.print(j+1);
        System.out.print(" ");
    }
    System.out.println("\n");
}
```
```python
for i in range(0,5,-1):
    for j in range(0,i+1):
        print(j+1,end=" ")
    print("\n")
```

#### **Pattern:7**
```java
/*
    *
   *** 
  *****
 *******
*********

@rows     --> 5
@columns  --> 9
@relation --> [spaces, stars, spaces]
              [4, 1, 4]
              [3, 3, 3]
              [2, 5, 2]
              [1, 7, 1]
              [0, 9, 0]
              [rows-1 to 0, 2*rows-1, rows-1 to 0]
*/

for(int i=0;i<n;i++){
    for(int k=0;k<n-i-1;k++){
        System.out.print(" ");
    }
    for(int j=0;j<2*i+1;j++){
        System.out.print("*");
    }
    for(int k=0;k<n-i-1;k++){
        System.out.print(" ");
    }
    System.out.print("\n");
}
```
```python
for i in range(n):
    for k in range(n-i-1):
        print(" ")
    for j in range(2*i+1):
        print("*")
    for k in range(n-i-1):
        print(" ")
    print("\n")
```

#### **Pattern:8**
```java
/*

*********
 *******
  *****
   ***
    *

@rows    --> 5
@columns --> 9
@relation --> [0, 9, 0]
[1, 7, 1]
[2, 5, 2]
[3, 3, 3]
[4, 1, 4]
[i, ,2*rows-(2*i+1), i]
*/

for(int i=0;i<n;i++){
    for(int k=0;k<i;k++){
        System.out.print(" ");
    }
    for(int j=0;j<2*n-(2*i+1);j++){
        System.out.print("*");
    }
    for(int k=0;k<i;k++){
        System.out.print(" ");
    }
    System.out.print("\n");
}
```
```python
for i in range(n):
    for k in range(i):
        print(" ")
    for j in range(2*n-(2*i+1)):
        print("*")
    for k in range(i):
        print(" ")
    print("\n")
```

#### **Pattern:9**
```java
/*

    *
   *** 
  *****
 *******
*********
*********
 *******
  *****
   ***
    *
@Hint: combination of pattern:7 & pattern:8
*/
```

#### **Pattern:10**
```java
/*

*
**
***
****
*****
****
***
**
*

@rows    --> 9
@columns --> 5

*/
for(int i=0;i<=2*n;i++){
    int stars = i;
    if (i>4)
        stars = 2*n-i;
    for(int j=0;j<=stars;j++){
        System.out.print("*");
    }
    System.out.print("\n");
}
```
```python
for i in range(2*n+1):
    stars = i
    if i>4:
        stars = 2*n-i
    for k in range(stars+1):
        print("*",end="")
    print("\n",end="")
```

#### **Pattern:11**
```java
/*

1
00
111
0000
11111

@rows --> 5
@columns --> 1 to 5
@Hint: even rows 1
        odd rows 0
*/

for(int i=0;i<n;i++){
    if (i%2 == 0) start = 1;
    else start = 0;
    for(int j=0;j<=i;j++){
        System.out.print(start);
    }
    System.out.print("\n");
}
```
```python
for i in range(n):
    if i%2==0:
        start = 1
    else:
        start = 0
    for j in range(i+1):
        print(start,end="")
    print("\n",end="")
```
#### **Pattern:12**
```java
/*

1
01
101
0101
10101

@rows    --> 5
@columns --> 1 to 5
@relation --> same as above pattern
              but flips b/w 0 & 1
*/

for(int i=0;i<n;i++){
    if (i%2 == 0) start = 1;
    else start = 0;
    for(int j=0;j<=i;j++){
        System.out.print(start);
        start = 1 - start;
    }
    System.out.print("\n");
}
```
```python
for i in range(n):
    if i%2==0:
        start = 1
    else:
        start = 0
    for j in range(i+1):
        print(start,end="")
        start = 1 - start
    print("\n",end="")
```

#### **Pattern:13**
```java
/*

1      1
12    21
123  321
12344321

@rows    --> 4
@columns --> 8
@relation--> [num, spaces, num]
             [1, 6, 1]
             [2, 4, 2]
             [3, 2, 3]
             [4, 0, 4]
             [row, 2*(n-1)-2, row]

*/

for(int i=0;i<n;i++){
    for(int j=0;j<=i;j++){
        System.out.print(j+1);
    }
    for(int j=0;j<spaces;j++){
        System.out.print("*");
    }
    for(int j=i;j>=0;j--){
        System.out.print(j+1);
    }
    System.out.print("\n");
    spaces -= 2;
}
```
```python
for i in range(n):
    for j in range(i+1):
        print(j+1,end="")
    for j in range(spaces):
        print(" ",end="")
    for j in range(i,-1,-1):
        print(j+1,end="")
    print("\n",end="")
    spaces -= 2
```

#### **Pattern:14**
```java
/*

1
2 3
4 5 6
7 8 9 10
11 12 13 14 15

@rows    --> 5
@columns --> 1 to rows
@Hint: increment the starting number for every iteration
*/
for(int i=0;i<n;i++){
    for(int j =0;j<=i;j++){
        System.out.print(num + " ");
        num++;
    }
    System.out.print("\n");
}
```
```python
for i in range(n):
    for j in range(i+1):
        print(num,end=" ")
        num += 1
    print("\n",end="")
```

#### **Pattern:15**
```java
/*

A
AB
ABC
ABCD
ABCDE

@rows   --> 5
@columns --> 1 to rows
@Hint: print chars starting from 'A'
*/

for(int i=0;i<n;i++){
    for(char c='A';c<='A'+i;c++){
        System.out.print(c + " ");
    }
    System.out.print("\n");
}
```
```python
for i in range(n+1):
    for j in range(ord('A'), ord('A')+i):
        print(chr(j),end=" ")
    print("\n",end="")
```

#### **Pattern:16**
```java
/*
ABCDE
ABCD
ABC
AB
A

@rows    --> 5
@columns --> rows to 1
*/

for(int i=0;i<n;i++){
    for(char c='A';c<='A'+(n-i-1);c++){
        System.out.print(c + " ");
    }
    System.out.print("\n");
}
```
```python
for i in range(n):
    for j in range(ord('A'), ord('A')+(n-i)):
        print(chr(j),end=" ")
    print()
```

#### **Pattern:17**
```java
/*

A
BB
CCC
DDDD
EEEEE

@rows   --> 5
@columns --> 1 to rows

*/

for(int i=0;i<n;i++){
    for(int j=0;j<=i;j++){
        System.out.print(ch);
    }
    System.out.print("\n");
    ch += 1;
}
```
```python
for i in range(n):
    for j in range(i+1):
        print(chr(ch),end=" ")
    print()
    ch += 1
```

#### **Pattern:18**
```java
/*

    A
   ABA
  ABCBA
 ABCDCBA
ABCDEDCBA

@rows   --> 5
@columns --> 1 to 5
@relation --> [space, char, space]
              [4, 1, 4]
              [3, 3, 3]
              [2, 5, 2]
              [1, 7, 1]
              [0, 9, 0]
              [(rows-i+1), , (rows-i+1)]
*/

for(int i=0;i<n;i++){
    for(int j=0;j<(n-i-1);j++){
        System.out.print("*");
    }
    char ch = 'A';
    int breakPoint = (2*i+1)/2;
    for(int j=0; j<2*i+1; j++){ 
        System.out.print(ch); 
        if (j<breakPoint) ch++; 
        else ch--;
    }
    for(int j=0;j<(n-i-1);j++){
        System.out.print("*");
    }
    System.out.print("\n");
}
```
```python
for i in range(n):
    for j in range(n-i+1):
        print(" ",end="")
    ch = ord('A')
    breakpoint = (2*i+1)//2
    for j in range(2*i+1):
        print(chr(ch),end="")
        if j<breakpoint:
            ch += 1
        else:
            ch -= 1
    for j in range(n-i-1):
        print(" ",end="")
    print()
```

#### **Pattern:19**
```java
/*

E
D E
C D E
B C D E
A B C D E

@rows    --> 5
@columns --> 1 to rows
@Hint    --> every consists characters from 'E'-i to E
*/

for(int i=0;i<n;i++){
    for(char ch= (char) ('E' - i);ch<='E';ch++){
        System.out.print(ch+" ");
    }
    System.out.print("\n");
}
```
```python
for i in range(n):
    for j in range(ord('E')-i, ord('E')+1):
        print(chr(j),end=" ")
    print()
```

#### **Pattern:20**
```java
/*

**********
****  ****
***    ***
**      **
*        *

@rows    --> 5
@columns --> 2*rows
@relation--> [stars, spaces, stars]
             [5, 0, 5]
             [4, 2, 4]
             [3, 4, 3]
             [2, 6, 2]
             [1, 8, 1]
             [(rows-i), 2*i, (rows-i)]
*/

for(int i=0;i<n;i++){
    for(int j=0;j<(n-i);j++){
        System.out.print("*");
    }
    for(int j=0;j<(2*i);j++){
        System.out.print(" ");
    }
    for(int j=0;j<(n-i);j++){
        System.out.print("*");
    }
    System.out.print("\n");
}
```
```python
for i in range(n):
    for j in range(n-i):
        print("*",end="")
    for j in range(2*i):
        print(" ",end="")
    for j in range(n-i):
        print("*",end="")
    print()
```

#### **Pattern:21**
```java
/*

*        *
**      **
***    ***
****  ****
**********

@rows    --> 5
@columns --> 2*rows
@relation--> [stars, spaces, stars]
             [1, 8, 1] // 0
             [2, 6, 2] // 1
             [3, 4, 3] // 2
             [4, 2, 4] // 3
             [5, 0, 5] // 4
             [row, 2*(n-i-1), row]
*/

for(int i=0;i<n;i++){
    for(int j=0;j<=i;j++){
        System.out.print("*");
    }
    for(int j=0;j<2*(n-i-1);j++){
        System.out.print(" ");
    }
    for(int j=0;j<=i;j++){
        System.out.print("*");
    }
    System.out.print("\n");
}
```
```python
for i in range(n):
    for j in range(i+1):
        print("*",end="")
    for j in range(2*(n-i-1)):
        print(" ",end="")
    for j in range(i+1):
        print("*",end="")
    print()
```
#### **Pattern:22**
```java
/*

    * * * * * * * * * *
    * * * *     * * * *
    * * *         * * *
    * *             * *
    *                 *
    *                 *
    * *             * *
    * * *         * * *
    * * * *     * * * *
    * * * * * * * * * *

@rows    --> 10 (5+5)
@columns --> 
@relation --> [stars, spaces, stars]
              [5, 0, 5]
              [4, 2, 4]
              [3, 4, 3]
              [2, 6, 2]
              [1, 8, 1]
              [(rows-i), 0(+2), (rows-i)]

@Hint: combination of above two patterns
*/
```

#### **Pattern:23**
```java
/*

*        *
**      **
***    ***
****  ****
**********
****  ****
***    ***
**      **
*        *

@rows    --> 9
@columns --> 2*rows
@relation--> [stars, spaces, stars]
             [1, 8, 1]
             [2, 6, 2]
             [3, 4, 3]
             [4, 2, 4]
             [5, 0, 5]
             [row, 2*(n-i-1), row]

             if (row>5) 

             [4, 2, 4]
             [3, 4, 3]
             [2, 6, 2]
             [1, 8, 1]
             [row-i-1, 2*i, row-i-1]

*/

for(int i=1;i<=2*n-1;i++){
    int stars = i;
    if (i>n) stars = 2*n-i; 
    for(int j=1; j<=stars;j++){
        System.out.print("*");
    }
    for(int j=1;j<=spaces;j++){
        System.out.print(" ");
    }
    for(int j =1;j<=stars;j++){
        System.out.print("*");
    }
    System.out.print("\n");
    if (i>=n) spaces += 2;
    else spaces -= 2;
}
```
```python
for i in range(1,2*n): # 5
    stars = i # 6
    if (i>n):
        stars = 2*n-i # 5
    for j in range(1,stars+1): 
        print("*",end="")
    for j in range(1,spaces+1):
        print(" ",end="")
    for j in range(1,stars+1):
        print("*",end="")
    print()
    if(i>=n):
        spaces += 2
    else:
        spaces -= 2
```

#### **Pattern:24**
```java
/*

* * * *
*     *
*     *
* * * *

@rows    --> 4
@columns --> rows
@relation--> [2, 0, 2]
             [1, 2, 1]
             [1, 2, 1]
             [2, 0, 2]
*/

for(int i=0;i<n;i++){
    for(int j=0;j<n;j++){
        if (i==0 || i == n-1 || j == 0 || j == n-1)
        System.out.print("*");
        else
            System.out.print(" ");
    }
    System.out.print("\n");
}
```
```python
for i in range(n):
    for j in range(n):
        if (i==0 or i==n-1 or j==0 or j==n-1):
            print("*",end="")
        else:
            print(" ",end="")
    print()
```

#### **Pattern:25**
```java
/*

4 4 4 4 4 4 4
4 3 3 3 3 3 4
4 3 2 2 2 3 4
4 3 2 1 2 3 4
4 3 2 2 2 3 4
4 3 3 3 3 3 4
4 4 4 4 4 4 4

@rows    --> 7 (2*n-1) n = 4
@columns --> 7
@Hint    --> form matrix A with n as elements

             4 4 4 4 4 4 4
             4 4 4 4 4 4 4
             4 4 4 4 4 4 4
             4 4 4 4 4 4 4
             4 4 4 4 4 4 4
             4 4 4 4 4 4 4
             4 4 4 4 4 4 4

             for another matrix B with minimum distance
             of each element from four sides

             0 0 0 0 0 0 0
             0 1 1 1 1 1 0
             0 1 2 2 2 1 0
             0 1 2 3 2 1 0
             0 1 2 2 2 1 0
             0 1 1 1 1 1 0
             0 0 0 0 0 0 0

             Distances: top = i
                        right = (2*n-1)-1-j
                        bottom = (2*n-1)-1-i
                        left = j

            now A-B gives you the resultant matrix
*/

for(int i=0;i<2*n-1;i++){
    for(int j=0;j<2*n-1;j++){
        int top = i;
        int right = (2*n-1)-1-j;
        int bottom = (2*n-1)-1-i;
        int left = j;
        int min_ = Math.min(Math.min(top,bottom), Math.min(right,left));
        System.out.print(n-min_ + " ");
    }
    System.out.print("\n");
}
```
```python
for i in range(2*n-1):
    for j in range(2*n-1):
        top = i
        right = (2*n-1)-1-j
        bottom = (2*n-1)-1-i
        left = j
        min_ = min(min(top,bottom), min(right,left))
        print(n-min_,end=" ")
    print()
```
## End of Patterns!

## Basic Math Cocepts

### Extraction of digits
- modulus with 10 gives the last digit of the number
    - 5667 % 10  == 7
    - 5667 % 100 == 67 ...
```java
while (num>0) {
    lastDigit = num % 10;
    System.out.print(lastDigit + " ");
    num = num/10;
    }
System.out.println("\nFinal num: " + num);
```
```python
while (num>0):
    lastDigit = num % 10
    print(lastDigit,end=" ")
    num = num // 10
```

### 

### Basic Math Problems

#### **Problem:1 **
- counting the number digits in a given number
```java
while(num>0){
    num = num/10;
    count++;
}
System.out.println("number od digits: " + count);

// --------------- OR ----------------

// int count = (int)Math.log10(num) + 1;
// System.out.println(count);
```
```python
while (num>0):
    num = num // 10
    count += 1
print(count)
# ------------------------------------
#print( int(math.log10(num) + 1) )
```
- **Time Complexity:** O(log10(N))
    - whenever the logic depends on division TC will be loagrithmic
    - if divided by 2 TC: O(log2(N))
    - O(log_base(N)) base --> divisor
#### **Problem:2**
- Reverse a number
    - if it has tailing zeroes ignore them
    - Example: 10400 --> 401

```java
static int reverseNumber(int num){
    int lastDigit;
    int reverseNumber = 0;
    while(num>0){
        lastDigit = num % 10;
        num = num / 10;
        reverseNumber = (reverseNumber*10) + lastDigit;
    }
    return reverseNumber;
}
```
```python
def reverseNumber(num):
    reversedNum = 0
    while(num):
        lastDigit = num % 10
        num = num // 10
        reversedNum = (reversedNum*10) + lastDigit
    return reversedNum
```
#### **Problem:3**
- check if the given number is palindrome or not
```java
static boolean checkPalindrome(int num){
    int tempNum = num;
    int lastDigit;
    int reverseNumber = 0;
    while(tempNum>0){
        lastDigit = tempNum % 10;
        tempNum = tempNum / 10;
        reverseNumber = (reverseNumber*10) + lastDigit;
    }
    if(num == reverseNumber)
        return true;
    else
        return false;
}
```
```python
def checkArmstrongNumber(num):
    tempNum = num
    reversedNum = 0
    while(tempNum>0):
        lastDigit = tempNum % 10
        tempNum = tempNum // 10
        reversedNum = (reversedNum*10) + lastDigit
    if(reversedNum == num):
        return True
    else:
        return False
```
#### **Problem:4**
- check if the given number is armstrong or not
```java
static boolean checkArmstrong(int num){
    int tempNum = num;
    int lastDigit;
    int sum = 0;
    while(tempNum>0){
        lastDigit = tempNum % 10;
        sum += Math.pow(lastDigit, 3);
        tempNum = tempNum / 10;
    }
    if(num == sum)
        return true;
    else
        return false;
}
```
```python
def checkArmstrongNumber(num):
    tempNum = num
    sum = 0
    while(tempNum>0):
        lastDigit = tempNum % 10
        sum += pow(lastDigit, 3)
        tempNum = tempNum // 10
    if(num == sum):
        return True
    else:
        return False
```
#### **Problem:5**
- find divisors of given number
```java
static void printDivisors(int num){
    System.out.println("divisors of " + num + " are");
    for(int i=1;i<=num;i++){
        if(num%i==0)
            System.out.print(i + " ");
    }
}
// 1 2 3 4 6 9 12 18 36
```
```python
def checkArmstrongNumber(num):
    for i in range(1,num+1):
        if num%i ==0:
            print(i,end=" ")
```
- Time Complexity: O(N)
**Better Solution**
```java
static void printDivisors(int num){
    System.out.println("divisors of " + num + " are");
    for(int i=1;i<=Math.sqrt(num);i++){
        if(num%i==0)
            System.out.print(i + " ");
            if(num/i != i){
                System.out.print((num/i) + " ");
            }
    }
}
// 1 36 2 18 3 12 4 9 7 6
```
```python
def checkArmstrongNumber(num):
    for i in range(1, int( math.sqrt(num) )+1):
        if num%i ==0:
            print(i,end=" ")
            if num//i != i:
                print(num//i,end=" ")
```
- Time Complexity: O(sqrt(N))
#### **Problem:6**
- checking if the given number is prime or not
```java
    static boolean checkPrime(int num){
        int count = 0;
        for(int i=1;i<=Math.sqrt(num);i++){
            if(num%i==0)
                count++;
                if(num/i != i)
                    count++;
        }
        if (count == 2)
            return true;
        else
            return false;
    }
```
```python
def checkPrime(num):
    count = 0
    for i in range(1, int( math.sqrt(num) )+1):
        if num%i ==0:
            count += 1
            if num//i != i:
                count += 1
    if count == 2:
        return True
    else:
        return False
```
#### **Problem:7**
```java
static int getGcd(int num1, int num2){
    int gcd = 1;
    for(int i=1;i<=Math.min(num1, num2);i++){
        if (num1%i == 0 && num2%i == 0){
            gcd = i;
        }
    }
    return gcd;
}
```
```python
def getGcd(num1,num2):
    gcd = 1
    for i in range(1, min(num1, num2)+1):
        if num1%i == 0 and num2%i == 0:
            gcd = i
    return gcd
```
- Time Complexity: O(min(num1, num2))

**Another Solution**
```java
static int getGcd(int num1, int num2){
    int gcd = 1;
    for(int i =Math.min(num1, num2);i>=1;i--){
        if (num1%i == 0 && num2%i == 0){
            gcd = i;
            break;
        }
    }
    return gcd;
}
```
```python
def getGcd(num1,num2):
    gcd = 1
    for i in range(min(num1,num2),0,-1):
        if num1%i == 0 and num2%i == 0:
            gcd = i
            break
    return gcd
```
- Time complexity: O(min(num1,num2))

**Better Solution**
- gcd(a,b) = gcd(a-b,b) if a>b --> Euclidian theory
- gcd(a,b) = gcd(a%b,b) if a>b

```java
static int getGcd(int num1, int num2){
    while(num1>0 && num2>0){
        if(num1>num2)
            num1 = num1%num2;
        else
            num2 = num2%num1;
    }
    if (num1 == 0)
        return num2;
    else
        return num1;
}
```
```python
def getGcd(num1,num2):
    while(num1>0 and num2>0):
        if(num1>num2):
            num1 = num1%num2
        else:
            num2 = num2%num1
    if num1==0:
        return num2
    else:
        return num1
```
- Time complexity: O(log_base(min(num1,num2)))
## End Basics of Maths Concepts


## Data Structures

- Arrays
- Strings
- Linked List
- Stack
- Queue
- Heap
- Hash
- Trees
    - Binary Tree
    - Binary Search Tree
    - Other tree data structures
- Graphs

## Algorithms

- Searching Algorithms
    - Linear Search
    - Binary Search
    - BFS and DFS
- Sorting Algorithms
    - Insertion Sort
    - Selection Sort
    - Bubble Sort
    - Merge Sort
    - Quick Sort
    - Heap Sort
- Divide and Conquer Algos
- Greedy Algorithms
- Recursion
- Backtracking Algorithms
- Dyanamic Programming
- Pattern Searching
- Bitwise Algorithm

[Reference](https://www.geeksforgeeks.org/learn-data-structures-and-algorithms-dsa-tutorial/?ref=lbp)

## Some popular Algorithms

- Kruskals Algorithm
- Floyd Warshall Algorithm
- Dijkstras Algorithm
- Bellaman Ford Algorithm
- Kadanes Algorithm
- Lee Algorithm
- Flood Fill Algorithm
- Topological Sorting
- Union Find lgorithm