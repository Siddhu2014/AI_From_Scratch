# Convolutional Neural Networks

This chapter is the first hands-on **CNN / Computer Vision** project in the `AI_From_Scratch` learning path.

The focus is understanding the complete CNN workflow rather than maximizing the CIFAR-10 leaderboard score.

## What was learned

- Convolutional layers (`Conv2d`)
- Input/output channels and learned filters
- Feature maps
- Kernel size, stride, and padding
- ReLU activation
- Max pooling
- Flattening convolutional features
- Fully connected classification
- `CrossEntropyLoss`
- Adam optimizer
- Epoch-based training loops
- GPU acceleration with PyTorch XPU
- Training vs. test accuracy
- Confusion matrices
- Model capacity and generalization
- Data augmentation
- Visual inspection of misclassified images

## Dataset

The project uses **CIFAR-10**:

- 50,000 training images
- 10,000 test images
- RGB images
- Image size: `32 × 32`
- 10 classes

Class indices:

| Index | Class |
|---:|---|
| 0 | airplane |
| 1 | automobile |
| 2 | bird |
| 3 | cat |
| 4 | deer |
| 5 | dog |
| 6 | frog |
| 7 | horse |
| 8 | ship |
| 9 | truck |

## Final CNN

```text
Input: 3 × 32 × 32
        ↓
Conv2d: 3 → 32, 3×3, padding=1
        ↓
ReLU
        ↓
MaxPool 2×2
        ↓
Conv2d: 32 → 64, 3×3, padding=1
        ↓
ReLU
        ↓
MaxPool 2×2
        ↓
Flatten: 64 × 8 × 8 = 4096
        ↓
Linear: 4096 → 10
```

## Training configuration

- Optimizer: Adam
- Learning rate: `0.001`
- Batch size: `64`
- Main experiment: `20` epochs
- Training augmentation:
  - `RandomHorizontalFlip`
  - `RandomCrop(32, padding=4)`
- Test transform:
  - `ToTensor()`

## Experiments

| Experiment | Training accuracy | Test accuracy |
|---|---:|---:|
| 16 → 32 channels, 10 epochs | 70.72% | 66.70% |
| 16 → 32 channels, 20 epochs | 73.74% | 68.63% |
| 32 → 64 channels, 20 epochs | 81.92% | 70.27% |
| 32 → 64 + horizontal flip | 76.98% | 72.24% |
| 32 → 64 + flip + random crop | 71.05% | **73.80%** |

### What these experiments showed

Increasing model capacity increased training performance substantially, but the improvement on unseen data was smaller.

Data augmentation reduced training accuracy while improving test accuracy. This provided a practical demonstration of the difference between **fitting** and **generalization**.

The final experiment reached **73.80% test accuracy**.

## Important formulas / dimension tracking

For a convolutional layer:

[
	ext{Output size} =
rac{N-K+2P}{S}+1
]

where:

- `N` = input spatial size
- `K` = kernel size
- `P` = padding
- `S` = stride

For this model:

```text
32×32
  ↓ MaxPool 2×2
16×16
  ↓ MaxPool 2×2
 8×8
```

The second convolution produces 64 feature maps:

```text
64 × 8 × 8 = 4096
```

Therefore the classifier is:

```text
Linear(4096, 10)
```

## Notebook

Open [`CNN_CIFAR10.ipynb`](./CNN_CIFAR10.ipynb) for the complete implementation and experiments.

## Next chapter

CNN / Computer Vision is now complete in this learning sequence.

Next:

**Sequence Models → RNNs → LSTMs/GRUs → Attention → Transformers**
