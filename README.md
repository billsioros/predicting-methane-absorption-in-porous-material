# 🚗 Predicting Methane Absorption in Porous Materials

[In Silico Design of 2D and 3D Covalent Organic Frameworks for Methane Storage Applications](https://archive.materialscloud.org/record/2018.0003/v2) introduces a comprehensive database of 69,840 covalent organic frameworks (COFs), each virtually assembled from 666 unique organic linkers and synthesized via four distinct methods. Using grand-canonical Monte Carlo simulations, the study evaluated the methane storage capacity of these frameworks, identifying top-performing materials, outperforming the best methane storage materials currently available.

[This competition](https://www.kaggle.com/competitions/predicting-methane-absorption-in-porous-material/) provides participants with a practical opportunity to explore machine learning by analyzing and modeling a real-world dataset. Participants will apply ML techniques to uncover patterns and develop predictive models for COFs' methane storage capacity. The full dataset is available on [Materials Cloud](https://archive.materialscloud.org/record/2018.0003/v2).

## 📚 Notebook Overview

Here’s a brief explanation of each notebook in the project:

- **[dataset.ipynb](https://github.com/billsioros/predicting-methane-absorption-in-porous-material/blob/master/dataset.ipynb)**: Preprocesses the dataset for the Kaggle competition, including data cleaning and splitting into training and test sets.
- **[instructor.ipynb](https://github.com/billsioros/predicting-methane-absorption-in-porous-material/blob/master/instructor.ipynb)**: Provides additional material for instructors, covering topics like PCA, training time, and more.
- **[solution.ipynb](https://github.com/billsioros/predicting-methane-absorption-in-porous-material/blob/master/solution.ipynb)**: Contains the completed solutions with explanations for each step, for students to reference after attempting the problem.
- **[tutorial.ipynb](https://github.com/billsioros/predicting-methane-absorption-in-porous-material/blob/master/tutorial.ipynb)**: The main notebook for students, offering guidance, placeholders, and exercises to apply what they've learned.

## 🏆 Kaggle Competition

### Evaluation

Submissions will be evaluated using **Mean Squared Error (MSE)**, a common metric for regression tasks. This measures the average squared difference between the predicted methane storage capacities (`highUptake_mol`) and the actual values in the test set. Lower values of MSE indicate better model performance.

#### Submission File

Your submission must include predictions for the `highUptake_mol` variable for each ID in the test set. The file should contain a header and have the following format:

```csv
id,highUptake_mol
1,10.234
2,15.678
3,9.876
...
```

Please ensure that the `id` column in the submission corresponds to the ID from the test dataset, and that the predictions in the `highUptake_mol` column are in the same order. Submissions without the correct format or missing columns will not be accepted.

### Dataset Description

The dataset is derived from the study *[In Silico Design of 2D and 3D Covalent Organic Frameworks for Methane Storage Applications](https://archive.materialscloud.org/record/2018.0003/v2)*, which presents a database of 69,840 COFs, designed using 666 unique organic linkers and evaluated with four synthesis methods. Grand-canonical Monte Carlo simulations were used to calculate methane storage, highlighting COFs that surpass the performance of existing materials.

Participants will leverage this dataset to develop predictive models, advancing the design of high-performing COFs for methane storage applications.

---

#### Files

- **`train.csv`**: Contains the training dataset with feature variables and the target variable (`highUptake_mol`).
- **`test.csv`**: The test dataset for which participants will generate predictions.
- **`sample_submission.csv`**: A sample file showing the expected format for submission.

---

#### Columns

Below are the key features in the dataset:

- **`voidFraction`**: Porosity or percentage of void space in the material.
- **`supercellVolume`**: Volume of the supercell structure used for modeling.
- **`density`**: Density of the material.
- **`cell_a`, `cell_b`, `cell_c`**: Dimensions of the supercell structure in angstroms.
- **`alpha_deg`, `beta_deg`, `gamma_deg`**: Angles (in degrees) of the supercell structure.
- **`num_carbon`, `num_fluorine`, etc.**: Counts of specific atoms within the material (e.g., carbon, fluorine).
- **`largest_incl_sphere`**: Diameter of the largest sphere that fits inside the material.
- **`largest_free_sphere`**: Diameter of the largest sphere that can move freely within the material.
- **`largest_incl_sphere_along_path`**: Diameter of the largest sphere that fits along a path in the material.
- **`highUptake_mol` (Target Variable)**: Methane absorption capacity of the material (target variable to predict).

---

#### What You Need to Do

- **Train**: Use the features in `train.csv` to model `highUptake_mol`.
- **Predict**: Generate methane uptake predictions for `test.csv`.
- **Submit**: Format predictions as per `sample_submission.csv` and submit your results.