<h2>Semantic Segmentation Utilities</h2>

Collection of useful classes and function for implementation of
semantic segmentation in PyTorch.

Repository contains the following code files:
- [basic_layer.py](https://github.com/Sergo2020/Segment_utils_pytorch/blob/master/basic_layers.py) - Basic convolutional layers, blocks and concatenation function.
- [model_UNET.py](https://github.com/Sergo2020/Segment_utils_pytorch/blob/master/model_UNET.py) - Modular U-Net [1].
- [loss.py](https://github.com/Sergo2020/Segment_utils_pytorch/blob/master/loss.py) - Segmentation loss and evaluation functions [2].


<h3>Basic convolutional layers</h3>

Building blocks of U-Net. 
Contains both modified 2D convolutional layer classes that combine standard API of [torch.nn.Conv2d()](https://pytorch.org/docs/stable/generated/torch.nn.Conv2d.html),
pooling, normalization and activations, and convolutional block which consists of two mentioned layers.
For convenience, there is also a concatenation function that matches skip connection dimensions to the current layer.

<h3>Modular U-Net</h3>

Classical U-Net [1], but with simpler and faster deployment. Instead of defining each layer separately,
only the number of layers, depth and skipp connection have to be specified. Additional detail in 
class description.


<h3>Semantic Segmentation loss functions</h3>

Various semantic segmentation loss functions and metrics [2]:
- Cross Entropy loss variants (binary, non binary, sample weighted and class weighted). 
- Dice loss variants (binary, non binary, sample weighted). 
- Focal loss.
- Twersky loss, including implementation of Focal Twersky Loss. 

<h2>References</h2>

[[1]](https://arxiv.org/abs/1505.04597) Ronneberger, Olaf, Fischer, Philipp; Brox, Thomas (2015). "U-Net: Convolutional Networks for Biomedical Image Segmentation".

[[2]](https://arxiv.org/abs/2006.14822) Shruti Jadon (2020). "A survey of loss functions for semantic segmentation".
