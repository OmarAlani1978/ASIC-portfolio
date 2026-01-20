# Precision Bandgap Reference – Requirements Specification

## 1. Purpose
The purpose of this block is to generate a stable, temperature- and supply-
independent voltage reference for use in mixed-signal and power management
circuits.

The reference is intended as a reusable analog IP block suitable for integration
into larger SoCs.

---

## 2. Process Technology
| Parameter | Value |
|---------|------|
| Process | SkyWater 130nm CMOS |
| Device Types | 1.8 V core devices |
| Temperature Range | –40 °C to +125 °C |

---

## 3. Electrical Specifications

### 3.1 Supply
| Parameter | Min | Typ | Max |
|--------|-----|-----|-----|
| Supply Voltage (VDD) | 1.7 V | 1.8 V | 1.9 V |

---

### 3.2 Output Reference
| Parameter | Target |
|---------|--------|
| Nominal VREF | 1.20 V |
| Initial Accuracy | ±1.5 % (untrimmed) |
| Load Regulation | < 1 mV / 100 µA |
| Output Current Capability | ≥ 100 µA |

---

### 3.3 Temperature Performance
| Parameter | Target |
|---------|--------|
| Temperature Coefficient | < 50 ppm/°C |
| Operating Range | –40 °C to +125 °C |

---

### 3.4 Line Sensitivity / PSRR
| Parameter | Target |
|---------|--------|
| DC Line Regulation | < 2 mV/V |
| PSRR @ 1 kHz | > 60 dB |
| PSRR @ 100 kHz | > 40 dB |

---

### 3.5 Startup Behavior
| Parameter | Target |
|---------|--------|
| Startup Circuit | Required |
| Startup Time | < 10 µs |
| Guaranteed Start | Across all PVT corners |

---

## 4. Functional Requirements

- The bandgap shall start reliably from power-off without external biasing.
- The reference shall be stable for all specified supply and temperature corners.
- The output shall be stable for capacitive loads up to 50 pF.
- No external trimming is required for baseline operation.

---

## 5. Verification Requirements

The following simulations are mandatory:

### 5.1 DC and Operating Point
- Nominal conditions
- All process corners

### 5.2 Temperature Sweep
- –40 °C to +125 °C
- Extraction of temperature coefficient

### 5.3 Supply Sweep
- VDD min to max
- Line regulation extraction

### 5.4 Startup Transient
- Cold start
- Worst-case corner

---

## 6. Layout Requirements

- Matched devices shall use common-centroid techniques where applicable.
- Sensitive nodes shall be shielded.
- Guard rings shall be used to reduce substrate noise coupling.
- Layout shall pass DRC and LVS without waivers.

---

## 7. Deliverables

- Schematic and simulation netlists
- Verified layout (GDS)
- LVS/DRC reports
- Performance summary document
- Reusable symbol and documentation

