<a href="https://github.com/MustafaKhan670093/Lane-And-Road-Detection-Research#lane-detection-research--autoronto-">
    <img src="Images/logo.png" alt="aUToronto" title="aUToronto" align="right" height="100" />
</a>

# Pedestrian Detection Research🚶| aUToronto 🚙

## Introduction

The focus of this research project is to develop the pedestrian detection capabilities of Zeus, the self driving car at aUToronto. As a member of the Perception Team at aUToronto I work to meet the milestone goals set by my team leads and the advising professors including but not limited to [Dr. Angela Schoellig](https://www.dynsyslab.org/prof-angela-schoellig/) and [Dr. Tim Barfoot](http://asrl.utias.utoronto.ca/~tdb/) from the University Of Toronto. 

My task along with [Brian Cheong](https://www.google.com/url?sa=i&url=https%3A%2F%2Fca.linkedin.com%2Fin%2Fbrian-cheong-36444517a&psig=AOvVaw3Qyh7_xY9BiQ8tx7N50ZXn&ust=1616559669719000&source=images&cd=vfe&ved=0CA0QjhxqFwoTCJju7ZjIxe8CFQAAAAAdAAAAABAD) and [Davendra Maharaj](https://www.linkedin.com/in/davendra-seunarine-maharaj-218023152/?originalSubdomain=ca) was to improve Zeus's existing pedestrian detection system which was based off of Squeezdet and replace it with a YoloV3 model with newly trained weights and fine tuned hyperparameters. [YoloV3](https://arxiv.org/pdf/1804.02767.pdf) is the latest variant of a popular object detection algorithm YOLO – You Only Look Once. It is extremely powerful and useful for real time object detection tasks and so was employed for the purpose of pedestrian detection in this project.

## Summary Of Results

These are some of the trials with the best results. Code and specific hyperparameters to be shared here once I get approval about what can and can't be made open source. Since we are currently still competing with our car in the SAE Autodrive Challenge, this may take some time. Thanks for understanding!

| Dataset     | Hyperparameters | Max mAP       |
|  :----:     |    :----:       |   :----:      |
| JAAD        |     ...         |   83.70%      |   
| JAAD        |     ...         |   81.30%      |
| JAAD+Scale  |     ...         |   83.58%      |    
| JAAD+Scale  |     ...         |   83.23%      |   
| JAAD+NuScenes+Scale  |     ...         |   78.97%      |  


## YoloV3 Model In Action

These are some videos of a test run of these trained models on Zeus, our self driving car at the University of Toronto Institute for Aerospace Studies (UTIAS). The videos were taken by the blackfly cameras on Zeus.

<p align="center">
  <img src="Images/blackfly_image_color_compressed_yolov3_inference.gif" alt="GSCNN" title="GSCNN" height="300" />
</p>

The trained YoloV3 model detects pedestrians well, however, there are false positives on dark objects in the white snow and it qualitatively appears as if detection performance is less confident on objects that are far away.

<p align="center">
  <img src="Images/blackfly_image_color_compressed_yolov3_inference_2.gif" alt="GSCNN" title="GSCNN" height="300" />
</p>


Additionally, it appears as if the recall is quite good, however, the precision suffers in cases where the model classifies the dummy of the deer as a pedestrian.

<p align="center">
  <img src="Images/blackfly_image_color_compressed_yolov3_inference_3.gif" alt="GSCNN" title="GSCNN" height="300" />
</p>
