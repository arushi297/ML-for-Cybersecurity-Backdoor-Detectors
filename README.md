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

The model can be found [here](https://github.com/csaw-hackml/CSAW-HackML-2020/tree/master/lab3) in the models directory and the data can be downloaded from [this link](https://drive.google.com/drive/folders/1Rs68uH8Xqa4j6UxG53wzD0uyI8347dSq?usp=sharing). The dataset comprises images sourced from the YouTube Aligned Face Dataset, featuring 1,283 individuals. The folder cl contains clean test and validation images while bd stores poisoned test and validation set. The files bd_valid.h5 bd_test.h5 contains test images associated with the activation of sunglasses triggers, which in turn activates the backdoor functionality in bd_net.h5.

## Running eval.py

1. Clone the repository
   
```
git clone https://github.com/arushi297/ML-for-Cybersecurity-Backdoor-Detectors.git
```

2. Download the dataset from the links provided above

3. Run the eval.py script

```
python /path/to/eval.py /path/to/clean_data_filename /path/to/poisoned_data_filename /path/to/pruned_model
```
 or if running from the jupyter notebook:
```
%run -i /path/to/eval.py /path/to/clean_data_filename /path/to/poisoned_data_filename /path/to/pruned_model
```
 Example usage: 
```  %run -i /scratch/aa10350/MLForCybersec/CSAW-HackML-2020/lab3/eval.py  /scratch/aa10350/MLForCybersec/Lab3/cl/test.h5  /scratch/aa10350/MLForCybersec/Lab3/bd/bd_test.h5 /scratch/aa10350/MLForCybersec/model_X=10.h5 ```

## Jupyter Notebook

To run fine pruning from scratch, run all the cells of `aa10350_backdoor_attacks.ipynb`. Make sure that the data and model are downloaded
