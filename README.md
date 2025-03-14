# CIFAR-10 Image Classification with Custom ResNet

## Project Overview

The goal is to develop a deep learning model that can effectively classify images from the CIFAR-10 dataset while adhering to specific constraints:
- Model size under 5 million parameters
- Test accuracy target of 80% or higher

## Dataset

CIFAR-10 consists of:
- 60,000 32x32 color images
- 10 different classes
- 50,000 training images and 10,000 test images
- Classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck

## Method

Our approach uses a custom ResNet architecture with several key optimizations:

### Architecture
- Custom ResNet with progressive channel expansion (3→32→64→128→256)
- Residual blocks with dual convolution layers and skip connections
- Total parameters: 2.76M (well under 5M limit)
- Integrated dropout (0.3) for regularization

### Training Strategy
- Advanced data augmentation pipeline including MixUp (α=0.2)
- RAdam optimizer with adaptive learning rate scheduling
- Label smoothing (0.1) and weight decay (1e-4)
- Comprehensive regularization techniques

## Results and Conclusion

The model demonstrated strong performance:
- Achieved 90.24% validation accuracy
- Successfully maintained parameter count under 5M (2.76M)

## References

1. He, K., Zhang, X., Ren, S., & Sun, J. (2016). Deep residual learning for image recognition. CVPR 2016.
2. CIFAR-10 dataset: https://www.cs.toronto.edu/~kriz/cifar.html

## Contributors

- Puneeth Kotha pk3058@nyu.edu
- Chenna Kesava Hemanth Reddy Narala cn2507@nyu.edu
- Sai Sandeep Mamidala mss9430@nyu.edu
  
