# Lesson 03 — Switch to Switch Connections

When two switches need to talk to each other, you've got a problem with straight-through cables: both switches transmit on the same pins (3 & 6) and receive on the same pins (1 & 2). So if you use a straight-through cable, you'd be connecting transmit → transmit and receive → receive. Nothing would get through.

The fix is a **crossover cable** — it swaps the pairs so each device's transmit pins hit the other's receive pins.

---

## Pin Wiring Diagram (to be added later)
---

## Why Crossover Is Required

| Device   | Transmits on | Receives on |
|----------|--------------|-------------|
| Switch A | Pins 3 & 6   | Pins 1 & 2  |
| Switch B | Pins 3 & 6   | Pins 1 & 2  |

With a straight-through cable:
```
Switch A [TX: 3&6] ──▶ Switch B [TX: 3&6]  ❌ TX into TX
Switch A [RX: 1&2] ◀── Switch B [RX: 1&2]  ❌ RX into RX
```

With a crossover cable:
```
Switch A [TX: 3&6] ──▶ Switch B [RX: 1&2]  ✅
Switch A [RX: 1&2] ◀── Switch B [TX: 3&6]  ✅
```

---

## The Rule

> **Same device type = crossover cable** (when using copper)

This applies to:
- Switch ↔ Switch
- Router ↔ Router  
- PC ↔ PC (direct connection)
- Hub ↔ Hub

---

## In Packet Tracer

1. Select **Copper Cross-Over** from the connections panel
2. Click Switch A → pick any available FastEthernet port
3. Click Switch B → pick any available FastEthernet port

The link should come up green on both ends after a moment.

---

## A Note on Auto MDI-X

Modern switches often have **Auto MDI-X** enabled, which automatically detects the cable type and adjusts internally. In practice, you can plug in a straight-through cable between two switches and it'll still work because the switch corrects for it.

But in exams and labs where Auto MDI-X isn't assumed, **always use a crossover** for same-device connections. Build the correct habit.

---
