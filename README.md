利用python将kitti的数据转为rosbag, 仅测试于grayscale数据集,测试过程如下. 
python代码请见:
http://git.oschina.net/taiping.z.git/image2rosbag_KITTIodometry

###1. 在KITTI网页下载[odometry dataset (grayscale, 22GB)](http://www.cvlibs.net/datasets/kitti/eval_odometry.php), 并解压. 

###2. 指定image路径, 生成的bag名,时间戳路径, 然后运行.
```
python img2bag_kitti_StereoBag.py ./00 00.bag ./00/times.txt
```
###3. 查看rosbag,并测试结果
**查看rosbag**
```
rosbag info image_0 kitti_00_l.bag
--------
path:        kitti_00_l.bag
version:     2.0
duration:    7:50s (470s)
start:       Jan 01 1970 08:00:00.00 (0.00)
end:         Jan 01 1970 08:07:50.58 (470.58)
size:        2.0 GB
messages:    4541
compression: none [2271/2271 chunks]
types:       sensor_msgs/Image [060021388200f6f0f447d0fcd9c64743]
topics:      camera/image_raw   4541 msgs    : sensor_msgs/Image
```
**播放rosbag**
rosbag play --pause img2bag_kitti_StereoBag_seq00.rosbag 
