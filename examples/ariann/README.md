# Installation
Change your PyGrid directory in the ``scripts/launch_***.sh``

Define a `HOME` in data.py

You need to install 2 datasets in your `HOME`:
- Tiny Imagenet, from https://github.com/tjmoon0104/pytorch-tiny-imagenet
- Hymenoptera using the instructions:
    ```
    wget https://download.pytorch.org/tutorial/hymenoptera_data.zip\n"
                "unzip hymenoptera_data.zip
    ```
    
# Usage

```
python main.py --model resnet18 --dataset hymenoptera --preprocess
```

```
usage: main.py [-h] [--model MODEL] [--dataset DATASET] [--preprocess]
               [--websockets]

optional arguments:
  -h, --help         show this help message and exit
  --model MODEL      model to use for inference (network1, network2, lenet,
                     alexnet, vgg16, resnet18)
  --dataset DATASET  dataset to use (mnist, cifar10, hymenoptera, tiny-
                     imagenet)
  --preprocess       preprocess data or not
  --websockets       use PyGrid nodes instead of a virtual network. (nodes are
                     launched automatically)
```

# Datasets

## MNIST

1 x 28 x 28 pixel images

Suitability: Network1, Network2, LeNet

## CIFAR10

3 x 32 x32 pixel images

Suitability: AlexNet and VGG16

## Tiny Imagenet

3 x 64 x 64 pixel images

Suitability: AlexNet and VGG16

## Hymenoptera

3 x 64 x 64 pixel images

Suitability: ResNet18