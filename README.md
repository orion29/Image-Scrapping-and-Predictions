# Image-Scrapping-and-Predictions

## Dataset: Imagewoof 
The dataset consist of 11385 images and includes next categories:
<ul>
  <li>black_dress: 450</li>
<li>black_pants: 871</li>
<li>black_shirt: 715</li>
<li>black_shoes: 766</li>
<li>black_shorts: 328</li>
<li>blue_dress: 502</li>
<li>blue_pants: 798</li>
<li>blue_shirt: 741</li>
<li>blue_shoes: 523</li>
<li>blue_shorts: 299</li>
<li>brown_pants: 311</li>
<li>brown_shoes: 464</li>
<li>brown_shorts: 40</li>
<li>green_pants: 227</li>
<li>green_shirt: 230</li>
<li>green_shoes: 455</li>
<li>green_shorts: 135</li>
<li>red_dress: 800</li>
<li>red_pants: 308</li>
<li>red_shoes: 610</li>
<li>white_dress: 818</li>
<li>white_pants: 274</li>
<li>white_shoes: 600</li>
<li>white_shorts: 120</li>
</ul>

## Transforms Used

### Resize
Resized an image to 224 * 224 pixel




## Training Details

### Model: ResNet 34
ResNet-34 is a convolutional neural network that is 50 layers deep. You can load a pretrained version of the network trained on more than a million images from the ImageNet database

### Loss Function :  FlattenedLoss of CrossEntropyLoss
Cross-entropy loss, or log loss, measures the performance of a classification model whose output is a probability value between 0 and 1. 

### Optimizer : ADAM
Adaptive Moment Estimation (Adam) is an optimizer that computes adaptive learning rates for each parameter. In addition to storing an exponentially decaying average of past squared gradients vt like RMSprop, Adam also keeps an exponentially decaying average of past gradients mt, similar to momentum.

### Scheduler : One cycle Policy
The 1cycle policy has three steps: We progressively increase our learning rate from base_lr to lr_max and at the same time we progressively decrease our momentum from mom_max to mom_min.

We do the exact opposite: we progressively decrease our learning rate from lr_max to lr_max/div_factor and at the same time we progressively increase our momentum from mom_min to mom_max.

