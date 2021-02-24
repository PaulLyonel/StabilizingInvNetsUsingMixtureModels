# StabilizingInvNetsUsingMixtureModels

This is the supplementary material for the paper "Stabilizing Invertible Neural Networks Using Mixture Models". The different notebooks for the experiments can be found in the respective folders. 

The following packages are required: 

1) PyTorch
2) FrEIA (available at https://github.com/VLL-HD/FrEIA) 
3) Numpy
4) Random
5) matplotlib

Some general advice on when and how to use Mixture Models:

1) All problems we experimented with had multimodal priors.
2) It is advisable to choose the latent space (i.e. the mixture means) in such a way that the random initial fit of the T_z component matches the latent space.
3) If modes get merged, one can use a sparsity prior on the probabilities.
4) If the y-space is continuous such as in 

