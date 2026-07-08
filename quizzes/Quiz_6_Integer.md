# Quiz 6 - Integer & Binary Programming
**OPIM 5641 · Business Decision Modeling - Dr. Dave Wanik, University of Connecticut**

*Quick warm-up for today's studio - 5 questions to flex what you picked up in the async videos. About 5-10 minutes. Answer key's at the bottom, but give it an honest shot first!*

---

**1. (concept)** When do you need an **integer** or **binary** variable instead of a regular continuous one? Give an example.

**2. (concept)** What's a **linking constraint**, and why does a fixed cost (a setup cost) require one?

**3. (read the code)** In Pyomo, what does this declaration create, and what values can it take?
```python
model.build = Var(domain=Binary)
```

**4. (why it matters)** You solved the LP and got 2.7 factories. Why can't you just round to 3 and call it done?

**5. (do it)** In project selection, each project `i` has cost `c[i]` and a binary `x[i]`. Write the shape of the **budget constraint** (total spend can't exceed budget `B`).

---

## Answer key

1. When a fraction makes no sense - you can't build **half a factory** or hire **2.7 nurses** - or when it's a yes/no **decision** (open this store or not). Example: siting warehouses, selecting projects, turning a production line on or off.
2. A linking constraint ties two variables together so one *controls* the other. A fixed cost needs a **binary switch** ("did we produce anything?") linked to the production variable, so you only pay the setup cost when production is actually turned on.
3. It creates a **binary decision variable** that can only be **0 or 1** (don't build / build). Perfect for yes/no choices.
4. Rounding can land you **outside the feasible region** (3 factories might blow the budget) or leave value on the table. The integer optimum can be a genuinely different solution than the rounded LP - you have to actually solve the integer program.
5. `sum(c[i] * x[i] for i in projects) <= B`


*Dr. Dave Wanik - University of Connecticut*
