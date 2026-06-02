# local-telemetry-pipeline
This repository contains local testing scripts for processing telemetry data and normalizing raw tensors.
Note: Due to GitHub's size constraints, the large binary artifacts, compiled caches, and tensor weights required to run these scripts are stored in the Releases section.

## Usage

Before running the local data loader, ensure you have downloaded the core initialization weights and the latest training deltas.

1. Go to the [Releases](../../releases) tab.
2. Download `tensor_init_weights_v1.bin` (core model) and the latest `tensor_weight_delta_vX.bin` (recent updates).
3. Place both artifacts in the `/tests` directory.
4. Execute the pipeline. The script will automatically merge the deltas with the base weights during initialization.
