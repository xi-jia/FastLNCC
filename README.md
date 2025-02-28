# FastLNCC
A Very Naive Trick to Accelerate Training of LNCC-Based Deep Image Registration Models


Many public PyTorch repositories implement Local Normalized Cross-Correlation Loss (LNCC) using five sequential convolution operations. This implementation is, however, slow, failing to fully utilize modern hardware's performance potential. By simply replacing these convolutions with one single group convolution, we found **the training time of LNCC-based image registration models can be halved without affecting the numerical results**, leading to notable cost savings. We hope that this straightforward approach will be beneficial to the community.


```
# For PyTorch versions > 2.0, if there are numerical differences, please add the following code.
torch.backends.cudnn.allow_tf32 = False
```

If you find this repo helpful, please consider citing our work.
```

@article{JiaFastLNCC2025,
	doi = {10.20944/preprints202502.2200.v1},
	url = {https://doi.org/10.20944/preprints202502.2200.v1},
	year = 2025,
	month = {February},
	publisher = {Preprints},
	author = {Xi Jia and Xinxing Cheng and Jinming Duan and Bartłomiej W. Papież},
	title = {A Naive Trick to Accelerate Training of LNCC-Based Deep Image Registration Models},
	journal = {Preprints}
}

```
