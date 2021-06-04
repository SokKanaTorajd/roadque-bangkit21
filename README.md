# RoadQue - Bangkit 2021 Capstone Project 0348

Steps in RoadQue-EDA(Exploratory Data Analysis):
1. download the datasets. (but there is some problems in annotations, so search for alternative source)
2. unpack the dataset. filter the images contain with the damaged road.
3. show some examples of images by creating the annotation for only several damages such as D00, D10, D20, and D40.
4. copy the new dataset and save into new tar.gz file (I named it 'data-train.tar.gz').

Steps in RoadQue-ML(Machine Learning):
1. Unpack data-train.tar.gz. and put it into images folder.
2. download the pretrained model. (I use SSD MobileNet V2 FPNLite 640x640, downloaded from <a href="https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md"> Detection Zoo Model</a>).
3. install protobufs and several libraries.
4. add python program to create TFRecord file. 
5. edit the pipeline.config from pretrained model (changed the num_classes, batch, steps, path_to_ckpt, path_to_tfrecord, path_to_label)
6. do the train. (right now there is a problem with the test set. annotation is missing or maybe it is never exist).

TO BE DONE:
- should split the data-train into train set and evaluation set.
- fixed the problem in the last training

NOTES:
- all the processes is executed in google colab, and the dataset and other files are stored in google drive.
