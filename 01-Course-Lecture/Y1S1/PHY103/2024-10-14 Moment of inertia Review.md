---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2024-10-14

# Moment of inertia
## Definition
แรงต้านการหมุน

$$
I=mR^2
$$
- R คือ จากจุดหมุนไปถึงขอบ

# Each Object

![[Pasted image 20241014134008.png]]

ถ้ากระจายทั่วๆ object จะมี
$$
I=kmR^2,0<k\leq 1
$$
วิธีคิด
- $\sum F=ma$ คือการที่หมุนทนต่อการเคลื่อนไปข้างหน้าจนสำเร็จ
- $\alpha$ คือ ความเร่งเชิงมุม
- $\tau = F \times R$ 
- $\tau=I\alpha$ คือแรงที่ทนต่อการหมุนไปทิศเดียวกับ $\alpha$

![[Pasted image 20241014134446.png]]

![[Pasted image 20241014134518.png]]

จะแตกต่างกันก็ต่อเมื่อวิธีการกระจายของ มวล

![[Pasted image 20241014134615.png]]

![[Pasted image 20241014134633.png]]

![[Pasted image 20241014134655.png]]

![[Pasted image 20241014134758.png]]

# Compound Structure
ทุกๆ Component ต้องหมุนจากจุดเดียวกัน
$$
I_{total}=I_{1}+I_{2}+I_{3}+\dots+I_{n}
$$

## Ex. 4 point
![[Pasted image 20241014134904.png]]

## Ex. 2 thin boards
![[Pasted image 20241014135024.png]]
คิดได้ 2 แบบคือ จากจุดกลาง หรือ จากจุดปลายของไม้
$$
\begin{align}
I_{t} & =\frac{1}{2}mL^2+\frac{1}{2}mL^2 \\
I_{t} & =\frac{1}{6}mL^2 \\
I_{t} & =4\left[ \frac{1}{3}\left( \frac{m}{2} \right)\left( \frac{L}{2} \right)^2 \right] \\
I_{t} = & \frac{1}{6}mL^2
\end{align}
$$
## Ex. Wagon wheel
![[Pasted image 20241014135227.png]]
$$
I_{t}=8I_{spoke}+I_{rim}
$$

# Object with hole

หลุมต้องอยู่ตรงกลางจุดหมุน
$$
I_{t}=I_{ของ}-I_{หลุ่ม}
$$

## Ex. แม่งกับหลุ่ม
![[Pasted image 20241014135535.png]]
$$
\begin{align}
m=\frac{1}{2}M  &  & M=2m
\end{align}
$$
$$
\begin{align}
I_{t} & =I_{bar}-I_{hole} \\
& =\frac{1}{12}ML^2-\frac{1}{12}\left( \frac{M}{2} \right)\left( \frac{L}{2} \right)^2 \\
 & M \text{ คือ ทั้งหมดของ Bar แปลงเป็น m} \\
& =\frac{1}{12}(2m)L^2-\frac{1}{12}\left( \frac{2m}{2} \right)\left( \frac{L}{2} \right)^2 \\
 & =\frac{7}{48}mL^2
\end{align}
$$

## Ex. Disk with Hole
![[Pasted image 20241014140008.png]]

$$
\begin{align}
I_{t} & =I_{bar}-I_{hole} \\
& =\frac{1}{2}MR^2-\frac{1}{2}\left( \frac{M}{4} \right)\left( \frac{R}{2} \right)^2 \\
 & M \text{ คือ ทั้งหมดของ Bar แปลงเป็น m} \\
& =\frac{1}{12}\left( \frac{4}{3}m \right)R^2-\frac{1}{12}\left( \frac{\frac{4}{3}m}{2} \right)\left( \frac{L}{2} \right)^2 \\
 & =\frac{5}{8}mR^2
\end{align}
$$

# Parallel Axis Theorem
## Definition
ถ้ารู้ moment of inertia จาก cm เราจะรู้ moment of intertia ออกจาก cm d ระยะได้

![[Pasted image 20241014140451.png]]

## Ex. Thin Rod

![[Pasted image 20241014140519.png]]

$$
\begin{align}
I & =I_{cm}+md^2 \\
 & =\frac{1}{12}mL^2+m\left( \frac{L}{2} \right)^2 \\
 & =\frac{1}{3}mL^2
\end{align}
$$

## Ex. Solid Disk

![[Pasted image 20241014140804.png]]

## Ex. wide Board

![[Pasted image 20241014140900.png]]

$$
\begin{align}
I & =I_{cm}+md^2 \\
 & =\frac{1}{12}m(L^2+W^2)+m\left( \frac{L}{2} \right)^2
\end{align}
$$

## Ex. Wide board angle

![[Pasted image 20241014141021.png]]

$$
\begin{align}
I & =I_{cm}+md^2 \\
 & =\frac{1}{12}m(L^2+W^2)+m\left( \sqrt{ \left( \frac{L}{2} \right)^2+\left( \frac{W}{2} \right)^2 } \right)^2
\end{align}
$$

## Ex. Holes
![[Pasted image 20241014141157.png]]
$$
\begin{align}
I & =I_{disk}-I_{hole} \\
I_{hole} & =I_{cm}+md^2 \\
 & =\frac{1}{2}\left( \frac{M}{4} \right)\left( \frac{R}{2} \right)^2+\left( \frac{M}{4} \right)\left( \frac{R}{2} \right)^2 \\
I_{hole} & =\frac{3}{32}MR^2 \\
I & =\frac{16}{32}MR^2-\frac{3}{32}MR^2
\end{align}
$$

# Calculus with I
## Definition
$$
I=\int_{0}^LdI
$$
โดยหา $dm$ จาก $dm=มวลทั้งหมดของวัตถุ\frac{dมวลขนาดเล็ก}{พื้นที่ทีมวลกระจายอยู่}$

## Ex. Thin Board

![[Pasted image 20241014141714.png]]
- หาจุดเล็กๆก่อน
- หามวลของจุดเล็กๆนั้นในนี้คือ $dm=m \frac{dx}{L}$

$$
\begin{align}
I & =\int_{0}^LdI \\
 & = \int_{0}^L dmx^2 \\
 & = \int_{0}^L m \frac{dx}{L}x^2 \\
 & = \frac{m}{L}\int_{0}^Lx^2dx \\
 & = \frac{m}{L} \frac{x^3}{3}\Biggr|_{0}^{L} \\
 & = \frac{1}{3}mL^2
\end{align}
$$

## Ex. Disk

![[Pasted image 20241014142645.png]]

## Ex. Triangle

![[Pasted image 20241014142910.png]]

# Moment of inertia and kinetic energy
## Definition
$$
\begin{align}
K_{e} & =\frac{1}{2}mv^2 \\
K_{e} & =\frac{1}{2}I\omega^2 \\
K_{total} & = \frac{1}{2}mv^2 + \frac{1}{2}I\omega^2
\end{align}
$$

## Ex. Rotational + Linear

![[Pasted image 20241014143244.png]]

$$
\begin{align}
K_{total} & = \frac{1}{2}mv^2 + \frac{1}{2}I\omega^2 \\
 & =\frac{1}{2}mv^2+\frac{1}{2}\left( \frac{1}{2}mR^2 \right)\left( \frac{v^2}{R^2} \right)
\end{align}
$$

## Ex. With Gravitational Energy

$$
PE_{0}=K_{ef}
$$

![[Pasted image 20241014143619.png]]

# Moment of Inertia and Acceleration

![[Pasted image 20241014143659.png]]

Use $\tau=I\alpha$

$$
\begin{align}
\tau_{net} & =I\alpha \\
\tau_{aid}-\tau_{opp} &= I{\alpha} \\
\text{จาก } \tau & =FR \\
T_{2}R-T_{1}R & =\frac{1}{2}MR^2\left( \frac{\alpha}{R} \right) \\
T_{2}-T_{1} & =\frac{1}{2m_{3}}\alpha
\end{align}
$$
$$
\begin{align}
T_{1} & =m_{1}g+m_{1}a \\
T_{2} & =m_{2}g-m_{2}a \\
\end{align}
$$
$$
\begin{align}
T_{2}-T_{1} & =\frac{1}{2m_{3}}\alpha \\
m_{2}g-m_{2}a-m_{1}g+m_{1}a & =\frac{1}{2m_{3}}\alpha
\end{align}
$$
