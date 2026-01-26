# RPX-Hinf-PI

**Version:** 1.0.0  
**Year:** 2025  
**Authors:** M. Schlegel, M. Brabec  
**Support contact:** brabecm@ntis.zcu.cz  

Department of Cybernetics  
Faculty of Applied Sciences  
University of West Bohemia in Pilsen  

---

## Description

A software tool has been developed for designing a PI controller for an LTI SISO system. The tool supports an arbitrary number of design requirements in the form of H-infinity specifications, including the H-infinity norm of weighted sensitivity functions and the H-infinity norm of the sums of the squares of their magnitudes. The tool also supports specifications on the closed-loop pole placement, such as σ-stability and damping of oscillatory modes.

The design method is based on the analytical computation of the solution region boundary in the controller parameter plane.

The tool is available as a standalone executable application.

---

### Supported Hinf constraints

| ID | Name | Constraint |
|---:|------|------------|
| 1 | Sensitivity | `\|\| W_s(s) · S(s) \|\|inf ≤ γ` |
| 2 | Complementary sensitivity | `\|\| W_t(s) · T(s) \|\|inf ≤ γ` |
| 3 | Control sensitivity | `\|\| W_c(s) · Sc(s) \|\|inf ≤ γ` |
| 4 | Process sensitivity | `\|\| W_p(s) · Sp(s) \|\|inf ≤ γ` |
| 5 | Mixed (S, T) | `\|W_s(s)·S(s)\|² + \|W_t(s)·T(s)\|² ≤ γ` |
| 6 | Mixed (S, Sc) | `\|W_s(s)·S(s)\|² + \|W_c(s)·Sc(s)\|² ≤ γ` |
| 7 | Mixed (S, Sp) | `\|W_s(s)·S(s)\|² + \|W_p(s)·Sp(s)\|² ≤ γ` |
| 8 | Mixed (S, Sc, Sp) | `\|W_s(s)·S(s)\|² + \|W_c(s)·Sc(s)\|² + \|W_p(s)·Sp(s)\|² ≤ γ` |
| 9 | Mixed (S, Sc, T) | `\|W_s(s)·S(s)\|² + \|W_c(s)·Sc(s)\|² + \|W_t(s)·T(s)\|² ≤ γ` |

---

## Features

- PI controller design for LTI SISO systems
- Multiple H-infinity design specifications
- Weighted sensitivity and complementary sensitivity shaping
- Closed-loop pole placement constraints
- Analytical computation of solution region boundaries

---

## Usage

1. Provide the plant model in the supported format.
2. Define the H-infinity design specifications.
3. Define the closed-loop pole placement constraints.
4. Run the design procedure to obtain the controller parameters.

---

## System Requirements

- Windows 10 or later
- MATLAB Runtime 2025

## Input format notice

Commas are reserved **only** for separating vector elements and must not be used as decimal separators.

### Examples

```text
Scalar: 3.14
Vector: [1.2, 3.4, 5] or [1.2 3.4 5]
```

---

## License

MIT License (c) 2025 ACROSS-UWB  
See the `LICENSE` file for full license text.  

---

## Acknowledgement

This outcome is linked to the research objective **RO 1.4 – Algorithms for industrial control** and has been supported by the **Roboprox project**  
(CZ.02.01.01/00/22_008/0004590).
