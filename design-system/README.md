# Penny

Spend a little less each month. Penny records what you spend in a few taps, sets a target a bit lower than last month, and shows every day whether you are on track. It runs as a web app you add to the Home Screen.

## Principles

1. **Less and less.** Every screen answers one question. Am I spending less than before? The change line, the target and the streak all serve that.
2. **Three taps or less.** Amount, category, save. No names, no shops, no forms. A note is optional.
3. **Quiet and minimal.** One warm background on every screen, light type, white cards, no hero, no shadows except the tab bar. The same direction as SaySay and Manna.
4. **Gold for one thing.** `primary` fills only the main action on a screen and this month's bar. Gold text is always `gold-text`.
5. **Less is gold, more is coral.** Saving shows in `gold-text`, spending more in `coral-text`, always with the words less or more.

## Content

- Plain words, sentence case, short. No colons, semicolons or dashes in UI text.
- Euro only. Totals round to whole euros, the amount in Add shows cents.
- An entry's title is its category. A note shows under it only when one was added.
- Changes read as €96 less or €22 more. No change reads Same.
- English only for now.

## Fair compare

- Month compares with the same days of last month. On the 18th it compares 1 to 18 November with 1 to 18 October, and reads €96 less than this time in October.
- A month still running is marked So far in charts and never counted as a full month.

## Target

- Each month's target is last month's total minus 5%. People can change the percentage in Settings.
- Month shows the target as one thin `gold-line` bar on `track` under the change line, with €141 left for 12 days on the left and Target €1,425 on the right.
- Over target, the bar and the left amount turn `coral-text` and read €40 over.
- A month that ends under target adds one to the streak, and the next target is set from it.

## Color

| Role | Tokens | Use |
| --- | --- | --- |
| Ground | `bg`, `surface` | Every screen, cards, pills, the tab bar |
| Text | `ink`, `muted`, `quiet` | Amounts and names, labels, unused arrows |
| Action | `primary`, `soft` | The one main button, this month's bar, selected tab and pill |
| Progress | `gold-line`, `track` | Target bar, category bars, chart bars |
| Saving | `gold-text` | Less than before, streaks, links |
| More | `coral-text`, `coral-soft` | More than before, over target, delete |

Rules
- `primary` is a fill. Text on it is `ink`, never white.
- No colour per category. The name is enough.
- Text passes 4.5 to 1 wherever it sits. The token notes list each pair.

## Categories

Eight to start. Groceries, Eating out, Home, Transport, Shopping, Fun, Health, Other. People can rename them and add more later.

## Typography

One typeface, Outfit, from Google Fonts. Weights 300, 400 and 500 only.

| Style | Size | Weight | For |
| --- | --- | --- | --- |
| `amount-entry` | 72 | Light | The amount in Add |
| `amount` | 60 | Light | Spent this month |
| `figure` | 56 | Light | The saving on Compare |
| `title` | 28 | Light | Screen titles |
| `button` | 17 | Medium | Buttons and section labels |
| `label` | 17 | Regular | The word above a big number |
| `body` | 16 | Regular | Names and amounts in cards |
| `small` | 15 | Regular | Change line, dates, Today |
| `caption` | 13 | Regular | Target line, pills, chart labels |

Rules
- Big numbers are light, never bold. Weight 500 only marks a change, a streak, a button or the selected tab.
- All amounts use tabular numbers.

## Layout

- 28 side margin and 64 from the top on every screen.
- The big number leads each screen. Cards follow, 24 apart.
- Cards are white with `radius-card` and no border. Rows have no dividers.
- The main button sits full width 16 above the tab bar.

## Navigation

- Three tabs, Month, Compare and Settings, in a full width white bar at the bottom with `shadow-nav`. The selected tab gets `soft` and `gold-text`.
- Add spending on Month opens Add.

## Screens

- **Month.** The month with arrows, Spent, the total, the change line, the target bar, then the top four categories with thin bars and a more link.
- **Add.** Close and Today at the top, the amount, Add a note, eight category pills in a 4 by 2 grid, the number pad, Save. The selected pill gets `soft` with a 1.5 `gold-line` ring.
- **Compare.** The title, the saving against June as the big number, the streak, bars for the last six months with this month in `primary` marked So far, then Since October with the four biggest changes.

## Iconography

- Line icons, round caps and joins, 24 grid, 1.6 line, 1.8 for small arrows.
- The mark is a smiling coin on `primary`.

## Accessibility

- WCAG 2.2 AA. Targets are at least 44.
- Every icon button has a label. Bars and charts have a text label with every value.
- Motion stops when reduced motion is on.
