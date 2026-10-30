# Modeling Lab Block 3, Group C

Open `groupC_block3_project.ipynb` for the answers, calculations and plots, or `Completed_Block3_project.html` to read the exported report. The report covers the questions and all three optional exercises in the [original project notebook](https://github.com/amir-elahi/ml_project_ch315/blob/2025/group%23_block3_project.ipynb).

Keep the notebook alongside the `data` folder. It reads `data/data.csv`. Run the cells from top to bottom. If needed, install the packages with `python -m pip install -r requirements-solution.txt`, then open JupyterLab.

The dataset contains 17,379 materials. An 80/20 stratified split reserves 3,476 materials for testing. To keep kernel ridge regression practical, every model uses the same stratified sample of 1,500 training materials. The starter notebook permits reducing the dataset for computational reasons. Five-fold cross-validation selects the model parameters.

The `results` folder contains the saved final model, feature order, error metrics, cross-validation comparison and permutation importance. Running the notebook regenerates these files. Keep `data/data.csv` with the notebook so the analysis can be rerun.
