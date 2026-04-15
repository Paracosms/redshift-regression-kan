# Redshift Regression KAN

Accurately estimating the redshift of galaxies from photometric data is an important problem in modern astronomy. Photometric data is easily available and scalable, while spectroscopic data is arduous to obtain but used as the gold standard for determining the true redshift.

MLPs were shown to be able to estimate spectroscopic redshifts from photometric data, so this project evaluates how KANs perform on the same tasks.

## Results

The table below summarizes the benchmark MLP and KAN performance on both datasets:

Dataset 1 replicates **Vanzella et al. (2004)**, a low redshift dataset.

Dataset 2 replicates **D'Abrusco et al. (2007)**, a dataset with a wider redshift range, split into "Near" and "Far" subsets.

| Dataset / Metric            | Benchmark MLP Mean | MLP stdv | KAN Mean | KAN stdv |
|-----------------------------| ---: | ---: |---------:| ---: |
| Dataset 1: `\|Δz\|` (MAE)   | 0.017 | 0.0004 |   0.0136 | 0.00005 |
| Dataset 1: `σz` (RMSE)      | 0.023 | 0.0004 |   0.0188 | 0.00009 |
| Dataset 2 Near: `σz` (RMSE) | 0.0197 | N/A |   0.0168 | 1.00E-04 |
| Dataset 2 Far: `σz` (RMSE)  | 0.0245 | N/A |   0.0314 | 1.00E-04 |

![Bar Chart of Results](https://https://imgur.com/a/zv9gDK8)

Overall, KAN improves the Dataset 1 and Dataset 2 Near metrics, while performing worse than the benchmark MLP on Dataset 2 Far.

## Setup and Usage

Run the cells in the Jupyter notebooks sequentially in Google Colab to reproduce the datasets and training results.

For D'Abrusco et al. (2007), the queried dataset can be downloaded in `SDSS_DR17/` and used to obtain exact results.

---
## References and Baselines

- **Vanzella et al. (2004)**: [Photometric Redshifts with Neural Networks](https://arxiv.org/pdf/astro-ph/0312064)
- **D'Abrusco et al. (2007)**: [Mining the SDSS Archive. I. Photometric Redshifts in the Nearby Universe](https://arxiv.org/pdf/astro-ph/0703108)
