# ML-for-Cybersecurity-Backdoor-Detectors

## Repository Structure
```
├── pruned_models  // Models saved after Pruning
    └── model_X=2.h5 // Model pruned with 2% drop in val acc
    └── model_X=4.h5 // Model pruned with 4% drop in val acc
    └── model_X=10.h5 // Model pruned with 10% drop in val acc
├── aa10350_backdoor_attacks.ipynb // ipynb with complete code execution
├── eval.py // Script to run evaluation, report accuracy and attack success rate
├── Backdoor_Detectors_Report.pdf  // Report
```
## Requirements:

1. Python 
2. Keras 
3. Numpy
4. Matplotlib 
5. H5py
6. TensorFlow
7. Seaborn
8. tqdm

## Model and Data

The model can be found [here](https://github.com/csaw-hackml/CSAW-HackML-2020/tree/master/lab3) in the models directory and the data can be downloaded from [this link](https://example.com/data](https://drive.google.com/drive/folders/1Rs68uH8Xqa4j6UxG53wzD0uyI8347dSq?usp=sharing)https://drive.google.com/drive/folders/1Rs68uH8Xqa4j6UxG53wzD0uyI8347dSq?usp=sharing).
