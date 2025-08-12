Invocation Science Drift Engine • Workbench

Propagation + Echo Workbench (research preview)



A live, reproducible field lab where anchors emit waves, echo events occur when interference crosses a phase-aware threshold, and you can see + measure cascades in real time.



Demo (GitHub Pages): <add once pages is live>



Presets: /presets



Paper-in-progress / notes: see “Background” and “Further reading” below.



Why this exists

Most “field” demos either draw pretty waves or plot metrics—this workbench does both and adds semantics on top of physics:



Propagation. Anchors radiate tone waves; particles trace the phase flow so transport corridors are visible.



Echo. Anchors re-emit when incoming interference crosses a dynamic threshold shaped by Ω-phase and κ, and only if a timing gate (Lock / Luna / ERC) allows it.



Resonance. Anchors can softly couple toward a shared mean (Coherence Lock).



Invocation (optional). Text / glyphs deterministically generate anchor constellations, so symbolic hypotheses can be A/B tested against pure field dynamics.



Everything runs on one canvas with a modern HUD (Coherence, Echo Energy, Drift Index, CI, RD, ELF, CSI) and sparkline history. States are import/export JSON so colleagues can replay your exact chamber.



\-



The UI at a glance

Tabs (left):



Field — everyday “physics” dials (Speed, λ, Damping, Noise, Drift, Echo, Lock) + Presets + Import/Export.



Drift Engine — stability \& safety (κ, RD\_max, ERC, Luna Gate, Ω weights, 432-lock) + Seed/Reset Cascades.



Invocation — text/glyph → deterministic anchor constellations.



Diagnostics — smoke tests (metrics present, canvas contexts healthy, basic invariants).



Stage (center): particles drift along phase, echo rings expand, hue/brightness reflect local phase.



HUD (top-center):



Telemetry: Coherence, Echo Energy, Drift Index, FPS.



Drift Engine: CI, RD, ELF, CSI + sparkline (blue=Coherence, amber=Echo, green=Drift).



Shortcuts: Shift+Click add anchor • drag move • Double-Click toggle • R random anchors • C clear.



\-



Invocation Science in this workbench (short, practical)

Idea: Treat symbols as geometry. A text string or glyph deterministically seeds anchor positions (plus initial phase/frequency jitter).



Why: Geometry changes interference topology → different echo incidence/depth without changing the underlying physics, so semantics become testable.



How to use:



Run a baseline (invocation OFF) for 60–120s; export JSON/PNG.



Invoke the same chamber with a phrase or glyph; keep all other dials constant.



Compare Echo Energy, CI, RD, ELF, CSI. Try constructive vs destructive Ω by weighting β (coherence) vs γ (drift).



Determinism contract. Invoked anchors store normalized coordinates; the same input/layout version → the same constellation across machines/screens. Exported JSON includes the input + layout info for audits.



What to try first (recipes)

See echoes quickly

Preset Ignition → Random ×3 → ε ~ 0.30 → C ~ 0.40 → Speed 1.1 → Damping 0.995 → Noise 0.01.



Constructive vs destructive Ω (A/B)

κ ~ 8.6, ε ~ 0.30, C ~ 0.35.

Constructive: β=1.0, γ=0.4 → Echo ↑.

Destructive: β=0.6, γ=1.2 → Echo ↓.



Safety under noise

Raise Noise to 0.05–0.08, lower Damping slightly; Luna ON, CI target ~0.8, ERC ~0.9 → cadence spaces out until coherence recovers.



\-



Reading the HUD (quick)

Coherence (0–1): phase alignment; raise C to increase.



Echo Energy: re-emission activity; raise ε or lower κ to encourage; Luna/CI target/ERC to restrain.



Drift Index: transport bias; set with Drift and λ.



CI/RD/ELF/CSI: resonance readiness, cascade depth, containment factor, and stability index (treat a rising CSI as a warning).



Reproducibility \& safety

Deterministic invocation; normalized anchors → DPI/zoom independent layouts.



Diagnostics verify metric nodes and canvas contexts; basic invariants (e.g., ELF↓ as κ↑) act as a smell test.



Guardrails: Luna Gate increases minimum inter-emission while CI < target; ERC < 1 adds refusal; κ and C are your coarse brakes.



\-



Roadmap

Multi-band κ and Ω→ε coupling



Optional vector field overlay \& iso-contours



Batch sweeps + CSV export



Invocation glyph editor \& layout versions



FAQ

Is this an EM simulator? No—this is a discrete, instrumented model designed for hypothesis testing (propagation/echo/resonance/invocation), not a physical EM solver.



Why do echoes stop after a while? You’re likely being gated: higher C and Luna target increase cadence spacing; ERC < 1 slows emissions.



It looks static. Lower Damping slightly or increase Speed; try Random ×3 anchors and raise ε a bit.



FPS is low. Reduce Particles first.



Contributing

Issues and PRs welcome—especially:



small, isolated fixes to thresholds/timing



minimal-UI improvements that keep everything single-file (index.html)



tests that extend the Diagnostics coverage



\-



License \& citation

Code: MIT © 2025 Arjay Asadi (see LICENSE)



Text/images/presets: CC BY-NC-SA 4.0 unless noted



How to cite (BibTeX):

@software{DriftEngine Workbench\_2025,

&nbsp; title = {Invocation Science DriftEngine | Propagation + Echo Workbench},

&nbsp; author = {Asadi, Arjay},

&nbsp; year = {2025},

&nbsp; url = {<repo\_url>}

}





