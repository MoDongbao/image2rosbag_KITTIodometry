利用python将kitti的数据转为rosbag, 仅测试于grayscale数据集.

 1. 在KITTI网页下载[odometry dataset (grayscale, 22GB)](http://www.cvlibs.net/datasets/kitti/eval_odometry.php), 并解压. 

 2. 指定image路径, 生成的bag名,时间戳路径, 然后运行.
```
  python img2bag_kitti_StereoBag.py ./00 00.bag ./00/times.txt
```

**播放rosbag**
```
  rosbag play --pause img2bag_kitti_StereoBag_seq00.rosbag 
```
