# A cusp-capturing PINN for elliptic interface problems

This repository contains the code for the paper:

* [A cusp-capturing PINN for elliptic interface problems](https://arxiv.org/abs/2210.08424)

In this paper, we propose a cusp-capturing physics-informed neural network (PINN) to solve discontinuous-coefficient elliptic interface problems whose solution is continuous but has discontinuous first derivatives on the interface. To find such a solution using neural network representation, we introduce a cusp-enforced level set function as an additional feature input to the network to retain the inherent solution properties; that is,  capturing the solution cusps (where the derivatives are discontinuous) sharply. In addition, the proposed neural network has the advantage of being mesh-free, so it can easily handle problems in irregular domains. We train the network using the physics-informed framework in which the loss function comprises the residual of the differential equation together with certain interface and boundary conditions. We conduct a series of numerical experiments to demonstrate the effectiveness of the cusp-capturing technique and the accuracy of the present network model. Numerical results show that even using a one-hidden-layer (shallow) network with a moderate number of neurons and sufficient training data points, the present network model can achieve prediction accuracy comparable with traditional methods. Besides, if the solution is discontinuous across the interface, we can simply incorporate an additional supervised learning task for solution jump approximation into the present network without much difficulty.

## Dependencies

* Python
	* [PyTorch](https://pytorch.org)
	* [Functorch](https://github.com/pytorch/functorch)

## Citations

```
@misc{TLHL23,
  title = {A cusp-capturing PINN for elliptic interface problems},
  author = {Tseng, Yu-Hau and Lin, Te-Sheng and Hu, Wei-Fan and Lai, Ming-Chih},
  year = {2023},
  eprint={2210.08424},
  archivePrefix={arXiv}
```

