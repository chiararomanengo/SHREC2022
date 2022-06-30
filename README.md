# SHREC 2022: Fitting and recognition of simple geometric primitives on point clouds

This repository contains the dataset, the ground truth and the results submitted by the participants of the track [1]. The routines that were used to produced the results in [1] can be found at:

https://github.com/rea1991/SHREC2022_evaluation.git

### Dataset
The data set is already divided into a training set and a test set. All participants, independently from the method they plan to employ, were asked to return their results only on the test set.

Input point clouds are provided in files named "pointCloudi.txt", where i is an integer: for example, "pointCloud1.txt", "pointCloud2.txt", "pointCloud56.txt". Each file lists the points belonging to the corresponding point cloud, one per row. Each point cloud is obtained by sampling one of the following simple geometric primitives: plane, cylinder, cone, sphere and torus. A point cloud can be:
- Clean.
- Perturbed by uniform noise of different intensity.
- Perturbed by Gaussian noise of different intensity.
- Clean but affected by undersampling.
- Clean but affected by missing parts.
- Perturbed by uniform noise of different intensity and undersampled.
- Perturbed by Gaussian noise of different intensity and undersampled.
- Perturbed by uniform noise of different intensity and affected by missing parts.
- Perturbed by Gaussian noise of different intensity and affected by missing parts.
- Clean but with local deformations.

### References
[1]  C. Romanengo, A. Raffo, S. Biasotti, B. Falcidieno, V. Fotis, I. Romanelis, E. Psatha, K. Moustakas, I. Sipiran, Q.-T. Nguyen, C.-B. Chu, K.-N. Nguyen-Ngoc, D.-K. Vo, T.-A. To, N.-T. Nguyen, N.-Q. Le-Pham, H.-D. Nguyen, M.-T. Tran, Y. Qie, N. Anwer. "SHREC 2022: Fitting and recognition of simple geometric primitives on point clouds". ArXiv: arXiv:2206.07636.
