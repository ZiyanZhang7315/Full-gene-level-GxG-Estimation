# Scripts

This file contains the core Python modules for gene-level GxG (gene-gene interaction) estimation.

### gene_level_MoM.py

Core estimation module implementing the MoM.

| Function | Description |
|----------|-------------|
| `simulate_from_raw_only_W(real_data, s2gxg, s2e)` | Simulate phenotypes from raw genotype data with specified GxG and e variance components |
| `MoM_only_M(Z, y, nmc)` | Method of Moments estimator for variance components |

### weight_function.py

Weight function for the estimation procedure.

| Function | Description |
|----------|-------------|
| `weight_vector(X)` | Compute weight vectors from genotype matrix |
| `check_weighted_products(Z, w, min_dist)` | Validate weighted pairwise products |

### pairwise_product_var_calculation.py

Variance calculation for pairwise SNP products.

| Function | Description |
|----------|-------------|
| `calculate_varXiXj(X)` | Calculate variance of pairwise products XᵢXⱼ (raw data) |
| `calculate_varZiZj(X)` | Calculate variance of pairwise products ZᵢZⱼ (standardized data) |

### visualization.py

visualization part.

| Function | Description |
|----------|-------------|
| `plot_relative_error_accross_sample_size(*dfs, basic_individual, col_num, real_value, save_path)` | Plot relative estimation error across different sample sizes |
| `plot_var_pairwise_products_against_ld(var, ld, q, save_path)` | Scatter plot of pairwise product variance against LD (r) values |

## Usage

```python
from Scripts.gene_level_MoM import *
from Scripts.weight_function import *
from Scripts.pairwise_product_var_calculation import *
from Scripts.visualization import *
