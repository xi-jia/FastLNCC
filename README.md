# FastLNCC
A Very Naive Trick to Accelerate Training of LNCC-Based Deep Image Registration Models

(A short description will appear on Arxiv soon.)

Many public PyTorch repositories implement Local Normalized Cross-Correlation Loss (LNCC) using five sequential convolution operations. This implementation is, however, slow, failing to fully utilize modern hardware's performance potential. By simply replacing these convolutions with one single group convolution, we found **the training time of LNCC-based image registration models can be halved without affecting the numerical results}**, leading to notable cost savings. We hope that this straightforward approach will be beneficial to the community.
