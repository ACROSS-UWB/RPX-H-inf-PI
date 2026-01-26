# RPX-Hinf-PI

**Version:** 1.0.0  
**Year:** 2025  
**Authors:** M. Schlegel, M. Brabec  

Department of Cybernetics  
Faculty of Applied Sciences  
University of West Bohemia in Pilsen  

---

## License

MIT License (c) 2025 ACROSS-UWB  
See the `LICENSE` file for full license text.  

**Support contact:** brabecm@ntis.zcu.cz  

---

## Acknowledgement

This outcome is linked to the research objective **RO 1.4 – Algorithms for industrial control** and has been supported by the **Roboprox project**  
(CZ.02.01.01/00/22_008/0004590).

---

## Description

A software tool has been developed for PI controller design for an LTI SISO system.

The tool supports an arbitrary number of design requirements in the form of H-infinity specifications, including:
- H-infinity norm of weighted sensitivity functions,
- H-infinity norm of sums of squared magnitudes.

The tool also supports closed-loop pole placement specifications, such as:
- sigma-stability,
- damping of oscillatory modes.

The design method is based on the analytical computation of the boundary of the solution region in the controller parameter plane.

---

## Input format notice

Commas are reserved **only** for separating vector elements and must not be used as decimal separators.

### Examples

```text
Scalar: 3.14
Vector: [1.2, 3.4, 5]
Vector: [1.2 3.4 5]
