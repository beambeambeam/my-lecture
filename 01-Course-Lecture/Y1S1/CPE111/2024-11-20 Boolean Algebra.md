---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2024-11-20

# Boolean Algebra

1. Boolean Functions.
2. Representing Boolean Function.
3. Logic Gates.
4. Minimization of Circuits.

# Boolean Functions

## The complement.

Logic → not
Boolean → $\overline{\square}$
$$
\begin{align}
\overline{1} & =0 \\
\overline{0} & =1
\end{align}
$$
## The Boolean sum

logic → $v$
Boolean → $+$
$$
\begin{align}
0+0 & =0 \\
0+1 & =1 \\
1+0 & =1 \\
1+1 & =0
\end{align}
$$

## The Boolean product (AND)
logic → $\wedge$
Boolean → $\cdot$

$$
\begin{align}
0\cdot 0  & = 0 \\
0 \cdot 1  & =0 \\
1 \cdot 0  & =0 \\
1 \cdot 1  & =1
\end{align}
$$

## Example 1.

$$
\begin{align}
1\cdot0+\overline{(0+1)} & =1\cdot0+0 \\
 & =0+0 \\
 & =0
\end{align}
$$

## Example 2.

$$
\begin{align}
1\cdot0+\overline{(0+1)} & =T\wedge F\vee \neg(F\vee T)
\end{align}
$$

## Example 3.
$$
\begin{align}
(T\wedge T)\vee \neg F & \equiv T \\
(1\cdot 1)+\overline{0} & =1
\end{align}
$$

## Boolean Variable

$$
x,y,z
$$
## Boolean function
$$
\begin{matrix}
f(x) & \leftrightarrow  &  \text{ input 1 bit} \\
g(x, y) & \leftrightarrow  &  \text{ input 2 bit} \\
h(a,b,c) & \leftrightarrow  &  \text{ input 3 bit} \\
\end{matrix}
\text{ output 1 bit}
$$

## Boolean Expression

$$
1,0,x,y,\overline{x},\overline{y}
$$

|     |  x  |  y  |  z  | $F(x,y,z)=xy+\overline{z}$ |
| :-: | :-: | :-: | :-: | -------------------------- |
|  0  |  0  |  0  |  0  | 1                          |
|  1  |  0  |  0  |  1  | 0                          |
|  2  |  0  |  1  |  0  | 1                          |
|  3  |  0  |  1  |  1  | 0                          |
|  4  |  1  |  0  |  0  | 1                          |
|  5  |  1  |  0  |  1  | 0                          |
|  6  |  1  |  1  |  0  | 1                          |
|  7  |  1  |  1  |  1  | 1                          |
x,y → MSB
z → LSB

Big Endian
MSB $\dots$ LSB

Little Endian
LSB $\dots$ MSB

ไม่ใส้ bar เป็น 1
$x \to 1$
$\overline{x} \to 0$

## Identities of Boolean Algebra

![[Pasted image 20241120144041.png]]

### Example 4.

$$
\begin{align}
x(x+y) & = x\cdot x + x \cdot y \\
 & =x+xy \\
 & =x(1+y) \\
 & =x\cdot1 \\
 & =x
\end{align}
$$

### Example 5.
$$
\begin{align}
x(y+0) & = x+(y\cdot 1) \\
\bar{x}\cdot1+(\bar{y}+z) & =\bar{x}+0 \cdot (\bar{y}\cdot z)
\end{align}
$$
duals
$+\leftrightarrow \cdot$
$0\leftrightarrow1$

### Example 6.
$$
x(x+y)=x+(x\cdot y)
$$

# Representing Boolean Function. 
## Sum-of-Products Expansions

SOP → $(\cdot)+(\cdot)+(\cdot)$
$xy+\bar{z}$

POS → $(+)(+)(+)$
$(x+y)(x+\bar{y})$

literal → จำนวนของตัวแปร และ จำนวน complement
minterm → 

### Example 7.
หา boolean expression

|     |  x  |  y  |  z  |  F  | G   |
|:---:|:---:|:---:|:---:|:---:| --- |
|  0  |  0  |  0  |  0  |  0  | 0   |
|  1  |  0  |  0  |  1  |  0  | 0   |
|  2  |  0  |  1  |  0  |  0  | 1   |
|  3  |  0  |  1  |  1  |  0  | 0   |
|  4  |  1  |  0  |  0  |  0  | 0   |
|  5  |  1  |  0  |  1  |  1  | 0   |
|  6  |  1  |  1  |  0  |  0  | 1   |
|  7  |  1  |  1  |  1  |  0  | 0   |

$$
\begin{align}
F & =x\bar{y}z \\
G & =\bar{x}y\bar{z}+xy\bar{z}
\end{align}
$$

### Example 8.

$$
\bar{x_{1}}x_{2}\bar{x}_{3}x_{4}x_{5} = m_{11}
$$
### Example 9.

$$
\begin{align}
F(x,y,z) & =(x+y)\bar{z} \\
 & = x\bar{z}+y\bar{z} \\
 & =x(y+\bar{y})\bar{z}+(x+\bar{x})y\bar{z} \\
 & =xy\bar{z}+x\bar{y}\bar{z}+xy\bar{z}+\bar{x}y\bar{z} \\
 & =xy\bar{z}+x\bar{y}\bar{z}+\bar{x}y\bar{z}
\end{align}
$$

# Logic Gates

## Example 10.

$f(x,y,z)$ pass → 1, fail → 0

|     |  x  |  y  |  z  | f(x,y,z) |
| :-: | :-: | :-: | :-: | :------: |
|  0  |  0  |  0  |  0  |    0     |
|  1  |  0  |  0  |  1  |    0     |
|  2  |  0  |  1  |  0  |    0     |
|  3  |  0  |  1  |  1  |    1     |
|  4  |  1  |  0  |  0  |    0     |
|  5  |  1  |  0  |  1  |    1     |
|  6  |  1  |  1  |  0  |    1     |
|  7  |  1  |  1  |  1  |    1     |

$$
f(x,y,z)=\bar{x}yz+x\bar{y}z+xy\bar{z}+xyz
$$
![[Pasted image 20241120154342.png]]

## Example 11.

$$
\begin{align}
0+0 & =0 \\
0+1 & =1 \\
1+0 & =1 \\
1+1 & = 10 \\
 & \text{0 คือ sum, 1 คือ carry}
\end{align}
$$
|  x  |  y  | s   | c   |
| :-: | :-: | --- | --- |
|  0  |  0  | 0   | 0   |
|  0  |  1  | 1   | 0   |
|  1  |  0  | 1   | 0   |
|  1  |  1  | 0   | 1   |
$$
\begin{align}
s & =\bar{x}y+x\bar{y} \\
c & =xy
\end{align}
$$

input: x,y
outputL s, c out

![[Pasted image 20241120160011.png]]

# Minimization

## Example 12.
$$
x\bar{y}z+x\bar{y}\bar{z}+\bar{x}\bar{y}z+\bar{x}\bar{y}\bar{z}
$$

NOT * 3
AND * 5
OR * 1

$$
\begin{align}
x\bar{y}z+x\bar{y}\bar{z}+\bar{x}\bar{y}z+\bar{x}\bar{y}\bar{z} & = (x\bar{y}z+x\bar{y}\bar{z})+(\bar{x}yz+\bar{x}\bar{y}z)+(\bar{x}\bar{y}z+\bar{x}\bar{y}\bar{z}) \\
 & = x\bar{y}(z+\bar{z})+\bar{x}z(y+\bar{y})+\bar{x}\bar{y}
(z+\bar{z}) \\
 & =x\bar{y}+\bar{x}z+\bar{x}\bar{y} \\
 & =(x\bar{y}+\bar{x}\bar{y})+\bar{x}z \\
 & =\bar{y}+\bar{x}z
\end{align}
$$

## Karnaugh Maps

รวมผล terms ของ Boolean functions
- ไม่เกิน 5 ตัวแปร

![[Pasted image 20241120161238.png]]

lock เป็น 
y→10
x→10

3 var
yz→11,10,00,01
x→1, 0

4 var
yz→11,10,00,01
wx→11,10,00,01

Implicant → การวงลดวงจร
Prime Implicant → ลดรูปไม่ได้

### Example 13.

$x\bar{y}+\bar{x}y+\bar{x}\bar{y}$

|           |  y  | $\bar{y}$ |
| :-------: | :-: | :-------: |
|     x     |  0  |     0     |
| $\bar{x}$ |  1  |     1     |

1. วง 1 เป็นจำนวน $2^n$
2. วง 1 ในแนวตั้งและแนวนอน

|           |  y  | $\bar{y}$ |
| :-------: | :-: | :-------: |
|     x     |  0  |    AC     |
| $\bar{x}$ |  B  |    BC     
