*(start)* | [🏠 Index](00_Index.md) | [T-01: Transformer Fundamentals →](T-01_Transformer_Fundamentals.md)

---

# T-00: Core Fundamentals — What You Should Know Before Starting

> This is not a topic that will appear in your exam. This is just a friendly warm-up. Read it once, casually, and you'll find that every other topic in this course suddenly makes more sense.

---

## What Is This Course Really About?

Electrical machines — transformers, motors, generators — are just devices that convert energy using **magnetic fields**. That's it. A transformer converts AC voltage from one level to another. A motor converts electrical energy to mechanical rotation. A generator does the reverse.

The entire course boils down to understanding:
1. How magnetic fields are created
2. How changing magnetic fields produce voltage
3. How current-carrying conductors feel force in magnetic fields

If you understand these three things, you understand electrical machines. Everything else is just applying them to specific devices.

---

## The Materials — What Machines Are Made Of

### Why Copper Everywhere?

Open up any motor or transformer and you'll see copper wire coils. Why copper? Because it conducts electricity really well (second only to silver, which costs a fortune) and it's tough enough to be wound tightly around iron cores without breaking. That's it. Practical + affordable = copper wins.

### What About Aluminium?

Aluminium is cheaper and lighter, but it doesn't conduct as well. To carry the same current with the same losses, you need a **thicker** aluminium wire — about 1.6 times the cross-section of copper. So aluminium makes the machine bigger. It's used where size isn't a problem — like the rotor bars inside induction motors (those thick bars cast right into the rotor) or flat foil windings in some transformers.

Fun fact: aluminium transformer tanks actually reduce stray losses because aluminium isn't magnetic.

### Carbon Brushes

In machines with rotating parts that need electrical contact (like DC motors), carbon brushes slide against the spinning shaft. Carbon is used because it's self-lubricating — it won't scratch up the metal surface. And here's a neat trick of physics: carbon's resistance *drops* when it heats up, so the voltage drop across the brush stays roughly constant (~1–2 V) no matter how much current flows. That's why we treat brush drop as a fixed number, not a variable.

### The Iron Core

The iron (actually silicon steel) core is what makes machines practical. Iron has a **relative permeability** ($\mu_r$) of about 2500 to 4000. In plain language: magnetic field lines *love* flowing through iron. They concentrate inside it. Without iron cores, you'd need enormous currents to create useful magnetic fields.

**Soft steel** (easy to magnetize and demagnetize) is used for machine cores because the magnetic field reverses every half cycle in AC machines. **Hard steel** (difficult to demagnetize) makes permanent magnets.

One more thing: **silicon is added to the steel** (up to about 4.5%) to reduce energy losses in the core. More silicon = less loss, but too much makes the steel brittle and it cracks when you try to cut lamination shapes from it.

**CRGO steel** (grain-oriented) has its crystals aligned in one direction — amazing permeability along that direction, poor in others. Perfect for **transformers** where flux goes in straight lines. **Non-oriented steel** works equally in all directions — used in **rotating machines** where flux rotates in space.

---

## The Laws — How Machines Actually Work

Don't worry about memorizing these. Just understand *what* each law tells you. When you need the formulas later in specific topics, they'll come naturally.

### "Current creates magnetic field" — Ampere's Law

Pass current through a wire, and a magnetic field appears around it. Wrap that wire into a coil with $N$ turns and the field gets $N$ times stronger. That's essentially what every machine winding does.

$$\mathcal{F} = NI \quad \text{(magnetomotive force — the "push" that creates flux)}$$

The more turns and the more current, the stronger the magnetic field. Simple.

### "Changing magnetic field creates voltage" — Faraday's Law

This is the single most important law in the entire course. If the magnetic flux through a coil changes with time, a voltage appears across the coil:

$$e = N \frac{d\Phi}{dt}$$

**No change = no voltage.** A steady magnetic field sitting there does nothing. You need *change* — either the field itself changes (like in a transformer where AC flux oscillates), or the conductor moves through the field (like in a generator where the rotor spins).

This one equation is behind:
- The EMF equation of transformers ($E = 4.44 f N \Phi_m$)
- The voltage induced in induction motor rotors
- Basically every "where does the voltage come from?" question

### "Induced effects oppose the cause" — Lenz's Law

When Faraday's law creates a voltage, the resulting current flows in a direction that *fights back* against whatever caused it. If flux is increasing, the induced current creates flux in the opposite direction to slow it down. If flux is decreasing, the induced current tries to maintain it.

This is why:
- A transformer's primary draws more current when you load the secondary
- An induction motor's rotor can never reach synchronous speed (if it did, there'd be no change, no induced voltage, no torque)

### "Moving charges feel force in a magnetic field" — Lorentz Force

Put a current-carrying conductor in a magnetic field and it feels a mechanical force:

$$F = BIL$$

(Force = flux density × current × length of conductor in the field)

This is literally how **every motor produces torque**. Current flows in the rotor conductors, the stator creates a magnetic field, and the force between them spins the rotor.

Quick memory aid:
- **Same-direction currents attract** each other
- **Opposite-direction currents repel** each other

### The Dot Convention (for transformers)

When two coils share a magnetic core, dots mark which terminals have the **same polarity at the same instant**. If the dot on the primary is positive right now, the dot on the secondary is also positive right now.

You'll use this when studying transformer connections and three-phase winding groups. For now, just know it exists and that's what the dots mean on circuit diagrams.

---

## Magnetic Circuits — Thinking About Flux Like Current

This is a really elegant trick. Instead of solving complicated field equations, we treat magnetic flux paths like electric circuits:

| Think of it as... | Electric Circuit | Magnetic Circuit |
|:---|:---|:---|
| **The "push"** | Voltage ($V$) | MMF = $NI$ |
| **What flows** | Current ($I$) | Flux ($\Phi$) |
| **What opposes** | Resistance ($R$) | Reluctance ($\mathcal{R} = l / \mu A$) |

So just like $I = V/R$, we have:

$$\Phi = \frac{NI}{\mathcal{R}}$$

And just like resistors, reluctances add in series and combine in parallel using the same rules you already know.

### The Air Gap Story

Here's something that will keep coming up throughout the course:

**Even a tiny air gap has huge reluctance compared to iron.**

Iron has $\mu_r \approx 3000$. Air has $\mu_r = 1$. So a 0.5 mm air gap can contribute *more reluctance than 40 cm of iron*. This has real consequences:

- **Transformers** have a continuous iron core with no air gap → they need very little magnetizing current.
- **Induction motors** *must* have an air gap (the rotor needs room to spin!) → they need much more magnetizing current → that's why their power factor is lower.

Every time you wonder "why does this motor draw so much no-load current?" — the answer is the air gap.

---

## The Per-Unit System — Making Numbers Friendly

In power systems, actual numbers are awkward. A generator might produce 11,000 V and 5,000 A while having a winding impedance of 0.3 Ω. These wildly different magnitudes make calculations messy.

The per-unit system fixes this by dividing everything by a "base" value:

$$\text{per-unit value} = \frac{\text{actual value}}{\text{base value}}$$

You pick two bases (usually rated voltage and rated MVA from the nameplate), and everything else follows. The result? All values end up near 1.0, and — the best part — **the $\sqrt{3}$ factor disappears** from three-phase calculations.

The key formula you'll actually use:

$$Z_{\text{base}} = \frac{V_{\text{base}}^2}{S_{\text{base}}}$$

And when you need to convert impedance from one machine's base to another:

$$Z_{\text{pu,new}} = Z_{\text{pu,old}} \times \left(\frac{V_{\text{old}}}{V_{\text{new}}}\right)^2 \times \frac{S_{\text{new}}}{S_{\text{old}}}$$

You'll see per-unit values in OC/SC tests, transformer equivalent circuits, and anywhere machines of different ratings connect together.

---

## How All This Connects to the Rest of the Course

Here's the payoff — a quick map of where these fundamentals show up:

| You learned... | You'll use it in... |
|:---|:---|
| Faraday's law | Transformer EMF equation, IM rotor EMF |
| Lenz's law | Why transformers draw more current under load, why IM rotor can't reach $N_s$ |
| Lorentz force ($F = BIL$) | Torque production in every motor |
| Magnetic circuit analogy | Building equivalent circuits for transformers and IMs |
| Air gap = high reluctance | Why IM needs large magnetizing current |
| Core losses (hysteresis + eddy) | OC test in transformers, no-load test in IM |
| CRGO vs non-oriented steel | Why transformer and motor cores are different |
| Per-unit system | OC/SC test calculations, referring impedances across windings |
| Dot convention | Transformer polarity, three-phase connections |

That's it. You now have the mental scaffolding for the entire course. Go read T-01 and you'll see how naturally these concepts flow into transformer theory. 🚀

---

*(start)* | [🏠 Index](00_Index.md) | [T-01: Transformer Fundamentals →](T-01_Transformer_Fundamentals.md)
