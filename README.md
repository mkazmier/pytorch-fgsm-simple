# pytorch-fgsm-simple
Simple example of Fast Gradient Sign Method adversarial attack on MNIST-trained convolutional neural net.

The method was first described by [(Goodfellow et al., 2015)](#1). As the name suggests, it uses the sign of the gradient of the cost function `J` wrt input `x` to generate a linear adversarial perturbation, shifting the model prediction towards the wrong class (see figure below):
```
eta = eps * sign(grad_x(J(w, x, y))).
```

![](https://www.tensorflow.org/tutorials/generative/images/adversarial_example.png)

## Usage

1. Make sure you have the latest Pytorch and torchvision installed.
2. To start training, run `python train.py`. To see the available settings, run `python train.py -h`.

## References
<a id="1"></a>
Goodfellow, Ian J., Shlens, Jonathon and Szegedy, Christian. Explaining and harnessing adversarial examples. ICLR, abs/1412.6572, 2015. URL [http: //arxiv.org/abs/1412.6572]().
