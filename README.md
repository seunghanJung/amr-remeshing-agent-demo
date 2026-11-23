# AMR-based CFD Remeshing Agent — demo

Interactive demo of an LLM agent (Qwen) that drives adaptive mesh refinement (NASA refine) + RANS CFD (SU2) on the ONERA M6 wing.

**Live page:** https://seunghanJung.github.io/amr-remeshing-agent-demo/

- Left: 3 × 3 panels — rows = starting-mesh Level 1 · 2 · 3, columns = mesh · CFD (Mach) · Cp vs experiment (y/b = 0.65); each level advances on its own clock (cycle 0 = 3 s, 1 s per cycle, 4 s for its final cycle).
- Right: one cycle indicator per level — CFD analysis → Convergence check → Agent judgment · Qwen → AMR; each level runs on its own clock; the light stops at Agent judgment when the agent ends the loop, FINAL MESH lights up and the panel glows.
- Controls: play / pause, ◀ ▶, slider; keyboard Space / ← / →. When the conclusion scene ends the page scrolls down to the 3D viewer by itself; scroll back up (or "▲ 데모 다시 보기") and the demo restarts.
- When all three levels have converged, a conclusion scene shows each level's initial mesh + flow field next to its converged mesh + flow field, with the Cp RMSE vs experiment.
- The blinking "3D VISUALIZE ▼" button at the middle-left (or just scrolling) opens a WebGL viewer showing the Level 1 · 2 · 3 wing surface meshes side by side (shared camera, top (planform) view root at the bottom, tip at the top, leading edge on the left; no rotation). The cycle autoplays and each level stops at its own last cycle; pause with the autoplay button or the slider. Under each panel a compact AMR-cycle ring (ring + cycle number only) turns once per cycle at 1.25x speed; when a level reaches its last cycle the ring turns gold and a "LEVEL n CONVERGED" banner appears on its mesh. View buttons (wireframe, auto-rotate, reset view) sit inside the first viewport; drag to rotate, wheel to zoom, double-click to reset. three.js is embedded, so it works offline.

Single self-contained HTML file (images, surface meshes and three.js embedded, ~28 MB). White theme; Inter for Latin text (Google Fonts, falls back to Segoe UI offline) and Pretendard for Korean (jsDelivr CDN, falls back to Malgun Gothic offline). Best viewed on a 16:9 monitor.
