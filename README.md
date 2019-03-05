# METU-ALET: A Dataset for Tool Detection in the Wild
ALET is an abbreviation for Autameted Labeling of Equipment and Tools. In Turkish, it also stands for the word “tool”.

METU-ALET is an image dataset for the detection of the tools in the wild. We provide an extensive dataset in order to detect tools that belongs to the categories such as farming, gardening, office, stonemasonry, vehicle, woodworking and workshop. The images in the dataset contains a total of 15612 bounding boxes and 53 different tool categories.  

<!--Please visit ____ for more information on the METU-ALET dataset including the data and the paper.-->

## METU-ALET Dataset at a Glance
Most of the scenes that reside in the dataset are not generated or constructed; they are snapshots of existing environments with or without humans using the tools. The rest of the scenes are generated; therefore, these scenes are considered as synthetic data.

The images that reside in the METU-ALET dataset can be split into three categories: 

### 1) Downloaded and Crawled Data
These are the images that are downloaded and crawled from the Internet. The websites that are used to gather the images are the following: Creativecommons, Wikicommons, Flickr, Pexels, Unsplash, Shopify, Pixabay, Everystock, Imfree. It should also be noted that while crawling and downloading images from these websites, license issues had also been considered. Therefore, we have only taken the royalty-free images from these websites. These type of images in the dataset contains 9262 bounding boxes.

<table>
  <tr>
    <td><img src="data/samples/flickr_stonemasonry3.jpg" height="250"/></td>
    <td><img src="data/samples/wikimgs_vehicle10.jpg" height="250"/></td>
    <td><img src="data/samples/m_flickr_workshop6.jpg" height="250"/></td>
    <td><img src="data/samples/m_flickr_workshop171.jpg" height="250"/></td>
  </tr>
</table>

### 2) Photographed Data
These are the images that are photographed by ourselves that are mostly consisting of office and workshop scenes. The images in the METU-ALET dataset contains 820 bounding boxes related to this type of data.

<table>
  <tr>
    <td><img src="data/samples/mixed0.jpg" height="250"/></td>
    <td><img src="data/samples/mixed8.jpg" height="250"/></td>
    <td><img src="data/samples/mixed12.jpg" height="250"/></td>
    <td><img src="data/samples/mixed17.jpg" height="250"/></td>
  </tr>
</table>

### 3) Synthetic data
The images that are called synthetic are the ones that are generated by us. In order to construct synthetic data, we have first  photographed several background images that belongs to different contexts. Then, for each class of tools, we have downloaded royalty-free transparent images, performed a set of random transformations on them, and finally, placed these transparent images of tools on top of the background images. In the METU-ALET dataset, the scenes that are considered as synthetic data contains 5530 bounding boxes.

## Why need METU-ALET dataset?
Through the recent advancements in the field of robotics, we have come to a point where humans and robots will be performing tasks in a collaborative manner. By the help of this dataset, we aim to solve the object detection tasks where robots will be able to detect tools that can be grabed or carried by them. As the definition of a tool is too broad, it had been decided to consider only the tools for the dataset which can be manipulated by the robots.

## The Aim of the METU-ALET dataset
As the datasets that are used in the field of robotics consider only a limited number of categories and instances, and they mainly focus on detection of tool affordances, they are not suitable for training a deep object detector. With METU-ALET, we introduce a dataset which consists of real-life scenes where the tools are unorganized as much as possible, and where the tools can be found in their natural habitat or while humans are using them.

The scenes that we consider also introduce several challenges for the object detection task, such as including the small scale of the tools, their articulated nature, occlusion and inter-class invariance.

## Annotated Samples
<table>
  <tr>
    <td><img src="data/samples/BB_1279041211_1dbc1e1473_z.jpg" height="250"/></td>
    <td><img src="data/samples/BB_380109183_decc403e84_z.jpg" height="250"/></td>
    <td><img src="data/samples/BB_2168968825_0c83b42dfb_z.jpg" height="250"/></td>
    <td><img src="data/samples/BB_m_flickr_gardening7.jpg" height="250"/></td>
  </tr>
</table>

## Tool Detection with Deep Networks

For tool detection in the wild, we trained several state of the art deep object detectors, namely, <a href="https://arxiv.org/abs/1506.01497">Faster R-CNN</a>, <a href="https://arxiv.org/abs/1512.02325">SSD</a>, <a href="https://arxiv.org/abs/1506.02640">YOLO</a> and <a href="https://arxiv.org/abs/1708.02002">RetinaNet</a>. The following table summarizes the mAP results for each one of the deep object detectors.


<!--| Faster-RCNN | YOLO | RetinaNet |
| --- | --- | --- |
| 0.52 | 0.61 | 0.53 |-->

## “Wearing Helmet?”: A Critical and Practical Usage of the METU-ALET Dataset

“Wearing Helmet?” is a usecase for METU-ALET, through which we are able to judge the safeness of the enviroments where the robots and humans work collaboratively. As the dataset contains 1037 instances of safety helmet, this information is used in order to train a tool detector and a human detector & pose estimator. By the help of these detectors, the robots are able to determine whether the human in the scene wears a safety helmet or not. Therefore, problems related to the safety issues in critical scenes can be solved accordingly.

<p float="left">
  <img src="data/samples/wikimgs_construction103.jpg" width="400"/> 
  <img src="data/samples/wikimgs_construction108.jpg" width="400"/>
</p>

## Citation

If you use the METU-ALET dataset or the related resources shared here, please cite the following work:
<pre>
@article{KurnazEtAl2019,
    author = {Kurnaz, F. C. and Hocaoglu, B. and Yilmaz, K. M. and Sulo, I. and Kalkan, S.},
    title = {ALET (Automated Labeling of Equipment and Tools): A Dataset, a Baseline and a Usecase for Tool Detection in the Wild},
    journal = {arxiv preprint},
    year = {2019}
}
</pre>

## Contact

For questions or comments please contact Sinan Kalkan at skalkan [@] ceng.metu.edu.tr or visit http://kovan.ceng.metu.edu.tr/index.php/Main_Page.
