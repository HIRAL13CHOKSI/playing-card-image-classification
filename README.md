# Playing-Card Image Classification

**Python · TensorFlow/Keras · Convolutional neural networks · Computer vision**

This project explores a convolutional neural network that classifies playing-card images into **52 categories**. It covers image preprocessing, augmentation, model training, validation, and test evaluation.

## Project at a glance

| | |
|---|---|
| Task | Classify an image as one of 52 cards |
| Original data split | 7,509 training images, 260 validation images, 260 test images |
| Image input | 150 × 150 color images |
| Framework | TensorFlow / Keras |
| Dataset | Private; not included in this repository |

## Approach

The original notebook loads images by class, rescales pixels, and applies training augmentation. Its model uses three convolution-and-pooling stages followed by a dense layer and a 52-class softmax output.

```mermaid
flowchart LR
    A["Card image"] --> B["Resize and rescale"]
    B --> C["Convolution and pooling"]
    C --> D["Dense classification"]
    D --> E["52 class probabilities"]
```

## Saved result

The original notebook reports **73.05% test accuracy**. This is a preliminary saved result: the evaluation used 8 full batches of 32 images (256 of 260 test images), and the training log reported an input-exhaustion warning. It has not been independently reproduced and should not be interpreted as accuracy over the complete test set.

## Notebook and next steps

[Evaluation revision (draft)](notebooks/playing_cards_full_evaluation_draft.ipynb) preserves the original CNN design while allowing Keras to infer the batch counts and include the final partial batch. The revised notebook has not been run and its outputs are cleared.

A clean rerun requires access to the private original dataset. It should verify the training and validation loops and evaluate all test images before the result is updated.

## Skills demonstrated

Image preprocessing and augmentation · neural-network design · multiclass classification · validation · evaluation review
