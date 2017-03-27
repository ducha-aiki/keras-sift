This is an [keras](https://github.com/fchollet/keras/) implementation of SIFT patch descriptor. It is very slow for describing one patch, but quite fast for batch.

Here are comparisons to the original Michal Perdoch implementation. 
The benchmark is on W1BS dataset from [WxBS: Wide Baseline Stereo Generalizations](https://arxiv.org/abs/1504.06603.pdf) paper, figure 3. So there is no difference between versions in performance 

Average performance on W1BS

![average](/img/total.png)
    
Speed: 
- 0.00246 s per 65x65 patch - [numpy SIFT](https://github.com/ducha-aiki/numpy-sift)
- 0.00028 s per 65x65 patch - [C++ SIFT](https://github.com/perdoch/hesaff/blob/master/siftdesc.cpp)
- 0.00100 s per 65x65 patch - CPU, 1 patch per batch
- 0.00087 s per 65x65 patch - CPU, 256 patches per batch
- 0.00236 s per 65x65 patch - GPU (GF940M), 1 patch per batch
- 0.00062 s per 65x65 patch - GPU (GF940M), 256 patches per batch



If you use this code for academic purposes, please cite the following paper:

    @article {tbd}
