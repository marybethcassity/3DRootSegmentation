# 3DRootSegmentation
dataPrep.ipynb takes sequential CT images and masks, stacks them, and slices the stack along the x, y, and z axis. 

tile.ipynn randomly tiles images and randomly rotates the tiles.

predict.ipynb can be used to predict on images for 
instance segmentation, then saves these predictions to a json file in coco format. Note, if a segmentation prediction only consists of 2 points, the second point will be copied and appended to make a 3rd point. Alternatively, this segmentation can just be removed. Either way, a segmentation consisting of only 2 points must be removed or edited.

Open3DDBSCANmetrics3view.ipynb can be used to rebuild the predictions into a 3d numpy array and filter the predictions using Open3D's implementation of DBSCAN with automated parameter tuning. You can calculate accuracy metrics or view a point cloud using Open3D from any view combination. 

