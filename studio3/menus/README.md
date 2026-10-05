# Restaurant menus for the diet problem (OPIM 5641, Studio 3)

One CSV per restaurant, all in the same format, so the same Pyomo notebook works for any of them:

`item, category, price, calories, protein, carbs, fiber, sugar, fat, sat_fat, sodium`

**The data is real, from two public sources:**

- **Nutrition:** MenuStat (New York City Department of Health and Mental Hygiene), 2018 edition, from
  NYC Open Data, dataset "DOHMH MenuStat (Historical)". Units: calories (kcal); protein, carbs, fiber,
  sugar, fat, saturated fat (grams); sodium (milligrams). One row is one menu item as sold.
- **Prices:** the chain's menu price list on fastfoodmenuprices.com, with the "prices updated" date
  shown in the table below. Prices vary by location.

A menu contains the items that appear in **both** sources under the same name (a handful of renamed
items were matched by hand). Combo meals, catering packs, condiments and zero-calorie drinks are left
out, and so are a few rows whose published numbers contradict each other (for example, more sugar
than total carbohydrates).

`team_rules.csv` holds the per-person, per-day nutrition rules used in class.
