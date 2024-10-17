---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2024-10-16

# SHM

# Hooke’s Law

$$
F=-kx
$$

F คือแรงที่กระทำต้อวัตถุโดยสปริง
k เป็น constant
x ออกไปเป็นบวก spring ดึงกับมาทำให้จริงๆได้ $-F=kx$ สลับข้่างก็จะได้ $F=-kx$

# Equation choose

1. ถ้าถามเกี่ยวกับ displacement ให้ใช่
$$
\begin{align}
E_{0} & =E_{f} \\
PE_{0} & = KE_{f}+PE_{f} \\
\frac{1}{2}kA^2 & = \frac{1}{2}mv^2+\frac{1}{2}kx^2 \\
v(x) & = \pm \sqrt{ \frac{k}{m}(A^2-x^2) } \\
x(v) & = \pm \sqrt{ A^2 - \frac{m}{k}v^2 } \\
a(x) & =-\frac{k}{m}x
\end{align}
$$
A คือระยะสูงสุดที่สปริงปีปได้ x คือระยะยืดสปริง
2. ถ้าถามเรื่องเวลา t
$$
\begin{align}
x(t) & =A\cos(\omega t) \\
v(t) & =-\omega A\sin(wt) \\
a(t) & =-\omega^2A\cos(\omega t)
\end{align}
$$
Radians เท่านั้น!

# Energy

$$
E_{0}=\frac{1}{2}kA^2
$$
![[Pasted image 20241016223545.png]]
$$
E_{f}=\frac{1}{2}kx^2+\frac{1}{2}mv^2
$$
![[Pasted image 20241016223550.png]]
$$
\frac{1}{2}kA^2=\frac{1}{2}kx^2+\frac{1}{2}mv^2
$$
$$
\begin{align}
v(x) & = \pm \sqrt{ \frac{k}{m}(A^2-x^2) } \\ \\
 & \text{v(x) เยอะน้อยตาม x}
\end{align}
$$

# Base on trig

![[Pasted image 20241016223912.png]]

$$
\begin{align}
x & =A\cos(\omega t) \\
\omega & =\sqrt{ \frac{k}{m} }
\end{align}
$$
k constant of spring m = mass
$\omega=2\pi f$

$$
\begin{align}
x(t) & =A\cos(\omega t) \\
 & =A\cos\left( \sqrt{ \frac{k}{m} } t \right) \\
 & =A\cos(2\pi ft) \\
 & =A\cos\left( 2\pi \left( \frac{1}{T} \right)t \right)
\end{align}
$$
$$
T=\frac{1}{f}=\frac{1}{\frac{\omega }{2\pi}}=\frac{2\pi}{w}=2\pi \sqrt{ \frac{m}{k} }
$$

## Ex.

![[Pasted image 20241016224423.png]]

$$
\begin{align}
x(t) & =A\cos(\omega t) \\
 & = (10cm)\cos\left( \sqrt{ \frac{800 \frac{N}{m}}{2.0kg} }1.5s \right) \\
 & =
\end{align}
$$

## SHM with Phase Angle

![[Pasted image 20241016224843.png]]

## Ex. setup trig eq.

$$
\begin{align}
m & =40kg \\
k & =\frac{400N}{m} \\
x(t & =1.375s)=? \\
@t=0 &,v=v_{max}=50 \frac{m}{s}
\end{align}
$$

![[Pasted image 20241016225026.png]]

เลือกกราฟ

$$
\begin{align}
w & =\sqrt{ \frac{k}{t} } \\
x(t) & =A\cos\left( \omega t+\frac{\pi}{2} \right) \\
 & = 10\cos\left( 13.75-\frac{\pi}{2} \right)
\end{align}
$$

## Ex. x(t)=Acos(wt) find v(t) and a(t)

### use cal

![[Pasted image 20241016225347.png]]

A กับ W เป็น constant ก็เลยถูกทิ้งไว้หาแค่ diff ของ t

### use energy

![[Pasted image 20241016225502.png]]

# Other type
## Pendulum
### Ex.

$$
w=\sqrt{ \frac{g}{l} }
$$
![[Pasted image 20241016225854.png]]

แก้ได้หมดแค่เปลี่ยนจาก w ปกติเป็น w ของวัตุนั้นๆ

