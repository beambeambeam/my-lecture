---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2024-10-07

## แรงดึงกลับ

- ตำแหน่งสมดุล
- เมื่อเกิดการเปลี่ยนแปลงของวัตถุ วัตถุจะกลับมาที่เดิมของตำแหน่งสมดุล
- สมดุลเสถียร
- ถ้าไม่มีแรงอื่นๆมากระทำ วัตถุจะเคลื่อนที่เข้าตำแหน่งสมดุลไปเรื่อยๆ

## มวลติดปลายสปริง
- ระบุตำแหน่งสมดุล
- $\vec{x}$ คือระยะจากตำแหน่งสมดุล
$$
\vec{F}=-kx
$$
- ความเร่ง
$$
\vec{\alpha}=\frac{\vec{F}}{m}=-\frac{k}{m}\vec{x}
$$
$$
\begin{align}
\vec{\alpha}=-\frac{k}{m}\vec{x} &\to \frac{d^2x}{dt^2}=-\frac{k}{m}x
\end{align}
$$
คำตอบมักจะเป็น $\sin (x),\cos(x)$

## คาบ และ ความถี่
$$
\begin{align}
f & =\frac{\omega}{2\pi} \\
 & =\frac{1}{2\pi}\sqrt{ \frac{k}{m} } \\
 & \text{รอบต่อเวลา}
\end{align}
$$
$$
\begin{align}
T & =\frac{1}{f} \\
 & =2\pi \sqrt{ \frac{m}{k} } \\
 & \text{เวลาที่ใช้ในการเคลื่อนที่ 1 รอบ}
\end{align}
$$

## ความเร่ง
$$
\alpha=w^2x \to x=-wx
$$
## การกระจัด
$$
x=A\sin(wt+\phi)
$$
$$
\begin{align}
\dot{x}=\frac{dx}{dt} & =A\frac{d}{dt}\sin(\omega t+\phi) \\
 & = A\cos(\omega t+\phi)\times \omega 
\end{align}
$$
v(t) ใดๆ
$$
\begin{align}
\dot{x}\dot{}=\dot{v} & =\frac{d}{dt}(A\omega \cos(\omega t+\phi)) \\
 & =A\frac{\omega d}{dt}\cos(\omega t+\phi) \\
 & =A\omega(-\sin(\omega t+\phi)) \\
 & =A\omega^2\sin(\omega t+\phi)
\end{align}
$$
$\therefore \dot{x}\dot{} = -\omega w^2x$
$x(t)=A\sin(wt+\phi)$ เป็นผลเฉลบของสมการ

## ความเร็ว
$$
v(t)=-\omega x_{m}\sin(\omega t+\phi)
$$
## ความเร่ง
$$
\begin{align}
a(t) & =\omega^2x_{m}\cos(\omega t+\phi) \\ \\
 & =wt^2(x)
\end{align}
$$
## Checkpoint
### 1
![[Pasted image 20241007112002.png]]

คาบคือ $t=2T,x=-x_{m}$

$$
\begin{align}
t & =2T  & =-x_{m} \\
t & =3.5T  & =x_{m} \\
t & =5.25T & =0
\end{align}
$$

### 2
![[Pasted image 20241007112836.png]]

$$
\begin{align}
 & a) & F & =-5x &  \\
 & b)  & F & \propto x^2  & not \\
 & c)  & F & =10x & not \\
 & d)  & F & =3(x)^2 & not
\end{align}
$$

## Energy in SHM

### พลังานศักย์
$$
U(t)=kx^2=\frac{1}{2}kx_{m}^2\cos^2(\omega t+\phi)
$$

### พลังานจลน์
$$
\begin{align}
K(t)=\frac{1}{2}mv^2 & =\frac{1}{2}kx_{m}^2\sin^2(\omega t+\phi) \\
 & =\frac{1}{2}kx_{m}^2\sin^2(\omega t+\phi)
\end{align}
$$

### พลังงานเชิงกล
$$
\begin{align}
E & =U+K \\
E & =\frac{1}{2}kx_{m}^2
\end{align}
$$
- พลังงานคงที่เสมอๆ

![[Pasted image 20241007113935.png]]

### Example
#### 1
![[Pasted image 20241007114234.png]]
$$
\begin{align}
a & =-2.65x \\
a  & =-\omega^2x \\
w & =\sqrt{ 2.65 }  & =1.63\text{ }rad\cdot t^{-1}
\end{align}
$$
$$
\begin{align}
v_{max} & =\omega A \\
 & =(1.63rad\cdot t^{-1}) (0.35m) \\
 & =0.57m\cdot t^{-1}
\end{align}
$$
$$
\begin{align}
x & =A\sin \omega t \\
 & =(0.35m)\sin((1.63rad\cdot t^{-1})(2.5s))
\end{align}
$$
## Pendulums

### Physical Pendulum

#### แรงดึงกลับและทอร์ก
- $\tau =-mgh\sin(\theta)$
- $\tau=Ia$

