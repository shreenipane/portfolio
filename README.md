# Shree Nipane · Portfolio

**Live site: [shreenipane.github.io/portfolio](https://shreenipane.github.io/portfolio/)** · [Résumé (PDF)](https://shreenipane.github.io/portfolio/resume.pdf)

B.Tech in Computer Science and Engineering at VIT Vellore, graduating 2028. I work on Linux systems, and I'm
looking for software engineering internships in systems, infrastructure and applied ML.

## Projects on the site

| Project | What it does | Result | Links |
|---|---|---|---|
| **Verdict** | Decides whether a network packet is malicious, inside the Linux kernel, at the earliest point on the receive path | 250 ns of CPU time per classified packet; 2,080,804 arithmetic cases checked exhaustively with zero mismatches | Code private while a patent application is considered |
| **VAGUS** | cgroup v2 resource manager that protects latency-critical services from noisy neighbours, with journaled limits and automatic rollback | Service P99 latency 258 ms → 9.0 ms beside a CPU hog and a UDP flood | [Repository](https://github.com/shreenipane/VAGUS) |
| **PulseGlass** | Estimates heart rate from webcam video in the browser and withholds the reading when the signal isn't reliable; video never leaves the device | Signal-processing core covered by 33 unit tests | [Live demo](https://pulse-glass.vercel.app) · [Repository](https://github.com/shreenipane/pulse-glass) |
| **Momentum** | Spreadsheet-style task manager with notebooks, inline editing, search and full undo/redo | Plain HTML, CSS and JavaScript, no dependencies | [Repository](https://github.com/shreenipane/momentum) |

## What's in this repository

| File | Purpose |
|---|---|
| `index.html` | The whole site in one file: markup, CSS and a few lines of script for the copy-email button |
| `resume.html` | Source of the résumé |
| `resume.pdf` | The résumé, printed from `resume.html` |

No framework, no build step and no tracking. Fonts come from Google Fonts (Big Shoulders Display, Hanken Grotesk and
Spline Sans Mono), and the page follows the visitor's light or dark setting.

## Run it locally

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Update the résumé

Edit `resume.html`, then print it to PDF. The time budget gives the web font a moment to load before printing:

```sh
google-chrome --headless --no-pdf-header-footer --virtual-time-budget=5000 --print-to-pdf=resume.pdf resume.html
```

## Publishing

GitHub Pages serves the `main` branch. A push to `main` is live in about a minute.

## Contact

shreenipane@gmail.com · [LinkedIn](https://www.linkedin.com/in/shreenipane) · [GitHub](https://github.com/shreenipane)
