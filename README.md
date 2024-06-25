## Dataset
A Dataset to train the few-shot pose classification model was derived from the publicly available datasets. We prepared a custom yoga pose dataset using publicly available datasets: Yoga Poses Dataset[28] and Yoga Postures Dataset[29]. The dataset we derived contains 20 yoga poses as classes. There, we split the dataset into two sets, such as 15 classes for the train set and 5 poses for the test set. Each class contains 45-55 instances.



## Pose Classification Model Development
The proposed methodology consists of two models: the pose estimation and classification models. The pose estimation model is used to obtain the
location of human body keypoints from a given image, and the pose classification model is used to classify poses using a given keypoint location set. 

After completing a comprehensive analysis, it was concluded that the Movenet Thunder model is to be used as the pose estimation model for our approach based on the comparison of some state-of-the-art pose estimation models.
First we obtained the keypoint locations for each image in our custom dataset using the Movenet Thunder model and then trained our Few shot pose classifier using those keypoint locations. The colab notebook to get keypoint locations for images is in the [this notebook](https://github.com/VisionPro19/Model/blob/main/convert_images_to_keypoints.ipynb) and the Few-shot pose classifier implementation using the Prototypical Network can be found in [this notebook](https://github.com/VisionPro19/Model/blob/main/new_few_shot_pose_classifier_PN_using_keypoints_TFLite.ipynb).


