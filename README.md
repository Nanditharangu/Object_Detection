# Object_Detection

This project is focused towards creating an Object detection model by use of Transfer learning, to detect user-defined categories. A pretrained [SSD MobileNet V2 FPNLite 320x320 model](<https://github.com/tensorflow/models/blob/master/research/object_detection/configs/tf2/ssd_mobilenet_v2_fpnlite_320x320_coco17_tpu-8.config>), provided by [TensorFlow 2 Detection Model Zoo](<https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md>) has been retrained on a dataset comprising 4 characters belonging to anime Naruto. 
And the trained model was successful in detecting all 4 categories with an accuracy > 90% each.

![result](https://user-images.githubusercontent.com/98893548/161387474-ff1ff949-2ffc-4f63-9360-4d925f7c6057.jpg)

The model was pre-trained on [COCO 2017 dataset](<https://cocodataset.org/#home>) which contains 118K training and 41K test images with 90 object classes, thus achieving an mAP of 22.2.

This model is then retrained on a dataset of 60 training & 4 test samples for 2000 steps. The loss & learning rate graphs are shown below. Here the total loss metric has 3 components, viz. classification loss, localization loss & regularization loss.

![image](https://user-images.githubusercontent.com/98893548/161674680-71eef8e7-a529-4c9d-ab72-3f566b7380e7.png) ![image](https://user-images.githubusercontent.com/98893548/161674702-01b76784-8556-41c2-bf65-d6252b3b7d0a.png)

The resultant model has precision & recall values of 0.775 & 0.775 (these metrics can be optimised further if trained on larger dataset)

 ![image](https://user-images.githubusercontent.com/98893548/161674768-f92be30c-5f2b-4753-8d8b-50cc1e0326ff.png) ![image](https://user-images.githubusercontent.com/98893548/161674786-3bda596a-f7bd-4136-9428-92b1c3316c10.png)
