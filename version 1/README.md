# Point Cloud Segmentation and Clustering using RANSAC and DBSCAN Algorithms

## Introduction
This repository contains code to preprocess point cloud data in .stl format. The code includes functions to sample points from .stl files and convert them to .ply or .pcd format, and to scale the resulting point clouds to match the size of a reference point cloud. The repository also contains a notebook to segment and visualize the preprocessed point cloud data.

## Requirements
The code was developed and tested with the following library versions:

1) Python 3.8.10
2) numpy 1.21.2
3) open3d 0.12.0
4) plotly 5.1.0
5) matplotlib 3.4.3
6) scikit-learn 1.1.1

## File Descriptions
file_setup.ipynb: Jupyter notebook containing functions to sample points from .stl files and scale resulting point clouds.
main.ipynb: Jupyter notebook containing code to segment and visualize the preprocessed point cloud data.

## Usage
To preprocess point cloud data, first run the file_setup.ipynb notebook. This notebook includes two functions:

stl_to_ply(fileName_stl, noOfPoints, source_folder, destination_folder): converts .stl files to .ply format by sampling points from the mesh.
scaler(fileName, reference, source_folder, destination_folder): scales .ply or .pcd files to match the size of a reference point cloud.
To use these functions, modify the folderNameSource, folderNameDestination, and referenceFile variables in the **sampleAllFiles()** and **scaleAllFiles()** functions to reflect the location of your input files and the reference point cloud file.

## Default folder Names
1) 'Archive' - This folder keeps the meshes in .stl format
2) 'unscaled' -  This folder stores the unscaled point clouds in .ply format
3) 'scaled' - This folder stores the scaled point clouds in .ply format

After preprocessing, use the main.ipynb notebook to segment and visualize the point cloud data. Use the **get_fileNames(folder_path)** function to retrieve the names of all the files in the directory to be segmented. The **refined_ransac(pcd)** function segments the point cloud data using a RANSAC algorithm and **euclidean_dbscan(rest)** function clusters the rest of the points after the segmentation.

## Acknowledgments
This code is based on the Open3D Python library.
