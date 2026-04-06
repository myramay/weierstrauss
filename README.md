# Weierstrass Function Explorer

An interactive browser-based explorer for the Weierstrass function — the classic example of a continuous, nowhere-differentiable curve.

## What is it?

The Weierstrass function is defined as:

```
W(x) = Σ aⁿ cos(bⁿπx),  n = 0 to N
```

Where:
- `a ∈ (0, 1)` controls amplitude decay
- `b` is a positive odd integer controlling frequency growth
- When `ab > 1 + 3π/2 ≈ 5.712`, the function is provably **nowhere differentiable**

No matter how far you zoom in, it never resolves to a smooth curve — it stays jagged and self-similar at every scale.

## Features

- **Smooth scroll zoom** toward the mouse cursor — zoom in indefinitely and the fractal structure persists
- **Drag to pan** along the x-axis
- **Partial sum layers** — see how each term builds up the function, colored blue → orange → teal
- **Live HUD** showing zoom level, self-similarity depth (in b-folds), center position, and whether the nowhere-differentiable condition is met
- **Sliders** for `a`, `b` (odd integers only), and `N` (number of terms)
- Touch support for mobile (swipe to pan, pinch to zoom)

## Usage

Open `index.html` in any modern browser. No build step, no dependencies.

| Input | Action |
|---|---|
| Scroll wheel | Zoom in/out toward mouse |
| Click + drag | Pan |
| `R` key | Reset view |
| `L` key | Toggle layer visibility |

## Self-similarity

The function satisfies an approximate scaling relation: zooming in by a factor of `b` reveals a pattern statistically similar to the original. The HUD displays your current depth in **b-folds** — at each integer value, you've descended one self-similar level.

## Live Demo

[https://myramay.github.io/weierstrauss/](https://myramay.github.io/weierstrauss/)
