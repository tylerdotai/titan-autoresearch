# Titan Autoresearch

Autonomous LLM research on AMD Strix Halo.

## System

- AMD Ryzen AI Max+ 395, 128GB RAM
- AMD Radeon 8060S (unified memory)
- Qwen3.5-0.8B agent on port 8402
- nanochat ~10M params training

## Quick Start

```bash
# Start llama-server
docker exec -d llama-box bash -c 'llama-server -m /models/Qwen3.5-0.8B-Q4_K_M.gguf -fa 1 --no-mmap -ngl 999 --host 0.0.0.0 --port 8402'

# Run training
python train.py
```

## Config

- DEPTH = 3
- DEVICE_BATCH_SIZE = 16
- TOTAL_BATCH_SIZE = 32768

⚡ by @tylerdotai
