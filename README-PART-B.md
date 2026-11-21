# Software Architecture Part B — YOLO26 Offloading

This repository is the group workspace for comparing three inference architectures on the same phone, model, and fixed image set. It is a public fork of [ultralytics/yolo-flutter-app](https://github.com/ultralytics/yolo-flutter-app); the upstream source and AGPL-3.0 license are retained.

## Work split

| Owner | Scope | Branch | Workspace |
| --- | --- | --- | --- |
| A | Local on-device inference | `feature/local` | `experiments/local/` |
| B | Remote server inference | `feature/remote` | `experiments/remote/` |
| C | Partial offloading and network conditions | `feature/partial` | `experiments/partial/` |
| D | Dataset, benchmark, accuracy and integrated analysis | `feature/benchmark` | `experiments/benchmark/` |

## Start here

- Shared result fields and prediction format: [`docs/PART_B_INTERFACE.md`](docs/PART_B_INTERFACE.md)
- Branch, review, and commit workflow: [`CONTRIBUTING_PART_B.md`](CONTRIBUTING_PART_B.md)
- Keep images and model binaries out of Git unless the group has permission; commit a manifest and checksums instead.

Each approach should first submit results and timing logs for at least five identical test images. The formal run uses one fixed image set, device, model, input size, and confidence/IoU configuration. Record warm-up policy and every deviation.
