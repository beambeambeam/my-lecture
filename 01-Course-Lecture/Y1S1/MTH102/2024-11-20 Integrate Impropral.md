---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2024-11-20

# 2.3 Integrate 2nd form

function ที่ไม่ต่อเนื่องหรือไม่นิยาม

$$
\int^a_{b} f(x) \, dx = \lim_{ t \to a^+ } \int_{t}^b f(x) \, dx 
$$
หมายเหตุ
- ถ้าลิมิตหาค่าได้ $\lim_{ b \to a }f(x)dx$ ลู่เข้า
- ถ้าลิมิตหาค่าไม่ได้ $\lim_{ b \to a }f(x)dx$ ลู่ออก

$$
\begin{align}
\int_{c}^b f(x) \, dx & = \int_{c}^a f(x) \, dx + \int_{a}^b f(x) \, dx  \\
 & = \lim_{ t \to a^- }  \int_{c}^t f(x) \, dx + \lim_{ t \to a^+ }  \int_{t}^b f(x) \, dx 
\end{align}
$$
## Ex. 23

$$
f(x)=\frac{1}{1-x}
$$
พิจรณาจุดที่ทำให้ฟังก์ชั่นไม่ต่อเนื่อง เราจะพบว่า $1-x\neq 0$ ดั้งนั้น $x\neq 1$
$$
\begin{align}
\int_{1}^2 \frac{1}{1-x}dx & =\lim_{ t \to 1 } \int_{t}^2 \frac{1}{1-x}dx \\
 &=\lim_{ t \to 1 } -\int_{t}^2 \frac{1}{u}dt \\
 &=\lim_{ t \to 1 } \ln|u|\biggr|^{u=-1}_{u=1-t} \\
 & =-\lim_{ t \to 1^+ } (\ln|-1|-\ln|1-t|) \\
 & =\lim_{ t \to 1^+ } \ln|1-t| \\
 & = inf
\end{align}
$$
$\therefore$ ลู่ออก

### Ex.

$\int_{0}^{-3} \frac{1}{x+2} \, dx$
x=-2

$$
\begin{align}
\int_{-3}^{0} \frac{1}{x+2} \, dx & =\int_{-3}^{-2} \frac{1}{x+2} \, dx +\int_{-2}^{0} \frac{1}{x+2} \, dx \\
 & = \lim_{ t \to -2^- }  \int_{-3}^{t} \frac{1}{x+2} \, dx +\lim_{ t \to -2^+ }  \int_{t}^{0} \frac{1}{x+2} \, dx \\
 & = \lim_{ t \to -2^- } \ln|x+2| \biggr|^{x=t}_{x=-3}+ \lim_{ t \to -2^+ } \ln|x+2| \biggr|^{x=0}_{x=t} \\
 & = \lim_{ t \to -2^- } (\ln|t+2|-\ln|-3+2|) + \lim_{ t \to -2^+ } (\ln|0+2|-\ln|t+2|) \\
 & = \lim_{ t \to -2^- } (\ln|t+2|) + \lim_{ t \to -2^+ } (\ln|t+2|)+\ln 2 \\
\end{align}
$$
## Ex.

$$
\int^0_{-\inf} \frac{1}{x^3} \, dx 
$$
จุด x=0 เป็นจุดที่ทำให้ $f(x)=\frac{1}{x^3}$ ไม่มีความต่อเนื่อง

$$
\begin{align}
\int^0_{-\inf} \frac{1}{x^3} \, dx  & = \int^0_{-1} \frac{1}{x^3} \, dx + \int^{-1}_{-\inf} \frac{1}{x^3} \, dx  \\
 & = \lim_{ t \to 0 }  \int^t_{-1} \frac{1}{x^3} \, dx + \lim_{ s \to \infty } \int^{-1}_{s} \frac{1}{x^3} \, dx  \\
\end{align}
$$
$$
\begin{align}
\lim_{ s \to \infty } \int^{-1}_{s} \frac{1}{x^3} \, dx  & =\lim_{ s \to \infty } \int^{-1}_{s} \frac{1}{x^3} \, dx   \\
 & =\lim_{ s \to \infty } \frac{1}{-2x^2} \biggr|^{x=-1}_{x=s} \\
 & =\lim_{ s \to \infty }  \left( -\frac{1}{2}-\left( \frac{1}{-2s^2} \right) \right)  \\
 & = -\frac{1}{2}
\end{align}
$$
ลู่เข้า

$$
\begin{align}
\lim_{ t \to 0 }  \int^t_{-1} \frac{1}{x^3} \, dx & = \lim_{ t \to 0 }  -\frac{1}{2x^2}\biggr|_{x=-1}^{x=t} \\
 & = \lim_{ t \to 0 }  \left( \frac{1}{2t^2} - \frac{1}{2} \right) \\
 & =+inf
\end{align}
$$

## Ex.

$$
\int_{-inf}^{1} xe^x \, dx 
$$
$$
\begin{align}
\int xe^x dx  & = \int xe^x dx \\
 & =\int ue^u du \\
 & =
\end{align}
$$