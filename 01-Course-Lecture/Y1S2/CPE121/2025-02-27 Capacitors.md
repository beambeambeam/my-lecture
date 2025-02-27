---
cssclasses:
  - center-images
  - center-titles
  - page-black
  - pen-white
date: 2024-09-24
---
2025-02-27

# Capacitors
- ไม่มีกำเนิดประจุ
- เป็นตัวกักประจุ
- หน่วยเป็ฯ farads (จำนวนประจุที่วิ่งผ่าน แผ่นประกบ 2 แผ่น)

## Capacirtors relation with current-voltage

$$
i = C \frac{dv}{dt}
$$

![[Pasted image 20250227085246.png]]

## Properties
- อุดมคติ → ประจุไม่หลุดออกมา
- ความเป็นจริง → ประจุหลุดออกมา
![[Pasted image 20250227085811.png]]
- Leakage resisitance เป็น load ทำให้มีแรงดัน + ตัวต้านทานวิ่งผ่าน ถ้าประจุเต็มแล้ว
- แทนด้วยวงจรเปิด

## Parallel

$$
C_{n}=\sum _{n=1}^{\infty}C_{n}
$$
![[Pasted image 20250227090035.png]]

## Series Capacitors

$$
\frac{1}{C_{n}}=\sum _{n=1}^{\infty} \frac{1}{C_{n}}
$$
### Two Capacitors

$$
C_{eq}=\frac{C_{1}C_{2}}{C_{1}+C_{2}}
$$

## Example 1.
![[Pasted image 20250227090251.png]]
$$
(\frac{1}{\frac{1}{20}+\frac{1}{5}})+6+(\frac{1}{\frac{1}{20}+\frac{1}{60}})
$$
# Inductors
- ตรงข้ามกับ Capacittors
- เก็บประแสโดยการกักเป็นสนามแม่เหล็กไฟฟ้า
- 

## Inductance
![[Pasted image 20250227090749.png]]

## Relation with voltage current
$$
v=L \frac{di}{dt}
$$

## Properties
![[Pasted image 20250227091231.png]]
- Ideal ไม่มี leakage
- leakge เป็นอนุกรม
- อาจมี Capacitors มาด้วย

## Series
$$
L_{eq}=\sum _{n=0}^\infty L_{n}
$$
## Parallel
$$
\frac{1}{L_{eq}}=\sum _{n=0}^\infty \frac{1}{L_{n}}
$$
### Two
$$
L_{eq}=\frac{L_{1}L_{2}}{L_{1}+L_{2}}
$$

## Example 2.

![[Pasted image 20250227091542.png]]

$$
\begin{align}
20+12+10  & =42 \\
\frac{42\times{7}}{42+7} & =
\end{align}
$$

# The Source-Free RC Circuit

![[Pasted image 20250227091734.png]]

- กระแสไม่เท่ากัน

## Natural Response
$$
\begin{align}
v(0) & =V_{0} \\
i_{c}+i_{r} & =0 \\
C \frac{dv}{dt}+ \frac{v}{R} & =0
\end{align}
$$

$$
\begin{align}
C \frac{dv}{dt}+ \frac{v}{R} & =0 \\
\frac{dv}{v} & = \frac{1}{RC}dt \\
\ln v & =-\frac{t}{RC}+\ln A \\
\ln \frac{v}{A} & =-\frac{t}{RC} \\
v(t) & = Ae^{-t/RC} \\
v(t) & = V_{0}e^{-t/RC}
\end{align}
$$

หน่วยเป็น วินาที
- ใน Exponential ต้องไม่มีหน่วย

## Example 3.

![[Pasted image 20250227093500.png]]

- หา $R_{eq}$
$$
\frac{5*20}{5+20}=4
$$
- หา $\tau$
$$
\begin{align}
\tau=R_{c}C & =4\times 0.1 \\
 & = 0.4
\end{align}
$$

- หา $v(t)$
$$
\begin{align}
V_{c}(t) & =V_{t=0}\times e^{-t/\tau} \\
 & =15 \times e^{-t/0.4}
\end{align}
$$
- หา $v_{x}(t)$
$$
\begin{align}
\frac{12}{8+12}\times 15 \times e^{-t/0.4}
\end{align}
$$
- หา $i_{x}$
$$
I_{x}(t)=\frac{V_{x}(t)}{12}=\frac{9}{12}\times 15 \times e^{-t/0.4}
$$

## Example 4.

![[Pasted image 20250227095158.png]]

![[Pasted image 20250227095441.png]]

$$
\begin{align}
v(t=0) & =20 \frac{9}{9+3} \\
 & = 15V
\end{align}
$$

$$
\begin{align}
\tau & =R\times C \\
 & = (1+9)\times 20 \\
 & =0.2 s
\end{align}
$$
$$
\begin{align}
v(t) & =v(t=0)\times e^{-t/\tau} \\
 & = 15\times e^{-t/0.2}
\end{align}
$$

# Source-Free RL Circuits

![[Pasted image 20250227095824.png]]

$$
\begin{align}
i(0) & =I_{0} \\
v_{L}+v_{R} & =0 \\
L \frac{di}{dt}+Ri & =0
\end{align}
$$

$$
\begin{align}
\frac{di}{dt}+ \frac{R}{L}i & =0 \\
\ln \frac{i(t)}{I_{0}} & = - \frac{Rt}{L} \\
  & i(t)I_{0}e^{-Rt/L}
\end{align}
$$
$$
\tau=\frac{L}{R}
$$
$$
i(t)I_{0}e^{-Rt/L}=i(t)I_{0}e^{-t/\tau}
$$

## Example 5.
![[Pasted image 20250227100519.png]]

- แปลง 0.5H เป็น 1V
- ทำ mesh analysis

$$
-1+2(i_{1}-i_{2}) =0
$$
$$
\begin{align}
2(i_{2}-i_{1})+4i_{2}+3i_{1} & =0 \\
i_{2}  & = \frac{5}{6}i_{1}
 \end{align}
$$

$$
\begin{align}
i_{1}=-3A, i_{2}=-2.5A
\end{align}
$$

$$
R_{eq}=\frac{V_{0}}{i_{3}}=\frac{1}{3}
$$

- หา $\tau$
$$
\frac{L}{R} = \frac{0.5}{\frac{1}{3}}=1.5
$$
- หา I(t)
$$
=10A\times e^{-t/1.5}
$$

- หา $I_{x}(t)$
$$
=\frac{V_{ab}(t)}{2}
$$
$$
\begin{align}
V_{ab}(t) & =L \frac{d}{dt} i(t) \\
 & = 0.5 \frac{d}{dt} 10 e^\left( -\frac{t}{1.5} \right) \\
 & = 0.5 \frac{1}{1.5} e^{-t/1.5}
\end{align}
$$

$$
\begin{align}
I_{x}(t) & = - \frac{1}{2} \frac{10}{3} e^{-t/1.5} \\
 & = - \frac{5}{3}e^{-t/1.5}
\end{align}
$$
