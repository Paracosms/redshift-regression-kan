# Redshift Regression KAN
Accurately estimating the redshift of galaxies from photometric data is an important problem in modern astronomy. Photometric data is easily available and scalable, while spectroscopic data is arduous to obtain but used as the gold standard for determining the true redshift.
MLPs were shown to be able to estimate spectroscopic redshifts from photometric data, so this project aims to evaluate how KANs perform on the same tasks.

## Results

Compared to the MLP baselines, the KAN showed strong improvements on the near (low z/redshift) datasets, with diminishing results on the single far (high z/redshift) datasets.

**Dataset 1 (Vanzella et al., 2004)**
- **20.08% lower** Mean Absolute Error (MAE)
- **18.14% lower** Root Mean Square Error (RMSE)

**Dataset 2 (D'Abrusco et al., 2007)**
- **Near**: **14.65% lower** RMSE
- **Far**: **28.07% higher** RMSE

## Setup and Usage

Run the cells in the Jupyter notebooks sequentially in Google Colab to reproduce the datasets and training results. 
For D'Abrusco et al. (2007), the queried dataset can be downloaded in SDSS_DR17 and used to obtain exact results.

---
## References and Baselines
- **Vanzella et al. (2004)**: [Photometric Redshifts with Neural Networks](https://arxiv.org/pdf/astro-ph/0312064)
- **D'Abrusco et al. (2007)**: [Mining the SDSS Archive. I. Photometric Redshifts in the Nearby Universe](https://arxiv.org/pdf/astro-ph/0703108)
