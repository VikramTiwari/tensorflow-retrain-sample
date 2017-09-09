# How to retrain

- Install tensorflow
- Put folders with images in "categories". The name of the folders will be the classifications.

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
