# Titan Autoresearch

Autonomous LLM research experiments focused on AMD Strix Halo hardware, local inference, and benchmark-driven iteration.

[![Platform](https://img.shields.io/badge/Platform-AMD%20Strix%20Halo-orange)](#)
[![Python](https://img.shields.io/badge/Python-3.11+-blue)](#)

## Live Demo

- Repository: `https://github.com/tylerdotai/titan-autoresearch`
- Dashboard prototype: `new-dashboard.html`

## About

Titan Autoresearch is a public snapshot of a local-first LLM research effort. The repo captures the hardware assumptions, benchmark data, and operating patterns behind autonomous experimentation on AMD Strix Halo systems, with a focus on practical throughput and iterative model scaling.

## Tech Stack

| Layer | Technology |
|-------|------------|
| Research Notes | Markdown |
| Dashboard | HTML |
| Runtime | Python workflows |
| Inference | `llama-server` / llama.cpp |
| Hardware Focus | AMD Strix Halo |

## Features

### Research Snapshot
- Hardware and model setup notes for AMD Strix Halo
- Throughput and scaling benchmarks across multiple model sizes
- Reference launch flags for local inference tuning

### Repo Assets
- Public benchmark documentation in `README.md`
- Dashboard prototype in `new-dashboard.html`
- Published view into the broader Titan Autoresearch effort

## Project Structure

```text
README.md             Public overview, benchmarks, and operating notes
new-dashboard.html    Dashboard prototype for viewing research progress
```

## Getting Started

### Prerequisites

- AMD Strix Halo-class hardware or comparable local inference setup
- Python 3.11+
- `llama-server` configured for local model serving

### Installation

```bash
git clone https://github.com/tylerdotai/titan-autoresearch.git
cd titan-autoresearch
```

## Deployment

There is no formal deployment target yet.

- Repository: `https://github.com/tylerdotai/titan-autoresearch`

## Usage

```bash
open new-dashboard.html
```

## Current Limitations

- The public repo does not yet include the full training harness
- Benchmarks are documented, but reproducible scripts are still limited
- Setup instructions are hardware-specific and assume a local experimentation workflow

## Roadmap

- Publish the reproducible training pipeline
- Add benchmark automation and result export
- Document the full local inference stack end to end
- Expand the dashboard beyond a static prototype

## License

No license has been added yet.
