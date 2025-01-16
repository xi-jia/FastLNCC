# FastLNCC
A Very Naive Trick to Accelerate Training of LNCC-Based Deep Image Registration Models

(A short description will appear on Arxiv soon.)

Many public repositories implement Local Normalized Cross-Correlation Loss (LNCC) using five sequential convolution operations. This approach, failing to fully utilize modern hardware's performance potential, may be slow. By simply replacing these convolutions with one single group convolution, **the training time of LNCC-based image registration models can be halved without affecting the numerical results**. Although this is an embarrassingly naive trick, (anyone who had Programming 101 may agree?) we believe it is worth sharing with the community due to the significant reduction in training time it offers for large registration models.
