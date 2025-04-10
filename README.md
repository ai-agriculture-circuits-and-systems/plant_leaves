 # Beans Dataset

## Description

The Beans dataset consists of images of beans taken in the field using smartphone cameras. It contains 3 classes:
- Healthy beans
- Beans with Angular Leaf Spot disease
- Beans with Bean Rust disease

The dataset was collected by the Makerere AI research lab and annotated by experts from the National Crops Resources Research Institute (NaCRRI) in Uganda.

## Dataset Details

- **Size**: 171.63 MiB
- **Image format**: RGB images (500×500×3)
- **Number of classes**: 3
- **Splits**:
  - Training: 1,034 images
  - Validation: 133 images
  - Test: 128 images

## Features

```
FeaturesDict({
    'image': Image(shape=(500, 500, 3), dtype=uint8),
    'label': ClassLabel(shape=(), dtype=int64, num_classes=3),
})
```

## Usage with TensorFlow Datasets

```python
import tensorflow_datasets as tfds

# Load the dataset
dataset = tfds.load('beans', split='train')

# Load with specific splits
train_ds = tfds.load('beans', split='train')
validation_ds = tfds.load('beans', split='validation')
test_ds = tfds.load('beans', split='test')

# Convert to a tf.data.Dataset
ds = tfds.as_supervised(dataset)

# Iterate through the dataset
for image, label in ds.take(1):
  print(image.shape, label)
```

## Citation

If you use this dataset in your research, please cite:

```
@ONLINE {beansdata,
    author="Makerere AI Lab",
    title="Bean disease dataset",
    month="January",
    year="2020",
    url="https://github.com/AI-Lab-Makerere/ibean/"
}
```

## Acknowledgments

This dataset was created by the Makerere AI Lab in collaboration with the National Crops Resources Research Institute (NaCRRI) in Uganda.

## Links

- [TensorFlow Dataset Catalog Entry](https://www.tensorflow.org/datasets/catalog/beans)
- [GitHub Repository](https://github.com/AI-Lab-Makerere/ibean/)