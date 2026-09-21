# Evan Mazurier

### I build agentic systems, and the validators that decide when to trust them.

Not *"I build with AI"* — everyone says that now. The interesting engineering isn't the automation, it's what decides whether its output can be trusted.

- **An explicit ladder.** Every task is assigned how much autonomy it has earned, up front. Nothing decides that in the moment, under pressure.
- **Test gates as the trust primitive.** Work reaches a merge by passing its gate, not by me judging it at 2am. A gate that can be talked around is not a gate.
- **Memory that outlives the session.** Projects carry their own decision record in a markdown vault, so an agent starting cold reads what was already settled instead of re-deciding it.

---

## Atlas

**An orchestration substrate I run every day.** It dispatches work across projects, decides how much each task may do unattended, and stops for a human at exactly two points — before the work starts, and before it merges.

```
queued → scoping → [human confirms the contract] → coding → test gate
       → review → ready → [human merges] → merged
```

Anything blocking becomes a question rather than a guess. Work lands on its own branch, and nothing reaches `main` without passing its gate. An event ledger measures the gate itself — tokens, rework, reverts — so the question "is this cheaper model good enough for this role?" is answered by data, not faith.

**14,145 lines of Python · 555 tests**

→ **[Atlas](https://github.com/evan-mazurier/atlas)**

---

## The brake tool

**A MATLAB → Python re-architecture I owned end to end**, for the brake engineering team at a European rolling stock manufacturer. 73,500 lines, 682 tests, six months, sole developer — and nobody on the team could read the code, so the tests and the benchmark campaign were the only reviewer the project had.

Other engineers have since used it on a real train programme to regenerate a braking specification.

→ **[brake-tool-migration](https://github.com/evan-mazurier/brake-tool-migration)** — the write-up. No code: that part isn't mine to publish.

---

## cavity-surrogate

**A 2D Navier–Stokes solver written from the equations up, and proven right before anything is built on it.** The lid-driven cavity — the benchmark every CFD code is checked against — solved with a projection method on a staggered grid in pure numpy. Divergence-free to 1e-14, second-order grid convergence measured, centreline profiles within 0.5% of Ghia et al. (1982) at Re 100 / 400 / 1000.

The checks caught two things a "looks right" pass would have missed: the residual gap to the 1982 reference is *their* discretisation error, not the solver's (it plateaus while the solver keeps converging), and one printed value in the paper's table is wrong — kept verbatim, flagged, and shown as such.

Then two surrogates trained on 86 solver runs and judged on Reynolds numbers they never saw. The classical one — 20 POD modes and a spline — reproduces the solver to **2e-6** in about a millisecond, a 40,000–400,000× speed-up; a 500k-parameter neural network reaches 0.7% and invents flow features that aren't there. Both degrade the moment they leave the training range, and the error-vs-Re plot says so rather than hiding it. A surrogate is a validated shortcut, not a replacement for physics.

→ **[Live demo](https://evan-mazurier.github.io/cavity-surrogate/)** — drag the Reynolds number, watch the fluid move, check the prediction against the solver · **[cavity-surrogate](https://github.com/evan-mazurier/cavity-surrogate)**

---

## alpine-descent

**A train coming down the Gotthard north ramp — traction, ETCS-style braking curves, and the brake discs that carry what the electric brake cannot — as one verified chain.** A generic 200 t regional unit descends 634 m in 28.6 km at 26 ‰, stopping at every station. The run-time simulation, the supervision curves in the shape of Subset-026 (braking parabolas integrated backwards through the grade under the train) and a brake-disc thermal model with the Eurocode steel heat capacity all read the same line and the same train, and every layer is checked against a closed form before the next one builds on it: balancing speed, coasting, an energy ledger that closes to 1e-5, the exact exponential and the erfc solution of the disc.

What the chain says: with the electric brake the descent is a net *generator* and the discs stay under 70 °C; without it one disc must take 54 MJ and reaches **615 °C**, because cooling gives back only a fifth of it in the 24 minutes available — the electric brake *is* the thermal design of the train. And an emergency stop on those discs is a surface problem: the rubbing face runs 60 K ahead of anything a lumped model can see, which is the number the 1-D layer exists for.

→ **[Live demo](https://evan-mazurier.github.io/alpine-descent/)** — set the electric brake share, watch the discs heat, pull the emergency brake; the page runs the same equations in the browser and checks itself against the Python chain · **[alpine-descent](https://github.com/evan-mazurier/alpine-descent)**

---

### Stack

`Python` · `numpy` · `PyTorch` · `pytest` · `TypeScript` · `React` · `SQLite` · `MATLAB`

### Looking for

Entry-level roles where the job is **building AI workflows or engineering tools**: AI operations / agentic-workflow engineering, applied AI inside an engineering or industrial company, or calculation, simulation and validation tooling. **Relocating to Switzerland** — Zurich, Lausanne–Geneva, Bern, Basel. **Available from October 2026.** French native · English C1 · German B2.

### Elsewhere

[LinkedIn](https://www.linkedin.com/in/evan-mazurier) · evan.mazurier@gmail.com
