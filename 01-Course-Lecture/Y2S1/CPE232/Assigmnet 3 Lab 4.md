---
cssclasses:
  - center-images
  - center-titles
  - image-borders
date: 2024-09-24
---

# Assigmnet 3 Lab 4

# 1. 

![[Pasted image 20250902141116.png]]

Even parity bit
$$
\begin{align}
F_{e} & =(A\oplus B)\oplus(C\oplus D)
\end{align}
$$

Odd parity bit
$$
F_{0}=[(A\oplus B)\oplus(C\oplus D)]\oplus 1
$$

# 2.
![[Pasted image 20250902141456.png]]

$$ \begin{array}{c|c|c|c}  \begin{array}{c} F_1 = xz + \overline{x}\overline{y}\overline{z} \\ \begin{array}{cc} \downarrow & \downarrow \\ 101 \ \& \ 111 & 000 \end{array} \end{array} & \longrightarrow F_1(0, 5, 7) & \begin{array}{cc} 000 & m_0 \\ 101 & m_5 \\ 111 & m_7 \end{array} & \begin{array}{c} 9\ (2Y0) \\ 6\ (1Y1) \\ 4\ (1Y3) \end{array} \\[3em] \begin{array}{c} F_2 = \overline{x}y + x\overline{y}\overline{z} \\ \begin{array}{cc} \downarrow & \downarrow \\ 010 \ \& \ 011 & 100 \end{array} \end{array} & \longrightarrow F_2(2, 3, 4) & \begin{array}{cc} 010 & m_2 \\ 011 & m_3 \\ 100 & m_4 \end{array} & \begin{array}{c} 11\ (1Y2) \\ 12\ (2Y3) \\ 7\ (1Y0) \end{array} \\[3em] \begin{array}{c} F_3 = xy + \overline{x}\overline{y}z \\ \begin{array}{cc} \downarrow & \downarrow \\ 110 \ \& \ 111 & 001 \end{array} \end{array} & \longrightarrow F_3(1, 6, 7) & \begin{array}{cc} 001 & m_1 \\ 110 & m_6 \\ 111 & m_7 \end{array} & \begin{array}{c} 10\ (2Y1) \\ 5\ (1Y2) \\ 4\ (1Y3) \end{array} \end{array} $$

# 3.
![[Pasted image 20250902141526.png]]

$$
\begin{array}{ccc}
\begin{array}{|c|c|c|c|}
\hline
\text{D} & \text{C} & \text{B} & \text{A} \\
\hline
0 & 0 & 0 & 0 \\
\hline
0 & 0 & 0 & 1 \\
\hline
0 & 0 & 1 & 0 \\
\hline
0 & 0 & 1 & 1 \\
\hline
0 & 1 & 0 & 0 \\
\hline
0 & 1 & 0 & 1 \\
\hline
0 & 1 & 1 & 0 \\
\hline
0 & 1 & 1 & 1 \\
\hline
1 & 0 & 0 & 0 \\
\hline
1 & 0 & 0 & 1 \\
\hline
1 & 0 & 1 & 0 \\
\hline
1 & 0 & 1 & 1 \\
\hline
1 & 1 & 0 & 0 \\
\hline
1 & 1 & 0 & 1 \\
\hline
1 & 1 & 1 & 0 \\
\hline
1 & 1 & 1 & 1 \\
\hline
\end{array}
&
\longrightarrow
&
\begin{array}{|c|c|c|c|}
\hline
\text{Z} & \text{Y} & \text{X} & \text{W} \\
\hline
0 & 0 & 0 & 0 \\
\hline
0 & 0 & 0 & 1 \\
\hline
0 & 0 & 1 & 0 \\
\hline
0 & 0 & 1 & 1 \\
\hline
0 & 1 & 0 & 0 \\
\hline
1 & 0 & 0 & 0 \\
\hline
1 & 0 & 0 & 1 \\
\hline
1 & 0 & 1 & 0 \\
\hline
1 & 0 & 0 & 1 \\
\hline
1 & 1 & 0 & 0 \\
\hline
1 & 0 & 1 & 0 \\
\hline
1 & 0 & 1 & 1 \\
\hline
1 & 1 & 0 & 0 \\
\hline
1 & 1 & 0 & 1 \\
\hline
1 & 1 & 1 & 0 \\
\hline
1 & 1 & 1 & 1 \\
\hline
\end{array}
\end{array}
$$

ไม่มี case ที่ input เป็น 1010 ขึ้นไป $|0101|0 \to |1000|0$

boolean function ของการบวก 3 สำหรับ binary ที่มีค่า > 4

$$
\begin{align}
\begin{array}{c}
\begin{array}{c|cccc}
\text{DC\BA} & 00 & 01 & 11 & 10 \\
\hline
00 & 0 & 1 & 1 & 0 \\
01 & 0 & 0 & 0 & 1 \\
11 & \times & \times & \times & \times \\
10 & 1 & 0 & \times & \times
\end{array} \\
\text{W}
\end{array} \\
W=D \overline{A}+CB \overline{A}+ \overline{DC}A
\end{align}
$$

$$
\begin{align}
\begin{array}{c} \begin{array}{c|cccc} \text{DC\BA} & 00 & 01 & 11 & 10 \\ \hline 00 & 0 & 0 & 1 & 1 \\ 01 & 0 & 0 & 1 & 0 \\ 11 & \times & \times & \times & \times \\ 10 & 1 & 0 & \times & \times \end{array} \\ \text{X} \end{array} \\
X=D \overline{A}+ \overline{CB}+BA
\end{align}
$$

$$
\begin{align}
\begin{array}{c} \begin{array}{c|cccc} \text{DC\BA} & 00 & 01 & 11 & 10 \\ \hline 00 & 0 & 0 & 0 & 0 \\ 01 & 1 & 0 & 0 & 0 \\ 11 & \times & \times & \times & \times \\ 10 & 0 & 1 & \times & \times \end{array} \\ \text{Y} \end{array} \\
Y=DA+C \overline{BA}
\end{align}
$$

$$
\begin{align}
\begin{array}{c} \begin{array}{c|cccc} \text{DC\BA} & 00 & 01 & 11 & 10 \\ \hline 00 & 0 & 0 & 0 & 0 \\ 01 & 0 & 1 & 1 & 1 \\ 11 & \times & \times & \times & \times \\ 10 & 1 & 1 & \times & \times \end{array} \\ \text{z} \end{array} \\
Z=D+CA+CB
\end{align}
$$
