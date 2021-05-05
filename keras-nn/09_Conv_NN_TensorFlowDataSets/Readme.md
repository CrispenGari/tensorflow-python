### TensorFlow datasets.
TFDS provides a collection of ready-to-use datasets for use with TensorFlow, Jax, and other Machine Learning frameworks.


### Instalation
```shell
pip install -q tfds-nightly
```

### Import it

```python
import tensorflow_datasets as tfds
```

### Available datasets

```python 
tfds.list_builders()
```

### Loading tfds dataset
* To load the dataset there's a method called `tfds.load()` that will:
    * download the tfrecods files
    * load the tfrecord and create a `tf.data.DataSet`

```python
ds = tfds.load('mnist', split='train', shuffle_files=True)
assert isinstance(ds, tf.data.Dataset)
print(ds)
```
**split** - train|test
**shuffle_files** - boolean (True|False)

### Iterating over data:
```
ds = tfds.load('mnist', split='train')
ds = ds.take(1)  # Only take a single example

for example in ds:  # example is `{'image': tf.Tensor, 'label': tf.Tensor}`
  print(list(example.keys()))
  image = example["image"]
  label = example["label"]
  print(image.shape, label)
```

### Read More
* [Docs](https://www.tensorflow.org/datasets/overview)
* [Docs2](https://www.tensorflow.org/datasets/catalog/overview)

