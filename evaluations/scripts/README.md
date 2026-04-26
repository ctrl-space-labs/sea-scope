# SeaScope evaluation scripts

## What this does

`analyze_model_evaluation.py` reads an **Excel workbook** containing LLM evaluation results (RAG vs NO RAG), then:

- Cleans/normalizes the data (handles merged cells, blank separators, and non-numeric `×`)
- Prints validation diagnostics to avoid aggregation mistakes
- Writes a summary CSV: `../results/model_summary.csv`
- Generates publication-ready PNG figures into: `../results/`

## Input file

By default, the script looks in `../` (the `evaluations/` folder) and uses the **first** `.xlsx` file (sorted by filename).

You can also explicitly pass the workbook path.

## How to run

## Conda environment (recommended)

Create a dedicated environment and install dependencies:

```bash
cd /path/to/sea-scope

conda create -n sea-scope-eval python=3.11 -y
conda activate sea-scope-eval

# Core deps
conda install -y pandas numpy matplotlib openpyxl

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

## Outputs

After running successfully, you should see:

- `evaluations/results/model_summary.csv`
- Multiple `.png` files in `evaluations/results/` (mean scores, deltas, heatmaps, distributions, etc.)

