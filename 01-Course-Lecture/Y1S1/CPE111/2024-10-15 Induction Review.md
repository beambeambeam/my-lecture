---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2024-10-15

n = k+1 ในการหา RHS

# 1.

$$
1+5+5^2+5^3+\dots+5^n=\frac{5^{n+1}-1}{4},n\geq 0
$$

1. กำหนด P(n)
$$
P(n)=1+5+5^2+5^3+\dots+5^n=\frac{5^{n+1}-1}{4},n\geq 0
$$
2. Basis step
$$
P(0)=\frac{5^{0+1}-1}{4}=\frac{4}{4}=1
$$
3. กำหนด $P(k)$
กำหนดให้ $P(k)$ เป็นจริงเมื่อ
$$
P(k)=1+5+5^2+5^3+\dots+5^k=\frac{5^{k+1}-1}{4},k\geq 0
$$
4. พิสูจน์ $P(k+1)$
RHS เป็น
$$
\frac{5^{(k+1)+1}-1}{4}
$$
$$
\begin{align}
1+5+5^2+5^3+\dots+5^k+5^{k+1} & =\frac{5^{k+1}-1}{4}+5^{k+1},k\geq 0 \\
 & = \frac{{5^{k+1}-1+4(5)^{k+1}}}{4} \\
 & =\frac{5^{k+1}(4+1)-1}{4} \\
 & =\frac{5^{k+2}-1}{4}
\end{align}
$$
5. สรุป
$$
\therefore P(n)\text{เป็นจริงเมื่อ},n\geq0
$$

# 2.

1. กำหนด P(n)
$$
\left( 1-\frac{1}{2^2} \right)\left( 1-\frac{1}{3^2} \right)\left( 1-\frac{1}{4^2} \right)\dots\left( 1-\frac{1}{n^2} \right)=\frac{n+1}{2n},n\geq 2
$$
2. Basis step
$$
P(2)=\frac{2+1}{2(2)}=\frac{3}{4},n\geq 2 \text{เป็นจริง}
$$
3. P(k)
$$
\left( 1-\frac{1}{2^2} \right)\left( 1-\frac{1}{3^2} \right)\left( 1-\frac{1}{4^2} \right)\dots\left( 1-\frac{1}{k^2} \right)=\frac{k+1}{2k},k\geq 2
$$
4. พิสูจน์ P(k+1)
RHS:
$$
\frac{k+2}{2(k+1)}
$$
$$
\begin{align}
\left( 1-\frac{1}{2^2} \right)\left( 1-\frac{1}{3^2} \right)\left( 1-\frac{1}{4^2} \right)\dots\left( 1-\frac{1}{k^2} \right)\left( 1-\frac{1}{(k+1)^2} \right) & =\left( \frac{k+1}{2k} \right)\left( 1-\frac{1}{(k+1)^2} \right),k\geq 2 \\
 & = \left( \frac{k+1}{2k} \right)\left( \frac{(k+1)^2-1}{(k+1)^2} \right) \\
& = \left( \frac{1}{2k} \right)\left( \frac{(k+1)^2-1}{k+1} \right) \\
 & = \left( \frac{(k+1)^2-1}{2k^2+2k} \right)  \\
& = \left( \frac{(k+1)^2-1}{2k^2+2k} \right)  \\
 & =\frac{k^2+2k}{2k^2+2k} \\
 & =\frac{k(k+2)}{2k(k+1)} \\
 & =\frac{(k+2)}{2(k+1)}
\end{align}
$$
5. สรุป k เป็นจริงเมื่อ $k\geq2$

# 3.

$$\sum_{i=1}^{n} \frac{1}{\sqrt{ i }} >\sqrt{ n },n\geq 2$$
1. กำหนดให้ P(n)
$$\sum_{i=1}^{n} \frac{1}{\sqrt{ i }} >\sqrt{ n },n\geq 2$$
2. Basis step
$$
\begin{align}
\frac{1}{\sqrt{ 1 }} + \frac{1}{\sqrt{ 2 }} & >\sqrt{ 2 } \\
1 &> \frac{1}{\sqrt{ 2 }}
\end{align}
$$
3. P(k)
$$\frac{1}{\sqrt{ 1 }}+\frac{1}{\sqrt{ 2 }}+\frac{1}{\sqrt{ 3 }}+\dots+\frac{1}{\sqrt{ k }}>\sqrt{ k },k\geq 2$$
4. P(k+1)
RHS:
$$
\sqrt{ k+1 }
$$
$$\begin{align}
\frac{1}{\sqrt{ 1 }}+\frac{1}{\sqrt{ 2 }}+\frac{1}{\sqrt{ 3 }}+\dots+\frac{1}{\sqrt{ k }}+\frac{1}{\sqrt{ k+1 }} & >\sqrt{ k } +\frac{1}{\sqrt{ k+1 }},k\geq 2 \\
 & =\frac{\sqrt{ k }\sqrt{ k+1 }+1}{\sqrt{ k+1 }} \\
 & =\frac{\sqrt{ k^2+k }+1}{\sqrt{ k+1 }} \\
\
 & > \frac{k+1}{\sqrt{ k+1 }}, \because  \sqrt{ k^2+k } > k, k\geq 2 \\
 & >\sqrt{ k+1 }
\end{align}$$

5. P(n)เป็นจริงเมื่อ $n\geq2$

# 5.

$$
\begin{align}
21|4^{n+1} & +5^{2n-1}, n\in Z^+ \\
4^{n+1}+5^{2n-1}  & = 21m, n\in Z^+,m\in Z^+
\end{align}
$$
1. P(n)
$$
21|4^{n+1} +5^{2n-1}, n\in Z^+ \\
$$
2. Basis Step
$$
\begin{align}
21|4^{0+1} & +5^{2(0)-1}, n\in Z^+ \\
21| & 21, n\in Z^+
\end{align}
$$
3. P(k)
$$
\begin{align}
21|4^{k+1} & +5^{2k-1}, k\in Z^+ \\
4^{k+1}+5^{2k-1}  & = 21m, k\in Z^+,m\in Z^+ \\
4^{k+1}  & = 21m+5^{2k-1},
\end{align}
$$
4. P(k+1)
RHS หา 24($\Box$)
แทน k+1 ลงใน n
$$
\begin{align}
 & = 4^{k+1}+5^{2(k+1)-1} \\
 & =4(4^{k+1})+5^{2k+1} \\
 & =4(21m-5^{2k-1})+25+5^{2k-1} \\
 & =4\times 21m-4\times 5^{2k-1} + 25+5^{2k-1} \\
 & =4\times 21m+21\times 5^{2k-1} \\
 & =21(4m+5^{2k-1})
\end{align}
$$
5. สรูป

$$
\therefore \text{P(n) เป็นจริง;}n\in Z^{+}
$$
