## MICCAI BRATS
[[BRATS2020 top1](https://arxiv.org/pdf/2011.00848.pdf)]: nnU-Net for Brain Tumor Segmentation
* 128x128x128 patch
* directly optimizing  whole tumor (consisting of all 3 classes), tumor core (non-enh. & necrosis + enh.tumor) and enhancing tumor.
* sigmoid and Dice loss + Binary cross-entropy loss that optimizes each of the regions independently
* Increased batch size to 5; 
* Augmentation
   1. increase the probability of applying rotation and scaling from 0.2 to 0.3
   2. increase the scale range from (0.85, 1.25) to (0.65, 1.6)
   3. select a scaling factor for each axis individually
   4. use elastic deformation with a probability of 0.3
   5. use additive brightness augmentation with a probability of 0.3
   6. increase the aggressiveness of the Gamma augmentation
* Post-Processing
