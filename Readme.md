## Summary

__Yi Li__

This notebook uses PCA to do dimension reduction on 400 face images (each one has 10304 pixels) to find the top k eigenfaces. After compressing images (dimension reduction), I find the most similar face image of a given face image by calculating the euclidian distance between each pair of the given image and the others in the database.


## PCA explanation
 $A$ is a $10304*400$ matrix, which represents the data of 400 face images (each one has 10304 pixels).
 
 $C = AA^T$ is a $10304*10304$ matrix,
 
 $C' = A^TA$ is a $400*400$ matrix.
 
 $A^TAV = \lambda V$, $V$ is the eigenvectors $(400*400)$ for the matrix $A^TA$, that is, $C'$.
 
 Using PCA and choose top $k$ eigenvectors, then $V$ becomes a $400*k$ matirx.
 
 $(AA^T)(AV) = \lambda(AV)$, $AV$ is the eigenvectors for the matrix $AA^T$, that is, $C$. 
 
 $AV$ is called eigenfaces. $A$ times the top $k$ eigenvectors of $V$, then $AV$ becomes a $10304*k$ matirx.
 