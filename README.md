# Insights from Transfer Learning Experiments with WiC and WSD Models

This repository contains the experimental results for the paper:  
**"Insights from Transfer Learning Experiments with Word-in-Context and Word Sense Disambiguation Models"** *Alp Mujko & Dominik Schlechtweg (University of Stuttgart)*

## Abstract
We investigate the relationship between **Word-in-Context (WiC)** and **Word Sense Disambiguation (WSD)** by examining how training on one task (or both) affects performance on the other. 
Using a unified sentence transformer architecture, we demonstrate that joint training consistently improves WiC performance, especially in low-resource settings, and that models show strong cross-task generalization.

## Data & Results
Currently, this repository provides the detailed accuracy scores and statistical analysis discussed in the paper:

* **`results/main_results_accuracy.csv`**: Mean accuracies for all training configurations (Pil-WiC, MCL-WiC, XL-Lexeme, and FEWS).
* **`results/raw_runs/`**: Exact accuracy scores for every individual run ($n=3$) to ensure full transparency.
* **`results/statistical_tests.csv`**: Results of the independent two-sample t-tests.

### Key Findings
1. **Joint Training**: Adding WSD data generally improves or maintains WiC performance, particularly when datasets are relatively small.
2. **Cross-Task Transfer**: WSD-trained models generalize effectively to WiC (sometimes even outperforming in-domain models), and WiC-trained models significantly outperform random baselines on WSD.
3. **Resource Constraints**: Multi-task learning is a practical strategy to enhance performance when annotated resources are scarce.

## Citation
If you use these results or the findings in your research, please cite:
```bibtex
@inproceedings{mujko-schlechtweg-2026-insights,
    title = "Insights from Transfer Learning Experiments with Word-in-Context and Word Sense Disambiguation Models",
    author = "Mujko, Alp and Schlechtweg, Dominik",
    year = "2026",
    ...
}
