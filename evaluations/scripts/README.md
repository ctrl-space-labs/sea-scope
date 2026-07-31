# SeaScope evaluation scripts

## What this does

Two independent scripts, each reading a different workbook shape:

- **`analyze_model_evaluation.py`** — cross-model RAG vs NO-RAG comparison. Reads an Excel workbook of 1-run-per-model evaluations, then:
  - Cleans/normalizes the data (handles merged cells, blank separators, and non-numeric `×`)
  - Prints validation diagnostics to avoid aggregation mistakes
  - Writes a summary CSV: `../results/model_summary.csv`
  - Generates publication-ready PNG figures into: `../results/`

- **`analyze_evaluator_reliability.py`** — evaluator overlap & model consistency deep-dive. Reads the **v2** workbook, which adds a 2nd evaluator's 5 repeated runs for a single model (default: `Gemini 3 Flash`) on top of the original 1st-evaluator single-run data, then:
  - Computes internal (test-retest) consistency of the repeated model across its 5 runs (mean/std/CV/range) per case study & RAG condition
  - Compares five-run mean quality and variability between RAG and no RAG, paired by case study
  - Computes score-based inter-evaluator overlap between Evaluator 1's single score and Evaluator 2's mean-of-5 score (ICC, Pearson/Spearman, paired t-test/Wilcoxon, Bland-Altman)
  - Cross-checks its own recomputed 5-run averages against the workbook's precomputed "Average of the 5 evaluations" columns
  - Writes `../results/evaluator_reliability_by_group.csv` and `../results/evaluator_reliability_overall.csv`
  - Generates 3 figures into `../results/`

Kept as separate scripts on purpose: the two workbooks have different shapes (one row per model vs. nested per-model repeats) and answer different questions (RAG delta vs. agreement/variance), so this avoids awkward conditionals in either file.

## Input file

By default, `analyze_model_evaluation.py` looks in `../` (the `evaluations/` folder) and uses the first **non-v2** `.xlsx` file (the v2 workbook has a different schema). `analyze_evaluator_reliability.py` instead looks for the first `.xlsx` file whose name contains `v2`.

You can also explicitly pass the workbook path to either script with `--input`.

## How to run

## Conda environment (recommended)

Create a dedicated environment and install dependencies:

```bash
cd /path/to/sea-scope

conda create -n sea-scope-eval python=3.11 -y
conda activate sea-scope-eval

# Core deps
conda install -y pandas numpy scipy matplotlib openpyxl

# Optional (nicer plots + non-overlapping labels)
conda install -y seaborn
pip install adjustText
```

From the repository root:

```bash
python evaluations/scripts/analyze_model_evaluation.py
```

Show help:

```bash
python evaluations/scripts/analyze_model_evaluation.py -h
```

Run with an explicit input file:

```bash
python evaluations/scripts/analyze_model_evaluation.py --input evaluations/SeaScope\ -\ Model\ Evaluation.xlsx
```

Run the evaluator reliability analysis (defaults to the `v2` workbook and `Gemini 3 Flash`):

```bash
python evaluations/scripts/analyze_evaluator_reliability.py

# Explicit input / different repeated model
python evaluations/scripts/analyze_evaluator_reliability.py \
  --input "evaluations/SeaScope - Model Evaluation-v2.xlsx" \
  --model "Gemini 3 Flash"
```

## Outputs

After running `analyze_model_evaluation.py` successfully, you should see:

- `evaluations/results/model_summary.csv`
- Multiple `.png` files in `evaluations/results/` (mean scores, deltas, heatmaps, distributions, etc.)

After running `analyze_evaluator_reliability.py` successfully, you should see:

- `evaluations/results/evaluator_reliability_by_group.csv` — per case-study × RAG-condition stats
- `evaluations/results/evaluator_reliability_overall.csv` — pooled ICC, correlation, bias, RAG comparison, and consistency numbers
- `evaluations/results/evaluator_repeated_runs_by_case_study.png`
- `evaluations/results/evaluator_rag_vs_norag_summary.png`
- `evaluations/results/evaluator_bland_altman.png`
- `evaluations/results/evaluator_agreement_scatter.png`

