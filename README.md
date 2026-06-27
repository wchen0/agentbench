# AgentBench 📊

**Agent Benchmark Trace Visualizer** — a static dashboard for browsing and comparing agent performance across multiple software engineering and deep-research benchmarks.

## What's Inside

This repo hosts interactive visualizations of agent evaluation runs on:

| Benchmark | Description |
|---|---|
| **SWE-bench-verified** | Curated software engineering tasks from real GitHub issues |
| **SWE-rebench** | Re-benchmarking runs with different models and configurations |
| **Deep-research-bench** | Multi-step research tasks evaluating agent reasoning depth |

Each run includes per-case trace data: the agent's actions, observations, tool calls, and final resolution status.

## Live Dashboard

👉 **[agentbench.whatever.com](https://wchen0.github.io/agentbench/)** (GitHub Pages)

## Structure

```
├── index.html                          # Landing page — directory of all runs
├── swe-bench-verified/                 # Verified SWE-bench traces (64 cases)
├── swe-bench-verified-legacy/          # Legacy SWE-bench traces (81 cases)
├── swe-rebench/                        # Legacy SWE-rebench traces (47 cases)
├── swe-rebench-20260614T175711/       # SWE-rebench run (64 cases)
├── swe-rebench-20260626T131158/       # SWE-rebench run — arm+qemu, qwen3.7-max (40 cases)
├── deep-research-bench-legacy/         # Legacy deep-research traces (7 cases)
├── deep-research-bench-20260608T052302/ # Deep-research run (10 cases)
├── deep-research-bench-20260608T085739/ # Deep-research run (53 cases)
├── deep-research-bench-20260612T054015/ # Deep-research run (13 cases)
└── deep-research-bench-20260623T075056/ # Deep-research run (32 cases)
```

## Adding New Runs

1. Create a new directory following the convention: `<benchmark-name>-<timestamp>` (e.g., `swe-rebench-20260627T120000/`)
2. Add an `index.html` with your trace data
3. Add a card to the root `index.html` linking to your new directory

## Local Development

Serve with any static file server:

```bash
python3 -m http.server 8080
# or
npx serve .
```

Then open `http://localhost:8080`.

## License

MIT © [wchen0](https://github.com/wchen0)
