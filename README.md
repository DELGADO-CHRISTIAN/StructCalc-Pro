# StructCalc Pro

> 🚧 **This project is currently under active development. Features may be incomplete or subject to change.**

<div align="center">

![Flutter](https://img.shields.io/badge/Flutter-3.32.0-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-3.8.0-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Status](https://img.shields.io/badge/Status-In%20Progress-orange?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20iOS%20%7C%20Windows-lightgrey?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**A professional structural & civil engineering toolkit built with Flutter.**  
Beam calculations · Column design · AR measurement · 3D modeling · AutoCAD-style floor plans

</div>

---

## ⚠️ Work In Progress

This application is actively being built. The table below shows the current state of each feature:

| Feature | Status | Notes |
|---|---|---|
| Beam Calculator | ✅ Complete | Simply supported beam — M, V, δ |
| Column Load | ✅ Complete | Euler buckling + slenderness ratio |
| Unit Converter | ✅ Complete | Force, Stress, Length, Mass, Moment |
| Floor Plan Designer | 🔄 In Progress | AutoCAD-style, furniture library |
| 3D Model Maker | 🔄 In Progress | Blender-style viewport, matrix engine |
| 3D Model Viewer | 🔄 In Progress | Wireframe on Windows, .glb on mobile |
| AR Measurement | 🚧 Planned | Requires physical Android/iOS device |
| Export to PDF | 🚧 Planned | Floor plans + calculation reports |
| Material Database | 🚧 Planned | Steel sections, concrete grades |
| RC Beam Design | 🚧 Planned | ACI 318 / NSCP code compliance |
| Foundation Design | 🚧 Planned | Spread footing calculator |
| Wind Load | 🚧 Planned | ASCE 7 wind pressure calculator |

> Legend: ✅ Complete · 🔄 In Progress · 🚧 Planned

---

## 📱 Screenshots

> Screenshots will be added as the UI is finalized.

---

## ✨ Features Overview

### 📐 Engineering Calculators
- **Beam Calculator** — Computes max bending moment (`M = wL²/8`), shear force (`V = wL/2`), and mid-span deflection (`δ = 5wL⁴/384EI`) for simply supported beams under uniform distributed loads.
- **Column Load** — Euler buckling load (`Pcr = π²EI/(KL)²`), slenderness ratio (`λ = KL/r`), and safety status with support for pin-pin, fixed-free, fixed-pin, and fixed-fixed end conditions.
- **Unit Converter** — Converts between engineering units across Force (N, kN, kip, lbf), Pressure/Stress (Pa, kPa, MPa, psi), Length (m, cm, mm, ft, in), Mass (kg, t, lb), and Moment (N·m, kN·m, lbf·ft).

### 📷 AR & 3D Tools
- **AR Measurement** — Uses the phone camera to measure distances by tapping two points on screen. Calibrated scale slider. Supports m/cm and ft/in units.
- **3D Model Viewer** — Interactive wireframe 3D viewer with perspective projection, orbit/zoom controls, and multiple structural models (building, steel frame, bridge). Loads `.glb` files on Android/iOS.
- **3D Model Maker** — Blender-style 3D editor with a full matrix-based rendering engine (model → view → projection pipeline), diffuse lighting, depth sorting, and structural primitives (cube, sphere, cylinder, cone, plane). Add, transform, scale, and color objects.
- **Floor Plan Designer** — AutoCAD-style floor plan editor with grid snapping, ortho mode, wall chaining, dimension labels, 16 furniture symbols (sofa, beds, bath, toilet, kitchen, etc.), door swing arcs, window pane symbols, column markers, stair blocks, undo/redo, and a professional title block.

---

## 🚀 Getting Started

### Prerequisites
- [Flutter SDK 3.32+](https://flutter.dev/docs/get-started/install)
- Dart 3.8+
- Android Studio (for Android emulator) or a physical device
- VS Code with Flutter extension (recommended)

### Installation

```bash
# 1. Clone this repository
git clone https://github.com/DELGADO-CHRISTIAN/StructCalc-Pro.git

# 2. Navigate into the project
cd StructCalc-Pro

# 3. Install dependencies
flutter pub get

# 4. Run on Windows (for testing without a phone)
flutter run -d windows

# 5. Run on Android phone (connect via USB with USB debugging ON)
flutter run -d android
```

### Project Structure

```
lib/
├── main.dart                        ← App entry point
└── screens/
    ├── home_screen.dart             ← Main menu
    ├── beam_calculator_screen.dart  ← Beam design
    ├── column_load_screen.dart      ← Column design
    ├── unit_converter_screen.dart   ← Unit conversion
    ├── ar_measurement_screen.dart   ← AR camera tool
    ├── model_viewer_screen.dart     ← 3D model viewer
    ├── model_maker_screen.dart      ← 3D model builder
    └── floor_plan_screen.dart       ← Floor plan CAD
```

---

## 🗺️ Roadmap

```
v1.0  ✅  Core calculators (beam, column, unit converter)
v1.5  🔄  3D tools + Floor plan designer  ← CURRENT
v2.0  🚧  AR camera measurement (physical device)
v2.5  🚧  PDF export for calculations and floor plans
v3.0  🚧  RC beam design (ACI 318 / NSCP)
v3.5  🚧  Foundation + wind load calculators
v4.0  🚧  Material & section database
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Framework | Flutter 3.32 / Dart 3.8 |
| 3D Engine | Custom matrix pipeline (CustomPainter) |
| CAD Engine | Custom vector renderer (CustomPainter) |
| State | StatefulWidget (no external state lib) |
| Platform | Windows · Android · iOS · Web |

---

## 📋 Engineering Formulas Reference

| Calculation | Formula |
|---|---|
| Beam max moment (UDL) | `M = wL² / 8` |
| Beam max shear (UDL) | `V = wL / 2` |
| Beam mid deflection | `δ = 5wL⁴ / (384EI)` |
| Euler buckling load | `Pcr = π²EI / (KL)²` |
| Slenderness ratio | `λ = KL / r` |

---

## 🤝 Contributing

This project is currently a solo work-in-progress. Contributions, suggestions, and issue reports are welcome once the v1.5 milestone is reached.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -m 'Add my feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## 👤 Author

**Delgado Christian**  
Engineering App Developer  
GitHub: [@DELGADO-CHRISTIAN](https://github.com/DELGADO-CHRISTIAN)

---
