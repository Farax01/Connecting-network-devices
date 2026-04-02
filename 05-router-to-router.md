# Lesson 05 — Router to Router Connections

Router-to-router links are typically your WAN connections — the long-distance links that tie separate networks together. Two things matter here: **cable type** and **distance**.

---

## Cable Type: Crossover

Since routers are in the same group (both transmit on pins 1 & 2), connecting them with copper requires a **crossover cable**.

```
Router A                      Router B
[TX: 1 & 2] ───────────▶ [RX: 3 & 6]
[RX: 3 & 6] ◀─────────── [TX: 1 & 2]
```

✅ Copper → **crossover cable**

---

## Distance: This Is Where Fiber Comes In

Copper UTP cable caps out at **100 meters**. For anything longer, you're moving to fiber. Here's the decision tree:

```
What's the distance between routers?

├── Under 100m?
│     └── Use copper crossover cable
│
├── 100m – 550m?
│     └── Use multimode fiber
│
└── Over 550m?
      └── Use single-mode fiber
```

---

## Real-World Example from the Lab

Three router-to-router links, three different decisions:

| Link     | Distance  | Cable Decision                                    |
|----------|-----------|---------------------------------------------------|
| R1 ↔ R2  | 50m       | Copper crossover (well within the 100m limit)     |
| R1 ↔ R3  | 3km       | Single-mode fiber (3000m is way past multimode's 550m cap) |
| R3 ↔ R4  | 250m      | Multimode fiber (over copper's limit, but not far enough to need single-mode) |

---

## Fiber in Packet Tracer

Packet Tracer doesn't distinguish between single-mode and multimode — it's just labeled "fiber." In a real exam question though, you're expected to know which type fits the scenario based on distance.

When you connect fiber in Packet Tracer, notice there are **two connectors per end** — one for transmit, one for receive. This mirrors how real fiber cables work: separate strands carry data in each direction.

---

## Summary: The Full Cable Decision Framework

| Connection        | Same TX/RX group? | Cable (copper)  | Notes                          |
|-------------------|--------------------|-----------------|--------------------------------|
| PC → Switch       | No                 | Straight-through| Different groups               |
| Server → Switch   | No                 | Straight-through| Servers behave like PCs        |
| Switch → Router   | No                 | Straight-through| Routers behave like PCs        |
| Switch → Switch   | Yes                | Crossover       | Both in Group B                |
| Router → Router   | Yes                | Crossover       | Both in Group A, watch distance|
| PC → PC (direct)  | Yes                | Crossover       | Both in Group A                |

---
