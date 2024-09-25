# Induction
## concept overview
1. $n=k \to T$
2. Prove $n=k+1\to T$
3. for all $n\to T$

## Mathematical Induction
- เพื่อพิสูจน์ความเป็นจริงของ infinite sequence
- base case และ induction step
	- assume $prove \to next$.
- Application
	- Use in summation proofs.
	- Prove continue of Algorithms.

## Principle of Mathematical Induction:
ต้องการพิสูจน์ $P(n)$ เป็นจริงในทุกจำนวนจริง
- Basis Step: $P(1)$ เป็นจริง
	- ขึ้นอยู่กับค่าเริ่มต้นของ $P(n)$ 
- Inductive Step: แสดงให้เห็ยว่า $P(k) \to P(k+1)$ เป็นจริงในทุกๆจำนวนจริง

$$
\begin{aligned}
(P(1)\lor \forall k(P(k)\to P(k+1))) \to \forall nP(n)
\end{aligned}
$$
ถ้า $P(k)$ เป็นจริง บังคับ $P(k)$ เป็นจริง แล้วจะพิสูจน์ได้ว่า $P(k+1)$

## ปืนบันได

- Basis Step: เราปืนได้ 1 ชั้น
- Inductive Step: ถ้าเราไปขั้น k ได้แล้วจะไปขั้น $k+1$ ได้

## โดมิโน
- Basis step: ตัวที่ 1 ล้มได้ $P(1)\to T$
- Inudctive Step: เรารู้ว่าถ้าโดมิโนที่ $k$ ล้มแล้วจะทำให้ $k+1$ ล้มไป้เรื่อยๆ

## Example: show that $\sum^n_{i=1} = \frac{n(n+1)}{2}$

ให้ $P(n)$ คือ $\sum^n_{i=1} = \frac{n(n+1)}{2}$
Basis step: $P(1)$; แทนค่า 1 เข้าไปใน n
$$
\begin{aligned}
\sum^n_{i=1} &= \frac{n(n+1)}{2}\\
\sum^1_{i=1} &= \frac{1(1+1)}{2} \\
&= 1
\end{aligned}
$$
เป็นจริง

Inductive step: กำหนดให้ $P(k)$ เป็นจริงจะได้
$$
\begin{aligned}
1+2+3+\dots+k &= \frac{k(k+1)}{2},k \in z^+
\end{aligned}
$$
Goal : $\frac{(k+1)(k+2)}{2}$ (RHS)
$$
\begin{aligned}
1+2+3+\dots+k+(k+1) &= P(k)+(k+1)\\
&=\frac{k(k+1)}{2}+(k+1)\\
&= \frac{k(k+1)}{2}+\frac{2(k+1)}{2} \\
&= \frac{k(k+1)+2(k+1)}{2} \\
\end{aligned}
$$

## Example: คาดเดา และ พิสูจน์ ผลบวกของจำนวนคี่
Conjecture

$$
\begin{aligned}
n=1&;1=1 \\
n=2&;1+3=4 \\
n=3&;1+3+5=9 \\
n=4&;1+3+5+7 \\
\end{aligned}
$$
$$
\begin{aligned}
1+3+5+\dots+(2n-1)&=n^2\\
Odd&\to 2n-1,2n+1\\
Even&\to 2n
\end{aligned}
$$

กำหนดให้ $P(n)$ คือ

$$
\begin{aligned}
1+3+5+\dots+(2n-1)&=n^2, n\in z^+
\end{aligned}
$$

Basis step: $P(1); 1=1^2$ เป็นจริง
Inductive step; กำหนดให้ $P(k)$ เป็นจริง จะได้ว่า

$$
\begin{aligned}
1+3+5+\dots+(2k-1) &= k^2,k \in z^+
\end{aligned}
$$

พิสูจน์ $P(k+1)$;
goal: $(k+1)^2$ RHS

$$
\begin{aligned}
1+3+5+\dots(2k-1)+2(k+1) &= k^2+(2k+1) \\
&= (k+1)^2
\end{aligned}
$$

## Example: พิสูจน์ $n<2^n$ สำหรับทุกจำนวนเต็มบวก
กำหนดให้ $n<2^n$,$n\in z^+$

Basis step: $P(1);1<2^1$
Inductive step: กำหนด $P(k)$ เป็นจริง จะได้ $k<2^k$,$k \in z^+$

พิสูจน์ $P(k+1)$ $k+1 < ?$
Goal: $k+1<2^{k+1}$

$$
\begin{aligned}
P(k+1);k+1&<2^k+1 &,P(k)\\
&<2^k+2^k&,1<2^k \\
&=2*2^k\\
&=2^{k+1}
\end{aligned}
$$

$\therefore$ $P(k)$ เป็นจริง จะได้ $k<2^k$,$k \in z^+$

## Example: พิสูจน์ $2^n < n!$ ในทุกจำนวนจริงที่ $n\geq 4$
Basis step: $P(4);$ $2^4=16<4! =24$
Inductive step: กำหนดให้ $P(k)$ เป็นจริง $2^k<k!$, $k \in z$, $k \geq 4$

พิสูจน์ $P(k+1); 2^{k+1}=?$
Goal: $2^k<(k+1)!$

$$
\begin{aligned}
2^{k+1}&=2*2^k\\
&=2*k! &,P(k) \\
&=(k+1)*k! &,2<k+1 \\
&=(k+1)! &True
\end{aligned}
$$
$$
\begin{aligned}
(k+1)! = (k+1)*k!
\end{aligned}
$$
$\therefore$ $P(n)$ เป็นจริง, $n\in z$, $n\geq 4$

## Example: พิิสูจน์ $n^3-n$ หาร 3 ลงตัวในจำนวนจริงบวก
ให้ $P(n)$ คือ $3|(n^3-3)$, $n\in z^+$

Basis step: $P(1)$; $3|(1^3-1) \to_{3}|0$ เป็นจริง
Inductive step: กำหนดให้ $P(k)$ เป็นจริงจะได้ $3|(k^3-k)$
หรือ $k^3-k=3m$, $m\in z^+$

พิสูจน์ $P(k+1)$; $(k+1)^3-(k+1)$
Goal: $(k+1)^3-(k+1)=3 \square$ ดึงตัวร่วม 3 ออกมาให้ได้ $\in z^+$

$$
\begin{align}
(k+1)^3-(k+1)&=(k^3+3k^2+1)-(k+1) \\
&= (k^3-k) + 3k^2+3k \\
&= 3m+3k^2+3k &,\therefore P(k) \\
&= 3(m+k^2+k) &True
\end{align}
$$
$\therefore P(n)$ เป็นจริง, $n\in z^+$

# Recursion
ทำวนซ้ำกับตัวเองไปเรื่อยๆ
โปรแกรมมื่งได้ 2 ประเถท
1. Iteration (for, while) → Bottom up
2. Recursion → Top down

## Definition
- Basis step → function at zero → stop criteria
- Recursive step → rule to find smaller integers.

## Example; Suppose that f is defined recursively by
$$
\begin{align}
f(0) &= 3. \\
f(n+1)&=2f(n)+3
\end{align}
$$
find $f(1)$, $f(2)$, $f(3)$. และ $f(4)$
$$
\begin{align}
f(1)&=2f(0)+3 =9 \\
f(2)&=2f(1)+3=21 \\
f(3)&=2f(2)+3=45 \\
f(4)&=2f(3)+3=93 \\
\end{align}
$$
$$
\begin{align}
f(2)&=2f(1)+3 \\
&=2[2f(0)+3]+3 \\
&=2[2(3)+3]+3 \\
&=21
\end{align}
$$

## Example n! in recursive
Basis step; $f(0)=1$

$$
\begin{align}
f(0)&=1 \\
f(1)&=f(0) \\
f(2)&=f(1)*2 \\
f(3)&=f(2)*3 \\
f(n)&=f(n-1)*n &,n\in z, n\geq 0\\
f(n+1)&=n+1*f(n) &,n\in z, n\geq 0
\end{align}
$$

## Example $\sum_{k=0}^na_{k}$
basis step: $\sum_{k=0}^na_{k}=a_{0}$
Recursive step:

$$
\begin{align}
\sum_{k=0}^{n+1}a_{k} &= (\sum_{k=0}^na_{k})+a_{n+1}
\end{align}
$$

ทั้ง 2 ข้อคือ
$f(n+1)$ กับ $f(n)$

## Overview
### Definition
1. Basis step: ให้ เบส case
2. Recursive Step: ให้กฏในการลูป
3. Exclusion step: ให้กฏแยก

### Example: Subset of Integers $S$
- Basis Step: $3 \in S$
- Recursive Step: if $x \in S$ and $y \in S$, then $x+y$ is in $S$
$$
\begin{align}
1)& 3\in S \wedge 3 \in S \to 3+3=6 \in S &: S=&\{ 3,6 \} \\
2)& 3\in S \wedge 3 \in S \to 3+6=9 \in S &: S=&\{ 3,6,9,12 \}  \\
\end{align}
$$

### Example: The natural numbers $N$
-Basis step 0

## Strings
### Definition
เซ็ต $\sum^c$ ของ strings ใน alphabet $\sum$:
- Basis Step: $\lambda \in \sum^*$
- Recursive Step: if $w$ is in $\sum^*$ and $x$ อยู่ใน $\sum$, แล้ว $wx \in \sum^*$

### Example: ถ้า $\sum$ = $\{ 0,1 \}$
$$
\begin{align}
\lambda \in \sum^* \wedge 0 \in \sum &\to 0 \\
\lambda \in \sum^* \wedge 1 \in \sum &\to 1 \\
\lambda \in \sum^* \wedge 0 \in \sum &\to 00 \\
\lambda \in \sum^* \wedge 0 \in \sum &\to 01
\end{align}
$$
$\sum^*$=$\{ \lambda,0,1,00,01,10,\dots \}$

### Example: ถ้า $\sum$ = $\{ a,b \}$ แสดงให้เห็นว่า $aab \in \sum^*$
$$
\begin{align}
\lambda \in \sum^* \wedge a \in \sum &\to a \\
\lambda \in \sum^* \wedge b \in \sum &\to b \\
\lambda \in \sum^* \wedge a \in \sum &\to aa \\
\lambda \in \sum^* \wedge b \in \sum &\to aab
\end{align}
$$

## String Concat ต่อสริง
$w_{1} * w_{2}$ เขียนในรูป $w_{1}w_{2}$

## Length of string
### Example: ให้ $l(w)$, หาความยาวของ สตริง
Basis step: $l(m)=0$ “”
$$
\begin{align}
"\text{ }" \to l(w) &=0 \\
"\text{a}" \to l(w) &=1 \\
\end{align}
$$
Recursive Step:
$$
l(wx)=l(w)+1
$$
$w \in \sum^* \wedge x \in \sum \to l(wx) = l(w)+1$
$l(wx)$ เป็น $f(x+1)$ และ $l(wx)$ เป็น $f(x)$

# Recursive Algorithms
## Definitions
- ลดขนาดของปัญหาลง
	- smaller input
	- ต้องมี base case

Example: $n!$ เมื่อ $n \in z^+$
formula $a^n=a*a^{n-1}$

## Example: GCD
basis step: if $a=0$ then return $b$ else return
gcd(b$||$a, a)
recursive step: gcd(b mod a, a) 

## Linear search
basis step: if a[i]=x return i else if i=k then return 0

recursive step: search(i+1, j, x)