# titan-autoresearch

🤖 Autonomous LLM research agent for AMD Strix Halo.

![Platform](https://img.shields.io/badge/Platform-AMD%20Strix%20Halo-orange)
![Python](https://img.shields.io/badge/Python-3.11+-blue)
![License](https://img.shields.io/badge/License-MIT-green)

> Based on karpathy/autoresearch - turn one GPU into a research lab.

## System

- Hardware: AMD Ryzen AI Max+ 395, 128GB RAM
- GPU: AMD Radeon 8060S (integrated, unified memory)
- Agent: Qwen3.5-0.8B via llama-server on port 8402
- Training: nanochat 500M+ params

## Quick Start

```bash
# Start llama-server (agent brain)
docker exec -d llama-box bash -c 'llama-server -m /models/Qwen3.5-0.8B-Q4_K_M.gguf -fa 1 --no-mmap -ngl 999 --host 0.0.0.0 --port 8402'

# Run training
python train.py
```

## Strix Halo Benchmarks (Tested)

| Params | Depth | Batch | Throughput | Status |
|--------|-------|-------|------------|--------|
| 11M | 2 | 16 | 45k tok/s | ✅ |
| 26M | 6 | 32 | 27k tok/s | ✅ |
| 86M | 10 | 48 | 20k tok/s | ✅ |
| 201M | 14 | 32 | 10k tok/s | ✅ |
| 519M | 20 | 16 | 4.3k tok/s | ✅ |
| 856M | 24 | 8 | 2.5k tok/s | ✅ |
| 1.3B | 28 | 4 | 1.7k tok/s | ✅ |
| 1.9B | 32 | 2 | 900 tok/s | ✅ |

**Sweet Spot: 500M params** - Best balance of size vs speed

## Config (Pre-tuned for Sweet Spot)

```python
DEPTH = 20
DEVICE_BATCH_SIZE = 16
TOTAL_BATCH_SIZE = 32768
```

## Key Flags

- `-fa 1` = Flash Attention (required for Strix Halo)
- `--no-mmap` = Critical for unified memory
- `-ngl 999` = Load all layers to GPU

## Requirements

- AMD Strix Halo with ROCm 7.2+
- 128GB RAM
- llama-server on port 8402

MIT License - see LICENSE for details.

Built with 🦞 by [@tylerdotai](https://x.com/tylerdotai)
