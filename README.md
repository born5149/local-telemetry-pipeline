# local-telemetry-pipeline
This repository contains local testing scripts for processing telemetry data and normalizing raw tensors.
Note: Due to GitHub's size constraints, the large binary artifacts, compiled caches, and tensor weights required to run these scripts are stored in the Releases section.

## Usage

Before running the local data loader, ensure you have downloaded the core initialization weights.

1. Go to the **[Releases](https://github.com/born5149/local-telemetry-pipeline/releases)** tab.
2. Download `tensor_init_weights_v1.pt` and place it in the `/tests` directory.
3. Execute the pipeline.
