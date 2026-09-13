## Parv Parakhiya

Mechanical engineer working on predictive maintenance for production equipment — the part where sensor data meets a machine somebody has to keep running.

M.Eng. Mechatronic and Cyber-Physical Systems at Deggendorf Institute of Technology. **Looking for an industry Master's thesis** in condition monitoring, industrial data or production engineering, starting October 2026. Based in Deggendorf, Bavaria.

---

### What I've been building

#### [pdm-audit](https://github.com/parvparakhiya/pdm-audit) — I audited my own predictive-maintenance pipeline and shipped less than I built

Three of the AI4I 2020 dataset's five failure modes are closed-form rules and two are stochastic by construction, so the tuned ensemble was fitting a known function against an irreducible noise floor. A three-predicate rule engine scored macro-F1 **0.796** against the model's **0.766**, at zero training cost.

The remaining-useful-life model — whose target I had synthesised myself, on a benchmark with no run-to-failure structure — fell from R² **0.845** to **−0.104** under contiguous-block cross-validation. That gap is the whole finding: it was interpolating between adjacent rows, not predicting anything.

The ship/no-ship gate deploys a model only when it beats the cheap baseline on held-out expected cost. It rejected every candidate I put through it.

#### [pdm-service](https://github.com/parvparakhiya/pdm-service) — what shipped instead

A stateless FastAPI detector with a joint-physics layer that separates instrument faults from machine faults, so a drifting transducer raises `CHECK_INSTRUMENTATION` rather than stopping a production line. Closed-form tool-wear hazard over an explicit horizon. A policy fingerprint on every prediction, so two results are comparable only if they were produced under the same policy.

Non-root multi-architecture images. 60 tests at 88 % coverage. CI enforces types, coverage, a feature-contract digest and a zero-HIGH-CVE scan. The serving path carries no model artifacts at all.

#### [elliptical-gear-generator](https://github.com/parvparakhiya/elliptical-gear-generator) — a non-circular gear pair, derived and printed

Both gears turn about a **focus** of their ellipse, so the transmission ratio varies continuously through every revolution instead of staying constant. Eccentricity is derived from the ratio range rather than specified, because nobody designs a gearbox by choosing an eccentricity. Teeth are distributed by arc length along the pitch curve rather than by angle — equal angles give unequal spacing, and two gears whose teeth don't line up jam. The undercut bound is rederived for varying curvature, since the textbook condition assumes a constant pitch radius.

Written in Lua for IceSL, exported to STL, printed, and made to mesh.

---

### Background

Three months on the floor of an ISO 9001 forging plant — closed-die forging, heat treatment, dimensional inspection to ASME and DIN standards. Goods-in inspection and quantity verification at an aerospace C-parts supplier in Munich. A bachelor's in mechanical engineering before the mechatronics master's.

I like problems where the data has a machine behind it.

---

**Python · scikit-learn · LightGBM · PyTorch · ONNX · FastAPI · Docker · GitHub Actions · MATLAB · SQL · Lua**

Deggendorf, Germany · parvparakhiya05@gmail.com
