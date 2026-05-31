# Training / Experiments

This folder contains the notebooks and artifacts for training and evaluating ERCP image classification models using the split defined in the repository.

---

## Notebooks

- `split_dataset.ipynb` - script/notebook used to create and validate the split (`train` / `val` / `test`) - note: fixed splits are included under `training/dataset/`. By Monica Martins on [GitHub](https://github.com/monicaccmartins/MIQR-CC-Dataset).
- `CONVNEXT_cinthia.ipynb` - training and evaluation for a ConvNeXt-based model.
- `DENSENET_cinthia.ipynb` - DenseNet-based training and evaluation.
- `EFFICIENTNET_v2s_cinthia_newtransform.ipynb` - EfficientNet-based experiment with tweeked transforms
- `EFFICIENTNET_v2s_cinthia.ipynb` - EfficientNet-based experiments.
- `RESNET_50_cinthia.ipynb` - ResNet-based experiments.
- `RESNEXT_50_cinthia.ipynb` - ResNeXt-50-based experiments.
- `RESNEXT_101_cinthia.ipynb` - ResNeXt-101-based experiments.
- `VGG19_cinthia.ipynb` - VGG-based experiments.
- `ViT_b16_cinthia.ipynb` - ViT-based experiments.
- `models/` - Trained model checkpoints used for experiments (and summary visuals).

Each notebook contains data loading, augmentations, training loop, validation and test evaluation, and plotting (confusion matrix, learning curves).

## Requirements

Install the training environment with:

```bash
conda create --name <ENV_NAME> --file requirements.txt
conda activate <ENV_NAME>
```

(`training/requirements.txt` contains the pinned packages used for experiments.)

## Models & Results

Trained checkpoints and summary visuals are under `training/models/` (checkpoints have the `.pth` extension; summary images include confusion matrices `.png`). See `training/models/README.md` for details on how to load them.

## Reproducibility notes

- Fixed splits are included in `training/dataset/` (no need to re-run `split_dataset.ipynb` unless you want a different split).
- Check each notebook for hyperparameters and random-seed usage.
