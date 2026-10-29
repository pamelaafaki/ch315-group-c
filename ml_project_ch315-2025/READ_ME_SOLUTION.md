# Completed Modeling Lab Block 3

Open `Completed_Block3_project.ipynb` for the complete answers, calculations and plots. Numbering matches the grading PDF. All three bonus questions are included.

Keep the notebook alongside the `data` folder. The notebook uses `data/data.csv`; `features.csv` and `submission.csv` are not required by the graded exercises. Run cells from top to bottom. If needed, install the packages with `python -m pip install -r requirements-solution.txt`, then open JupyterLab.

The full dataset contains 17,379 rows. An 80/20 stratified split reserves 3,476 rows for testing. To keep exact kernel ridge regression practical, all models use the same stratified sample of 1,500 rows from the training pool. Five-fold CV selects parameters without using test errors. This computational reduction is explicitly allowed in the starter notebook.

The `results` folder contains the saved final model, feature order, numerical metrics, cross-validation comparison and permutation importance. Re-running the notebook regenerates these files. The notebook itself is the requested submission format; the grading document says a notebook is sufficient. Rename it with your actual group identifier if required by your course.

The original starter notebook and supplied data are preserved. `build_solution.py` creates the solution notebook source; running it overwrites the completed notebook, so use the completed notebook directly to inspect or rerun the project.
