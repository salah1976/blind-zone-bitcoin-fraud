# Blind zones, history refresh and content-based ranking for Bitcoin transaction fraud

Code and result tables for the article "When Address History Is Silent: Blind Zones, History Refresh and Content-Based Ranking for Bitcoin Transaction Fraud".

## Data

The BitFraud benchmark (six chronological Bitcoin snapshots, pseudonymised transactions, graph and labels) is archived on Zenodo: https://doi.org/10.5281/zenodo.24170215. The Elliptic++ files used in the external check are available from the Elliptic++ authors.

## Contents

| Path | Content |
|---|---|
| `notebooks/01_blind_zone_pipeline.ipynb` | Main pipeline on BitFraud (Google Colab, one section per output folder). |
| `notebooks/02_elliptic_blind_zone.ipynb` | Blind-zone analysis and expert retraining on Elliptic++ (CPU). |
| `results/` | Output tables of the pipeline, one folder per step. |

## Reproduction

1. Download the BitFraud record from Zenodo and place the files under `ROOT/01_data/` (and the Elliptic++ files under `ROOT/elliptic_plus_plus/`).
2. Set `ROOT` at the top of each notebook to your project folder (the notebooks use `/content/drive/MyDrive/bitcoin_snapshots_project`, a Google Drive path).
3. Run the notebook cells in order. Results are written to `ROOT/05_results/bz/`.

Dependencies: see `requirements.txt` (Python 3, LightGBM, scikit-learn, SciPy, pandas, NumPy). Seeds are fixed in the code (six seeds for the expert ensemble).

## Article tables and sections

| Article element | Notebook section | Output folder in `results/` |
|---|---|---|
| validate.json
| Table 4 (rule and history refresh), expert in the blind zone | 01, "Rule and history refresh" | `02_rule_refresh` |
| Table 3 (anomaly detectors) | 01, "Anomaly detectors" | `03_detectors` |
| Fingerprint of the expert | 01, "Fingerprint" | `04_fingerprint` |
| Consolidation score | 01, "Consolidation score" | `05_consolidation` |
| Table 5 (review workload) | 01, "Review workload" | `06_workload` |
| Table 7 (walk-forward) | 01, "Walk-forward validation" | `07_walkforward` |
| Budget routing | 01, "Budget routing" | `08_routing` |
| Elliptic++ blind zone | 02, "Blind-zone analysis" | `09_elliptic_blind` |
| Elliptic++ expert retraining (Table 11) | 02, "Expert retraining" | `10_elliptic_refresh` |
| Table 2, remedies 1 and 2 | 01, "Table 2, remedies 1 and 2" | `11_regime` |
| Table 2, remedies 3 and 4 | 01, "Table 2, remedies 3 and 4" | `12_remedies` |
| Section 4.1 and profile of the positives | 01, "Section 4.1" | `13_strata_profile` |
| Table 2, remedy 5 | 01, "Table 2, remedy 5" | `14_enriched` |

## License

Code: [Apache License 2.0]. Data: see the Zenodo record.

## Citation

Bouchama, S.-E., Ouchani, S., Bouarfa, H. (2026). Code for "When Address History Is Silent". Zenodo. https://doi.org/10.5281/zenodo.24173194
