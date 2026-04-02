# Lesson 04 — Switch to Router Connections

This is where a lot of beginners second-guess themselves. A router is clearly a "different" kind of device from a switch — so which cable do you use?

The answer comes back to pins, not device roles.

---

## How Routers Handle Pins

Routers are wired the same way as PCs:

| Device | Transmits on | Receives on |
|--------|--------------|-------------|
| Router | Pins 1 & 2   | Pins 3 & 6  |
| Switch | Pins 3 & 6   | Pins 1 & 2  |

They're opposites, just like a PC and a switch. So again, a **straight-through cable** does the job.

---

## The Connection

```
Router                        Switch
[TX: 1 & 2] ───────────▶ [RX: 1 & 2]
[RX: 3 & 6] ◀─────────── [TX: 3 & 6]
```

✅ Use a **straight-through copper cable**

---

## The Mental Model

You don't need to memorize every device combination. Just remember two groups:

**Group A — Transmit on pins 1 & 2:**
- PCs
- Servers
- Routers

**Group B — Transmit on pins 3 & 6:**
- Switches
- Hubs

- **Group A ↔ Group B** = straight-through
- **Same group ↔ same group** = crossover

---

## In Packet Tracer

1. Select **Copper Straight-Through**
2. Click the switch → choose a FastEthernet port
3. Click the router → choose the appropriate interface (e.g. GigabitEthernet0/0)

---
