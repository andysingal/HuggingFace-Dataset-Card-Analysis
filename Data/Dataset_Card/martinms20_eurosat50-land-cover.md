---
task_categories:
- image-classification

---
# AutoTrain Dataset for project: klasifikasi-tutupan-lahan

## Dataset Description

This dataset has been automatically processed by AutoTrain for project klasifikasi-tutupan-lahan.

### Languages

The BCP-47 code for the dataset's language is unk.

## Dataset Structure

### Data Instances

A sample from this dataset looks as follows:

```json
[
  {
    "image": "<64x64 RGB PIL image>",
    "target": 8
  },
  {
    "image": "<64x64 RGB PIL image>",
    "target": 0
  }
]
```

### Dataset Fields

The dataset has the following fields (also called "features"):

```json
{
  "image": "Image(decode=True, id=None)",
  "target": "ClassLabel(names=['AnnualCrop', 'Forest', 'HerbaceousVegetation', 'Highway', 'Industrial', 'Pasture', 'PermanentCrop', 'Residential', 'River', 'SeaLake'], id=None)"
}
```

### Dataset Splits

This dataset is split into a train and validation split. The split sizes are as follow:

| Split name   | Num samples         |
| ------------ | ------------------- |
| train        | 400 |
| valid        | 100 |
