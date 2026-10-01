[← T-23: 1-Phase Starting Methods](T-23_Single-Phase_IM_Starting_Methods.md) | [🏠 Index](README.md) | [T-25: Misc Induction Motor Topics →](T-25_Miscellaneous_IM_Topics.md)

---

# T-24: Single Phasing

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Single Phasing** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2018 Q6(a)]
> 📋 **Appeared in:** 2018 Q6(a)

**(a) What is single phasing? Explain its effect on a 3-phase induction motor. [04]**

**Single phasing:** One of the three supply phases is lost while the motor is running. This can happen due to a blown fuse, a broken supply wire, or a faulty contactor contact.

**Effects on a running 3-phase motor:**

1. **Unbalanced supply:** Only two phases now feed the stator. The magnetic field becomes pulsating and unbalanced instead of uniformly rotating.

![3-Phase Supply Stator connection showing three phase winding supply](../Books/diagrams/Ch-34_p09_fig11.jpg)

2. **Higher current in remaining phases:** To maintain the same torque, current in the two active phases increases by 1.5–2 times normal. This causes overheating in the active stator windings.

3. **Speed may drop:** The motor can continue running (it developed enough momentum) but with reduced torque and higher slip.

4. **Torque dip:** The pulsating component of the magnetic field produces oscillating torque. The motor vibrates and runs noisily.

5. **Motor may burn out:** Sustained single-phase operation causes overheating in two windings. Without a protection relay (negative-sequence relay or thermal overload), the motor will eventually fail.

**Protection:** Use negative-sequence relays or single-phase preventers to detect and trip on single phasing.

---

[← T-23: 1-Phase Starting Methods](T-23_Single-Phase_IM_Starting_Methods.md) | [🏠 Index](README.md) | [T-25: Misc Induction Motor Topics →](T-25_Miscellaneous_IM_Topics.md)
