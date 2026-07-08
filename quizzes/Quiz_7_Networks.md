# Quiz 7 - Network Optimization
**OPIM 5641 · Business Decision Modeling - Dr. Dave Wanik, University of Connecticut**

*Quick warm-up for today's studio - 5 questions to flex what you picked up in the async videos. About 5-10 minutes. Answer key's at the bottom, but give it an honest shot first!*

---

**1. (concept)** What is a **minimum-cost-flow** problem? Name two specific problems it covers.

**2. (concept)** The **assignment problem** matches N things to N slots. What's remarkable about its solution even when you solve it as a plain LP?

**3. (interpret)** Shortest path isn't just for maps. Give one **non-map** example of a shortest-path problem.

**4. (why it matters)** Why is the **Traveling Salesman Problem** the perfect "hard problem" capstone for this course?

**5. (concept)** What's the difference between a **transportation** problem and a **transshipment** problem?

---

## Answer key

1. Min-cost flow moves goods through a **network of nodes and arcs** as cheaply as possible while respecting supply, demand, and capacities. It covers, e.g., **transportation** (plants to warehouses) and **transshipment** (through intermediate hubs) - also assignment and shortest path as special cases.
2. It comes out **whole numbers automatically** - even solved as a regular LP with no integer restriction, the assignment problem lands on a clean 0/1 matching. (That's a special, beautiful property of the network structure.)
3. Lots of options: **project scheduling** (cheapest sequence of tasks), **equipment replacement** (when to replace a machine over N years), or converting a currency through a chain of exchanges. Any "cheapest sequence of steps" is a shortest path.
4. Because it's where brute force **spectacularly dies** - the number of routes explodes factorially (remember the googol), so you can't enumerate. It's the perfect motivation for specialized solvers and heuristics, and it ties the whole course together.
5. **Transportation** ships directly from sources to destinations. **Transshipment** adds **intermediate pass-through nodes** (warehouses/hubs) that goods can flow *through* on the way - same min-cost-flow model, just extra nodes.


*Dr. Dave Wanik - University of Connecticut*
