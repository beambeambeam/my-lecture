---
cssclasses:
  - center-images
  - center-titles
  - image-borders
date: 2024-09-24
---

# Welcome Session | Intro duction to Quantum Computing

# Prospects of Quantum Computing

Quantum Money, ไอเดียของการนำ Quantum Computing มาแก้ปัญหาที่ Classical ไม่อาจจะทำได้ หรือถ้าทำได้ก็ใช้เวลานานมากๆ

Quantum Key distribution - BB84

Simulate Quantum Systems, Classical ถูกใช้ในการ Simulate Quantum Systems แต่ก็พบปัญหาว่า particles มีขนาดของการใช้ variable มากขึ้นเรื่อย ๆ ทำให้ ไม่สามารถทำได้ (exponential overhead) หมายความว่าเราไม่สามารถใช้ Classical; จำลองขึ้นมาได้ โดย Quantum Computing $\neq$ Turing Machine Killer feature ณ​ ตอนนี้เช่น Quantum chemistry ที่ simulate ระดับ particle ได้, Shor’s Algorithms ในการหา factorization จำนวนมหาศาล

## Touring Machine
Touring Machine ประกอบไปด้วย software แล้วก็ตัวประมวลผลตาม software ที่ได้ access เข้าไป

![[Pasted image 20250606160948.png]]

### Extended Church-Turing Thesis
Extended Church-Turing Thesis ว่าด้วยการคำนวนที่เป็นไปได้และอยู่บน phyiscal world จะสามารถคำนวนได้ดีใน Turing machine

### P vs NP
##### P
ปัญหาที่แก้ได้ดีใน classical มักอยู่ในรูปของ $L \subseteq \{0,1\}*$ โดยที่มี input $x \in L$ โดยที่ ถ้าปัญหาเรานี้ถูกแก้ได้ด้วยเวลา Polynomial จาก Input แล้วสามารถแก้ไขปัญหาได้ด้วย การตัดสินใจ นั้นคือปัญหาที่แก้ได้ด้วย Classical Computing i.e. คือปัญหาถูกแก้ได้แน่นอนจากการประมวลผลข้อมูลนำเข้า

ตัวอย่างเช่น: หาจำนวน Prime, Linear Programing หรือการหา Path ในการเดินทาง

![[Pasted image 20250606162407.png]]

#### NP
NP (Nondeterministic Polynomial-Time) เป็นโปรแกรมที่ แก้ไขปัญหาได้ยากมาก ๆ แต่สามารถตรวจสอบความถูกต้องในรูปเวลา Polynomial ได้ 

เช่นหา factorization โปรแกรม ให้ Input เลขเข้าไปแล้วได้ Array ออกมานั้นทำได้ยากมากใช้เวลานานมากๆ (Big-O อย่าง $2^n$ หรือใด ๆ ที่ n เป็นตัวยกกำลัง) แต่เราสามารถตรวจไปเรื่อย ๆ ว่าเลขไหนบ้าง คู่กับเลขไหนเป็น factorization ของเลขที่เราสนใจอยู่ ได้ง่ายมากๆ

ตัวอย่างเช่น Factoring, Bin Packing, Theorem Proving and Traveling Salesperson.

![[Pasted image 20250606164201.png]]

## BQP
**การแยกตัวประกอบจำนวนเต็ม (Integer Factorization) อยู่ในคลาส BQP** ซึ่งหมายถึงปัญหาที่แก้ได้โดย Quantum Computing ภายในเวลา Polynomial แต่คำตอบจะเป็นแบบ **probabilistic** เท่านั้น ไม่ได้การันตีว่าได้คำตอบแน่นอน 100%

ตาม [[#Extended Church-Turing Thesis]] ถ้าเราแก้ปัญหาได้ดีในโมเดลหนึ่ง ปัญหาคล้ายกันในโมเดลอื่นก็ควรจะแก้ได้ดีเช่นกัน แต่ Quantum Computing ดูเหมือนจะท้าทาย Thesis นี้ เพราะมันให้คำตอบแบบ probabilistic ไม่ใช่ deterministic

อย่างไรก็ตาม นี่ไม่ได้แปลว่า Thesis ผิด เพราะเราไม่ได้มี proof ว่าแก้ไม่ได้ เราแค่ยังไม่มี algorithm ที่ deterministic และแก้ได้ดีในตอนนี้เท่านั้น

## Why Is Building A Quantum Computer So Hard
ตอนนี่เรามีคำถามว่า เราไม่สามารถสร้างได้สมบูรณ์เพราะ law of nature หรือ techonological เรายังแค่ไม่ถึง 

### Coherence
ปัญหาอยู่ที่ว่าเราไม่สามารถ protect Quantum states จาก Noise ได้ (Decoherence)

[My Quantum Debate with Aram Harrow: Timeline, Non-technical Highlights, and Flashbacks I](https://gilkalai.wordpress.com/2013/03/16/my-quantum-debate-with-aram-harrow-timeline-non-technical-highlights-and-flashbacks-i/)

### A Win-Win Situation
Scalable Quantum Computers Are Possible
- Simulation
- Chemistry
- factorization
- Optimization and Machine Learning

Scalable Quantum Computers Are Not Possible
- New Physics understanding!

## NISQ Era
Noisy Intermediate-Scale Quantum คือยุคที่เรามี 50 → 100 นิดๆ qubits

### Noisy
คือปัญหาของการที่เราไม่สามารถควบคุมการทำงานของ qubits ได้ 100% ทำให้เกิด limitation

## Potential Applications of Quantum Computers
Probably
- Cryptography
- Optimization
- Simulation
- Science
- Philosophy

Maybe
- Machine Learning
	- Dequantization

Not Really
- Efficiently solve NP-Complete problems

## Expect QC to Solve

![[Pasted image 20250606171132.png]]

![[Pasted image 20250606171635.png]]

# Reference
[lecture video](https://www.youtube.com/watch?v=-JBdbOlhmMs)