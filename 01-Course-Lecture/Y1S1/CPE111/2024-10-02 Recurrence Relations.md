---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2024-10-02

Recurrence Relations
1. Applications of Recurrence Relations.
2. Solving Linear Recurrence.
3. Divide-and-Conquer Algorithms and Recurrence Relations.

# Recurrence Relations
## Definition
ความสัมพันธ์​ของ sequence $\{ a_{n} \}$ 
$$
\begin{align}
a_{n} & =a_{n-1}+3,  & n=1,2,3 \dots \\
a_{0} & =2
\end{align}
$$
general term: $a_{n}=a_{1}+(n-1)d$

- seq คือ solution
- inital conditions คือ เริ่มเเท่าไร่
- หาไป n รอบ

## Fibonacci Numbers

1. เอากระต่ายไปเพาะพันธุ์ คู่ 1 ลูก
2. คลอดทุกๆ 1
3. ผ่านไป n เดือนจะได้กี่คู่?

![[Screenshot 2567-10-02 at 14.14.57.png]]

$1,1,2,3,5,8,\dots$

Recurrence Relation:
$f_{n}$ เป็นจำนวนคู่ผ่านไป n เดือน
$$
\begin{align}
f_{1}  & = 1 \\
f_{2}  & = 1 \\
f_{3}  & = 2 \\
f_{4}  & = 3 \\
\end{align}
$$
initial condition : $f_{1} = 1, f_{2}=1$
*Breeding of rabbit

$$
\begin{align}
f_{3} & =f_{1}+f_{2} \\
f_{4}  & =f_{3}+f_{2} \\
f_{n} & =f_{n-1}+f_{n-2},n\geq_{3}
\end{align}
$$

## Tower of Hanoi

![[Pasted image 20241002142301.png]]

ย้ายที่ล่ะ 1 Disk
Disk ใหญ่ ห้ามอยู่บน Disk เล็ก
ย้ายจากเสา 1 ไป เสา 2

$$
\begin{align}
f_{1} & =1 \\
f_{2} & =3 \\
f_{n} & =2f_{n-1}+1  & ,n\geq_{2}
\end{align}
$$

![[IMG_4227.jpg]]

iterative approach

$$
\begin{align}
H_{n} & =2H_{n-1}+1 \\
 & =2(2H_{n-2}+1)+1   & = &  2^2H_{n-2}+2+1 \\
 & =2(2H_{n-3}+1)   & = & 2^3H_{n-3}+2^2+2+1 \\
 & =2(2H_{n-4}+1)  & = & 2^4H_{n-4}+2^3+2^2+2+1 \\
 & \vdots \\
 & =2^{n-2}(2H_{n-(n-1)}+1)\times 2^{(n-3)}+2^{(n-4)}+\dots+1 \\
 & H_{1}=1 \\
 & =2^{n-2}(2+1)+2^{n-3}+2^{n-2}+\dots+1 \\ \\
 & =2^{n-1}+2^{n-2}+2^{n-3}+\dots+1  & = 2^{n}-1
\end{align}
$$

solution คือ $2^{n-1}$
ถ้า มี n disk เราจะย้ายได้ทั้งหมด $2^n-1$

## Count Bit Strings
Problems: มี initial conditions หา

Solution : $a_{n}$ หาระยะของ bit strings ของ n ไม่มี 0 2 ตัวติดกัน
1. จบด้วย 1 ไม่เติม => $\square$ 1 $a_{n-1}$
2. จบด้วย 0 ต้องเตืม 1 => $\square 0 1$ $a_{n}-2$
3. รวม $a_{n}=a_{n-1}+a_{n-2}$

Recurrence Relation:

$$
\begin{align}
a_{1} & =\{ 0,1 \} \\
a_{2} & =\{ 01,10,11 \} \\
a_{3}  & = \{ 010, 011,101,110,111 \} \\ \\

a_{3}  & = a_{2}+a_{1} \\
a_{4}  & =a_{3}+a_{2}
\end{align}
$$
เติม 1 และ 10

$$
\begin{align}
a_{1} & =\{ 0,1 \} \\
a_{2}  & =\{ 01,10,11 \} \\
a_{3}  & = a_{2}<concat>1+a_{1}<concat>10 \\
 & = a_{3}=a_{2}
+a_{1} \\
a_{4}=a_{3}<>1+a_{2}<>10
\end{align}
$$
relation = $a_{n}=a_{n-1}+a_{n-2},n\geq 3$
initial condition = $a_{1}=2,a_{2}=3$

## Counting the Ways to Parenthesize a Product

**Problem** : find $C_{n}$

$C_{3}=5$
$$
\begin{align}
((x_{0}\times x_{1})\times x_{2})\times x_{3}
\end{align}
$$
มี 3 ตัว n=3 เติมวงเล็บได้ 2 อัน

$$
\begin{align}
C_{2}\times C_{0} \\
C_{2} \times C_{0} \\
C_{1} \times C_{1} \\
C_{0} \times C_{2} \\
C_{0} \times C_{2}
\end{align}
$$
$C_{0}=1$
$$
x_{0}
$$
$C_{1}=1$
$$
x_{0}\times x_{1}
$$
$C_{2}=C_{0}+C_{1}=2$
$$
\begin{align}
(x_{0}\times x_{1})\times x_{2} \\
x_{0}\times (x_{1}\times x_{2})
\end{align}
$$
$C_{3}=C_{2}\times C_{0}+C_{1}\times C_{1}+C_{0}\times C_{2}=(2)(1)+(1)(1)+(1)(2)=5$

initial condition => $C_{0},C_{1}$
หาความสัมพันธ์ระหว่างกันไม่ได้

$$
\begin{align}
C_{n} & =C_{0}C_{n-1}+C_{1}+C_{n-2}+\dots+C_{n-2}C_{1}+C_{n-1}C_{0} \\
\end{align}
$$
$$
\sum^{n-1}_{k=0}C_{k}C_{n-k-1} ,n\geq_{2}
$$
# Solving Linear Recurrence Relations

## Definition
$$
\begin{align}
a_{n} & =c_{1}a_{n-1}+c_{2}a_{n-2}+\dots+c_{k}a_{n-k} \\
c_{1},c_{2},\dots c_{k} \in R,c_{k}  &  \neq 0
\end{align}
$$
1. **Linear**: ทุกๆ term คือผลรวมของ term ก่อนหน้า คูณด้วย constants
2. **Homogeneous**: ไม่มีการบวกเพิ่มใดๆเลย
3. **Degree k**: ตาม k

Linear
1. เอาอะไรไป ใส่เพิ่มได้เพิ่ม ใส่ลดได้ลด

Homo
1. ย้าย $a_{n}$ ไปอีกฝั่งแล้วที่เหลืออยู่เป็น 0

Degree k:
1. ไม่มีอะไรกระทำเลย

### Example:
1. $P_{n}=(1.11)P_{n-1}$
	1. Linear เพราะไม่มี var มาคูณ $P_{n}$
	2. ย้ายได้ $0=(1.11)P_{n-1}-P_{n}$
	3. degree = 1
2. $f_{n}=f_{n-1}+f_{n-2}$
	1. Linear
	2. Homo
	3. degree=1
3. $a_{n}=a_{n-1}$
	1. Non-linear
	2. Homo
	3. Degree =2
4. Tower of hanoi
	1. Linear
	2. Non-homo เพราะย้ายแล้วเหลือ -1
	3. degree = 1 *แก้โดยใช้วิธีนี้ได้ ถ้า มี degree เท่ากับ 1
5. $B_{n}=nB_{n-1}$
	1. Non-linear มี var คูณ
	2. Homo ย้ายไปมาได้
	3. degree = 1

## Solve Linear Monogynous Recurrence Relations

สร้าง **characteristic equation**
1. $a_{n}=r^n$
$$
r^n=c_{1}r^{k-1}+c_{2}r^{k-2}+\dots+c_{k}
$$
2. หารด้วย $r^{n-k}$
3. ได้คำตอบ

พอเราได้ roots แล้ว
$r^2+3r+2=0$
$(r-2)(r-1)=0$
$r=1,2$

## solve with Distinct Roots

Theorem
$$
\begin{align}
a_{n} &= a_{1}r_{1}^n + a_{2}r_{2}^n
\end{align}
$$

### Example:

จาก $a_{n}-a_{n-1}-2a_{n-2}=0$ เมื่อ $a_{0}=2$ และ $a_{1}=7$
Char. Eq;
$$
\begin{align}
r^2-r-2 & =0 \\
(r-2)(r+1) & =0 \\
r & =-1,2
\end{align}
$$
$\therefore a_{n}=a_{1}(-1)^n+a_{2}(2)^n$
หา $a_{1},a_{2}$

$$
\begin{align}
a_{0}=2 & ; & 2=a_{1}+a_{2} &  & (1) \\
a_{1}=7 & ; & 7=-a_{1}+2a_{2} &  & (2) \\
\end{align}
$$
$(1)+(2)$
$$
\begin{align}
a_{2} & =3 \\
a_{1} & =-1
\end{align}
$$
$\therefore a_{n}=-(-1)^n+3\times 2 ^ n$

### Example:
Fibonacci
$$
\begin{align}
f_{n} & =f_{n-1}+f_{n-2} \\
f_{n}-f_{n-1}-f_{n-2} & =0
\end{align}
$$
char. eq. $r^2-r-1=0$

$$
\begin{align}
r & =\frac{-b\pm \sqrt{ b^2-4ac }}{2a} \\
r & =\frac{1+\sqrt{ 5 }}{2},\frac{1-\sqrt{ 5 }}{2}
\end{align}
$$
$$
\begin{align}
f_{n} & =a_{1}\left( \frac{1+\sqrt{ 5 }}{2} \right)^n+a_{2}\left( \frac{1-\sqrt{ 5 }}{2} \right)^n \\
f_{0} & =1; \\
0 & = a_{1} +a_{2}  & \dots (1) \\
f_{1} & =1; \\
1 & =a_{1}\left( \frac{1+\sqrt{ 5 }}{2} \right)+a_{2}\left( \frac{1-\sqrt{ 5 }}{2} \right) & \dots(2) \\
f_{n} & =\frac{1}{\sqrt{ 5 }}\left( \frac{1+\sqrt{ 5 }}{2} \right)^n+\frac{1}{\sqrt{ 5 }}\left( \frac{1-\sqrt{ 5 }}{2} \right)^n \\
\end{align}
$$

$\therefore f_{n} = \frac{1}{\sqrt{ 5 }}\left( \frac{1+\sqrt{ 5 }}{2} \right)^n+\frac{1}{\sqrt{ 5 }}\left( \frac{1-\sqrt{ 5 }}{2} \right)^n \in O(2^n)$

## Repeated Root รากซ้ำ

$$
a_{n}=a_{1}r_{0}^n+a_{2}n_{0}^n
$$

for $n=0,1,2,\dots,n \in R$

### Example:
$a_{n}= 6a_{n-1}-9a_{n-2}$ โดย $a_{0}=1,a_{1}=6$

จาก $a_{n}-6a_{n-1}+9a_{n-2}=0$
char eq,;
$$
\begin{align}
r^2-6r+9 & =0 \\
r & =3,3 \\
a_{n}  & =a_{1}\times 3^n + a_{2}\times n\times 3^n
\end{align}
$$
แทน $a_{0}=1$
$$
a_{1}=1
$$
แทน $a_{1}=6$
$$
\begin{align}
6 & =3a_{1}+3a_{2} \\
a_{2} & =1
\end{align}
$$
$\therefore a_{n}=3^n+n\times 3^n$

ถ้ามันมีหลายตัว
$r=2,3,3$
$a_{n}=a_{1}\times 2^n+a_{2}\times 3^n + a_{3} \times n \times 3^n$

# Divide-and-Conquer Algorithms

## Definition
1. **Divide**: แบ่งปัญหา → จำนวนของ input 
2. **Conquer**: แก้ปํญหาง่ายๆ
3. **Combine**: รวมคำตอบ

## Relations
1. size n into subproblems
2. size of each is n/b
3. $g(n)$ จำนวนที่ต้องทำ
4. $f(n)$ ทำกี่รอบได้ตามต้องการ

$$
f(n)=a\times f\left( \frac{n}{b} \right)+g(n)
$$

### Example: Binary Search != recursive binary search
Number of comparisons
$$
\begin{align}
f(n)  & \implies \text{Sorted array with n element} \\
 & = 1 \times f\left( \frac{n}{2} \right)+2
\end{align}
$$
## Fast Multiplication of Integers
$$
\begin{align}
a & =(a_{2n-1}a_{2n-2}\dots a_{1}a_{0})_{2} \\
b & =(b_{2n-1}b_{2n-2}\dots b_{1}b_{0})_{2}
\end{align}
$$
Let $a=2^n A_{1}+A_{0},b=2^nB_{1}+B_{2}$
shift bit ไปทางซ้าย
$$
ab=(2^{2n}+2^n)A_{1}B_{1}+2^n(A_{1}-A_{0})(B_{0}-B_{1})+(2^n+1)A_{0}B_{0}
$$
$$
\begin{align}
f(2n)=3f(n)+cn\to \text{จำนวนของการ บวก,ลบ,คูณ,shift}
\end{align}
$$

## Size of DC problems

### Theorem
$$
f(n)=af\left( \frac{n}{b} \right)+c
$$
Big-O
$$
f(n) \in \begin{array} \\
O(n^{\log_{b}a}) \\
O(\log n)
\end{array}
$$
## Complexity of Binary Search

$f(n)=af\left( \frac{n}{b} \right)+c$
binary search : $f(n)=f\left( \frac{n}{2} \right)+2$
$a=1$

$\therefore f(n) \in O(\log(n))$

## Master theorem

$$
f(n)=af\left( \frac{n}{b} \right)+cn^d
$$
$$
f(n)=
\begin{array}{lcl}
O(n^d)  & \text{if } a<b^d \\
O(n^d\log n)  & \text{if } a=b^d  \\
O(n^{\log_{b}a})  & \text{if } a>b^d \\
\end{array}
$$
### Example
Big-O of Fast Integer Multiplication

$f(n)=3f\left( \frac{n}{2}+cn \right)$
$a=3,b=2,d=1 \to a>b^d$
$$
\begin{align}
f(n)  & \in O(n^{\log_{b}^a}) \\
 &=  O(n^{\log_{2}3})
\end{align}
$$
