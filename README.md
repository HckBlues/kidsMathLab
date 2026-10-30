# kidsMathLab

Little Math Lab: simple, visual math helpers for a first grader. One HTML file, no build step, no dependencies.

Open `index.html` in any browser (double-click it). Nothing is installed and nothing is sent anywhere.

## Subjects

| Subject | Status |
| --- | --- |
| Add past a ten (e.g. 28 + 5, 10 + 18) | ready |
| Subtract across a ten (e.g. 32 − 5, 35 − 18) | ready |
| Count by tens | planned |
| Tens and ones | planned |

Pick a subject at the top of the page. Opening `index.html#subtract` starts on subtraction.

## The idea

Crossing a ten is the hard part: 28 + 5 means the ones digit wraps and the tens digit changes at the same moment. The page teaches *make a ten*:

- Adding: fill up to the next ten first, then add what is left. 28 + 5 = 28 + 2 + 3 = 30 + 3 = 33.
- Subtracting: go down to the ten first, then take away what is left. 32 − 5 = 32 − 2 − 3 = 30 − 3 = 27.
- When the number has a ten in it (10 + 18, 35 − 18) the whole ten goes first, then the ones.

The same colours mean the same thing everywhere: blue is the number you start with, teal is a whole ten, orange is the part that lands on the ten, pink is what is left over.

## Ways to watch it

Choose under "Show me as":

- **Car**: a car drives along a road with a fuel tank counting down the steps. A checkpoint sits on each ten and gives a big celebration when the car lands on it. The finish flag only appears when the tank is empty. Subtraction drives the other way.
- **Hops**: a number line with a dashed jump for the whole sum and real hops that draw themselves.
- **Beads**: one straight row of 10 beads per ten.
- **Boxes of ten**: ten-frames (2 rows of 5). A frame has a grey outline until it is full.
- **Train**: each car holds 10 people. Fill a car to make a ten, then a new car pulls up. For subtraction, people get off.

## Controls

- Type or step the two numbers, or use the example buttons.
- **Next / Back / Play / Start over** step through the sum. In the car view use **Drive 1 step** and **Drive all the way**.
- Keyboard: `Space` or `→` goes forward one step, `←` goes back.
- Limits: the answer stays within 0–99 and the number added or taken away is 1–20.
- Your last chosen view is remembered in the browser.

## Notes

- Fonts load from Google Fonts. Offline, the page falls back to system fonts and works the same.
- Animations respect the system "reduce motion" setting. Light and dark themes follow the system.

## Development

Everything lives in `index.html`: styles, a step builder (`build` for adding, `buildSub` for subtracting) that every view draws from, and one renderer per view. To add a subject, add an entry to `SUBJECTS` and a step builder that returns the same shape.

## License

MIT, see [LICENSE](LICENSE).
