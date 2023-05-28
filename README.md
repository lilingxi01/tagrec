<img src="https://imagedelivery.net/Dr98IMl5gQ9tPkFM5JRcng/e2604641-7154-467c-7a2f-5c50f4293b00/HD" alt="Cover"/>

# File Structures

- `baseline_analysis` - This folder contains organized CSV files used in baseline analysis. Note: This file only contains error cases, but not our written analysis.
- `data` - This folder contains the data files for the project. We have organized all data files with the following naming convention: `<dataset_name>_<split>.csv` for raw data or `<dataset_name>_<model_type>_<split>.pt` for pre-processed data. We did not collect any of them, therefore we do not own the copyright of them.
- `figures` - This folder contains all figures automatically generated from the training process.
- `models` - This folder contains the trained models (the best checkpoints) for the project. Files are organized by model names.
- `notebooks` - This folder contains all jupyter notebooks we used when developing the project.
  - `Baseline.ipynb` - This notebook contains the training and evaluation code for baseline models (and comparing with our proposed model).
  - `TagRec_ARC.ipynb` - TagRec models trained on ARC dataset.
  - `TagRec_KhanAcad.ipynb` - TagRec models trained on Khan Academy dataset.
  - `TagRec_NonHierarchicalARC.ipynb` - TagRec models trained on non-hierarchical ARC dataset for exploring the performance effect with/without hierarchical information.
  - `TagRec_WDC.ipynb` - TagRec models trained on WDC dataset.

# Notebooks-related Information

1. We have tested that all notebooks can be run successfully on Colab. But please make sure that you configure your workspace path correctly in the "Drive Mount" section. Everyone has different workspace path.
2. We re-run the notebook after finalizing the result on a faster machine for validating the notebook. Due to the randomness of every execution, the output shown on notebook here might be slightly different from what you might see in the report, but they should be very close to each other.
3. Have fun replicating it!

# Model Checkpoints

We have used Git-LFS for storing files greater than 100MB. All model checkpoints are around 400MB, so you need to configure Git-LFS at your side in order to get them via Git.

First, you need to make sure that you have installed Git-LFS on your local machine correctly. Check here for more information: https://github.com/git-lfs/git-lfs

After cloning the repo, you just need to run following commands to get the model checkpoints rather than meaningless pointer files:

```bash
git lfs install
git lfs pull
```

# Error Analysis
The folder error_analysis contains the annotated files, which includes some samples that: the baseline model failed at; our TagRec model failed at; both failed at. These samples are annotated to see if there are any semantic or syntactic commonalities between them. 

