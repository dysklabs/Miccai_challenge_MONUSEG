## Nucleus Segmentation 

Please install following package
```
pip install imgaug numba numexpr
```


First, setup your model hyper-parameter config in the **monuconfig.py**. We support backone: resnet50/101, densenet121/169 and inception-resnetv2, please set the model in BACKBONE.

```python
class Config(object):
  NAME = "name your model"
  RPN_ANCHOR_SCALE = (2, 4, 6, 8, 10)
  BACKBONE = "resnet101"
  ...
```

Then train the Mask-RCNN by
```
python train.py --weight imagenet --dataset dataset/ --logs logs/ --subset train
```

## Inference result
