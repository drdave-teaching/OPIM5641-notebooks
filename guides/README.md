# Course Guides

**OPIM 5641 - Business Decision Modeling · Dr. Dave Wanik · University of Connecticut**

Everything that isn't a notebook lives here. Start with **[Working in this Course](00_Working_in_this_Course.md)** — how to open notebooks in Colab, save your own copies, and hand work in.

Each module comes in three parts:

- **📺 Video Guide** — what each video covers, in order, with runtimes and the notebook it drives
- **✅ Skills** — checkboxes: what you can *do* after watching
- **🧠 Talking Points** — the theory you should be able to explain without opening a notebook

---

## The course, by sub-module

| Sub-module | Topic | Notebooks | 📺 Video Guide | ✅ Skills | 🧠 Talking Points |
|---|---|---|---|---|---|
| **M1.1** | Exploratory data analysis | [`1_EDA_Intro/`](../1_EDA_Intro) | [Videos](M1.1_EDA_Video_Guide.md) | [Skills](M1.1_EDA_Skills.md) | [Theory](M1.1_EDA_Talking_Points.md) |
| **M1.2** | Monte Carlo simulation | [`2_MonteCarlo/`](../2_MonteCarlo) | [Videos](M1.2_MonteCarlo_Video_Guide.md) | [Skills](M1.2_MonteCarlo_Skills.md) | [Theory](M1.2_MonteCarlo_Talking_Points.md) |
| **M2.1** | Brute force optimization | [`3_BruteForce/`](../3_BruteForce) | [Videos](M2.1_BruteForce_Video_Guide.md) | [Skills](M2.1_BruteForce_Skills.md) | [Theory](M2.1_BruteForce_Talking_Points.md) |
| **M2.2** | The graphical method | [`4_Graphical/`](../4_Graphical) | [Videos](M2.2_Graphical_Video_Guide.md) | [Skills](M2.2_Graphical_Skills.md) | [Theory](M2.2_Graphical_Talking_Points.md) |
| **M2.3** | The Simplex method | [`5_Simplex/`](../5_Simplex) | [Videos](M2.3_Simplex_Video_Guide.md) | [Skills](M2.3_Simplex_Skills.md) | [Theory](M2.3_Simplex_Talking_Points.md) |
| **M3.1** | Pyomo — allocation, covering, blending, sensitivity | [`6_Pyomo_LP/`](../6_Pyomo_LP) | [Videos](M3.1_Pyomo_Video_Guide.md) | [Skills](M3.1_Pyomo_Skills.md) | [Theory](M3.1_Pyomo_Talking_Points.md) |
| **M4.1** | Nonlinear — curves, regression as optimization, warehouse location | [`7_Nonlinear/`](../7_Nonlinear) | [Videos](M4.1_Nonlinear_Video_Guide.md) | [Skills](M4.1_Nonlinear_Skills.md) | [Theory](M4.1_Nonlinear_Talking_Points.md) |

Every notebook's banner tells you which sub-module it belongs to, so you can always tell where you are.

## The through-line

**M1.1** you explore data you *have*. **M1.2** you simulate data you *don't*. Then the third verb: when you have to **decide**, you optimize.

**M2.1** brute force is the dumbest honest method — always correct, and it dies on real problems. **M2.2** the graphical method turns millions of combinations into five corner points, and dies at two decision variables. **M2.3** Simplex walks those same corners algebraically, in any number of dimensions.

**Wyndor Glass** is the Rosetta Stone — solved three ways across M2.1, M2.2 and M2.3, landing on **\$36,000 at (2, 6)** every time.

Then **M3** hands all of it to a solver — and because you did it by hand first, the solver is never a black box.

## By-hand worksheets

Separate repo: [`drdave-teaching/opim-math`](https://github.com/drdave-teaching/opim-math) — worksheet/key pairs plus Dr. Wanik's handwritten longhand notes for the graphical and Simplex solves.
