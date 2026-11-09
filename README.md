# AMR-based remeshing agent — demo

Interactive demo of an LLM agent (Qwen) that drives adaptive mesh refinement (NASA refine) + RANS CFD (SU2) on the ONERA M6 wing.

**Live page:** https://seunghanJung.github.io/amr-remeshing-agent-demo/

- Left: 3 × 3 panels — rows = starting-mesh Level 1 · 2 · 3, columns = mesh · CFD (Mach) · Cp vs experiment (y/b = 0.65), all advancing on a common cycle axis.
- Right: one cycle indicator per level — CFD analysis → Convergence check → Agent judgment · Qwen → AMR; the light stops at Agent judgment when the agent ends the loop and FINAL MESH lights up.
- Controls: play / pause, ◀ ▶, slider; keyboard Space / ← / →.

Single self-contained HTML file (images embedded). Best viewed on a 16:9 monitor.
