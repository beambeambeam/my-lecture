---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2024-11-26

Input → a1,a2,a3,a4

output → b1,b2

|     | $A_{1}$ | $A_{2}$ | $A_{3}$ | $A_{4}$ | $B_{1}$ | $B_{2}$ |
| :-: | :-----: | :-----: | :-----: | :-----: | ------- | ------- |
|  0  |    0    |    0    |    0    |    0    | 0       | 0       |
|  1  |    0    |    0    |    0    |    1    | 0       | 1       |
|  2  |    0    |    1    |    0    |    0    | 0       | 0       |
|  3  |    0    |    1    |    0    |    1    | 0       | 1       |

$$
\begin{align}
B_{2} & =\bar{A_{1}}\bar{A_{2}}\bar{A_{3}}A_{4}+\bar{A_{1}}A_{2}\bar{A_{3}}A_{4} \\
 & = \bar{A_{1}}\bar{A_{3}}A_{4}(\bar{A_{2}}+A_{2}) \\
 & = \bar{A_{1}}\bar{A_{3}}A_{4}
\end{align}
$$

