# Quiz 3 - Brute Force & the Graphical Method
**OPIM 5641 · Business Decision Modeling - Dr. Dave Wanik, University of Connecticut**

*Quick warm-up for today's studio - 5 questions to flex what you picked up in the async videos. About 5-10 minutes. Answer key's at the bottom, but give it an honest shot first!*

---

**1. (concept)** Name the **four building blocks** of every optimization model.

**2. (concept)** Brute force always finds the right answer, so why does it "fall apart" on real problems?

**3. (read the code)** In a brute-force nested for-loop, what job does this `if` do, and why does keeping it as one `and` statement mean you *don't* need a `continue`?
```python
if (4*c + 6*d + 2*t <= 1850) and (3*c + 5*d + 7*t <= 2400):
    profit = 15*c + 24*d + 18*t
```

**4. (concept)** For a two-variable LP, where in the feasible region does the optimal solution *always* sit?

**5. (why it matters)** If brute force is so slow, why do we bother learning it at all?

---

## Answer key

1. **Decision variables, the objective, constraints, and data (parameters).**
2. The running time explodes. Add variables or widen their ranges and the number of combinations grows combinatorially - a problem that's instant at small size takes hours (or longer than the universe has existed) at real size.
3. The `if` is the **feasibility check** - it only lets through combinations that satisfy every constraint. Writing it as a single `and` means the profit line only runs for feasible plans, so there's nothing to skip - no `continue` needed. (Cleaner, and exactly what the midterm wants.)
4. At a **corner point** (a vertex of the feasible region). That's why we only ever have to check the corners.
5. It's the honest baseline and a great **sanity check** - if you're unsure your model is right, brute-force a small version. And feeling it fall apart is exactly what motivates Simplex.


*Dr. Dave Wanik - University of Connecticut*
