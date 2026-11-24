# 18-83. Windows : Preparing dataset and splitting the dataset automatically

Splitting a dataset into training, validation, and test sets.
```shell
python split_dataset_class.py \
    --train 80 \
    --val 10 \
    --test 10 \
    --folder data/classify/weather \
    --dest data/classify/weather_dataset
```

Check the dataset structure after splitting.
```shell
python check_images.py \
    --src data/classify/weather_dataset
```