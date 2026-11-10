# AMR-based CFD Remeshing Agent — demo

Interactive demo of an LLM agent (Qwen) that drives adaptive mesh refinement (NASA refine) + RANS CFD (SU2) on the ONERA M6 wing.

**Live page:** https://seunghanJung.github.io/amr-remeshing-agent-demo/

- Left: 3 × 3 panels — rows = starting-mesh Level 1 · 2 · 3, columns = mesh · CFD (Mach) · Cp vs experiment (y/b = 0.65); each level advances on its own clock (cycle 0 = 3 s, 1 s per cycle, 4 s for its final cycle).
- Right: one cycle indicator per level — CFD analysis → Convergence check → Agent judgment · Qwen → AMR; each level runs on its own clock; the light stops at Agent judgment when the agent ends the loop, FINAL MESH lights up and the panel glows.
- Controls: play / pause, ◀ ▶, slider; keyboard Space / ← / →.
- When all three levels have converged, a conclusion scene shows each level's initial mesh + flow field next to its converged mesh + flow field, with the Cp RMSE vs experiment.
- Scroll down (or "▼ 3D wing mesh"): an interactive WebGL viewer of the wing surface mesh for every cycle of every level — drag to rotate, wheel to zoom, double-click to reset, wireframe on/off, single level or all three side by side (shared camera). three.js is embedded, so it works offline.

Single self-contained HTML file (images, surface meshes and three.js embedded, ~28 MB). Best viewed on a 16:9 monitor.
