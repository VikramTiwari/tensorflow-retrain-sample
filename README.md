# Tensorflow Retrain

## About

This is an example on how to use pre-existing TensorFlow models to retrain on your data. In this example, we use [Inception](https://github.com/tensorflow/models/tree/master/inception) which is an image classifier. You can train it on the existing images of different noodles type and then use images in the test directory to get the predictions.

## Setup

- Install [TensorFlow](https://www.tensorflow.org/install/)
- Put directories with images in `categories` directory. The name of the directories will be the classifications

## Training

``` bash
python retrain.py \
  --bottleneck_dir=bottlenecks \
  --how_many_training_steps=500 \
  --model_dir=inception \
  --summaries_dir=training_summaries/basic \
  --output_graph=retrained_graph.pb \
  --output_labels=retrained_labels.txt \
  --image_dir=categories
```

## Predicting

``` bash
python label_image.py <insert_file_path_to_predict_here>
```

## Visualize

See the model and progress in TensorBoard

``` bash
tensorboard --logdir training_summaries
```

## Credits

- [Albert Padin](https://github.com/albertpadin)
- Based on [Image Retraining Example](https://www.tensorflow.org/tutorials/image_retraining)
