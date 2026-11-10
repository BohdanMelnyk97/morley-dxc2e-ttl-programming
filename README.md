# Morley-IAS DXc2E — 3.3 V TTL programming connector pinout

Community-contributed field note for the **Morley-IAS DXc2E** fire alarm control panel.

> **Source and verification status:** The connector order and 3.3 V TTL programming method were reported from hands-on experience by [BohdanMelnyk97](https://github.com/BohdanMelnyk97). This is **not** manufacturer documentation or an independently verified pinout. Check against the specific panel revision before use.

## Connector pinout

**Orientation:** Viewed as reported, from **top to bottom**. The connector face, board orientation, and viewing side have not been independently documented; confirm pin 1 before connecting anything.

| Position (top → bottom) | Signal | Notes |
| --- | --- | --- |
| 1 | RXD | Receive data on panel |
| 2 | TXD | Transmit data from panel |
| 3 | GND | Signal ground |
| 4 | Unknown | **Leave disconnected** |

**Reported logic level:** **3.3 V TTL** (not RS-232 voltage levels).

## USB-to-TTL adapter wiring

| USB-to-TTL adapter (3.3 V logic) | DXc2E connector |
| --- | --- |
| TXD | Pin 1 — RXD |
| RXD | Pin 2 — TXD |
| GND | Pin 3 — GND |
| No connection | Pin 4 — Unknown |

```text
USB–TTL adapter (3.3 V logic)       Morley-IAS DXc2E
          TXD --------------------> 1  RXD
          RXD <-------------------- 2  TXD
          GND --------------------- 3  GND
          (not connected)           4  Unknown
```

**Do not connect the adapter's 3.3 V/VCC or 5 V power output to the panel.**

## Safety and limitations

- **Fire alarm equipment is safety-critical.** Work only if authorized and qualified; follow the manufacturer instructions and local requirements for isolation, testing, and reinstatement.
- Verify connector orientation, ground reference, and signal voltage using appropriate equipment before connecting an adapter. **Do not assume** the pin numbering applies to other Morley-IAS models or board revisions.
- Use a **3.3 V logic-level USB–TTL interface**, not a true RS-232 adapter and not 5 V TTL.
- This note does **not** establish the serial baud rate, framing, software compatibility, or any programming procedure.
- Do not change panel configuration or interrupt a live fire detection system without the necessary precautions, approvals, and commissioning checks.

## Contributing

If you can confirm the connector orientation, board revision, fourth pin, baud rate, or supported programming software, please open an issue or pull request with non-sensitive technical evidence.

## Disclaimer

Unofficial community information provided **as-is**, without manufacturer endorsement or warranty. Verify all connections independently. The authors are not affiliated with Morley-IAS or Honeywell.
