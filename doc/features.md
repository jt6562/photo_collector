# 想法与特性

1. 导入照片，支持:

  - 通过指定目录导入
  - 通过web页面拖动导入图片或文件夹
  - 通过监听特定微信群，导入群内照片。

2. 自动去重，按照MD5(或SHA1)去重。后台使用OpenCV之类的工具计算图片特征向量，根据图片内容进行去重。在专门的页面，手动确认保留哪一张图片。手动确认时，提供图片信息（分辨率，原图，位置，拍摄时间等）。

3. 后台分析照片EXIF信息，导出照片基本信息，主要是拍摄地点，时间，分辨率等。数据保存到数据库中。

4. 前端页面至少有三个标签，一个时间线展示图片，一个是通过地图热点展示，最后一个是图片导入标签。

5. 有简单的搜索功能，比如按照地点搜索，按照时间段搜索等。

  - 地点搜索可以通过从百度地图之类的地图应用，将搜索地址转换为经纬度，以此经纬度为圆心，N公里为半径，返回所有在此范围内的图片。
  - 时间段搜索，简单说就是在给定时间段的拍摄时间都作为结果返回。

参考：

> - <http://icodeit.org/2015/09/visualize-your-steps/?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io>
> - <http://icodeit.org/placesihavebeen/>
