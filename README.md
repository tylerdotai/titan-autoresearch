# Titan Autoresearch

Autonomous LLM research experiments focused on AMD Strix Halo hardware, local inference, and benchmark-driven iteration.

## Status

- Experimental research repo
- Current repo is primarily documentation and benchmark tracking
- Training harness and reproducible automation are not fully published here yet

## About

Titan Autoresearch is a working notebook-style repository for local LLM research on AMD Strix Halo hardware. It captures the hardware setup, benchmark results, and operating assumptions behind an autonomous research workflow built around local inference and iterative model training.

## Current Scope

- Hardware and model setup notes for AMD Strix Halo
- Throughput and scaling benchmarks across model sizes
- Reference launch flags for local inference
- A dashboard prototype in `new-dashboard.html`
- A public snapshot of the broader Titan Autoresearch effort

## Built With

- Markdown
- HTML
- Python workflows
- llama.cpp / `llama-server`
- Local LLM research infrastructure

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

## Development

This repo currently serves best as a reference for the research setup rather than a turnkey training package.

```bash
open new-dashboard.html
```

## Deployment

There is no formal deployment target yet.

- Repository: `https://github.com/tylerdotai/titan-autoresearch`

## Current Limitations

- The public repo does not yet include the full training pipeline
- Benchmarks are documented, but reproducible scripts are still limited
- Setup instructions are hardware-specific and assume a local experimentation workflow

## Roadmap

- Publish the reproducible training harness
- Add benchmark automation and result export
- Document the full local inference stack end to end
- Expand the dashboard beyond a static prototype

## License

No license has been added yet.
