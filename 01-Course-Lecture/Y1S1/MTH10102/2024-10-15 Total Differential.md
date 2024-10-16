---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2024-10-15

# Total Differential

## Ex.
$$
f(x,y)=f_{x}dx+f_{y}dy=\sin y+x\ln y
$$
$$
\begin{align}
df & =f_{x}dx+f_{y}dy \\
 & =[0+\ln y]dx+\left[ \cos y+\frac{x}{y} \right]d
y\end{align}
$$

## Ex.

$$
\begin{align}
df & =f_{x}dx+f_{y}dy \\
 & =[y+2x]dx+[x+2y]dy
\end{align}
$$


# Approx

$$
\begin{align}
f(x+\Delta x) & \approx f(x)+f'(x)dx \\
f(x+\Delta x, y+\Delta y) & \approx f_{x}dx+f_{y}dy
\end{align}
$$

## Ex.
$\sqrt{ (3.01)^2+(3.99)^2 }$

พิจรณา
$x=3,y=4,dx=0.01,dy=-0.01$

แทนค่า
$$
\begin{align}
f(3.01,3.99) & \approx \sqrt{ 3^2+4^2 }+\frac{3}{\sqrt{ 3^2+4^2 }}(0.01){+\frac{4}{\sqrt{ 3^2+4^2 }}}(-0.01) \\
 & ช
\end{align}
$$

## Ex. 
$h=9, dh=-0.11, r=3,dr=0.15$
$$
\begin{align}
V & =\frac{1}{3}\pi r^2h \\
dV & = V_{r}dr+V_{h}dh \\
 & = \frac{1}{3}\pi r^2hdr+\frac{1}{3} \pi r^2hdh \\
\end{align}
$$

# Maximum and minimum

## นิยาม
- จุดวิกฤต : $f_{x}(x,y)=f_{y}(x,y)=0$
- จุดวิกฤตจะเป็นจุดบ่งบอกว่าจุดไหนจะเป็นสูงสุด ต่ำสุด

## Ex. 
$$
\begin{align}
f(x,y) & =x^2+y^2 \\
f_{x}(x,y)=2x & ,f_{y}(x,y)=2y \\
0=2x & ,0=2y \\
\therefore critical & =(0,0)
\end{align}
$$

*** ถ้า กำลัง diff ในส่วนของ x ถ้า y อยู่เดียวๆให้แปลงเป็น 0 แต่ถ้าอยู่กับ x ให้มองเป็นค่าคงที่