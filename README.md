# Convolutional-differentiable mesh architecture (for PINNs)
This repository contains a convolutional architecture that 
- takes an input function
- transforms that function into an output over a mesh
- allows a single point along that mesh to be extracted
- allows differentiability along that point with respect to the domain (mesh) and time, thus suitable for physics-informed applications.
  
The architecture thus outputs both the entire mesh at once as well as a single, specified point. This architecture is notable because differentiation in this process is traditionally nontrivial (i.e. we can bypass the error "One of the differentiated tensors has not been used in the graph"), and it prevents the need for concatenation over the entire grid (i.e. it is already done for us).

