# Module 2 Video Guide — The Simplex Method (M2.2)

**OPIM 5641 - Business Decision Modeling · Dr. Dave Wanik · University of Connecticut**

The graphical method rescued us from brute force — millions of combinations down to five corner points — and then it hit a wall at **two decision variables.** Three needs a 3-D plot. Four has nothing to draw. So the rest of Module 2 builds the **algebraic extension of that geometric technique**: Simplex. Same corner walk, no picture required, any number of dimensions.

Watch in order. The 🔴 markers inside the notebooks show exactly where each video starts, and every marker carries a hidden talking-points block — **double-click the cell** to read it while you record.

:::note
**Not yet recorded.** All ten notebooks in `5_Simplex/` have been verified to run top to bottom. Video numbering continues from the graphical block, which ended at Video 15.
:::

---

## Notebook 1 · `5_Simplex/0_BigIdeas_Simplex_vs_Graphical.ipynb` — **lead with this**
**The big ideas:** the optimum sits at a corner (CPF solution) · you only ever step to an **adjacent** corner · if no neighbor is better, you're done — convexity makes that shortcut legal · slack variables turn inequalities into equations · **corner point = basic feasible solution**, the bridge from geometry to algebra.

**Video 16 — Big Ideas, Part 1: the geometry (why a corner walk works)**
The motivating example, and the one that earns everything else. Open on the wall: graphical gave us five corners instead of eleven million combinations, and then it died at two variables. Pay off the promise you made on camera in Video 12 — *as you walk around the feasible region the objective climbs, climbs, climbs, and then falls off; that isn't random, and I'll tell you why in the Simplex video.* This is that video. Walk the Wyndor picture with your finger: start at the origin (free, always feasible), step to a better neighbor, repeat. Two steps and you're at (2, 6). Close on why the "no better neighbor means stop" rule is safe — LP feasible regions are convex, so a local optimum **is** the global optimum.

**Video 17 — Big Ideas, Part 2: the algebra (slack variables and the augmented form)**
Now do it without the picture. Slack variables: an inequality is a headache, an equation is easy, and slack is *real* — it's idle capacity in the plant. Augmented form is the same problem in friendlier clothes. Degrees of freedom → set $n - m$ variables to zero and solve for the rest → **basic** vs. **nonbasic** variables. Land the sentence the whole module rests on: **a basic feasible solution IS a corner point.** Then the three moving parts — optimality test, entering variable, and the minimum ratio test (which is just *which constraint hits zero first*).

---

## Notebook 2 · `5_Simplex/1_General Simplex Maximization Steps.ipynb`
**The big ideas:** the recipe, in order, every time · objective row on the **bottom**, entered **negated** · most-negative rule for entering · smallest-positive-ratio rule for departing · pivot to 1, then Gauss-Jordan the column · stop when no negatives remain.

**Video 18 — The general recipe: Simplex maximization steps**
The cheat sheet. Two gatekeepers first — is it a **max**, and is every constraint LHS ≤ RHS? If not, you're in a different recipe (both are coming). Then slacks, then the tableau. Say the thing students trip on out loud: the objective goes on the **bottom row** and it goes in **negated**, because you rearranged $Z - 4x_1 - 6x_2 = 0$ — and those minus signs are the *signal that you can still improve.* Entering = most negative in the bottom row. Departing = smallest **positive** $b/a$ ratio (a zero or negative denominator isn't a wall, so it doesn't count). Your line for the elimination step: *leave the row of interest alone and add multiples of the pivot row to it.*

---

## Notebook 3 · `5_Simplex/Wyndor_Glass_Simplex_Method.ipynb` — **the payoff**
**The big ideas:** the Rosetta Stone closes its third loop · each pivot is one step along the graph you already drew · reading the final tableau · slack as idle capacity.

**Video 19 — Wyndor Glass by Simplex (the third solve)**
Open big: you solved Wyndor with brute force, you solved it graphically, and today the same **\$36,000** falls out of a completely different machine. Don't re-derive the model — point at it and go. Iteration 1: $-5000$ is most negative so $x_2$ enters; R1 has no $x_2$ so skip it, $12/2 = 6$ beats $18/2 = 9$, so R2 leaves; pivot on the 2. **Stop right there and show that you are standing on (0, 6) — point A on last video's graph.** That single moment is the point of the whole module. Iteration 2 takes you to **(2, 6)**, point B. Read the final tableau: $x_1 = 2$, $x_2 = 6$, $Z = 36{,}000$, and $s_1 = 2$ means Plant 1 has two idle hours. Close on the scoreboard: brute force checked 1,681 combinations, graphical checked 5 corners, Simplex checked 3.

---

## Notebook 4 · `5_Simplex/2_TheSimplexMethod_Maximization2D.ipynb`
**The big ideas:** every row operation done by hand in SymPy, nothing hidden · `Rational` keeps fractions exact · a variable *replacing* another in the basis is literally a step to the next corner · Simplex never computes a single line intersection.

**Video 20 — 2D Max, Part 1: standard form and the initial tableau**
Fresh problem, same algorithm, and this time every row operation happens on screen. Build the tableau, point at the bottom row showing $-4$ and $-6$, and explain the negatives one more time. The starting solution — $x_1 = 0$, $x_2 = 0$, slacks at 11, 27, 90 — is the **origin**, and it's free. Slacks are basic (clean unit columns); the $x$'s are nonbasic. Close: *we're at the origin making zero dollars; let's go find a better corner.*

**Video 21 — 2D Max, Part 2: Pivot #1 start to finish**
$-6$ beats $-4$, so $x_2$ enters — and tie the *why* back to $Z = 4x_1 + 6x_2$: a unit of $x_2$ simply buys more. Show the **losing** ratios too, so the winner earns it. Pivot to 1, then Gauss-Jordan R1, R2, R3 out loud. Use `Rational`, not floats — the tableau stays exact and readable. Then the moment: $x_2$ has **replaced** $s_1$ in the basic column, and that swap *is* the step to the next corner. Optimality test: still a negative, so no, not done.

**Video 22 — 2D Max, Part 3: Pivots #2 and #3, and reading the answer**
Run the last two pivots with less narration and let them feel the rhythm — it's a recipe, not an insight. Scan the bottom row: no negatives, done. Read the tableau (unit column → basic, read its value from $b$; everything else is zero) using the pandas view with headers so the mapping is obvious. Then the big line: **Simplex never found a single intersection of two lines and never drew anything** — and it works in 40 dimensions, which is why every commercial solver on earth is built on it. Close: *that's maximization; minimization has one twist, and it's a beautiful one.*

---

## Notebook 5 · `5_Simplex/4_General Simplex Minimization Steps.ipynb`
**The big ideas:** you don't learn a second algorithm — you **convert** · $A$ with the objective row, transposed, is the **dual** · rename $x \to y$ to stay honest · the min answer is read from the **bottom row**, not the $b$ column.

**Video 23 — The general recipe: Simplex minimization (and the dual)**
Here's the twist you promised. Gatekeepers flip: must be a **min**, and every constraint must be LHS ≥ RHS. Write $A$ with the coefficients *and* the objective row all in one matrix, then take the **transpose** — rows become columns. That transpose **is** the dual problem, and it deserves its name on camera: **von Neumann duality**. Every minimization has a mirror-image maximization with the same optimal value. From there it's the identical recipe. The only thing that changes is how you *read* the answer, and that's the single most common place students lose points — so point at the bottom row twice.

## Notebook 6 · `5_Simplex/5_TheSimplexMethod_Minimization2D.ipynb`

**Video 24 — 2D Minimization: solve the dual, read the min**
Minimize cost subject to ≥ constraints — the shape of every diet, blending, and staffing problem they'll ever meet. Build $A$ with the objective row, transpose, rename $x \to y$, and let them stare at it until it clicks. Then announce it: *this is a maximization problem, and we already know how to do those.* Two pivots (show the close call on the first ratio test), `Rational` over `Fraction` with `nsimplify` to tidy up, then read the original minimum out of the **bottom row under the slack columns.** Close on duality: the min and the max hit the same optimal value, and that is not a coincidence.

---

## Notebook 7 · `5_Simplex/7_TheSimplexMethod_Maximization_Mixed.ipynb`
**The big ideas:** real problems are mixed · the free start at the origin disappears · there's no tidy first-pivot rule, so we use trial and error · this is exactly why solvers exist.

**Video 25 — Mixed constraints: when the recipe gets messy**
Be honest on camera: this one is uglier, and they should see that, because real problems are mixed. Some ≤, some ≥, maybe an =, and the comfortable "start at the origin" freebie is gone — the origin may not even be feasible. That's why there's no single clean rule for the first pivot; you use trial and error and you get to say *yuck* out loud. Three pivots, same mechanics, same stopping rule. The takeaway: this is where by-hand Simplex stops being pleasant, and Big-M and two-phase methods are what commercial solvers use instead — they don't need to *do* those, they need to know **why they exist.** Close straight into Module 3: Pyomo takes it from here, and now you know what the solver is doing under the hood.

---

## Optional · the 3-D notebooks
Both have a 🔴 marker in place if you want them, but they're skippable — nothing new happens, which is arguably the point.

- **`3_TheSimplexMethod_Maximization_3D.ipynb`** — three decision variables, so the graphical method is already dead and Simplex doesn't blink. One genuinely new wrinkle worth mentioning: **ties for the entering variable** — pick either, you may take a different path, you land on the same optimum.
- **`6_TheSimplexMethod_Minimization3D.ipynb`** — same transpose-and-solve-the-dual move as 2-D min. Watch the ratio test: one denominator is **0**, an invalid ratio you skip. That's a real exam trap.

If you'd rather not record them, link both as practice — they're solved soup to nuts in the notebook.

## Also in the folder
- `S26_MidtermReview_Wanik.ipynb` — the midterm review driver. Reproduces the Veerman answer (**\$8,400** at 0 chairs, 275 desks, 100 tables) and carries five 🔴 markers from the live class.

## Coming next
**Module 3 — Pyomo.** You've now done optimization the honest-but-slow way (brute force), the visual way (graphical), and the algebraic way (Simplex). Module 3 hands all of it to a solver — and the whole reason Module 2 exists is so that solver is never a black box.

---

*Companions: [Module2_Skills.md](Module2_Skills.md) · [Module2_Talking_Points.md](Module2_Talking_Points.md) · [Module2_Video_Guide.md](Module2_Video_Guide.md) · [Working in this Course](Module1_Working_in_this_Course.md)*
