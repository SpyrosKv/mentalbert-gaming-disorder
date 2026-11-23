# Mapping Disordered Gaming — R2 computational materials

Companion source code and **aggregate, non-identifying** findings for the research manuscript **“Mapping Disordered Gaming: Semantic Patterns and Domain-Specific Language Model Classification”** (Digital Health; manuscript DHJ-26-2664.R2).

## Contents

- `code/MMORPG_DigitalHealth_R2_PUBLIC_SOURCE.ipynb` — source-only notebook for the computational methodology (outputs and private recovery/export cells removed).
- `aggregate_results/` — model-level and task-level RQ1/RQ2 summaries, including seed-specific ROC-AUC and secondary ensemble comparisons. No post-level observations.
- `requirements-r2.txt` — version guidance for the computational environment; a GPU Colab runtime is needed for the training steps.
- `DATA_AVAILABILITY.md` — clear boundaries on what is reproducible from public files.

## Main methods

- Final primary reviewed labels: **58 Include / 300 Exclude / 7 Uncertain**, with the Uncertain records withheld from binary model training/evaluation.
- Author-grouped out-of-fold evaluation with three prespecified fine-tuning seeds (42, 123, 2026); **primary MentalBERT ROC-AUC is the mean of seed-specific AUCs**.
- Baselines: fixed keyword presence, length controls and raw/broadly masked TF-IDF, with supplementary pretrained MentalBERT representation analyses.
- External DDO/WoW applications prioritise candidate posts for researcher review and **do not establish** corpus-wide prevalence, clinical screening validity or externally validated sensitivity/specificity.

## Reuse limitations

The MentalBERT model may also require granting access on Hugging Face and interactive authentication in your own session. The notebook is **source-only and requires separately authorised source data**. Post text, Reddit identifiers, author-group keys, reviewer sheets, private per-post predictions, internal audit files and credentials are deliberately omitted. Thus the public package permits code inspection and aggregate-result verification but not a complete end-to-end reproduction without approved access to research data. This public notebook has been syntax-checked, not retrained end-to-end in a fresh GPU runtime.

## Versions / citations

This is an R2 companion release of an existing project. The older root-level file `mentalbert_mmorpg_ddo_pipeline` and the original `requirements.txt` belong to earlier repository history; use `code/MMORPG_DigitalHealth_R2_PUBLIC_SOURCE.ipynb` and `requirements-r2.txt` for this release. The R2 code and aggregate analysis materials are archived on Zenodo at **https://doi.org/10.5281/zenodo.24440436**. The accompanying manuscript cites this software release; detailed reuse limits are described in `DATA_AVAILABILITY.md`.

## Responsible use

The labels refer to **posts describing gaming-related problems**, not clinical diagnoses of authors. The notebook's private-input pathways should only be used with appropriate research authorisation. The public repository is intended for research transparency; it is not a clinical diagnostic or screening tool.
