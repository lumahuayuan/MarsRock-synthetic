# SynMars-TW

We release **SynMars-TW**, an all-terrain synthetic dataset for Martian objects segmentation. It is an extension of our previous [SynMars](https://github.com/CVIR-Lab/SynMars) <sup>[1]</sup> dataset and contains 8 categories: big rock, small rock, gravel, bedrock, ridge,sand, soil and sky, all of which are labeled regardless of size, helping to more accurately assess the robustness of various segmentation methods. Currently, SynMars-TW has a total of 21,000 labeled images with a resolution of 512 × 512 available for experiments. We divided them into 17,000 images for training, 2,000 for validation and 2,000 for testing. It was collected from a simulation environment generated by [Blender](https://wiki.blender.org/wiki/Main_Page), an open source and versatile 3-D computer graphics software allowing users to create and arrange 3-D objects. 
<div align=center>
  <img src=https://github.com/lumahuayuan/SynMars/blob/SynMars-TW/IMG/rover.png width="60%" />
  <br>
  <strong> Fig.1. </strong>
  <em> (a) Overview of the SynMars-TW dataset. The colored lines represent different routes of the rover. (b) Percentage of pixels by category.</em>
</div>

The simulated environment is a Mars-like terrain with an area of 300 x 300 m that is populated by thousands of rocks. We built this terrain by referring to objects' distribution photographed by Zhurong rover. Currently, representative objects in scenes of the ZhuRong rover are small rocks. For object diversity, we added some new object categories drew from Curiosity rover as shown in Fig.2. Referring to the parameter settings of NaTeCam[^2] of the ZhuRong rover, with a distance of about 1.2 meters from the ground.
<div align=center>
  <img src=https://github.com/lumahuayuan/SynMars/blob/SynMars-TW/IMG/mars_contrast.png width="60%" />
  <br>
  <strong> Fig.2. </strong>
  <em> left subfigures of (a)-(d) are images taken by the Curiosity rover, and the right ones are some images from our SynMars-TW</em>
</div>

In each scene, the RGB imgae pairs with corresponding depth image pairs are drawn from the left and right virtual cameras as shown in Fig3. and therefore SynMars-TW can support downstream vision missions like Stereo Matching and 3D reconstruction, etc. The intrinsics and extrinsics of the camera were set according to those on the Zhurong rover such that the landform of SynMars-TW is closer to that of the TianWen-1 dataset. A sample with 8 categories is shown below.
<div align=center>
  <img src=https://github.com/lumahuayuan/SynMars/blob/SynMars-TW/IMG/reverse_9_0053_l_image.png width="25%" />
  <img src=https://github.com/lumahuayuan/SynMars/blob/SynMars-TW/IMG/reverse_9_0053_l_mask.png width="25%" />
  <img src=https://github.com/lumahuayuan/SynMars/blob/SynMars-TW/IMG/reverse_9_0053_l_depth.png width="25%" />
  
  <img src=https://github.com/lumahuayuan/SynMars/blob/SynMars-TW/IMG/reverse_9_0053_r_image.png width="25%" />
  <img src=https://github.com/lumahuayuan/SynMars/blob/SynMars-TW/IMG/reverse_9_0053_r_mask.png width="25%" />
   <img src=https://github.com/lumahuayuan/SynMars/blob/SynMars-TW/IMG/reverse_9_0053_r_depth.png width="25%" />
  <br>
  <strong> Fig.3. </strong>
  <em> left to right: stero images and corresponding masks as well as the depth imags in SynMars-TW dataset</em>
</div>

Limited by the file size, we temporarily release 70 samples for the training set and 10 samples for both the validation and test sets. 
Currently, you can download **SynMars-TW** by the following ways, we will soon release more efficient ways to get them.


[**SynMars-TW**:](http://gofile.me/6V28a/PhCZj11Vd) or by [Baidu Cloud](https://pan.baidu.com/s/1i8sIwIkErI8edqrqcUANzQ) with passcode: **sytw**


If you use **SynMars-TW** for your research, please cite all the following papers：
```
@article{xiong2024light4mars,
  title={Light4Mars: A lightweight transformer model for semantic segmentation on unstructured environment like Mars},
  author={Xiong, Yonggang and Xiao, Xueming and Yao, Meibao and Cui, Hutao and Fu, Yuegang},
  journal={ISPRS Journal of Photogrammetry and Remote Sensing},
  volume={214},
  pages={167--178},
  year={2024},
  publisher={Elsevier}
}

@article{xiong2023marsformer,
  title={Marsformer: Martian rock semantic segmentation with transformer},
  author={Xiong, Yonggang and Xiao, Xueming and Yao, Meibao and Liu, Haiqiang and Yang, Hong and Fu, Yuegang},
  journal={IEEE Transactions on Geoscience and Remote Sensing},
  year={2023},
  publisher={IEEE}
}
```


**Reference**  

[1] Xiong, Y., Xiao, X., Yao, M., Liu, H., Yang, H., & Fu, Y. (2023). MarsFormer: Martian Rock Semantic Segmentation with Transformer. IEEE Transactions on Geoscience and Remote Sensing. 61,1-16.
[^2]: To get a larger percentage of each type of target in each image, we increase the focal length.
