# PyMastery

**Master Python by solving, not scrolling.** A self-paced, non-linear Python curriculum that runs entirely in your browser from a single HTML file — no install, no build step, no server, no internet connection required.

Start anywhere. Jump anywhere. Every topic is reachable instantly, and every problem comes with a hint and a fully worked solution that explains *why*, not just *what*.

---

## What's inside

- **5 tracks · 24 topics · 72 problems**
- Roughly **10 hours** of guided reading, plus far more in solving time
- Every topic has **3 laddered problems**: Easy → Hard → Super Hard
- Every problem has a **hint** (open after a real attempt) and a **worked solution** with the reasoning spelled out
- **Progress tracking** you can save to a file and reload later
- **Search**, **light/dark themes**, **copy-to-clipboard** on every code block
- Fully **responsive** — works on phone, tablet, and desktop
- **Zero dependencies**, **zero network calls**, ~248 KB total

---

## Quick start

1. Download `pymastery.html`.
2. Double-click it. It opens in your default browser.

That's it. There is nothing to install and nothing to configure. The file is completely self-contained.

To run the Python code you learn, keep an interpreter open alongside it — [VS Code](https://code.visualstudio.com/) with the Python extension, a terminal running `python3`, or any online REPL. **This app is your map and problem book; the interpreter is your gym.**

---

## How to use it (this part matters)

No website can honestly promise a success rate — but *how you use one* changes your outcome enormously. PyMastery is built around five habits, and it will nudge you toward all of them:

1. **Type every example yourself.** Never copy-paste while learning. Your fingers are part of your memory.
2. **Struggle before the hint.** Give each problem about 15 focused minutes before opening the hint, and another 10 before the solution. The struggle *is* the learning; the solution just confirms it.
3. **Explain the solution back.** After reading a solution, close it and re-write the code from your own understanding. If you can't, you haven't learned it yet — and that's useful information.
4. **Revisit on a delay.** Re-solve yesterday's Super Hard problem from scratch today. Spaced recall beats re-reading ten times over.
5. **Build after every track.** Finish Fundamentals, then build a tiny CLI tool. Finish pandas, then analyze a dataset you actually care about. Projects convert knowledge into skill.

The suggested order in the sidebar is a **map, not a fence**. If you already know loops but want dictionaries, jump straight there — nothing is locked.

---

## Curriculum

### Track I — Python Fundamentals *(8 topics)*
The core language: how Python thinks, the data types you touch every day, and the control flow that turns ideas into programs.

Getting Started & How Python Runs · Variables, Data Types & Operators · Strings & Text Processing · Conditionals & Logic · Loops & Iteration · Lists & Tuples · Dictionaries & Sets · Functions

### Track II — Intermediate Python *(7 topics)*
Where Python starts feeling like Python: the constructs and structure that separate scripts from software.

Comprehensions · Error Handling & Exceptions · Files & Paths · OOP: Classes & Objects · OOP: Inheritance, Dunders & Dataclasses · Modules, Packages & Environments · Iterators, Generators & Functional Tools

### Track III — Advanced Python *(6 topics)*
The deep machinery, and the profiling mindset that separates guessing from engineering.

Decorators & Closures · Context Managers · Regular Expressions · Type Hints & Modern Python · Concurrency: Threads, Processes & Asyncio · Performance & Pythonic Optimization

### Track IV — NumPy & Scientific Computing *(2 topics)*
The array is the foundation every data library stands on. Vectorization, broadcasting, and the numerical thinking that makes pandas, scikit-learn, and PyTorch make sense.

The ndarray & Vectorization · Indexing, Slicing & Boolean Masks

### Track V — Data Analysis with pandas *(1 topic)*
Where analytics actually happens: labeled data, selection, and filtering.

Series, DataFrames & Selection

---

## Features in detail

**Non-linear navigation.** The left sidebar lists every track and topic. Click any topic to open it immediately — there are no prerequisites enforced anywhere. Prev/Next buttons at the bottom of each topic let you move linearly if you prefer.

**The question ladder.** Each topic ends with three problems on a color-graded rail — green (Easy), orange (Hard), pink (Super Hard). Each rung has a difficulty badge, the problem statement, a collapsible hint, a collapsible solution, and a **Mark solved** toggle.

**Progress tracking.** Marking problems solved updates the counter and progress bar in the sidebar, and completed topics get a filled dot. Use **Save progress ↓** to download your progress as a JSON file, and **Load ↑** to restore it later or on another device. (Progress lives in the file you download, so it survives even if the browser clears its data.)

**Search.** Press `/` anywhere to jump to search, then type to filter topics by title or keyword. Press Enter to open the first match, Escape to clear.

**Themes.** Toggle between dark and light with the theme button in the top bar.

**Copy code.** Hover any code block and click **copy** to grab the snippet.

---

## Design & technical notes

- **Single file.** Everything — HTML, CSS, JavaScript, and all curriculum content — lives in `pymastery.html`. Nothing is loaded from a CDN or server.
- **No tracking, no telemetry, no ads.** The file makes zero network requests. It works fully offline.
- **Security.** There is no `eval` and no untrusted HTML injection. All lesson content is HTML-escaped before rendering, so content can never inject or execute script.
- **Custom renderer.** Lessons are authored in a compact markdown-lite format and rendered by a small built-in parser, with a hand-written Python syntax highlighter for code blocks.
- **Accessibility.** Keyboard-navigable, visible focus rings, and it respects `prefers-reduced-motion`.

The whole build was validated before shipping: every embedded script was parsed with Node, all 72 problems checked for well-formedness, all 240 rendered fragments checked for balanced HTML, and the UI screenshotted on desktop and mobile.

---

## Roadmap

The curriculum is intentionally weighted toward the language core, where deep understanding compounds. Planned additions:

- **Track IV/V expansion** — more pandas (groupby and split-apply-combine, joins, time series, pivot tables) and NumPy.
- **Track VI — Data Visualization** — matplotlib and seaborn.
- **Track VII — Web & APIs** — Flask, FastAPI, and Streamlit.

The app's structure already supports new tracks; adding one is a matter of appending a data block.

---

## FAQ

**Do I need to be online?** No. Download once and it works forever, offline.

**Where is my progress stored?** In your browser session while you use it, and in the JSON file you download with **Save progress**. Reload it any time with **Load**.

**Can I use this on my phone?** Yes — the layout collapses to a single column with a slide-out menu.

**Is it really beginner-friendly?** Track I assumes no prior Python. It does assume you can open a terminal or editor to run code. If a concept references something from an earlier topic, the text says so and links the idea, but never forces the order.

**Can I edit or extend it?** Yes. Open the file in any text editor. Curriculum lives in `addTrack({...})` blocks near the bottom; each topic is a plain JavaScript object with a `body` string and a `questions` array.

---

## License

Personal, educational use. Do as you like with your own copy.
