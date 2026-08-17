# Oxford-Pet-Image-Segmentation

A semantic image segmentation project using a U-Net convolutional neural network to segment pet images into pixel-level classes.

The model was trained on the Oxford-IIIT pet dataset and learns to distinguish different regions of cats and dogs at the pixel level.

Unlike image classification, where a model predicts a single label for an entire image, semantic segmentation assigns a class to each pixel.

This project implements a U-Net architecture with:

- Convolutional encoder
- Bottleneck feature representation
- Decoder with upsampling
- Skip connections
- Multi-class pixel-level prediction

The dataset contains images of pets with pixel-level segmentation annotations

Images were resized to:

`128 × 128 × 3`

The segmentation masks contain three classes.

## Model

The segmentation model is based on the U-Net architecture.

### Architecture

- Input: `128 × 128 × 3`
- Encoder with progressively deeper convolutional layers
- Bottleneck with 256 feature channels
- Decoder with upsampling
- Skip connections between encoder and decoder
- Output: `128 × 128 × 3`

Total parameters:

**1,946,947**

## Training

The model was trained for 10 epochs.

Training results:

- Final training accuracy: **85.62%**
- Final validation accuracy: **83.57%**
- Final training loss: **0.3711**
- Final validation loss: **0.4075**

## Evaluation

The trained model was evaluated on the test set.

| Metric | Score |
|---|---:|
| Pixel Accuracy | 84.46% |
| Class 0 IoU | 71.03% |
| Class 1 IoU | 82.70% |
| Class 2 IoU | 36.29% |
| Mean IoU | **63.34%** |

The model achieved a mean Intersection over Union (IoU) of **63.34%** across the three segmentation classes.

## Results

Example predictions are shown below:

![Segmentation Results](<img width="2042" height="1777" alt="segmentation_results" src="https://github.com/user-attachments/assets/8bf5dd14-5e34-4744-9ec7-48bb36a08656" />
)

The model is able to produce visually meaningful segmentation masks and capture the overall shape and structure of the pets.

