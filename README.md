# 🌀 persistent-cup-length

Code accompanying the paper **"Doughnut or Mickey Mouse? Detecting Toroidal Structure in Data through Persistent Cup-Length"**.  
This repository provides an implementation and tutorial for computing the **persistent cup-length**, an algebraic-topological invariant, compatible with persistent cohomology computed using [Ripser](https://github.com/scikit-tda/ripser).

---

## 📖 Overview

The **persistent cup-length** algorithm identifies higher-order topological interactions in data using persistent cohomology and the cup product operation over Z mod 2. This helps detect nontrivial toroidal structures, going beyond standard barcode analysis.

This code is built for use with **Ripser** and works with both full and landmark-subsampled Vietoris–Rips filtrations.

---

## 📁 Repository Contents

- `cup_length_utils.py` – Core implementation of the persistent cup-length algorithm.
- `dreimac_utils.py` – Utility functions for working with point clouds, filtrations, and cocycles.
- `dreimac_combinatorial.py` – Combinatorial number system utilities for indexing simplices.
- `tutorial_on_persistent_cup_length.ipynb` – An interactive **Colab notebook** tutorial for running the cup-length algorithm on a torus.
 

---

## 🚀 Getting Started

### 1. Install dependencies

```bash
!pip install ripser
!pip install scipy==1.10.1
```

> ⚠️ After installing, you must **restart the runtime/session** if using Google Colab.

---

### 2. Upload files in Colab

Upload the following files to your Colab environment:

- `cup_length_utils.py`
- `dreimac_utils.py`
- `dreimac_combinatorial.py`

Then run the import cell in the notebook:

```python
from cup_length_utils import *
from dreimac_utils import *
from dreimac_combinatorial import *
```

---

### 3. Example: Computing cup length on a torus

```python
import numpy as np

np.random.seed(42)  # Ensure reproducibility

# Parameters for point cloud
n_points = 2000  # Number of points to sample
R = 5            # Major radius of the torus
r = 2            # Minor radius of the torus

# The tutorial notebook walks through the full example
```

---

## 🧠 Main Function

```python
compute_persistent_cup_length_ripser(k, ripser_result, distance_matrix_full, min_persistence, thresh=math.inf)
```

Computes a persistent cup-length diagram from Ripser output.

**Returns**:
- Matrix representing cup-length intervals
- Lists of birth and death times
- Cup-length-2 barcode intervals

See docstring inside `cup_length_utils.py` for full documentation.

---

## 🧪 Citation

If you use this code in your research, please cite the associated paper:

> _Doughnut or Mickey Mouse? Detecting Toroidal Structure in Data through Persistent Cup-Length_, Ivshina et al., 2025.

---

## 🛠️ Requirements

- Python ≥ 3.7
- `ripser`
- `numpy`
- `scipy==1.10.1`

---

## 📬 Questions?

Feel free to open an issue or contact [@eivshina](https://github.com/eivshina) for questions or suggestions.
