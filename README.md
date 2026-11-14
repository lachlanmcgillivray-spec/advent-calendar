# Santi Claws Christmas Joke Advent Calendar

A 24-door advent calendar. Each day in December a new door unlocks with a kid-friendly Christmas joke and a Santi Claws picture.

Live site: https://lachlanmcgillivray-spec.github.io/advent-calendar/

- Works on older iPads (plain HTML, CSS and ES5 JavaScript, no build step).
- Doors unlock by the device's date. Doors the kids open are remembered on that device, separately for each year.
- **Grown-up preview:** add `#preview` to the address to unlock every door. Doors opened in preview aren't remembered, and the "Close all doors & leave preview" button clears anything saved on that device.
- **Past years:** add `#year-2026` (or any year) to the address to see that year's calendar with every door open. Links to past years appear at the bottom of the page.

## How it's organised

| Path | What it is |
|---|---|
| `index.html` | The calendar page |
| `years/2026.js` | The 2026 jokes: one line per door with its picture, emoji, question and punchline |
| `img/2026/` | The 24 Santi Claws door pictures for 2026 |
| `img/background.jpg` | The village background |

## Starting a new year (e.g. 2027)

1. Add 24 new door pictures to `img/2027/` named `santi-01.png` to `santi-24.png`.
2. Copy `years/2026.js` to `years/2027.js`, change `year: 2026` to `year: 2027`, point each `pic` at `img/2027/…`, and write the new jokes.
3. In `index.html`, add `<script src="years/2027.js" charset="utf-8"></script>` under the 2026 line.
4. Check it with `#preview` before December 1.

The calendar automatically shows the set for the current year. If a new year's set hasn't been added, it reuses the most recent one. The 2026 calendar then moves to "Past calendars".
