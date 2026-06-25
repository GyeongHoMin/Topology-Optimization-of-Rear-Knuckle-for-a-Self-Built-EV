# Topology Optimization of Rear Knuckle for a Self-Built EV

> **69.25% weight reduction** while maintaining a minimum safety factor of **3.14** under cornering conditions.

This repository contains the paper and poster presented at the **2025 KSAE (Korean Society of Automotive Engineers) Conference**, conducted by the SV Student Formula Car Research Club at Hankyong National University.

---

## 📌 Background

In student EV competitions, reducing component weight is critical for improving driving performance and efficiency. The rear knuckle used in the **2024 KSAE Student-Built EV Competition** had a split-type structure that unintentionally increased overall mass due to additional thickness at the joint. Furthermore, the use of a thinner bearing led to axial play in the rear axle shaft during driving.

This study aimed to resolve these issues by proposing a new integrated (one-piece) knuckle design that simultaneously achieves **lightweight construction** and **structural integrity**.

---

## 🔧 Methodology

### 1. Load Analysis
Equivalent loads acting on the rear knuckle were calculated under three driving conditions:

| Condition | Rear Wheel Load (one side) |
|-----------|---------------------------|
| Acceleration | 1,236.83 N |
| Braking | 423.02 N |
| Cornering (outer) | 1,181.65 N |

- Vehicle mass: **280 kg**, wheelbase: **1,300 mm**, CG height: **270 mm**
- Dynamic load factor of **1.3** applied to account for vibration and road impact
- Contact forces and moments at the bearing center were derived and used as FEA boundary conditions

### 2. Material Selection
**AL6061-T6** was selected based on:
- No failure history in previous knuckle designs using the same material
- 0.2% offset yield strength of **240 MPa**, fully satisfying structural requirements
- Approximately **2× lower CNC machining cost** compared to AL7075-T6

### 3. Topology Optimization
- Tool: **Altair Inspire 2025**
- Objective: Maximize stiffness
- Target mass: **0.500 kg**
- Caliper and arm mounting regions were excluded from the design space

Optimization was run separately under acceleration, braking, and cornering loads. All three results showed structurally similar trends, confirming common high-stress regions that required reinforcement.

### 4. Redesign & Additional Weight Reduction
Based on topology results, the knuckle was redesigned using **AutoCAD 2026** and **Fusion 2026**. Low-stress regions around the bearing area were identified and material was removed in three steps (±4 mm, ±6 mm, ±8 mm per side) to find the optimal balance between weight and structural safety.

---

## 📊 Results

### Safety Factor Comparison

| Condition | Initial Shape (1.626 kg) | Final Shape (0.500 kg) | Change |
|-----------|--------------------------|------------------------|--------|
| Acceleration | 9.90 | 4.28 | −56.77% |
| Braking | 12.05 | 5.69 | −52.78% |
| Cornering | 4.69 | 3.14 | −33.05% |

### Weight Reduction Summary

| Comparison | Mass | Reduction |
|------------|------|-----------|
| Initial shape → Final shape | 1.626 kg → 0.500 kg | **−69.25%** |
| 2024 knuckle → Final shape | 0.563 kg → 0.500 kg | **−11.29%** |

### Final Shape Analysis
- Maximum von Mises stress: **76.39 MPa** (cornering)
- Minimum safety factor: **3.14** (cornering) — exceeds the target range of 2.7–2.9
- Stress distribution was uniformized, improving overall structural efficiency
- Fillets were applied at sharp edges to reduce stress concentration and improve CNC machinability

---

## 🛠️ Tools Used

| Category | Tool |
|----------|------|
| Topology Optimization & FEA | Altair Inspire 2025 |
| CAD Redesign | Autodesk AutoCAD 2026, Fusion 2026 |
| Stress Criterion | Von Mises Stress |
| Safety Factor Formula | S.F = R_P0.2 / σ_v |

---

## 📁 Repository Structure

```
rear-knuckle-optimization/
│
├── README.md
├── paper/
│   └── KSAE2025_Rear_Knuckle_Optimization.pdf
└── poster/
    └── KSAE2025_Poster.pdf
```

---

## 🔭 Future Work

- **Fatigue life evaluation** and durability testing under real driving conditions
- **Nonlinear dynamic analysis** incorporating dynamic load variation and vibration during driving

---

## 👥 Authors

**Gyeongho Min · Bomyeong Seo · Kangmin Kim**  
Department of Mechanical Engineering, Hankyong National University  
Anseong-si, Gyeonggi-do, Korea

---

## 📄 Citation

If you reference this work, please cite the original KSAE 2025 conference paper:

```
Min, G., Seo, B., Kim, K., "Optimization of Rear Knuckle Design for a Self-Built EV
Considering Weight Reduction and Structural Strength," Proceedings of KSAE 2025.
```

---

*This work was supported by the Hankyong National University Development Project.*
