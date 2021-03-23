<a href="https://github.com/MustafaKhan670093/Lane-And-Road-Detection-Research#lane-detection-research--autoronto-">
    <img src="Images/logo.png" alt="aUToronto" title="aUToronto" align="right" height="100" />
</a>

# Pedestrian Detection Research🚶| aUToronto 🚙

## Introduction

The focus of this research project is to develop the lane detection capabilities of Zeus, the self driving car at aUToronto. As a member of the Perception Team at aUToronto I work to meet the milestone goals set by my team leads and the advising professors including but not limited to Prof. Angela Schoellig and Prof. Tim Barfoot from the University Of Toronto.

My task was to improve upon the results of Zeus, whose current lane detection system runs on the [GSCNN](https://github.com/nv-tlabs/GSCNN), a powerful network architecture created by the Toronto Nvidia AI Lab. 

## Summary Of Results

These are some of the trials with the best results. Code and specific hyperparameters to be shared here once I get approval about what can and can't be made open source. Since we are currently still competing with our car in the SAE Autodrive Challenge, this may take some time. Thanks for understanding!
<center>
| Dataset     | Hyperparameters | Max mAP       | Precision On JAAD Valid. | Recall On JAAD Valid.  |
|  :----:     |    :----:       |   :----:      |        :----:            |          :----:        |
| JAAD        |     ...         |   83.70%      |        97.53%            |        83.89%          |      
| JAAD        |     ...         |   81.30%      |        98.34%            |        81.26%          |   
| JAAD+Scale  |     ...         |   83.58%      |        89.46%            |        83.98%          |      
| JAAD+Scale  |     ...         |   83.23%      |        93.84%            |        83.54%          |   
| JAAD+NuScenes+Scale  |     ...         |   78.97%      |        88.96%            |        79.51%          |   
</center>

## YoloV3 Model In Action

These are some videos of a test run of these trained models on Zeus, our self driving car at the University of Toronto Institute for Aerospace Studies (UTIAS). 

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
