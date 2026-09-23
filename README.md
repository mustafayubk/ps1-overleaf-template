# Observability and Sovereign Disclosure

**An Observability-Based Public Goods Approach**

Individual research proposal · COMSCI/ECON 206 Computational Microeconomics · Autumn 2026 Session 1 · Instructor Prof. Luyao Zhang

**Author:** Mustafa Ayub Khan ([mak156@duke.edu](mailto:mak156@duke.edu)) · Duke Kunshan University

![Research design teaser](figures/ps1_teaser.png)

## What this is

A prospective research proposal connecting economics, computation, and behavioral science around one question: **when does peer observability cause genuine, rather than merely performed, sovereign disclosure transparency?**

- **Economics:** Does higher-quality climate disclosure causally lower a country's borrowing cost?
- **Computation:** Does an observability-based public goods game show that visibility of peers' contributions alone — with no payoff change — raises voluntary contribution?
- **Behavior:** Does peer visibility raise genuine transparency, or teach "disclosure theater"?

Full argument, model, and results are in the compiled PDF (`main.tex` → `sections/proposal.tex` + `appendices/supporting.tex`).

## Live artifacts

| Artifact | Link |
|---|---|
| Compiled paper (this repo) | `main.tex`, built from `sections/proposal.tex` + `appendices/supporting.tex` |
| Interactive game (Hugging Face) | [huggingface.co/spaces/dku-comsci-econ206-2026/mustafa-observability-game](https://huggingface.co/spaces/dku-comsci-econ206-2026/mustafa-observability-game) |
| Companion notebook (Colab) | [companion/notebooks/06_ps1_strategic_reasoning_demo.ipynb](https://colab.research.google.com/github/mustafayubk/ps1-overleaf-template/blob/main/companion/notebooks/06_ps1_strategic_reasoning_demo.ipynb) |

**Current verified commits (v2):** Hugging Face Space `c84ab29`; companion notebook `bab5cb2`; `companion/hf_space/index.html` synced to the live game at `814d2b9`.

## Repository structure

- `main.tex` — identity, title, metadata, teaser, source includes.
- `sections/proposal.tex` — the five main sections (Q1–Q3, methods, results, future directions).
- `appendices/supporting.tex` — Author Notes, references, Appendix A (technical/reproducibility), B (cumulative intellectual development), C (field observations), D (review response and revision record), E (structured abstract).
- `figures/` — `ps1_teaser` (research-design diagram, above), plus field-trip photographs (`IMG_6881.jpeg`, `IMG_6947.jpeg`) used in Appendix C.
- `companion/notebooks/06_ps1_strategic_reasoning_demo.ipynb` — payoff-engine verification, multi-schedule sweep (500 random peer schedules), and adaptive-strategy extension. Run fresh via **Runtime → Restart session and run all**.
- `companion/hf_space/` — the actual source (`index.html`, `model.js`) behind the deployed Hugging Face Space; kept in sync with the live artifact.
- `companion/src/`, `companion/tests/` — supporting code and test suite for the notebook.

## The observability game

Five simulated countries play six rounds. Each round a country splits a 10-token endowment between a Personal Fund (private payoff `a=4`/token) and a Group Fund (shared payoff `b=2`/token to everyone). Rounds 1–3 (**Low Observability**) show only the sum of peers' prior contributions; rounds 4–6 (**High Observability**) show each peer's individual prior contribution. The peer schedule is fixed so the *total* peer contribution is always 10 in every round, in both phases — only the visibility of the individual breakdown changes with observability, isolating the observability manipulation from peer generosity.

Verified test cases (Appendix A.3): boundary strategy (`c=0` every round) → \$360.00 cumulative; typical strategy (`c=5` every round) → \$300.00 cumulative, matching the game's Nash prediction (`c* = 0`, since `a > b`).

## Revision history

This proposal went through a full peer-review cycle. v1 (Sept 13, 2026) was reviewed by Temur Akhtamjonov and Yiqiao Liu in the Week 4 workshop, who identified that the original peer schedule confounded observability with peer generosity and that the GitHub repository didn't yet reproduce the deployed game. v2 (Sept 20, 2026) fixed both issues — see Appendix D for the full review-response record and Appendix E for the structured abstract's revision log.

## Reuse note

Built from the class starter template (Prof. Luyao Zhang, DKU COMSCI/ECON 206). ACM class/bibliography files (`acmart.dtx`, `acmart.ins`, `acmart.cls`, `ACM-Reference-Format.bst`) retain their original third-party notices.
