---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2024-09-24
CB2607


Locate the intervals of x where each function’s graph is

concave up and where it is concave down. Identify the inflection

points and calculate relative extreme values.

1. $f(x) = x^4-4x^3+8x-2$

$$ 

\begin{aligned}
f(x) &= x^4-4x^3+8x-2 \\
f(x)' &= 4x^3 -12x^2+8-4[4x] = 4[x^3-3x^2+2 -4(x-1)(x^2-2x-2)]\\
f(x)'' &=12x^2-24x = 12x[x-2]
\end{aligned}
$$

$$
\begin{aligned}
x &= \frac{2+\sqrt{ 12 }}{2} \\
x &= \frac{2+\sqrt{ 3 }}{2} \\
&=1\pm \sqrt{ 3 }
\end{aligned}
$$

$x=2.732, -0.732$

| interval                  | $f(x)$ | $f'(x)$ | $f''(x)$ | explain                 |
| ------------------------- | :----: | ------- | -------- | ----------------------- |
| $(-\infty, 1-\sqrt{ 3 })$ |        | -       | +        | ฟังก์ชั่นลด โค้งงาย     |
| $x=1-\sqrt{ 3 }$          |  $-6$  |         |          | จุดต่ำสุดสัมพัมธ์       |
| $(1-\sqrt{ 3 }, 0)$       |        | +       | +        | ฟังก์ชั่นเพิ่ม โค้งงาย  |
| $x=0$                     |   -2   |         |          | จุดเปลี่ยนเว้า          |
| $(0, 1)$                  |        | +       | -        | ฟังก์ชั่นเพิ่ม โค้งคว่ำ |
| $x=1$                     |   3    |         |          | สูงสุดสัมพัมธ์          |
| $(1,2)$                   |        | -       | -        | ฟังก์ชั่นลด โค้งคว่ำ    |
| $x=2$                     |   -2   |         |          | จุดเปลี่ยนเว้า          |
| $(2, 1+\sqrt{ 3 })$       |        | -       | +        | ฟังก์ชั่นลด โค้งหงาย    |
| $x=1+\sqrt{ 3 }$          |  $-6$  |         |          | จุดต่ำสุดสัมพัมธ์       |
| $(1+\sqrt{ 3 },\infty)$   |        | -       | +        | ฟังก์ชั่นลด โค้งหงาย    |
|                           |        |         |          |                         |

```functionplot
---
title: 2024-09-25 1.
xLabel: x
yLabel: y
bounds: [-10,10,-10,10]
disableZoom: true
grid: true
---
y=x^4-4x^3+8x-2
```

2. $f(x)=\frac{2x^2-8}{x^2-16}$

$$
\begin{aligned}
f(x) &= \frac{2x^2-8}{x^2-16} \\
f'(x) &= -\frac{48x}{(x^2-16)^2} \\
f''(x) &= \frac{48\left(-3x^2-16\right)}{\left(x^2-16\right)^3}
\end{aligned}
$$


```functionplot
---
title: 2024-09-25 2.
xLabel: x
yLabel: y
bounds: [-10,10,-10,10]
disableZoom: true
grid: true
---
x=(2x^2-8)/(x^2-16)
```

จากสมการ $f'(x)$ ที่ $x=0$ เป็นจุดวิกฤต
จากสมการ $f''(x)$ ที่ $x=0$ เป็นจุดวิกฤต

$x$ when $y$ = 0
$$
\begin{aligned}
f(x)&=\frac{2x^2-8}{x^2-16}\\
\end{aligned}
$$
$x=2,x=-2$

$y$ when x = 0
$$
\begin{aligned}
y&=\frac{2(0)^2-8}{(0)^2-16}\\
y&=\frac{-8}{-16} \\
y&=\frac{1}{2}
\end{aligned}
$$
$y=\frac{1}{2}$

find เส้นกำกับแนวดิ่งของ $f(x)=\frac{2x^2-8}{x^2-16}$

$f(x)=\frac{2x^2-8}{x^2-16}$ when $x=4$ and $x=-4$
$$
\begin{aligned}
\lim_{ x \to 4^- } &= \frac{2x^2-8}{x^2-16} \\
&= -\infty \\
\lim_{ x \to 4^+ } &= \frac{2x^2-8}{x^2-16} \\
&= +\infty \\
\lim_{ x \to -4^- } &= \frac{2x^2-8}{x^2-16} \\
&= +\infty \\
\lim_{ x \to -4^+ } &= \frac{2x^2-8}{x^2-16} \\
&= -\infty \\
\end{aligned}
$$
then $x=4$ and $x=-4$

find เส้นกำกับแนวนอน
$$
\begin{aligned}
\lim_{ x \to \infty }\frac{2x^2-8}{x^2-16} &= \lim_{ x \to \infty }\frac{2x^2-8}{x^2-16} \\
&= \lim_{ x \to \infty } \frac{\frac{2x^2}{x^2}-\frac{8}{x^2}}{1-\frac{16}{x^2}} \\
&= 2 \\
\lim_{ x \to -\infty } &= \frac{2x^2-8}{x^2-16} \\
&= 2
\end{aligned}
$$

เส้นตรง $y=2$ เป็นเส้นกำกับแนวนอน

