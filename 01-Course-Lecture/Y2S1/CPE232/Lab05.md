---
cssclasses:
  - center-images
  - center-titles
  - image-borders
date: 2024-09-24
---

# Lab05


$$
\begin{array}{|c|c|c|c|c|}
\hline
\text{Cin} & \text{A} & \text{B} & \text{S} & \text{Cout} \\
\hline
0 & 0 & 0 & 0 & 0 \\
\hline
0 & 0 & 1 & 1 & 0 \\
\hline
0 & 1 & 0 & 1 & 0 \\
\hline
0 & 1 & 1 & 0 & 1 \\
\hline
1 & 0 & 0 & 1 & 0 \\
\hline
1 & 0 & 1 & 0 & 1 \\
\hline
1 & 1 & 0 & 0 & 1 \\
\hline
1 & 1 & 1 & 1 & 1 \\
\hline
\end{array}
$$

	$$
\Large\text{Sum (S)} \qquad\qquad\qquad\qquad \Large\text{Cout}
$$
$$
\begin{array}{|c|c|c|c|c|}
\hline
\text{Cin\AB} & \text{00} & \text{01} & \text{11} & \text{10} \\
\hline
\text{0} & 0 & 1 & 0 & 1 \\
\hline
\text{1} & 1 & 0 & 1 & 0 \\
\hline
\end{array}
\qquad
\begin{array}{|c|c|c|c|c|}
\hline
\text{Cin\AB} & \text{00} & \text{01} & \text{11} & \text{10} \\
\hline
\text{0} & 0 & 0 & 1 & 0 \\
\hline
\text{1} & 0 & 1 & 1 & 1 \\
\hline
\end{array}
$$

$$ \text{Boolean Expressions: S} = \overline{ \overline{(A' \cdot B' \cdot C_{in})} \cdot \overline{(A' \cdot B \cdot C'_{in})} \cdot \overline{(A \cdot B' \cdot C'_{in})} \cdot \overline{(A \cdot B \cdot C_{in})} } $$ $$ \text{Cout} = \overline{ \overline{(A \cdot B)} \cdot \overline{(A \cdot C_{in})} \cdot \overline{(B \cdot C_{in})} } $$
