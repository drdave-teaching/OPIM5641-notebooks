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

Where the price list gives no size (just "French Fries"), the regular or medium size from MenuStat is
used and the item name says so, for example "French Fries (medium)".

## The rules files

- `team_rules.csv` - the per-person, per-day rules used in class with McDonald's.
- `assignment_rules.csv` - a looser set that **every** restaurant below can satisfy (checked with a
  solver). Many of these menus are **infeasible** under the tighter class rules, mostly because of sodium.

## The menus

| Restaurant | File | Items | Prices updated |
|---|---|---|---|
| McDonald's (class example) | `mcdonalds_menu.csv` | 23 | July 11, 2026 |
| Arby's | `arbys_menu.csv` | 18 | July 12, 2026 |
| Bojangles | `bojangles_menu.csv` | 17 | July 26, 2026 |
| Burger King | `burger_king_menu.csv` | 18 | July 11, 2026 |
| Chick-fil-A | `chick_fil_a_menu.csv` | 21 | July 24, 2026 |
| Culver's | `culvers_menu.csv` | 14 | August 16, 2026 |
| Dairy Queen | `dairy_queen_menu.csv` | 13 | July 12, 2026 |
| Del Taco | `del_taco_menu.csv` | 28 | July 27, 2026 |
| Hardee's | `hardees_menu.csv` | 11 | July 28, 2026 |
| Jack in the Box | `jack_in_the_box_menu.csv` | 30 | July 12, 2026 |
| Krystal | `krystal_menu.csv` | 12 | July 30, 2026 |
| Panera Bread | `panera_bread_menu.csv` | 30 | July 26, 2026 |
| Sonic | `sonic_menu.csv` | 18 | July 22, 2026 |
| Starbucks | `starbucks_menu.csv` | 19 | July 11, 2026 |
| Steak 'n Shake | `steak_n_shake_menu.csv` | 13 | July 28, 2026 |
| Subway | `subway_menu.csv` | 16 | July 12, 2026 |
| Taco Bell | `taco_bell_menu.csv` | 20 | July 11, 2026 |
| Wendy's | `wendys_menu.csv` | 29 | July 22, 2026 |
| Whataburger | `whataburger_menu.csv` | 19 | July 26, 2026 |
| White Castle | `white_castle_menu.csv` | 16 | August 16, 2026 |
| Zaxby's | `zaxbys_menu.csv` | 11 | July 28, 2026 |

`menus_index.csv` has the same list in a file.
