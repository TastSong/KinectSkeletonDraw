# KinectSkeletonDraw

## 环境配置
* opencv2.4.9
* vs2013
* Kinectsdk2.0
## 注释
不难发现代码跟[之前的项目](https://github.com/TastSong/KinectSkeletalTracking)  一篇非常类似，不同的地方就在于绘图部分。首先要将关节点用的`CameraSpace`转换到`ColorSpace`，
这一操作可以借助`ICoordinateMapper`完成，然后就用两个关节点来作为线段的两端画线。这里采用了广度优先的办法，从上到下一层一层选取关节点。
