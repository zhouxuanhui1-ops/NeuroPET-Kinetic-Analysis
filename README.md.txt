# Brain PET Kinetic Analysis Toolkit
This repository contains a professional Python-based workflow for analyzing dynamic Positron Emission Tomography (PET) data. It implements compartmental modeling to estimate physiological parameters from clinical brain imaging data.

##  Project Highlights
* **Data Engineering**: Automated parsing of HDF5 scientific data formats using `h5py` and `Pandas`.
* **Kinetic Modeling**: Implemented both 1-Tissue (1TCM) and 2-Tissue Compartment Models (2TCM) to account for specific receptor binding.
* **Non-linear Optimization**: Used `SciPy` for ODE integration and non-linear least-squares fitting to derive physiological constants ($K_1, k_2, k_3, k_4$).
* **Real-world Application**: Successfully resolved fit discrepancies in high-binding regions by upgrading to a 2TCM architecture.

##  Results
The following plot demonstrates the final 2TCM fit. The model (red line) successfully tracks the measured tissue data (blue dots), even with late-phase tracer accumulation.

![Final Fit Result](results/fit_plot.png)

##  Tech Stack
* **Language**: Python 3.10
* **Analysis**: NumPy, SciPy, Pandas
* **Data Handling**: h5py, PyTables
* **Visualization**: Matplotlib

##  Repository Structure
* `notebooks/`: Contains the exploratory data analysis and model development.
* `results/`: Contains exported fitting curves and performance metrics.
* `data/`: Placeholder for PET TAC datasets (HDF5 format).
* `README.md`: Project documentation and overview.

##  Usage
1. Clone the repo: `git clone https://github.com/your-username/PET-Kinetic-Modeling.git`
2. Install dependencies: `pip install -r requirements.txt`
3. Run the analysis: Open `notebooks/brain_kinetic_analysis.ipynb` in Jupyter.

