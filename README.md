# dbscan_ransac_2
Segmentation and clustering of metal parts (.stl) format using ransac and dbscan algorithms in open3d and trimesh

version 2: Only uses open3d and uses the mesh.sample_points_uniformly() function to sample points and applies ransac and dbscan to segment and cluster the metal parts

version 3: Uses open3d and trimesh to sample points and applies ransac and dbscan to segment and cluster the metal parts. It also finds the majority color of the points
in each of the triangles in the mesh and assigns all the points inside of the each triangle the majority color of the points.
