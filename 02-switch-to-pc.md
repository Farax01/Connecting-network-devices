# Lesson 02 — Switch to PC / Server Connections

This is usually the first wiring you'll do in any network — connecting your end devices (PCs, servers) to a switch.

---

## Pin Wiring Diagram (to be added later)
---

## Understanding TX and RX Pins

Every Ethernet interface has **transmit (TX)** pins and **receive (RX)** pins. The key rule is:

> A device's **transmit pins** must connect to the other device's **receive pins**. Otherwise no data flows.

Here's how PCs and switches are set up by default:

| Device  | Transmits on | Receives on |
|---------|--------------|-------------|
| PC      | Pins 1 & 2   | Pins 3 & 6  |
| Server  | Pins 1 & 2   | Pins 3 & 6  |
| Switch  | Pins 3 & 6   | Pins 1 & 2  |

Notice they're **opposites**. A PC transmits on 1 & 2, and the switch receives on 1 & 2. A switch transmits on 3 & 6, and the PC receives on 3 & 6.

Because they're already set up as opposites, a **straight-through cable** works perfectly — no need to cross anything.

---

## The Connection

```
PC                          Switch
[TX: 1 & 2] ───────────▶ [RX: 1 & 2]
[RX: 3 & 6] ◀─────────── [TX: 3 & 6]
```

✅ Use a **straight-through copper cable**

---

## In Packet Tracer

When connecting a PC to a switch in Packet Tracer:

1. Select **Copper Straight-Through** from the cable menu (bottom left)
2. Click the PC → select **FastEthernet0** (this is the NIC)
3. Click the switch → select any available **FastEthernet** port

The same applies for servers — they behave just like PCs electrically.

---

## Common Mistake

People sometimes reach for a crossover cable thinking "the PC is connecting to a network device so I need a special cable." Nope. The logic isn't about the device's role — it's about what the **pins are doing**. Since PC and switch pins are already opposites, straight-through is correct.

---
