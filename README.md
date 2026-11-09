# AMR-based CFD Remeshing Agent — demo

Interactive demo of an LLM agent (Qwen) that drives adaptive mesh refinement (NASA refine) + RANS CFD (SU2) on the ONERA M6 wing.

**Live page:** https://seunghanJung.github.io/amr-remeshing-agent-demo/

- Left: 3 × 3 panels — rows = starting-mesh Level 1 · 2 · 3, columns = mesh · CFD (Mach) · Cp vs experiment (y/b = 0.65); each level advances on its own clock (cycle 0 = 3 s, 1 s per cycle, 4 s for its final cycle).
- Right: one cycle indicator per level — CFD analysis → Convergence check → Agent judgment · Qwen → AMR; each level runs on its own clock; the light stops at Agent judgment when the agent ends the loop, FINAL MESH lights up and the panel glows.
- Controls: play / pause, ◀ ▶, slider; keyboard Space / ← / →.

Single self-contained HTML file (images embedded). Best viewed on a 16:9 monitor.
