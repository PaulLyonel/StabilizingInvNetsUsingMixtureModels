# Stabilizing Inv Nets Using Mixture Models

This is the supplementary material for the paper "Stabilizing Invertible Neural Networks Using Mixture Models". The different notebooks for the experiments can be found in the respective folders and are based on the official implementation of "Analyzing inverse problems with invertible neural networks", https://github.com/vislearn/analyzing_inverse_problems. 

The following packages are required: 

1) PyTorch (version: 1.7.1+cu101)
2) FrEIA (available at https://github.com/VLL-HD/FrEIA, commit 26a5d4a901831a7f0130c6059b9d50ac72ae6f47) 
3) Numpy (version 1.18.1)
4) Random
5) matplotlib (version 3.1.3)
6) tqdm (version 4.42.1)

The code was tested on that specific version with python 3.7.6 with cuda. Particularly the MNIST example runs very slow on CPU.

Some general advice on when and how to use Mixture Models:

1) All problems we experimented with had multimodal priors.
2) It is advisable to choose the latent space (i.e. the mixture means) in such a way that the random initial fit of the T_z component matches the latent space.
3) If modes get merged, one can use a sparsity prior on the probabilities.
4) If the y-space is continuous such as in the inverse kinematics example, one should use quite large batch-sizes in order to learn the correct probabilities.
5) Clamping can go a long way in order to preserve Lipschitz continuity.

