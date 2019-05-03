# CarND - Semantic Segmentation Rubrics

## Build the Neural Network
### Does the project load the pretrained vgg model?
The pretrained `vgg` model is downloaded using helper fuction and loaded using Tensorflow API (v1.3.0) `tf.saved_model.loader.load()`. The function `load_vgg` at `main.py` is implemented to get references to important layers. See [load_vgg](main.py#23-46) implementation.

### Does the project learn the correct features from the images?

### Does the project optimize the neural network?

### Does the project train the neural network?

## Neural Network Training
### Does the project train the model correctly?

```
Model build successful, starting training
EPOCH 1: Average loss for the current epoch = 0.803
EPOCH 2: Average loss for the current epoch = 0.487
EPOCH 3: Average loss for the current epoch = 0.178
EPOCH 4: Average loss for the current epoch = 0.147
EPOCH 5: Average loss for the current epoch = 0.129
EPOCH 6: Average loss for the current epoch = 0.109
EPOCH 7: Average loss for the current epoch = 0.095
EPOCH 8: Average loss for the current epoch = 0.091
EPOCH 9: Average loss for the current epoch = 0.082
EPOCH 10: Average loss for the current epoch = 0.070
EPOCH 11: Average loss for the current epoch = 0.065
EPOCH 12: Average loss for the current epoch = 0.068
EPOCH 13: Average loss for the current epoch = 0.062
EPOCH 14: Average loss for the current epoch = 0.056
EPOCH 15: Average loss for the current epoch = 0.052
EPOCH 16: Average loss for the current epoch = 0.048
EPOCH 17: Average loss for the current epoch = 0.046
EPOCH 18: Average loss for the current epoch = 0.044
EPOCH 19: Average loss for the current epoch = 0.042
EPOCH 20: Average loss for the current epoch = 0.039
EPOCH 21: Average loss for the current epoch = 0.038
EPOCH 22: Average loss for the current epoch = 0.036
EPOCH 23: Average loss for the current epoch = 0.035
EPOCH 24: Average loss for the current epoch = 0.037
EPOCH 25: Average loss for the current epoch = 0.037
EPOCH 26: Average loss for the current epoch = 0.047
EPOCH 27: Average loss for the current epoch = 0.037
EPOCH 28: Average loss for the current epoch = 0.033
EPOCH 29: Average loss for the current epoch = 0.031
EPOCH 30: Average loss for the current epoch = 0.030
```

### Does the project use reasonable hyperparameters?

No of epochs: 30
Batch size: 8

### Does the project correctly label the road?