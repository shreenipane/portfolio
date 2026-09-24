# Shree Nipane · Portfolio

**Live site: [shreenipane.github.io/portfolio](https://shreenipane.github.io/portfolio/)** · [Résumé (PDF)](https://shreenipane.github.io/portfolio/resume.pdf)

B.Tech in Computer Science and Engineering at VIT Vellore, graduating 2028, based in Vellore, India. I work on Linux
systems, from packet processing inside the kernel to resource management for servers, and I'm looking for software
engineering internships in systems, infrastructure and applied ML.

## Projects on the site

| Project | What it does | Result | Links |
|---|---|---|---|
| **Verdict** | Decides whether a network packet is malicious, inside the Linux kernel, at the earliest point on the receive path | 250 ns of CPU time per classified packet; 2,080,804 arithmetic cases checked exhaustively with zero mismatches | Code private while a patent application is considered |
| **VAGUS** | cgroup v2 resource manager that protects latency-critical services from noisy neighbours, with journaled limits and automatic rollback | Service P99 latency 258 ms → 9.0 ms beside a CPU hog and a UDP flood | [Repository](https://github.com/shreenipane/VAGUS) |
| **PulseGlass** | Estimates heart rate from webcam video in the browser and withholds the reading when the signal isn't reliable; video never leaves the device | Signal-processing core covered by 33 unit tests | [Live demo](https://pulse-glass.vercel.app) · [Repository](https://github.com/shreenipane/pulse-glass) |
| **Momentum** | Spreadsheet-style task manager with notebooks, inline editing, search and full undo/redo | Plain HTML, CSS and JavaScript, no dependencies | [Repository](https://github.com/shreenipane/momentum) |

## How I work

- **I check my own numbers.** When a review I ran found that VAGUS's first benchmark was starving its own load
  generator, I withdrew the headline result, re-ran the experiment with an open-loop load and a protected client, and
  published the raw latencies.
- **I'd rather report nothing than something wrong.** PulseGlass shows no heart rate instead of a noisy one. VAGUS
  refuses to act on missing or stale telemetry and rolls back any change that makes the protected service's stall rate
  worse.
- **I compare against the strongest simple baseline.** VAGUS's placement policy is reported against forecast-aware
  First-Fit (12.3% vs 10.2% overload), not only plain First-Fit. Its LSTM forecaster is compared with ARIMA and a
  seasonal-naive model; the naive model came close and the attention layer measured as inert, and the write-up says so.
- **I test whether my tests can fail.** Verdict's tests caught 22 of 23 deliberately injected bugs, and the one that
  survived turned out to be equivalent code. Every one of its 2,080,804 arithmetic cases is checked against a separately
  written implementation.
- **I make changes to live systems reversible.** VAGUS previews every change by default, journals each one before
  writing it so an interrupted apply can be undone exactly, and lets only one writer run at a time.

## Skills

- **Languages:** C (primary), Python, C++, Java, SQL, TypeScript
- **Linux and kernel:** eBPF and the BPF verifier, cgroups v2, PSI, softirq accounting, systemd, /proc and cgroupfs
- **Networking:** TCP/IP header parsing, packet processing, pcap/pcapng datasets
- **Machine learning:** PyTorch (sequence forecasting, reinforcement learning)
- **Testing:** differential, exhaustive and mutation testing; performance measurement
- **Tools:** Git, GCC, Make, QEMU/KVM, bubblewrap, pytest; daily Linux (Fedora) user

## Education and certification

- **Vellore Institute of Technology (VIT), Vellore** · B.Tech in Computer Science and Engineering · 2024 – 2028
- **AWS Certified AI Practitioner (AIF-C01)** · Amazon Web Services

## What's in this repository

| File | Purpose |
|---|---|
| `index.html` | The whole site in one file: markup, CSS and a few lines of script for the copy-email button |
| `resume.html` | Source of the résumé |
| `resume.pdf` | The résumé, printed from `resume.html` |

No framework, no build step and no tracking. Fonts come from Google Fonts (Big Shoulders Display, Hanken Grotesk and
Spline Sans Mono), and the page follows the visitor's light or dark setting. GitHub Pages serves the `main` branch.

## Contact

shreenipane@gmail.com · [LinkedIn](https://www.linkedin.com/in/shreenipane) · [GitHub](https://github.com/shreenipane)
