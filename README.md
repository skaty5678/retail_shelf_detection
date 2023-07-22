# Retail Shelf Prediction

## Introduction
Fast-Moving Consumer Goods (FMCG) brands seek insights into retail shelves to enhance their sales performance. One crucial aspect is understanding the presence of their products compared to competitors' products on retail store shelves. This requires determining the total number of products present on each shelf in a store.

## Dataset Preparation

I leveraged the Grocery dataset, thanks to the repository https://github.com/gulvarol/grocerydataset, which provided the necessary dataset. (for dataset details, please refer to the provided link).

For effective model training and evaluation, I employed Roboflow, which provided the platform for data annotation, data augmentation and train-validation-test splits within the Google Colab environment. The applied data augmentation techniques included:
* Bounding Box Flip: Horizontal, Vertical
* Bounding Box Rotation: -15° to +15°
* Bounding Box Shear: ±15° Horizontal, ±15° Vertical
* Bounding Box Exposure: -25% to +25%

## Utilizing YOLOv8 Model

To achieve cutting-edge performance, I employed the latest YOLOv8 model by Ultralytics. YOLOv8 represents the state-of-the-art in object detection, building upon the success of previous YOLO versions.

## Overcoming Challenges

During the project, I encountered a challenge related to evaluating test performance and obtaining precision, recall, and mAP metrics. As YOLO lacked the specific tools for this task, creatively tweaked the YAML file to overcome this hurdle.

## Result Summary

I saved the results for each test image's total bounding boxes in the image2products.json file, providing a comprehensive overview of product counts per shelf. Additionally, I stored the test metrics in the results.json file, offering valuable insights into the model's performance.

## Conclusion

While the YOLOv8 model has demonstrated efficient performance in retail shelf prediction,
I also acknowledge that there is always room for improvement. Future endeavours may explore further fine-tuning,
advanced architectural modifications, and incorporation of cutting-edge techniques to enhance accuracy and predictive capabilities.

In conclusion, the work focuses on empowering FMCG brands with crucial shelf insights, helping them optimize product placement
and enhance sales strategies. The approach, using the latest YOLOv8 model and advanced data augmentation, ensures accurate
predictions and valuable performance metrics for retail shelf prediction, while also acknowledging the scope for continuous
improvement in the field of object detection and computer vision.
