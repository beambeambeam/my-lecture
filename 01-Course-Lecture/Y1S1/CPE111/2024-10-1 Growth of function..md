---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2024-10-01
# Growth of function

## Big O Notation

Big Notation: ใช้ Big-O หาขนาดของ operations หรือการ comparisons

$x: x^2,3x^2+25,4x^2+7x+10$ เหมือนกันเสมอๆใน order: $O(x^2)$

### Formal Definition
$f(x)$ is $O(g(x))$ ถ้ามี C และ k ที่ทำให้ $|f(x)|\leq C|g(x)|$ เมื่อ $x>k$

### Corollary
$f_{1}(x),f_{2}(x) \implies O(g(x))$ แล้ว $(f_{1}+f_{2})(x)$ คือ $O(g(x))$

### Theorem
$f_{1}(x)\text{ is } f_{2}(x) \implies O(g_{1}(x)) \text{ Then } (f_{1}f_{2})(x) \text{ is } O(g_{1}(x)g_{2}(x))$

### Example: Show that $3x^2+25$ is $O(x^2)$
$$
\begin{align}
3x^2+25 & = ? \\
x&=  5 \\
3(5)^2+25 & =100 \\
C(5)^2 & \geq 100 \\
25C & \geq 100 \\
C  & \geq 4
\end{align}
$$
$k = 5, C = 4$
let both be
$$
\begin{align}
|3x^2+25|\leq 4|x^2|,x>5
\end{align}
$$
### Other Approach
$$
\begin{align}
3x^2+25 & \leq 3x^2+25x^2 \text{ if } 0<x<1 \\
 3x^2+25  & \leq |28x^2|, x>1 \\ \\
|Cx^2| \\
C=28  & ,k=1
\end{align}
$$
ทำให้ทุกตัวเป็น highest degree ถ้า x>1


```functionplot
---
title: Compare both
xLabel: x
yLabel: y
bounds: [0,2,0,30]
disableZoom: true
grid: true
---
f(x)=28x^2
y=3x^2+25
```

ถ้า polynomial of degree ของ n $p(x)=a_{n}x^n+a_{n-1}x^{n-1}+\dots+a_{1}x+a_{0}$ เป็น $O(x^n)$

### Example: $4x^3+7x^2+12$ is $O(x^3)$ หา C และ k
$$
\begin{align}
4x^3+7x^2+12  & \leq 4x^3+7x^3+12x^3,x>1 \\
|4x^3+7x^2+12| & \leq |23x^3|,x>1 \\
 C=23 & ,k=1
\end{align}
$$

### Example: $x^3+5x$ ไม่ใช่ $O(x^2)$

$$
\begin{align}
|x^3+5x| \leq & C|x^2|,x>k \\
x^3+5x, & Cx^2, C=x \\
x^3+5x  & > \frac{x*x^2}{x^3}
\end{align}
$$
หาผั่ง $C|x^2|$ ให้ใหญ่กว่าอีกฝั่งให้ได้

### list ลำดับขนาด

| order | form         |
| ----- | ------------ |
| most  | $n^n$        |
|       | $n!$         |
|       | $c^n$        |
|       | $n^c$        |
|       | $n\log n$    |
|       | $n$          |
|       | $\sqrt{ n }$ |
|       | $\log n$     |
|       | c            |

![[Screenshot 2567-10-01 at 22.10.12.png]]

### Example: พิสูจน์ $2n+3 \text{ not } O(1)$

ถ้า $2n+3$ is $O(1)$ แล้ว
มีจำนวนเต็ม $C$ และ $k$ ที่ทำให้ $2k+3 \leq c*1$ เมื่อ $n\geq n_{0}$

### Example: $f(x)=(x+1)\log(x^2+1)+3x^2.$

$$
\begin{align}
(x+1)\log(x^2+1)+3x^2 & \leq (x+1)\log(x^2+1)+3x^2 \\
 & \leq (2x^2)\log(x^2)+3x^2 \\
 & \leq (x^2)\log(x^2)+3x^2 \\
 & \leq 2(x^2)\log(x)+3x^2 \\
 & \leq (2\log(x)+3)x^2 \\
C=2\log(x)+3,k=1
\end{align}
$$



```functionplot
---
title: Compare both
xLabel: x
yLabel: y
bounds: [0,2,0,2]
disableZoom: true
grid: true
---
y=x^2
y=(2log(x)+3)x^2
```


## Time Complexity Calculations

### คอมคำนวน $10^{12}$ bit operations per second. หา largest problem

$$
\begin{align} \\
& n^4 \\
(n^4)^{1/4} & =(10^{12})^{1/4} \\
n & =10^{3}
\end{align}
$$
$$
\begin{align}
&2^n \\
2^n  & = 10^{12} \\
\log 2^n  & = \log 10^{12} \\
n  & = \frac{12}{\log 2} \\
 & \approx 39.8
\end{align}
$$
### $10^{12}$ โดย $n^3+\log n$
n=1000,$n=10^8$

$$
\begin{align}
f(x) & =n^3+\log n \\
 & = 1000^3+\log 1000 \\
 & = 10^9 * \frac{1}{10^{12}}  & = \frac{1}{10^3}s \\
 &  & =\frac{1}{1000}s
\end{align}
$$



