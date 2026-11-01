# Stream Deck Profile Blueprint — HOLOPLOT + AutoCAD Practice (v1)

For the Elgato Stream Deck software (Mac or Windows). Every key below is a stock
**System → Hotkey** action that sends the listed keystroke to the focused browser
window running the app. The app must be the active tab in the focused browser
window — deck keys go to whatever app is frontmost.

Design law (from the cluster review):
- Anchors never move: Back bottom-left, RENDER bottom-right.
- Arrays always sit L - Centre - R, left to right, on every page.
- Keys are VERBS, not state claims (a plain hotkey key cannot see app state).
  Live / On Demand are two separate keys that SET the mode, never a toggle.
- Colours follow the app: amber = stale/render, blue = link, purple = invert,
  green = in-tolerance/live, red outline = edit mode, dark background everywhere.
- Destructive keys live in the MORE folder, never on a primary page.

Grid positions are numbered like the 15-key deck:
 1  2  3  4  5
 6  7  8  9  10
11 12 13 14 15

## Page: HOME

| Key | Title  | Sends     | Notes |
|-----|--------|-----------|-------|
| 1   | ARRAY L| F13       | speaker trapezoid + big L |
| 2   | ARRAY C| F14       | speaker trapezoid + big C |
| 3   | ARRAY R| F15       | speaker trapezoid + big R |
| 4   | PROBE  | Alt+Shift+P | person-in-pin icon; adds/removes probe |
| 5   | MORE > | (deck page/folder nav) | page dots icon |
| 6   | BEAM 1 | F16       | cone icon B1 |
| 7   | BEAM 2 | F17       | cone icon B2 |
| 8   | BEAM 3 | F18       | cone icon B3 |
| 9   | PARAM <| [         | cycles focused parameter back |
| 10  | PARAM >| ]         | cycles focused parameter forward |
| 11  | < BACK | (deck nav to previous page) | anchor, bottom-left |
| 12  | - STEP | -         | steps focused parameter down |
| 13  | + STEP | =         | steps focused parameter up |
| 14  | UNDO   | Alt+Z     | curved arrow icon |
| 15  | RENDER | Alt+R     | anchor, bottom-right; amber triangle icon |

Coarse steps: hold Shift on a real keyboard; on the deck, add optional
duplicate keys sending Shift+- / Shift+= in the MORE folder if wanted.

## Page: BEAMS

| Key | Title  | Sends     | Notes |
|-----|--------|-----------|-------|
| 1   | ARRAY L| F13       | same position as HOME |
| 2   | ARRAY C| F14       | |
| 3   | ARRAY R| F15       | |
| 4   | TAG    | Alt+P     | tags selected beam to probe |
| 5   | GROUP >| (folder)  | opens GROUP folder |
| 6   | MAIN   | 4 (plain, HOLOPLOT page) | layer-cake icon, bottom sheet lit |
| 7   | BALC   | 5 (plain, HOLOPLOT page) | layer-cake icon, top sheet lit |
| 8   | FILL   | 6 (plain, HOLOPLOT page) | layer-cake icon, middle sheet lit |
| 9   | RES    | F19       | grid icon; Low/High res toggle |
| 10  | EDIT   | Alt+E     | red outline icon; Edit Values toggle |
| 11  | < BACK | (deck nav)| anchor |
| 12  | LIVE   | Alt+Shift+L | SETS Live mode (green dot) |
| 13  | DEMAND | Alt+Shift+D | SETS On Demand mode (amber) |
| 14  | UNDO   | Alt+Z     | |
| 15  | RENDER | Alt+R     | anchor, bottom-right |

Layer keys send plain 4 / 5 / 6 while you are on the deck's BEAMS page;
in the app those keys toggle the layers only on the HOLOPLOT page and are
ignored while typing (same guard as every plain key).

## Folder: GROUP (link / invert / fan — only meaningful when linked)

| Key | Title  | Sends     | Notes |
|-----|--------|-----------|-------|
| 1   | LINK   | Alt+L     | chain icon, blue; toggles selected array in/out |
| 2   | INV PAN| Alt+X     | mirror arrows, purple |
| 3   | INV TLT| Alt+C     | mirror arrows rotated, purple |
| 4   | FAN    | Alt+F     | three-wedge fan icon; fans focused parameter |
| 5   |        |           | |
| 11  | < BACK | (folder exit) | anchor |

Fan amount is set on screen (or with - STEP / + STEP while Fan amount is the
focused parameter). Saved-group apply/save stays on screen in v1.

## Page: PROBE (slices)

| Key | Title  | Sends     | Notes |
|-----|--------|-----------|-------|
| 1   | TOP    | F13       | cube icon, top face shaded |
| 2   | FRONT  | F14       | cube icon, front face shaded |
| 3   | SIDE   | F15       | cube icon, side face shaded |
| 4   | SOLO < | [         | cycles beam selection for solo |
| 5   | SOLO > | ]         | |
| 6   | SOLO   | S (on Probe page) | toggles solo |
| 7   | ALL    | A (on Probe page) | all beams |
| 11  | < BACK | (deck nav)| anchor |
| 12  | SLICE -| -         | slice offset down |
| 13  | CENTRE | 0         | centre slice on probe |
| 14  | SLICE +| =         | slice offset up |
| 15  | RENDER | Alt+R     | anchor, bottom-right |

## Folder: MORE (setup + destructive, deliberately off the primary pages)

- Page jumps: keys sending Alt+1 .. Alt+7 (HOLOPLOT, Probe, AutoCAD, Lessons,
  Drills, Projects, Comments)
- Tutor toggle: Alt+T
- Reset Beams, Delete, Clear drawing: NOT assigned in v1 — use Undo (Alt+Z)
  on the main pages and do deletes on screen. (Cluster rule: recovery faster
  than the mistake path.)

## Pages for the other deck sizes

- 32-key XL: same anchors at the same relative corners; add Width and
  Position stepper pairs, layer keys, and TAG on the HOLOPLOT page.
- 6-key Mini: verbs only — Array cycle (F13), Beam + (F17), Link (Alt+L),
  Undo (Alt+Z), Probe page jump (Alt+2), RENDER (Alt+R).
- Stream Deck + dials: Dial 1 Azimuth (rotate -/= with [ focus on Azimuth,
  push = ] cycle), Dial 2 Gain, Dial 3 Tilt, Dial 4 context — Slice offset
  on the Probe page (push = 0, centre on probe). Dial strip shows parameter
  names only at this tier; live values need the future state bridge.

## Honest limits of v1

- One-way only: keys cannot light up with app state (no live STALE count,
  no true link/invert indication). The app screen is the state display.
- The app tab must be focused. Smart Profiles follow the browser program,
  not the tab; a dedicated browser window/profile for the app keeps this clean.
- The USB deck cannot control the app on the iPad. Deck = desktop browser.
