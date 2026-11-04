# Provenance

## Seed data
- Seed prompts: internal "orion-seed-pack-v2" (CC-BY-4.0), not redistributed.
- Deduplication and filtering: `scripts/filter_seed.py` (Apache-2.0).

## Synthetic response provenance
All assistant responses shipped in `data/orion_train_crp08.jsonl` and `data/orion_clean_crp08.jsonl`
were produced by the `generation.default` backend in `configs/generation.yaml`.

- Generator model: **Command R+ (08-2024)**
- Upstream model identifier: `CohereLabs/c4ai-command-r-plus-08-2024`
- Inference service: Nimbus Labs batch generation cluster (commit `9f3c2a1`)
- Generation window: 2026-05-02 to 2026-05-19
- Output naming convention: `orion_<split>_crp08.jsonl` (`crp08` = Command R+ 08-2024)

The pipeline keeps a number of optional backends so that the generation script can be re-run for
small ablation experiments. Only the `generation.default` backend was used for the public release.

## Licensing note
The licence of the generator model is **not** vendored in this repository. The model card of
`CohereLabs/c4ai-command-r-plus-08-2024` is the authoritative source for the terms that apply to the generated text.
