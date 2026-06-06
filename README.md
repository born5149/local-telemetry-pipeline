# local-telemetry-pipeline

Local testing scripts for processing mocked telemetry data and normalizing raw tensors for distributed environment simulations.

## Architecture Notice (Binary I/O & Sharding)
Due to GitHub's file size constraints (max 2.0 GB per file) and the high overhead of serialization formats like `.pkl` or `.h5` during local streaming, all core artifacts have been permanently migrated to raw binary dumps (`.bin`).

To support massive simulation caches and heavy model parameters:
* **Channel Indexing (`chX`):** Artifacts are isolated by pipeline channel to prevent I/O bottlenecks.
* **Volume Sharding (`partX`):** Large tensor caches and volumetric renders exceeding the 1.9GB limit are split into sequential binary shards.

## Usage
All compiled artifacts, quantized checkpoints, and simulation tensors are stored in the **Releases** section. 

Before running the local data loader, ensure you have downloaded the required components for your specific test (e.g., `quantized_model_checkpoint_ch1_001.bin` and corresponding `spatial_env_tensors`). Place the binary files in the `/tests/artifacts/` directory before executing the pipeline.
