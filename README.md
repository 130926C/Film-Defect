# Film-Defect


This repository is the code part of our article "XXX".

Because our unit undertakes defense-related tasks, we will try our best to keep the original code about the model in the paper as much as possible.

If you would like a copy of our self-made laser damage film dataset, or more details from the model, please contact us use the email address below and we will contact you if you pass the review session and negotiate how to deliver this data.

---------

# Installation
```python
sudo pip install -r requirements.txt
```
We use Ubuntu 20.04 Server as platform, cuda version is 11.3 and cuDNN version is 8.1. If you have any question about TensorFlow and cuda version, click this [link](https://tensorflow.google.cn/install/source#gpu) to check.
  
4 Nvidai Titan V GPU is used to train our model, total GPU memory is 48 GB (12 x 4).

-----------

# File Organize

We organize the file in the following way. 

```python

DataFolder/
    ...
utils/
    ...
models/
    ...
```

**DataFolder**:   
You can put your data here and use the type name as the folder name. Since we use [tf.keras.preprocessing.image_dataset_from_directory](https://tensorflow.google.cn/versions/r2.6/api_docs/python/tf/keras/preprocessing) interface to load image streams from this folder, you must follow the file types supported by this interface. Otherwise, unexpected bugs may appear.

For images, currently only png format images are allowed, the original image can be any size and will be resized to (224,224,3) by default during the pre-processing process.


**utils**
This folder holds some tool files that are used to building model, loading data, and pre-processing. 

In addition, the global configuration file is also here, and you can modify the **global_params.py** file to adjust the global parameters.