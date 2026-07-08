# Quiz 5 - Nonlinear Optimization & Portfolios
**OPIM 5641 · Business Decision Modeling - Dr. Dave Wanik, University of Connecticut**

*Quick warm-up for today's studio - 5 questions to flex what you picked up in the async videos. About 5-10 minutes. Answer key's at the bottom, but give it an honest shot first!*

---

**1. (concept)** What makes an optimization problem **nonlinear**, and why can't Simplex handle it?

**2. (concept)** In portfolio optimization, what are you trying to maximize, and what's the measure of **risk** you're trading against?

**3. (read the code)** Why do these notebooks install **Ipopt** (or Bonmin) instead of the `cbc` solver we used for LPs?

**4. (why it matters)** On the **efficient frontier**, what does a single point represent?

**5. (concept)** In plain English, why does mixing assets that *don't* move together (low covariance) reduce portfolio risk?

---

## Answer key

1. A problem is nonlinear when the objective or a constraint has a **curve** in it - a square, a product of two variables, a ratio. Simplex is built on straight lines and corner points, so it simply can't represent the curve.
2. You maximize **expected return** (or minimize risk for a target return). Risk is **variance** (or standard deviation) of the portfolio - and variance is nonlinear, which is the whole reason we need a nonlinear solver.
3. `cbc` is a **linear** solver. Portfolio risk (variance) is nonlinear, so we need a solver built for it - **Ipopt** for nonlinear, **Bonmin** when it's nonlinear *and* has integer variables.
4. A point on the frontier is a **portfolio** - the best possible expected return for that level of risk (or the least risk for that return). You can't do better than the frontier; you just pick where on it you want to live.
5. Because when one asset dips, the other doesn't dip with it - their ups and downs partly cancel out. Low covariance means the swings offset, so the *combined* portfolio bounces around less than either asset alone.


*Dr. Dave Wanik - University of Connecticut*
