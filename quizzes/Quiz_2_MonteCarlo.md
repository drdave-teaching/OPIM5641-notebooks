# Quiz 2 - Monte Carlo Simulation
**OPIM 5641 · Business Decision Modeling - Dr. Dave Wanik, University of Connecticut**

*Quick warm-up for today's studio - 5 questions to flex what you picked up in the async videos. About 5-10 minutes. Answer key's at the bottom, but give it an honest shot first!*

---

**1. (concept)** In one sentence each: what's the difference between a **parametric** and a **nonparametric** Monte Carlo simulation?

**2. (concept)** Why do we run 10,000 trials instead of just one?

**3. (read the code)** This line draws one year's stock growth from a normal distribution:
```python
growth = 1 + np.random.normal(loc=8, scale=17) / 100
```
If you wanted to make this **nonparametric** instead, what would you change - and what would replace `np.random.normal(...)`?

**4. (why it matters)** Monte Carlo and optimization answer two different questions. Which one answers *"what might happen?"* and which answers *"what should I do?"*

**5. (do it)** You ran 10,000 sims and have a dataframe `resultDF` with a `Savings` column. Write the line that estimates the probability your savings end up **below \$50,000**.

---

## Answer key

1. **Parametric** = you assume a named distribution (normal, triangular, etc.) and sample from it. **Nonparametric** = you sample straight from the data you actually have, no distribution assumed.
2. One trial is just one possible future - it tells you nothing about risk. 10,000 trials give you the whole *distribution* of outcomes, so you can talk about averages, best/worst cases, and probabilities.
3. Swap `np.random.normal(loc=8, scale=17)` for a **resample from your historical data** - e.g. `df['percChange'].sample(1).values[0]`. You stop assuming a bell curve and start drawing from the real numbers you observed.
4. Monte Carlo answers *"what might happen?"* (the range of outcomes under uncertainty). Optimization answers *"what should I do?"* (the best decision).
5. `(resultDF['Savings'] < 50000).mean()` - the fraction of sims below 50k *is* the estimated probability.


*Dr. Dave Wanik - University of Connecticut*
