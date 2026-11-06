# Bench measurement evidence and scope

## Pack B — final cell readings

Firmware RAM symbol: `bq7693_cell_voltages`, extracted from the corresponding build ELF. The exact RAM address is intentionally omitted from this public case study.

| Cell | Reading (V) |
|---|---:|
| C1 | 4.152 |
| C2 | 4.151 |
| C3 | 4.160 |
| C4 | 4.153 |
| C5 | 4.146 |
| C6 | 4.154 |
| C7 | 4.147 |

**Total:** 29.063 V. **Maximum–minimum spread:** 0.014 V (14 mV).

These are BMS-reported readouts. They were taken after physical repairs and replacement of seven cells in Pack B; the before/after difference should **not** be interpreted as evidence that the same cells charged from 3.4 to 4.15 V.

## Debugging milestones

| Stage | Recorded value | Interpretation |
|---|---|---|
| Faulted | `0B 07` | Error/status pair in a build-specific BMS state mapping |
| Electrical fault | ~3.89 V across F1 | Abnormal fuse/connection voltage drop |
| Restored readout | 29.063 V total, 14 mV spread | Coherent seven-cell readings |
| Controller state | `00 01` | No active error, IDLE at inspection time |
| Standalone response | LED/button response after a private intervention | Bench response observed; not a functional qualification |

**Limit:** no demonstrated sustained vacuum load test, repeated full charging cycle, or long-term reliability assessment is provided for Pack B.

The specific final standalone-startup electrical diagnosis and corrective method are retained privately by the investigator.
