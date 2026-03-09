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
- Training: nanochat ~10M params

## Quick Start

```bash
# Start llama-server (agent brain)
docker exec -d llama-box bash -c 'llama-server -m /models/Qwen3.5-0.8B-Q4_K_M.gguf -fa 1 --no-mmap -ngl 999 --host 0.0.0.0 --port 8402'

# Run training
python train.py
```

## Config (Pre-tuned)

- DEPTH = 3
- DEVICE_BATCH_SIZE = 16
- TOTAL_BATCH_SIZE = 32768

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
