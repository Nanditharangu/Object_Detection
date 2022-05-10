# Object_Detection

This project is focused towards creating an Object detection model by use of Transfer learning, to detect user-defined categories. A pretrained [SSD MobileNet V2 FPNLite 320x320 model](<https://github.com/tensorflow/models/blob/master/research/object_detection/configs/tf2/ssd_mobilenet_v2_fpnlite_320x320_coco17_tpu-8.config>), provided by [TensorFlow 2 Detection Model Zoo](<https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md>) has been retrained on a dataset comprising 4 characters belonging to anime Naruto. 
And the trained model was successful in detecting all 4 categories with confidence > 90% for each.

![result](https://user-images.githubusercontent.com/98893548/161387474-ff1ff949-2ffc-4f63-9360-4d925f7c6057.jpg)

The model was pre-trained on [COCO 2017 dataset](<https://cocodataset.org/#home>) which contains 118K training and 41K test images with 90 object classes, thus achieving COCO mAP of 22.2 %

This model is then retrained on a dataset of 60 training & 4 test samples for 2000 steps. The loss & learning rate graphs are shown below. Here the total loss metric has 3 components, viz. classification loss, localization loss & regularization loss.

![image](https://user-images.githubusercontent.com/98893548/161675365-4d36ea05-745f-4b3b-965b-f1d057e367d1.png) ![image](https://user-images.githubusercontent.com/98893548/161675394-320afb44-f542-42ab-9c23-74da3ded6ee9.png)

The resultant model has average precision & average recall (averaged over IoU ∈ [0.5,1.0]) of 0.775 & 0.775

![image](https://user-images.githubusercontent.com/98893548/161675426-9505da7b-f59a-44ae-8600-d3ff3e520eb8.png) ![image](https://user-images.githubusercontent.com/98893548/161675449-1baa3a67-0556-405a-ae43-6ba2ed119f7f.png)
