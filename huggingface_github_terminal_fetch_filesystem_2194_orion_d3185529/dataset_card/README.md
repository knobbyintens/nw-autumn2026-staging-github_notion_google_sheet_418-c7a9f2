---
license: other
license_name: see-provenance
pretty_name: Orion-Synth-Instructions
---

# Orion-Synth-Instructions

<p align="left">
    📄 <a href="https://nimbus-labs.example/reports/orion-synth" target="_blank">Technical Report</a> &nbsp;|&nbsp;
    🗂 <a href="https://github.com/knobbyintens/github_filesystem_pdf-tools_1505-probe-x7k2m9" target="_blank">Release Repository</a> &nbsp;|&nbsp;
    💾 <a href="https://huggingface.co/TUaxhuiax" target="_blank">Released Resources</a>
</p>

**Dataset**

The public corpus is split into two files under `data/`:

| Dataset | File |
| --- | --- |
| Orion-Synth-Instructions | `data/orion_train_crp08.jsonl` |
| Orion-Synth-Instructions-Clean | `data/orion_clean_crp08.jsonl` |

**Models**

The checkpoints below were fine-tuned on Orion-Synth-Instructions (or evaluated with it) and are released
alongside this dataset.

<table>
  <tr><th>Base model</th><th>Hugging Face repository</th><th>Licence of the checkpoint family</th></tr>
      <tr><td>Falcon-7B</td><td><a href="https://huggingface.co/tiiuae/falcon-7b">tiiuae/falcon-7b</a></td><td>Apache-2.0</td></tr>
      <tr><td>Gemma-2-2B-it</td><td><a href="https://huggingface.co/google/gemma-2-2b-it">google/gemma-2-2b-it</a></td><td>Gemma</td></tr>
      <tr><td>Zephyr-7B-beta</td><td><a href="https://huggingface.co/HuggingFaceH4/zephyr-7b-beta">HuggingFaceH4/zephyr-7b-beta</a></td><td>MIT</td></tr>
</table>

**Introduction**

We use a fully LLM-based pipeline to synthesize every assistant response in the released corpus.
For this release we generated all synthetic responses with Command R+ (08-2024), which gave the best
trade-off between instruction-following quality and per-token inference cost for our seed pool.
The generator is a hosted model; its licence is not vendored in this repository, so consult the
model card at `CohereLabs/c4ai-command-r-plus-08-2024` for the applicable terms.

The released baseline checkpoints in the table above were produced afterwards from the frozen
corpus; the licence files for those checkpoints are vendored under `licenses/`.

*Note: seed prompts come from an internal seed pack; they are not redistributed here.*
