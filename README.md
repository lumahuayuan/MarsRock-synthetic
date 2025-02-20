# SynMars

We release **SynMars**, a wide-angle synthetic dataset for Martian rock segmentation. This contains a large number of rocks of different sizes, all of which are labeled regardless of size, helping to more accurately assess the robustness of various segmentation methods. SynMars has a total of 60,000 labeled images with a resolution of 1024 × 1024 available for experiments. We divided them into 4,8000 images for training, 6,000 for validation and 6,000 for testing. It was collected from a simulation environment generated by [Blender](https://wiki.blender.org/wiki/Main_Page), an open source and versatile 3-D computer graphics software allowing users to create and arrange 3-D objects. 

The simulated environment is a Mars-like terrain with an area of 100 x 100 m that is populated by thousands of rocks. We built this terrain by referring to the rock distribution photographed by TianWen-1. In each scene, an imgae pair is drawn from the left and right virtual cameras, and therefore SynMars can support downstream vision missions like Stereo Matching and 3D reconstruction, etc. The intrinsics and extrinsics of the camera were set according to those on the TianWen-1 rover such that the landform of SynMars is closer to that of the TianWen-1 dataset. The distribution of all rocks in SynMars is displayed as follow, where 6 colored lines represent the traverse routes. 

<div align=center>
  <img src=https://github.com/lumahuayuan/SynMars/blob/master/samples/synmars_route.png width="60%" />
</div>

On each route, a virtual camera on a rover captured images with a resolution of 1920 x 1080. For a standard experiment, all images were divided into two 960 × 1080 sub-images for efficiency and resized to 1024 × 1024. We show a sample of each route as follow, where a background of undulating textured terrain, a foreground of Martian rocks with complex polygonal shapes, and a realistic lighting model casting shadows are well simulated. 

Route 1-2:
<div align=center>
  <img src=https://github.com/lumahuayuan/SynMars/blob/master/samples/a6r1_rgb0001.png width="20%" />
  <img src=https://github.com/lumahuayuan/SynMars/blob/master/samples/a6r1_label0001.png width="20%" />
  <img src=https://github.com/lumahuayuan/SynMars/blob/master/samples/a6r2_rgb0001.png width="20%" />
  <img src=https://github.com/lumahuayuan/SynMars/blob/master/samples/a6r2_label0001.png width="20%" />
</div>

Route 3-4:
<div align=center>
  <img src=https://github.com/lumahuayuan/SynMars/blob/master/samples/a6r3_rgb0241.png width="20%" />
  <img src=https://github.com/lumahuayuan/SynMars/blob/master/samples/a6r3_label0241.png width="20%" />
  <img src=https://github.com/lumahuayuan/SynMars/blob/master/samples/a6r4_rgb0505.png width="20%" />
  <img src=https://github.com/lumahuayuan/SynMars/blob/master/samples/a6r4_label0505.png width="20%" />
</div>

Route 5-6:
<div align=center>
  <img src=https://github.com/lumahuayuan/SynMars/blob/master/samples/a6r5_rgb0001.png width="20%" />
  <img src=https://github.com/lumahuayuan/SynMars/blob/master/samples/a6r5_label0001.png width="20%" />
  <img src=https://github.com/lumahuayuan/SynMars/blob/master/samples/a6r6_rgb0001.png width="20%" />
  <img src=https://github.com/lumahuayuan/SynMars/blob/master/samples/a6r6_label0001.png width="20%" />
</div>
Limited by the file size, we temporarily release 25 samples of each route. 

### SynMars-8k
We also released a sub-dataset **SynMars-8k** sampled regularly from SynMars for preliminary testing and optimizing your model, since direct training on SynMars with 48k images needs a little bit of time. **SynMars-8k** contains 8,000 images for training, 1,000 for validation and 1,000 for testing. 


You can download **SynMars** and **SynMars-8k** by the following ways.

**SynMars**: [**CVIR filestation**:](http://gofile.me/6V28a/wIrQtb7Pt) or by [Baidu Cloud](https://pan.baidu.com/s/1AsBSG7gwWxAkCW6ILfxU9A) with passcode:**synm**


**SynMars-8k**: [**CVIR filestation**](http://gofile.me/6V28a/2BegJScZw) or by [Baidu Cloud](https://pan.baidu.com/s/1nhG4RBV5VZAHH7EPW4a4hA) with passcode: **synm**

If you use **SynMars** or **SynMars-8k** for your research, please cite the following paper：

```
@article{xiong2023marsformer,
  title={MarsFormer: Martian Rock Semantic Segmentation With Transformer},
  author={Xiong, Yonggang and Xiao, Xueming and Yao, Meibao and Liu, Haiqiang and Yang, Hong and Fu, Yuegang},
  journal={IEEE Transactions on Geoscience and Remote Sensing}, 
  volume={61},
  pages={1-12},
  year={2023},
  doi={10.1109/TGRS.2023.3302649}
}
```
<!--
@article{liu2023rockformer,
  title={RockFormer: A U-Shaped Transformer Network for Martian Rock Segmentation},
  author={Liu, Haiqiang and Yao, Meibao and Xiao, Xueming and Xiong, Yonggang},
  journal={IEEE Transactions on Geoscience and Remote Sensing},
  volume={61},
  pages={1--16},
  year={2023},
  publisher={IEEE}
}
-->
