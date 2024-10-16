---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2024-10-16

# How to solve multiple variable graphs

1. หา $f_{x}$ และ $f_{y}$
2. แก้ระบบสมการ $f_{x}=0$ $f_{y=0}$
3. หา $f_{xx}(x_{0},y_{0})=A$ $f_{xy}(x_{0},y_{0})=B$ $f_{yy}(x_{0},y_{0})=C$
4. $AC-B^2$

# Ex. 2

![[Pasted image 20241016090432.png]]

หาสูงสุด ต่ำสุด สัมภัทธ

- z คงที่ เป็นกราฟพาราโบรา
- x คงที่ เป็น พาราโบราหงาย
- y คงที่ เป็น ไฮเปอร์โบลา

แสดงให้เห็นว่าเป็น กราฟอ้านม้า

$$
\begin{align}
f(x,y) & = \frac{1}{2c}\left[ \frac{x^2}{a^2}+\frac{y^2}{b^2} \right]
\end{align}
$$
$$
\begin{align}
f_{x} & =0 \\
 & =\frac{2x}{2ca^2}
\end{align}
$$
$$
\begin{align}
f_{y} & =0 \\
 -\frac{2y}{2cb^2} & =0
\end{align}
$$
จะได้ว่าจุด $(0,0)$ คือจุดวิกฤต
$$
\begin{align}
A & =\frac{2}{2ca^2} \\
B & = 0 \\
C & =\frac{2}{2cb^2}
\end{align}
$$
$$
\begin{align}
 & AC-B^2 \\
 & =\left( \frac{2}{2ca^2} \right)\left( \frac{2}{2cb^2} \right)-C \\
 & =-\frac{1}{c^2b^2a^2}
\end{align}
$$
$\therefore (0,0) \text{ เป็นจุดอานม้า เนื่องจาก } AC-B^2<0$

