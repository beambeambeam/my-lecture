---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2024-10-30

# Limit integrate

$$
\begin{align}
 & \int_{a}^bCdx=C(x)|^b_{a}=C(b-a) \\
 & \int_{a}^bCdx=C\int_{a}^bf(x)dx \\
 & \int_{a}^bf(x)dx = -\int_{b}^{a}f(x)dx \\
 & \int_{a}^b[f(x)\pm g(x)]dx=\int_{a}^bf(x)\pm \int_{a}^bg(x)dx \\
* & \int_{a}^{b}f(x)dx=\int_{a}^cf(x)dx+\int_{c}^bf(x)dx & a<c<b
\end{align}
$$

## Example 6 Evaluate

$$
\int_{-2}^{1}f(x) \, dx \text{ where }f(x)=\biggl\{
\begin{matrix}
 & 2-x^2 & ;x\geq 0 \\
 & x & ;x< 0
\end{matrix}
\biggl\}
$$

$$
\begin{align}
\int_{-2}^{1}f(x) \, dx  & =\int_{-2}^{0}f(x) \, dx+\int_{0}^{1}f(x) \, dx  \\
 & =\int_{-2}^{0}x \, dx +\int_{0}^{1}(2-x^2) \, dx  \\
 & = \frac{x^2}{2}|^o_{-2}+\left( 2x-\frac{x^3}{3} \right)|^1_{0} \\
 & =\left[ 0-\frac{(-2)^2}{2} \right]+\left[ 2-\frac{1}{3}-0 \right] \\
 & =-2+2-\frac{1}{3} \\
 & =-\frac{1}{3}
\end{align}
$$


## Example 7.

$$
\int_{-1}^4|x|dx
$$
$$
|x|=\biggl\{ \begin{align}
x & ; & x\geq0 \\
-x & ; & x<0
\end{align}
\biggl\}
$$

# Technique of integration

## U Subsitiutaion

### Example 8.
$$
\int(1-3x)^6dx
$$
$$
\begin{align}
 & u=1-3x \\
 & du=-3dx \\
 & dx=-\frac{du}{3}\\
 & &  \int(1-3x)^6dx & =-\frac{1}{3}\int u^6 \, du  \\
 &  &  & =-\frac{1}{3}\cdot \frac{u^7}{7}+C \\
 &  &  & =-\frac{1}{21}(1-3x)^7+C
\end{align}
$$
### Example Extra.
$$
\int (3x+1)^{200}dx
$$
$$
\begin{align}
u & =3x+1 \\
dx  & =\frac{du}{3}
\end{align}
$$
$$
\begin{align}
= & \int u^{200} \, dx \\
= & \frac{1}{3} \cdot\int u^{200} \, du \\
= & \frac{1}{3} \cdot\frac{u^{201}}{201} \, +C \\
= & \frac{1}{3} \cdot \frac{(3x+1)^{201}}{201}+C
\end{align}
$$

### Example Extra 2.
$$
\int 2x\sqrt{ x^2-7 }
$$
$$
\begin{align}
u  & = x^2-7 \\
dx & =\frac{du}{2x}
\end{align}
$$
$$
\begin{align}
\int 2x\sqrt{ x^2-7 } & =\int2x\sqrt{ u } \frac{du}{2x} \\
 & =\int \sqrt{ u }du \\
 & =\frac{2}{3}u^{3/2}+C \\
 & =\frac{2}{3}(x^2-7)^{3/2}+C
\end{align}
$$
### Example Extra 3.
$$
\int 4x \sin(x^2+4)dx
$$
$$
\begin{align}
u & =x^2+4 \\
dx & = \frac{du}{2x}
\end{align}
$$
$$
\begin{align}
\int 4x \sin(x^2+4)dx & =\int 2(2x)\sin(u) \cdot \frac{du}{2x} \\
 & = 2\int\sin(u)\cdot du \\
 & =2\cos(u)+C \\
 & =2\cos(x^2+4)+C
\end{align}
$$
### Example Extra 4.

$$
\int\left[ \frac{1-\ln x}{x^2} \right]5^{\frac{\ln x}{x}}dx
$$
$$
\begin{align}
\int\left[ \frac{1-\ln x}{x^2} \right]5^{\frac{\ln x}{x}}dx & =\int\left[ \frac{1-\ln x}{x^2} \right]5^{\frac{\ln x}{x}} \frac{d\left[  \frac{\ln x}{x} \right]}{\left[ \frac{1-\ln x}{x^2} \right]} \\
 & =\int 5^{(\ln x)/x}d\left( \frac{\ln x}{x} \right) \\
 & =\frac{5^{(\ln x)/x}}{\ln 5}+C
\end{align}
$$
