# Quiz 1 - Python & pandas Fundamentals
**OPIM 5641 · Business Decision Modeling - Dr. Dave Wanik, University of Connecticut**

*Quick warm-up for today's studio - 5 questions to flex what you picked up in the async videos. About 5-10 minutes. Answer key's at the bottom, but give it an honest shot first!*

---

**1. (concept)** Python counts from zero. In the list `prices = [10, 20, 30, 40]`, what does `prices[2]` give you?

**2. (concept)** You just loaded a dataframe `df`. What's the difference between `df.dtypes` and `df.describe()` - when would you reach for each?

**3. (read the code)** What does this line return, and how is it different from `df['population']`?
```python
df[df['population'] <= 1000]
```

**4. (why it matters)** Why do I nag you to run `df.shape` right after you load data, every single time?

**5. (do it)** In one line of pandas, get the **average** `median_income` for the rows where `population` is less than 1000.

---

## Answer key

1. **30.** Index 0 is 10, index 1 is 20, index 2 is 30. Counting from zero trips up everyone at first.
2. `df.dtypes` tells you the *type* of each column (is `percChange` secretly a string?); `df.describe()` gives you the *summary stats* (count, mean, min/max, quartiles) for the numeric columns. Check dtypes when something won't compute; describe when you want the shape of the data.
3. It returns **all the rows** where population is 1000 or less (a filtered dataframe, all columns). `df['population']` returns a **single column** (all rows). One filters rows, the other selects a column.
4. Because you can't trust code you can't size up. Knowing it's (17000, 9) tells you the filter worked, the merge didn't explode, and you didn't accidentally drop half your data. It's the cheapest sanity check there is.
5. `df[df['population'] < 1000]['median_income'].mean()`


*Dr. Dave Wanik - University of Connecticut*
