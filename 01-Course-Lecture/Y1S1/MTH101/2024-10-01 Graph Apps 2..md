---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2024-10-01

### Example. เขียนกราฟจากเงื่อนไขต่อไปนี้
1. $f$ vertical asymptote at $x=4$
2. $\lim_{ n \to \infty } f(x)=1$
3. $f(0)=2$
4. $f(5)=2$
5. $(0,2)$ จุดเปลี่ยนเว้าาา
6. $f$ diff ได้ในช่วง $(-\infty,4)$ and $(4, \infty)$
7. $f''(x)<0$ for $0<x<4$
8. $f'(2)=0$
9. $f'(2)=0$
10. $f''(x)>0$ for $x<0$
11. For all $x>4$ ลดลงและหงาย

![[Screenshot 2567-10-01 at 08.51.34.png]]

### Example วาดกราฟ $f$ จาก
1. $f$ เป็น $f(x)$ คู่
2. $f(0)=1$
3. $f(4)=0$
4. $f'(x)=2$ $(0,2)$
5. $f'(x)<0$ $x>2$
6. $f''(x)<0$ $x<-2$
7. $\lim_{ n \to \infty }f(x)=-1$

![[JPEG image-44B3-B9DC-CE-0.jpeg]]

### Example $f(x)=\frac{3x^2-6}{x^2-x-12}$ หา
1. Vertical Asymptote(s) of $f(x)$
2. Horizon too

$$
\begin{align}
x^2-x-12&=0 \\
(x-4)(x-3)&=0 \\
x&=4,x=3
\end{align}
$$
$$
\begin{align}
\lim_{ x \to -4^- } \frac{3x^2-6x}{x^2-x-12} &= \frac{3x^2-6x}{x^2-x-12} \\
&= -\infty \\
\lim_{ x \to -4^+ } \frac{3x^2-6x}{x^2-x-12} &= \frac{3x^2-6x}{x^2-x-12} \\
&=\infty \\
\lim_{ x \to 3^- } \frac{3x^2-6x}{x^2-x-12} &= \frac{3x^2-6x}{x^2-x-12} \\
&= \infty \\
\lim_{ x \to 3^+ } \frac{3x^2-6x}{x^2-x-12} &= \frac{3x^2-6x}{x^2-x-12} \\
&=-\infty
\end{align}
$$
$\text{horizon}=$
$$
\begin{align}
\lim_{ x \to \infty } \frac{3x^2-6x}{x^2-x-12}=3
\end{align}
$$
### Example $f(x)=\arctan x$
$$
\begin{align}
\lim_{ x \to \infty } \arctan x&=\frac{\pi}{2} \\
\lim_{ x \to \infty } \arctan x&=-\frac{\pi}{2}
\end{align}
$$
### Example $g(x)=\frac{|x|}{1+x}$
$$
\begin{align}
\lim_{ x \to +\infty } \frac{|x|}{1+x}&=\frac{|x|}{1+x} \\
&=\frac{x}{1+x} \\
&=\frac{\frac{x}{x}}{\frac{1}{x}+\frac{x}{x}} \\
&=\frac{1}{0+1} \\
&=1
\end{align}
$$

$$
\begin{align}
\lim_{ x \to -\infty } \frac{|x|}{1+x}&=\frac{|x|}{1+x} \\
&=\frac{-x}{1+x} \\
&= -1
\end{align}
$$
### Example
![[Screenshot 2567-10-01 at 09.43.20.png]]
$$
\begin{align}
\therefore V&=x(12-2x)^2 \\
V'&=12x^2-96x+144 \\
V' &= 2,V'=6
\end{align}
$$
$$
\begin{align}
V'' &  =24x-96+144 \\
 &  =0-96 \\
 & =-96
\end{align}
$$
### Example

```functionplot
---
title: parabola
xLabel: x
yLabel: y
bounds: [-10,10,-10,10]
disableZoom: true
grid: true
---
y=x^2
y=4
y=2
```
$$
\begin{align}
\therefore A & =2xy=2x(4-x^2)=8x-2x^3 \\
 \frac{d}{dA}  &  =8-6x^2 \\
 & x=\frac{2}{\sqrt{ 3 }} \\
\frac{d^2}{d^2A}] & =-12x<0,x=\frac{2}{\sqrt{ 3 }} \\
2x & =2\left( \frac{4}{\sqrt{ 3 }} \right) \\
x & =\frac{4\sqrt{ 3 }}{3} \\
y & =\frac{8}{3}
\end{align}
$$

