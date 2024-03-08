

# Project Title

#Water mark recognition of Isaac Newton's Manuscript

## Installation

This code is tested under a Pytorch > 1.0 + Python 3.9.6 environment. To install all dependencies, run the following command:

```bash
bash requirement.sh
```

## Datasets

This project uses the Isaac Newton Watermark dataset with different wavelengths and pre-processing:

- IRT-940-DIV-IRR-940
- IRT-940
- IRT-735
- VIST-500

To directly download the dataset, run the following commands:

```bash
cd data/
bash download_data.sh ## Watermark 
```

## Models

To download pretrained models, run the following commands:

```bash
cd model/
bash download_model.sh # classification models + fine-tuned models
```

## Classification

For the Briquet Train dataset, run the following commands:

```bash
cd classification/
bash demo_train.sh # Training with Dropout Ratio 0.7
```

## Local Matching

### One-shot Recognition

For the Isaac Newton Test dataset, run the following commands:

```bash
cd localMatching/
bash demo_ISAC.sh 
```

### Feature Similarity Baselines

Run the following commands:

```bash
cd featComparisonBaseline/
bash bestParam.sh # Run with resolution 256 * 256
bash run.sh # Run with different resolutions
```

### One-shot Cross-domain Recognition

For the Briquet Test dataset, run the following commands:

```bash
cd localMatching/
bash demo_Briquet.sh # Using drawing or synthetic as references with finetuned model
```

For the Isaac Newton IRT-940-DIV-IRR-940+ synthetic Briquet dataset, run the following commands:

```bash
cd localMatching/
bash demo_IsaacNWM.sh # Evaluate on synthetic Briquet + Newton watermark dataset with / without finetuned model
```

## Large Scale One-shot Cross-domain Recognition

For the B Test_IRT-940-DIV-IRR-940+ Briquet dataset, follow the instructions in the `localMatching` section.

## Feature Learning

For the B Train dataset, run the following commands:

```bash
cd featureLearning/
bash demo_B_Isaac_Finetune.sh # for Newton + synthetic dataset
```
