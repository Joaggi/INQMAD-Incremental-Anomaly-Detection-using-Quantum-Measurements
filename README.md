# InQMAD: Incremental Quantum Measurement Anomaly Detection
This is the official repository for INQMAD. It has been created using Tensorflow and Jax. 


## Abstract:

Streaming anomaly detection refers to the problem of detecting anomalous data samples in streams of data. This problem poses challenges that classical and deep anomaly detection methods are not designed to cope with, such as conceptual drift and continuous learning. State-of-the-art flow anomaly detection methods rely on fixed memory using hash functions or nearest neighbors that may not be able to constrain high frequency values or remove seamless outliers and cannot be trained in an end-to-end deep learning architecture. We present a new incremental anomaly detection method that performs continuous density estimation based on random Fourier features and the mechanism of quantum measurements and density matrices. The method continuously updates the estimation of the density of normal samples, giving more importance to new samples and decreasing the importance of older samples. It can process potentially endless data and its update complexity is constant O(1). A systematic evaluation against 12 state-of-the-art streaming anomaly detection algorithms and using 12 streaming datasets is presented.

## Published in: 
- 2022 IEEE International Conference on Data Mining Workshops (ICDMW)
## Date of Conference: 
- 28 November 2022 - 01 December 2022
## Date Added to IEEE Xplore: 
- 08 February 2023
## DOI: 
- 10.1109/ICDMW58026.2022.00107
## Conference Location: 
- Orlando, FL, USA 

## Cite

If you found this repository interesting, please cite as:
```bibtex
@article{gallego2025inqmad,
  title={INQMAD: incremental streaming anomaly detection with density matrices, quantum measurement, and density estimation},
  author={Gallego, Joseph and Bustos-Brinez, Oscar A and Gonz{\'a}lez, Fabio A},
  journal={Neural Computing and Applications},
  volume={37},
  number={32},
  pages={27475--27503},
  year={2025},
  publisher={Springer}
}
``
