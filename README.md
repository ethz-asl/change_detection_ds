# Change Detection Datasets

Paper: 
```
@inproceedings{fehr2017changedetection,
  title={{TSDF}-based Change Detection for Consistent Long-Term Dense
          Reconstruction and Dynamic Object Discovery},
  author="Fehr, Marius and Furrer, Fadri and Dryanovski Ivan and Sturm, Jurgen and Gilitschenski, Igor and Siegwart, Roland and Cadena, Cesar",
  booktitle={2017 IEEE International Conference on Robotics and Automation (ICRA)},
  year={2017},
  organization={IEEE}
}
```

## [DOWNLOAD](http://robotics.ethz.ch/~asl-datasets/icra_2017_change_detection/)

**Dataset Contents:**
 * For every observation:
    * Complete mesh of the aligned TSDF reconstructions.
    * Rosbag
      * `T_G_C`: Color camera transform (*geometry_msgs/TransformStamped*)
      * `T_G_D`: Depth camera transform (*geometry_msgs/TransformStamped*)
      * `color_image`: Color image (*sensor_msgs/Image*)
      * `point_cloud_D`: Point cloud in camera frame (*sensor_msgs/PointCloud2*)
      * `point_cloud_G`: Point cloud in global frame (*sensor_msgs/PointCloud2*)
      * `tf`: tf tree for `world`, `depth_camera` and `color_camera` (*tf/tfMessage*)



## living_room

![living_room](https://github.com/ethz-asl/change_detection_ds/blob/master/previews/living_room.png?raw=true)

This is the baseline dataset and consists of 9 hand-held recordings in a controlled indoor environment. It provides nearly 100% observation overlap and also provides depth measurements from a large variety of viewpoints for most objects resulting in 3D models with a high coverage. The scene changes not only overlap in between observations but the dynamic objects also come in contact with different other objects.

## office

![office](https://raw.githubusercontent.com/ethz-asl/change_detection_ds/a854383e2ba7d706db46876ce5fe93b5bf50a7ad/previews/office.png)

This dataset consists of 4 observations of a controlled office environment recorded from a single point at the center of the room using a tripod. Hence the overlap of the observations is close to 100%. Its purpose is to be able to compare our approach to the meta-room algorithm which assumes a robotic platform with a pan-tilt RGB-D sensor unit that scans a single, convex room from a central point.

## lounge

![lounge](https://github.com/ethz-asl/change_detection_ds/blob/master/previews/lounge.png?raw=true)

This is the most challenging dataset and consists of 10 hand-held recordings in an uncontrolled, challenging environment, a highly frequented meeting area/office lounge over the course of two weeks where objects are shifted on a daily basis. The observation overlap varies between approx. 50 - 100% and many dynamic objects are only partially observed.

## Contact:
marius.fehr(at)mavt.ethz.ch
