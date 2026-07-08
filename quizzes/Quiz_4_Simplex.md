# Quiz 4 - The Simplex Method
**OPIM 5641 · Business Decision Modeling - Dr. Dave Wanik, University of Connecticut**

*Quick warm-up for today's studio - 5 questions to flex what you picked up in the async videos. About 5-10 minutes. Answer key's at the bottom, but give it an honest shot first!*

---

**1. (concept)** In a maximization tableau, how do you pick the **entering** variable? How do you pick the **departing** variable?

**2. (concept)** In our convention, which row of the simplex tableau holds the **objective function**?

**3. (interpret)** You've done one iteration and the bottom row still has a negative number in it. Are you done? What does that negative tell you?

**4. (concept)** What's the stopping rule - how do you know the current solution is optimal?

**5. (why it matters)** Graphical and Simplex give the same answer on a 2-variable problem. So why do we need Simplex at all?

---

## Answer key

1. **Entering:** the column with the biggest *negative* number in the bottom row (that's the variable that improves Z fastest). **Departing:** the row with the smallest *positive* ratio $b/a$ (the minimum-ratio test) - that's the basic variable that hits zero first.
2. The **bottom row**. (Keep it there - that's our convention all semester.)
3. **No, you're not done.** A negative in the bottom row means you can still improve the objective by bringing that variable in - do another iteration.
4. Stop when there are **no negative numbers left in the bottom row**. At that point no variable can improve Z, so the solution is optimal.
5. Because graphical only works with **two** variables (you can't draw four dimensions). Simplex is the algebra that scales the exact same corner-hopping idea to dozens, hundreds, or thousands of variables.


*Dr. Dave Wanik - University of Connecticut*
