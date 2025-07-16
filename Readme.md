# Shear-Driven Cavity Flow Simulation (Re = 7500)
## Overview
This simulation models a 2D shear-driven cavity flow over a rectangular cavity, inspired by the setup presented in the paper by Callaham, Brunton, and Loiseau.

## Simulation Goals

- Analyze recirculation patterns inside the cavity
- Observe shear layer development over cavity
- Compare velocity fields across mesh levels
- Assess convergence with mesh refinement
# ----------------------------- 

## Geometry & Domain Setup
Domain Type: 2D (planar)

Cavity Width: 1.0 m

Cavity Depth: 1.0 m

Upstream/inlet Length: 0.8 m

Slip Inlet length: 0.4 m

Downstream Channel Length: 2.5 m

Outlet Height: 0.5 m

## Boundary Conditions

| Boundary      | Type     | Description                          |
|---------------|----------|--------------------------------------|
| `inlet`       | `patch`  | Uniform velocity: **1 m/s**          |
| `outlet`      | `patch`  | Zero-gradient pressure               |
| `top` (upstream) | `slip`   | Slip condition                     |
| `cavity walls`| `wall`   | No-slip on cavity walls              |
| `bottom wall` | `wall`   | No-slip                              |
| `front/back`  | `empty`  | 2D simulation                        |

## Flow Parameters

- **Inlet velocity**: `1 m/s`
- **Reynolds number**: `Re = 7500`
- **Solver**: `pimpleFoam` 

## Mesh Independence Study
To ensure solution accuracy and assess mesh sensitivity, three cases were simulated:

Case	Cells (approx.)	Description
base	    	Lower resolution mesh
coarse	 5k 	Moderate resolution 
fine	 20k	High resolution mesh

## TO DO 
1.Mesh Independence

