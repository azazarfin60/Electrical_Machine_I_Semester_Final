# T-14: IM as Rotating Transformer

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **IM as Rotating Transformer** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### Q5(b): Why is an IM called a rotating transformer?: Advantages and disadvantages

> 📋 **Appeared in:** 2017 Q1(a), 2019 Q5(b), 2020 Q5(b)

#### Extended advantages list

Beyond simplicity, the squirrel-cage IM has these specific advantages:
- **Completely sealed construction possible:** Since there are no brushes or slip rings, the rotor is electrically isolated from the housing. The motor can be totally enclosed and fan-cooled (TEFC), suitable for dusty, wet, or explosive environments.
- **Self-regulating to some extent:** Under increased load, slip increases slightly, rotor current increases, torque increases to match the load: all without any external control action.
- **No commutator:** No sparking, no radio interference. Safe in hazardous areas.

#### Extended disadvantages list

- **Reactive power consumption:** The motor always draws lagging reactive power from the supply to magnetize its air gap. This degrades the power factor of the supply system and requires capacitor banks for correction.
- **Air gap sensitivity:** Unlike transformers (which have a very thin effective magnetic gap through the iron core), an IM has a physical air gap (0.3–1.5 mm). This air gap requires much more magnetizing current than a comparable transformer, contributing to the poor no-load power factor (typically 0.1–0.3).
- **Hazardous starting conditions:** Without a starter, motors above ~4 kW draw 6–8 times rated current from the supply at the instant of starting.

![Induction motor as a generalized rotating transformer showing stator primary, air gap, and short-circuited rotor secondary](../Books/diagrams/Ch-34_p58_fig45.jpg)

---

