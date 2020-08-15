# DeepSolar
Nationwide houseshold-level solar panel identification with deep learning. See details from our [project website](http://web.stanford.edu/group/deepsolar/home). We used [Inception-v3](https://arxiv.org/pdf/1512.00567.pdf) as the basic framework for image-level classification and developed greedy layerwise training for segmentation and localization.
CNN model was developed with [TensorFlow](https://github.com/tensorflow). `slim` package is credited to Google. `train_classification.py` and `train_segmentation.py` were developed with reference to [inception](https://github.com/tensorflow/models/tree/master/inception).


## Usage instructions for classification module

Clone repo, pip install requirements.txt and then run

```
python test_classification.py <img_dir>
```

This will run inference on all images in `<img_dir>`. For example, run `python test_classification.py ./imgs` to run on the sample images in this repository.

When downloading images from google maps api note that their zoom level must be set to 22 otherwise inference will not work properly. This is likely because the models were originally trained on images of this zoom level


### More:

This is a fork of https://github.com/wangzhecheng/DeepSolar, see that repo for more info