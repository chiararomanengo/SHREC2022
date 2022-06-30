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

### Ground truth and mandatory output
The participants were asked to return, for the $i$-th point cloud, a file "pointCloudi\_prediction.txt"; the corresponding ground truth file is named "GTpointCloudi.txt".

Each of such files contains a column vector. The first entry is the primitive type: 1=plane, 2=cylinder, 3=sphere, 4=cone, 5=torus. The remaining entries depends on the primitive type:
- *Plane*. The vector lists the unit normal vector and a point sampled on the plane. For example, "GTpointCloud1.txt" in the training set is sampled from a plane having unit normal vector 
    <div style="text-align: center;">[0.849231978395892, 0.525751207196367, 0.0488949384022809]</div> 
    and passing through 
    <div style="text-align: center;">[10.3882508683517, 27.3806667550332, 25.4929773938063].</div>
- *Cylinder*. The vector lists the radius, the unit vector determining the rotational axis, and a point sampled on the axis. For example, "GTpointCloud1001.txt" in the training set is sampled from a cylinder of radius 2.09364548494983, with rotational axis given by  [0,0,1] and passing through 
    <div style="text-align: center;">[-2.31402922020771, 0.928760027158196, 4.88122040084436].<\div>
- *Sphere*. The file lists the radius and the center. For example, "GTpointCloud3001.txt" in the training set is sampled from a sphere of radius 3.92976588628763 and with center  
    <div style="text-align: center;">[-10.7846958533457, -8.00726733221012, -8.18455000377197].<\div>
- *Cone*. The file lists half the aperture, the unit vector determining the rotational axis and the vertex. For example, "GTpointCloud2001.txt" in the training set is sampled from a cone having half the aperture equals to 0.73548991890062, rotational axis 
    <div style="text-align: center;">[0.649523443358968, -0.392136665104304, -0.651420089042382]<\div>
    and vertex  [0,0,0].
- *Torus*. The file lists the major and minor radii, the unit vector determining the rotational axis and the center. For example, "GTpointCloud4001.txt" in the training set is sampled from a torus of major radius 1, minor radius 0.71356783919598,  rotational axis
    <div style="text-align: center;">[0.822071130738891, 0.0766518567043369, 0.564201691657744]<\div> 
    and center [0,0,0].
The reader is reminded to [1] for a complete description of the dataset and of the ground truth.

### References
[1]  C. Romanengo, A. Raffo, S. Biasotti, B. Falcidieno, V. Fotis, I. Romanelis, E. Psatha, K. Moustakas, I. Sipiran, Q.-T. Nguyen, C.-B. Chu, K.-N. Nguyen-Ngoc, D.-K. Vo, T.-A. To, N.-T. Nguyen, N.-Q. Le-Pham, H.-D. Nguyen, M.-T. Tran, Y. Qie, N. Anwer. "SHREC 2022: Fitting and recognition of simple geometric primitives on point clouds". ArXiv: arXiv:2206.07636.
