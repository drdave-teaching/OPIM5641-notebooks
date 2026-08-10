# Module 2.2 Talking Points - The Simplex Method

**OPIM 5641 - Business Decision Modeling · Dr. Dave Wanik · University of Connecticut**

The ideas behind the Simplex videos - the things I say out loud that you should be able to explain to a
classmate or an interviewer without opening a notebook. Skills are what you can *do*; this is what you
*understand*.

---

## 1 · Why Simplex has to exist

**Three methods, one scoreboard.** Brute force ground through **10 million combinations** for the
furniture problem and was *transparent but horrible* - correct, and hopelessly inefficient. The graphical
method was *fantastic* - millions of combinations collapse to **five corner points** - and then it dies,
because **it only works in two dimensions.** Simplex evaluated **three** solutions on Wyndor and stopped.
That progression is the whole story of this module.

**The one-sentence definition:** Simplex is an **iterative, algebraic technique** - the *algebraic
enhancement of the geometric graphical method*. Everything we did by eye on a graph gets condensed into a
compact **tableau** we can work through systematically.

**The payoff is dimensions.** Three decision variables, five, **forty** - Simplex doesn't care. You can't
draw 40 dimensions; you can still pivot in them.

## 2 · The geometry (before any algebra)

**Adjacency has a definition.** Two corner points are **adjacent if they share a constraint boundary**.
$(0,0)$ shares the $x_1$ axis with $(4,0)$; $(0,6)$ shares the $x_2$ axis with $(0,0)$.

**The optimality test, formally:** for any LP that possesses at least one optimal solution, **if a corner
point feasible solution has no adjacent corner point feasible solutions that are better as measured by
$Z$, then that corner point is optimal.** That is why you can stop early - you never have to check the
rest of the region.

**Walking the edges, not the interior.** Simplex isn't going clockwise or counterclockwise on purpose -
it is **tracing the edges of the feasible region** until no neighbor improves.

**Greed picks the direction.** From the origin: across $x_1$ earns \$3,000, up $x_2$ earns \$5,000.
**You're going to be greedy and go up $x_2$.** Slope tells you where to go before you know a single
neighbor's value - and in a real problem you *never* know your neighbors in advance.

**Corner point vs. corner point *feasible*.** $(0,9)$ is a genuine corner point and it is **not** feasible.
Only points on the feasible region count. Knowing where to stop is the minimum ratio test's whole job.

## 3 · Slack variables and augmented form

**Slack = surplus = the unused quantity.** If $x_1 \le 4$ and $x_1 = 1$, then $x_3 = 3$. If that's painting
hours in a department, you have **three hours nobody used**. Slack is real; it's idle capacity.

**One slack variable per constraint.** Three constraints, three slacks. Inequalities become **equations** -
and equations are what algebra can chew on.

**"Do nothing" is a feasible plan.** From my environmental engineering days: you walk into a contaminated
site and the first candidate solution is genuinely *leave it alone*. Same in manufacturing - **make
nothing**. It's a bad solution and a perfectly feasible one, which is exactly why **the origin is our free
starting point.**

**Naming is your choice, theory isn't.** Call them $x_3, x_4, x_5$ or $s_1, s_2, s_3$ - doesn't matter.
The theory doesn't move.

## 4 · The vocabulary that everything else rests on

> **Non-basic variables are set equal to ZERO. Basic variables are NON-zero.**

**Write it on a piece of paper - notice how it's kind of backwards.** This is the single most important
line in the notebook.

**How you spot them in a tableau:** **basic variables appear once and have a coefficient of 1.** If a
column is *full of junk* - appears more than once, non-zero coefficients - that variable is zero.

**Degrees of freedom explain the whole setup.** Five variables and three equations means **two degrees of
freedom**, which means you *cannot* solve the system - too many unknowns. So you **zero two of them out**,
and Simplex chooses which two, systematically.

**The count is fixed:** the number of basic variables equals the number of functional constraints.

**Basic solution vs. corner point solution:** the *only* difference is whether the slack variables' values
are written down. A **basic feasible solution IS a corner point feasible solution in augmented form.**

## 5 · The four moves

1. **Entering variable** - the **biggest negative number in the bottom row**; circle that column.
2. **Departing variable** - the **minimum ratio test**: right-hand side ÷ the element in that column, and
   take the **smallest** result. A zero denominator is unbounded and doesn't count.
3. **Pivot element** - where the circled row and column intersect. Divide the whole row to make it a **1**.
4. **Gauss-Jordan** - add multiples of that cleaned-up row to the others so the entering variable appears
   once with coefficient 1. *"The opposite of whatever's sitting there, times your new special row."*

**Why the row operations are legal:** multiplying an equation of a line by a constant leaves the same line.
That's the entire licence for pivoting.

**Why the bottom row is negated.** $Z = 3x_1 + 5x_2$ gets rearranged so everything sits on the left and a
constant sits on the right - **that's where the minus signs come from.** And then the sign convention does
the work: **a negative number in the bottom row means a rate of improvement is still available.** No
negatives left means your neighbors can't beat you, so **you're optimal.**

**The minimum ratio test in one sentence:** it tells you **where to stop** - which constraint you smack
into first.

## 6 · Reading the answer, and what it means

**Read-off rule:** appears once with coefficient 1 → read its value straight off the right-hand side.
Full of junk → it's zero.

**Tie every tableau back to the picture.** After pivot 1 on Wyndor you're at $(0,6)$ with $Z = 30$ - *that
is a point you already drew.* After pivot 2 you're at $(2,6)$ with $Z = 36$. **Tie it back to graphical so
it really sticks.**

**Binding vs. non-binding.** A constraint with **slack left over is non-binding** - there's wiggle room.
A constraint whose **slack variable went to zero is binding** - it is genuinely constraining your problem.
That's the seed of **sensitivity analysis** later.

**Where people actually lose points:** not the concept - **careless arithmetic in the intermediate row
operations.** Negative five plus five is zero; zero plus five halves is five halves. It isn't hard, but
you can get lost in it. Be careful.

## 7 · What's tested, and what isn't

**Not tested:** the longhand algebra walk. It exists so you appreciate the equalities and the math
underneath.

**Tested:** translate the word problem into **augmented form** (that's the first 10 points), write the
**initial simplex tableau** (another 10 points), then **perform the iterations** and read off the solution
in augmented form. On many assessments you only pivot **once**, to prove you know the mechanics.

**And the study method, said out loud:** solve it once, put it away, come back three hours later and solve
it again, sleep, wake up, solve it again. **You're going to have Simplex down cold, I promise.**

---

## The bridge to what's next

Brute force is honest and dies. Graphical draws a picture and dies at two variables. Simplex walks corners
algebraically in any number of dimensions - and you just watched a computer do in a second what took pages
of longhand.

That's the handoff to **Module 3 and Pyomo**: you now know what the solver is doing under the hood, which
is the entire reason this module exists.
