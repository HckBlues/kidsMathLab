# Little Math Lab: Free 1st Grade Math Visualizer for Adding and Subtracting Past 10

**Little Math Lab** is a free, interactive math visualizer for 1st and 2nd grade. It helps children see how to **add and subtract across a ten** (like 28 + 5 or 32 − 5), **count by tens**, and understand **tens and ones (place value)**, using a car, a number line, beads, ten frames and a train.

**[▶ Try it online: hckblues.github.io/kidsMathLab](https://hckblues.github.io/kidsMathLab/)**

It is a single HTML file. No install, no sign-up, no ads, no tracking. Open the link above, or open `index.html` in any browser, on a computer, tablet or phone.

> Made by a parent for a first grader who kept getting stuck on "going over the ten": why does 10 + 18 become 28, and why does 28 + 5 go past 30?

## Math topics covered

| Topic | Examples | What the child sees |
| --- | --- | --- |
| [Adding past a ten](#adding-past-a-ten-the-make-a-ten-strategy) | 28 + 5, 17 + 6, 49 + 4, 10 + 18 | Fill up to the next ten, then add what is left |
| [Subtracting across a ten](#subtracting-across-a-ten) | 32 − 5, 41 − 6, 14 − 6, 35 − 18 | Go down to the ten, then take away the rest |
| [Counting by tens](#counting-by-tens) | 14, 24, 34, 44 | Each jump adds one ten, the ones never change |
| [Tens and ones (place value)](#tens-and-ones-place-value) | 34 = 3 tens and 4 ones | A number built from full tens and loose ones |

Related ideas: make-a-ten strategy, bridging through ten, ten frames, number line jumps, regrouping, place value, mental math within 100.

## Five ways to watch the same problem

Pick a picture under "Show me as". Every picture uses the same colours: **blue** is the number you start with, **teal** is a whole ten, **orange** is the part that lands on the ten, **pink** is what is left over.

- **Car**: a car drives along a number road with a fuel tank that counts down the steps. A checkpoint sits on each ten and gives a big celebration when the car lands on it. The finish flag appears only when the tank is empty. Subtraction drives the other way.
- **Hops** (number line): a dashed jump for the whole sum, then real hops that draw themselves.
- **Beads**: one straight row of 10 beads per ten.
- **Boxes of ten** (ten frames): 2 rows of 5. A frame keeps a grey outline until it is full.
- **Train**: each car holds 10 people. Fill a car to make a ten, then a new car pulls up. For subtraction, people get off.

## How it teaches

### Adding past a ten: the make-a-ten strategy

Counting on past 30 is hard because the ones digit wraps back to 0 and the tens digit changes at the same moment. Instead, make a ten first:

28 + 5 = 28 + 2 + 3 = 30 + 3 = **33**

When the number being added has a ten in it, add the whole ten first: 10 + 18 = 20 + 8 = **28**. Only the tens digit changes, then the ones are added.

### Subtracting across a ten

Going back past a ten has the same problem in reverse. Take away just enough to land on the ten, then take away the rest:

32 − 5 = 32 − 2 − 3 = 30 − 3 = **27**

When there are not enough ones, a ten opens up into 10 ones. When the number to take away has a ten in it, take the whole ten first: 35 − 18 = 25 − 8 = **17**.

### Counting by tens

14, 24, 34, 44, 54. Adding ten only changes the tens digit. The ones digit stays put, which is the basis of place value and of adding 10 or 20 to any number.

### Tens and ones (place value)

34 is 3 tens and 4 ones, or 30 + 4. Full frames (or full train cars) are tens and the loose counters in the last frame are ones.

## Frequently asked questions

**How do I teach a first grader to add past 10?**
Use the make-a-ten strategy: ask "how many more to the next ten?", fill that gap first, then add the leftover. The car, ten-frame and train views all show this step by step.

**How do you explain 28 + 5?**
28 needs 2 more to become 30. Split the 5 into 2 and 3. 28 + 2 = 30, then 30 + 3 = 33.

**Why is crossing a ten so confusing for kids?**
At the moment the count passes a ten, the ones digit resets and the tens digit goes up at once. Seeing a full ten frame, a full train car or a checkpoint on the number line makes that moment visible.

**How do you subtract across a ten?**
Go down to the ten first (32 − 2 = 30), then subtract what is left (30 − 3 = 27).

**What grade is this for?**
1st grade, and it is a handy review for 2nd grade. It lines up with the ideas in Common Core 1.OA.C.6 (making ten), 1.NBT.B.2 (tens and ones) and 1.NBT.C.4 (adding within 100).

**Does it cost anything or collect data?**
No. It is free and open source (MIT). Everything runs in your browser. There is no tracking and no analytics, and the only request it makes is for the rounded font from Google Fonts.

## Use it

Open `index.html` in a browser. To start on a given subject, add `#add`, `#subtract`, `#tens` or `#place` to the address, for example `index.html#subtract`.

- Type or step the numbers, or use the example buttons.
- **Next / Back / Play / Start over** step through the sum. In the car view use **Drive 1 step** and **Drive all the way**.
- Keyboard: `Space` or `→` goes forward one step, `←` goes back. In the car view the arrows move the car left and right, and the key legend in the top right shows what each key does.
- The answer stays within 0–99 and the number added or taken away is 1–20.
- Your last chosen view is remembered in the browser.

## Notes

- Light colour scheme, with animations that respect the system "reduce motion" setting.
- Fonts load from Google Fonts. Offline, the page falls back to system fonts and works the same.

## Development

Everything lives in `index.html`: styles, step builders (`build`, `buildSub`, `buildTens`, `buildPlace`) that all views draw from, and one renderer per view. To add a subject, add an entry to `SUBJECTS` and a builder that returns the same shape (see `finishModel`).

## License

MIT, see [LICENSE](LICENSE).
