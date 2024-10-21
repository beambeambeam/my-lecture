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


# Ex. 6

![[Pasted image 20241016093003.png]]

x = กว้าง
y = ยาว
z = สูง

$$
\begin{align}
12 & =xy+2xz+2yz \\
12-xy & =2xz+2yz \\
z & =\frac{12-xy}{2x+2y}
\end{align}
$$
$$
\begin{align}
V & =xyz \\
 & =xy[\frac{12-xy}{2x+2y}]
\end{align}
$$
จะได้ว่า $x>0,y>0$ และ $xy<12$

$$
\begin{align}
V & =\frac{12xy-x^2y^2}{2x+2y} \\ \\

V_{x}  & = \frac{(2x+2y)[12y-2xy^2]-(12xy-x^2y^2)[2]}{(2x+2y)^2} \\
 & =\frac{24xy-4x^2y^2+24y^2-4xy^3-24xy+2x^2y^2}{{(2x+2y)^2}} \\
 & =\frac{-2x^2y^2+24y^2-4xy^3}{(2x+2y)^2} \\
 & =\frac{-2y^2[x^2-12+2xy]}{(2x+2y)^2} \\ \\

V_{y} & = \frac{(2x+2y)[12x-2x^2y]-[12xy-x^2y^2][2]}{ \\
2x+2y}^2 \\
 & =\frac{24x^2-4x^3y+24xy-4x^2y^2-24xy+2x^2y^2}{(2x+2y)^2} \\
 & = \frac{24x^2-4x^3y-2x^2y^2}{(2x+2y)^2} \\
 & = \frac{2x^2[12-2xy-y^2]}{(2x+2y)^2}
\end{align}
$$

$$
\begin{align}
V_{x}= & 0 & =x^2-12+2xy \\
V_{y}= & 0 & =12-2xy-y^2
\end{align}
$$
$x=2,y=2$

$$
z=\frac{12-xy}{2x+2y}=\frac{8}{8}=1
$$
# ข้อสอบเก่า

## 3. particial derivetive
![[Pasted image 20241016100810.png]]

$$
\begin{align}
3y^2x^2+e^2 \\
6xy^2
\end{align}
$$

## 4.
![[Pasted image 20241016101135.png]]

$$
dz=-6y
$$
$\therefore$ ความชันมีค่าคือ -6

## 4.

![[Pasted image 20241016101829.png]]

$$
\begin{align}
\lim_{ (x,y) \to (0,0) } \frac{x^2+\arctan(y^2)}{x^2-3y^2} & = \frac{1}{3}
\end{align}
$$
มันไม่มีค่าเมื่อเข้าใกล่ 0,0
ก ค จ