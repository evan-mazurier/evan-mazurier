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

Anything blocking becomes a question rather than a guess. Work lands on its own branch, and nothing reaches `main` without passing its gate.

**12,920 lines · 507 tests**

→ **[Atlas](https://github.com/evan-mazurier/atlas)**

---

## The brake tool

**A MATLAB → Python re-architecture I owned end to end**, for the brake engineering team at a European rolling stock manufacturer. 73,500 lines, 682 tests, six months, sole developer — and nobody on the team could read the code, so the tests and the benchmark campaign were the only reviewer the project had.

Other engineers have since used it on a real train programme to regenerate a braking specification.

→ **[brake-tool-migration](https://github.com/evan-mazurier/brake-tool-migration)** — the write-up. No code: that part isn't mine to publish.

---

### Stack

`Python` · `TypeScript` · `React` · `SQLite` · `pytest`

### Looking for

Agentic / AI engineering roles, remote in the EU. Available from **January 2027**.

### Elsewhere

[LinkedIn](https://www.linkedin.com/in/evan-mazurier) · evan.mazurier@gmail.com
