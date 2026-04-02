# Lesson 01 — The Three Cable Types You Need to Know

Before you plug anything in, you need to understand what cable to reach for. 
There are three you'll encounter constantly in networking: 
**straight-through**, 
**crossover**, and 
**fiber**.

---

## Visual Overview (to be added later)

---

## 1. Copper Straight-Through Cable

This is your everyday workhorse. The wire on pin 1 on one end connects to pin 1 on the other end, pin 2 to pin 2, and so on — straight through, no crossing.

You use this when connecting **devices of different types** — for example, a PC to a switch, or a router to a switch.

```
End A                End B
Pin 1 ─────────────▶ Pin 1
Pin 2 ─────────────▶ Pin 2
Pin 3 ─────────────▶ Pin 3
Pin 6 ─────────────▶ Pin 6
```

---

## 2. Copper Crossover Cable

This one swaps the transmit and receive pairs. Pin 1 on one end connects to pin 3 on the other, and pin 2 connects to pin 6.

You use this when connecting **devices of the same type** — switch to switch, router to router, PC to PC. If you don't cross the wires, both devices end up transmitting to each other's transmit pins, and nothing works.

```
End A                End B
Pin 1 ─────────────▶ Pin 3
Pin 2 ─────────────▶ Pin 6
Pin 3 ─────────────▶ Pin 1
Pin 6 ─────────────▶ Pin 2
```

> **Note:** Modern switches support **Auto MDI-X**, which means they automatically detect and fix a wrong cable type. But for the CCNA, assume this isn't available and pick your cable correctly.

---

## 3. Fiber-Optic Cable

When copper cable just can't cover the distance (UTP maxes out at **100 meters**), you switch to fiber. Fiber uses light instead of electrical signal, so it travels much farther and isn't affected by electromagnetic interference.

There are two types:

### Multimode Fiber
- Uses **multiple light paths** (modes) bouncing through a wider core
- Good for **medium distances** — up to around **550 meters**
- Cheaper than single-mode
- Common inside buildings or across a campus

### Single-Mode Fiber
- Uses a **single, focused light path** through a narrower core
- Built for **long distances** — 10km, 40km, even more
- More expensive
- Used for connections between cities, data centers across a campus, or any long WAN link

---

## Choosing the Right Fiber: Distance Is Everything

| Distance          | Cable Choice         |
|-------------------|----------------------|
| 0 – 100m          | UTP copper (any type)|
| 100m – 550m       | Multimode fiber      |
| 550m and beyond   | Single-mode fiber    |

---

## Summary

- **Same device type** → crossover
- **Different device types** → straight-through
- **Too far for copper** → fiber (multimode for medium, single-mode for long)

---

## Real-World Cable Photos

For photos of actual cables and connectors, these are good reference points:
- **RJ45 wiring color order** — search "T568B wiring diagram" for the standard color sequence used in straight-through cables
- **Crossover vs straight-through physical** — both look identical externally; the difference is only in how the internal wires are crossed
- **Fiber connectors** — LC connectors are most common in modern networking; SC connectors are also widely used. Single-mode fiber cables are typically **yellow**, multimode are **orange or aqua**
