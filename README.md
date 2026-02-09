# RPX-H-inf-PI

**Version:** 1.0.0  
**Year:** 2025  
**Authors:** M. Schlegel, M. Brabec  
**Support contact:** brabecm@ntis.zcu.cz  

Department of Cybernetics  
Faculty of Applied Sciences  
University of West Bohemia in Pilsen  

---

## Description

A software tool has been developed for PI controller design for an LTI SISO system. The tool supports an arbitrary number of design requirements in the form of H-inf specifications, including the H-inf norm of weighted sensitivity functions and the H-inf norm of the sums of the squares of their magnitudes. In addition to classical H-inf specifications, frequency-limited requirements on the sensitivity function can also be defined in the form ∣S(jω)∣≤ε for ω∈⟨ω1,ω2⟩. The tool also supports specifications on the closed-loop pole placement, such as σ-stability and damping of oscillatory modes.

The design method is based on the analytical computation of the boundary of the feasible solution region in the controller parameter plane. The resulting region contains all solutions satisfying the specified design constraints. The optimal PI controller parameters are selected from this region based on the IE (Integral Error) criterion.

The tool is available as a standalone executable console application.

---

### Supported Hinf constraints

| ID | Name | Constraint |
|---:|------|------------|
| 1 | Sensitivity | `\|\| W_s(s) · S(s) \|\|inf ≤ γ` |
| 2 | Complementary sensitivity | `\|\| W_t(s) · T(s) \|\|inf ≤ γ` |
| 3 | Control sensitivity | `\|\| W_c(s) · Sc(s) \|\|inf ≤ γ` |
| 4 | Process sensitivity | `\|\| W_p(s) · Sp(s) \|\|inf ≤ γ` |
| 5 | Mixed (S, T) | `\|\| \|W_s(s)·S(s)\|² + \|W_t(s)·T(s)\|² \|\|inf ≤ γ` |
| 6 | Mixed (S, Sc) | `\|\| \|W_s(s)·S(s)\|² + \|W_c(s)·Sc(s)\|² \|\|inf ≤ γ` |
| 7 | Mixed (S, Sp) | `\|\| \|W_s(s)·S(s)\|² + \|W_p(s)·Sp(s)\|² \|\|inf ≤ γ` |
| 8 | Mixed (S, Sc, Sp) | `\|\| \|W_s(s)·S(s)\|² + \|W_c(s)·Sc(s)\|² + \|W_p(s)·Sp(s)\|² \|\|inf ≤ γ` |
| 9 | Mixed (S, Sc, T) | `\|\| \|W_s(s)·S(s)\|² + \|W_c(s)·Sc(s)\|² + \|W_t(s)·T(s)\|² \|\|inf ≤ γ` |

---

## Features

- PI controller design for LTI SISO systems
- Multiple H-inf design specifications
- Weighted sensitivity and complementary sensitivity shaping
- Frequency-limited requirements on the sensitivity function
- Closed-loop pole placement constraints
- Analytical computation of solution region boundaries
- Selection of the final solution based on the IE criterion

---

## Usage

1. Provide the plant model in the supported format.
2. Define the H-inf design specifications.
3. Define frequency-limited requirements on the sensitivity function.
4. Define the closed-loop pole placement constraints.
5. Run the design procedure to obtain the controller parameters.

---

## System Requirements

- Windows 10 or later
- MATLAB Runtime 2025b (www.mathworks.com/products/compiler/matlab-runtime.html)

---

## Input format notice

Commas are reserved **only** for separating vector elements and must not be used as decimal separators.

When entering polynomials, provide them as a vector of coefficients ordered **from the highest power to the lowest power**.

### Examples

```text
Scalar: 3.14
Polynomial: [1, -3.5, 2.1] or [1 -3.5 2.1]   // represents 1*s^2 - 3.5*s + 2.1
```

---

## License

MIT License (c) 2025 ACROSS-UWB  
See the `LICENSE` file for full license text.  

---

## Acknowledgement

This outcome is linked to the research objective **RO 1.4 – Algorithms for industrial control** and has been supported by the **Roboprox project**  
(CZ.02.01.01/00/22_008/0004590).
