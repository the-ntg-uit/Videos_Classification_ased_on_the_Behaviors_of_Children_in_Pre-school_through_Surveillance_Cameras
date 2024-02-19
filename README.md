# Videos Classification based on the Behaviors of Children in Pre-school through Surveillance Cameras
By 
Nguyen Tran Gia The,
Do Pham Phuc Tinh, 
Cao Dinh Duy Ngoc,
Nguyen Huu Minh Tam, 
Ngo Huynh Truong, 
Do Trong Hop

## About
This paper has been published in ICIT 2023: Intelligence of Things: Technologies and Applications.
https://link.springer.com/chapter/10.1007/978-3-031-46749-3_5
## Abstract 
In preschool, children are active and curious about the world around them. The tendency to engage in unusual or dangerous behaviors can pose a significant risk to their safety. Constantly monitoring surveillance camera footage and analyzing it to determine if any abnormal behavior is occurring requires considerable attention and effort from human observers. Therefore, applying technology to monitor the abnormal behavior of children is crucial in preschool education settings. With the development of technology, the problem of classifying video through surveillance cameras can be solved. However, there is still a shortage of datasets for this task with video data in preschool environments due to difficulties in collecting data and potential violations of children’s privacy and safety. Therefore, in this paper, we propose Behaviors of Children in Preschool (BCiPS), a new dataset for the above problem. BCiPS consists of 4268 videos with lengths ranging from 3-6 seconds. We evaluate some machine learning and deep learning models on BCiPS. The CNN-LSTM model achieves the highest performance, over 75\%, with four performance metrics: accuracy, recall, precision, and F1_score. Additionally, we will analyze cases where the models fail to identify abnormal behavior to determine the reasons for these failures, identify weaknesses in the dataset, and improve the accuracy of the dataset to create a reliable tool for building an effective warning system in real-life situations.

## 1. The BCiPS dataset

### Dataset Creation
![dataset creation](https://github.com/the-ntg/Videos_Classification_based_on_the_Behaviors_of_Children_in_Pre-school_through_Surveillance_Cameras/assets/109457460/b1d0d9d7-fbe5-4f07-93ab-d079b2f31eef)
#### Phase 1. Data Collection and Pre-processing:
- **Data collection**: We describe creating the BCiPS dataset for human action classification in videos task. The dataset was created by collecting video footage from two surveillance cameras in two preschool classrooms. The cameras recorded the daily activities of students during various times of the day, including studying, entertaining, and napping. Careful consideration was given to ensuring the privacy and safety of the children. 
- **Data pre-processing**: Video data were collected in .dav format and then converted to .mp4 format using the web tool 123APPS 1. This format is widely used and easy to work with various tools. As the study focuses on human actions, we removed any periods when no students were in the classroom from the videos. Subsequently, we used the FFmpeg library provided by Python to split the videos into 3-6 seconds segments.

#### Phase 2. Guidelines and Agreement:
**Guidelines**: The purpose of the task is to classify whether the input video contains normal or abnormal actions. Therefore, the output will be one of two labels: "Normal" or "Abnormal". We define the labels as follows:
- **Abnormal**: Videos contain unusual and dangerous actions for children, such as fighting (children physically impact each other or play excessively, causing harm to other children), falling (falling on the ground suddenly), chasing (more than two students run fast, they run without a certain trajectory, make noise and may have an accident), carrying heavy or oversized objects (tables, chairs, beds, or similarly large-sized items can cause injury to children if they trip or if heavy objects fall on them), and other abnormal activities (other less common cases can still pose dangers to children). These actions can be dangerous, leading to injury and accidents or affecting the children's mental health.
- **Normal**: Videos contain actions that are not dangerous in the observed environment. For example, walking, talking, eating, playing, studying, ..., performed normally and regularly in a school or preschool domain. 

### Phase 3. Labeling and data splitting:
The inter-annotator agreement results for both Cohen's Kappa and Krippendorff measures were good, meeting the set requirements. Therefore, we proceeded to label the videos in our dataset. It is inevitable to encounter challenging and ambiguous cases during the labeling process. To address these issues, the annotators will have meetings to discuss and agree on how to label these problematic and ambiguous cases and update the guidelines to make them more complete. Following this process, we obtained a total of 4268 labeled videos. Finally, we split 4268 videos into three sets: training set, validation set (development set), and test set.

## 2. Model
- CNN+LSTM (ConvLSTM2D)
- CNN+SVM
- CNN+Random Forest
- TimeSformer
- MoViNets
- (2+1)D Resnet-18
- EfficientNetB0

## 3. Results
|      | accuracy | recall | precision | F1 |
|--------------|----------|----------|---------|---------|
| `CNN + LSTM` | `75.88` | `75.63` | `75.43` | `75.53` |
| Timesformer | 74.71 | 74.80 | 74.82 | 74.81 |
| CNN + RandomForest  | 74.00 | 73.97 | 73.98 | 73.98 |
| EfficientNetB0  | 73.30 | 73.48 | 73.70 | 73.59 |
| Movinet  | 70.02 | 69.61 | 71.30 | 70.44 |
| CNN + SVM  | 65.57 | 65.61 | 65.59 | 65.60 |
| (2+1)D Resnet-18 | 61.12 | 60.42 | 63.37 | 61.86 |

## BibTeX
```
@InProceedings{10.1007/978-3-031-46749-3_5,
author="Nguyen, Tran Gia The
and Do, Pham Phuc Tinh
and Cao, Dinh Duy Ngoc
and Nguyen, Huu Minh Tam
and Ngo, Huynh Truong
and Do, Trong-Hop",
editor="Dao, Nhu-Ngoc
and Thinh, Tran Ngoc
and Nguyen, Ngoc Thanh",
title="Video Classification Based on the Behaviors of Children in Pre-school Through Surveillance Cameras",
booktitle="Intelligence of Things: Technologies and Applications",
year="2023",
publisher="Springer Nature Switzerland",
address="Cham",
pages="45--54",
abstract="In preschool, children are active and curious about the world around them. The tendency to engage in unusual or dangerous behaviors can pose a significant risk to their safety. Constantly monitoring surveillance camera footage and analyzing it to determine if any abnormal behavior is occurring requires considerable attention and effort from human observers. Therefore, applying technology to moni- tor the abnormal behavior of children is crucial in preschool education settings. With the development of technology, the problem of classifying video through surveillance cameras can be solved. However, there is still a shortage of datasets for this task with video data in preschool environments due to difficulties in collecting data and potential violations of children's privacy and safety. Therefore, in this paper, we propose Behaviors of Children in Preschool (BCiPS), a new dataset for the above problem. BCiPS consists of 4268 videos with lengths ranging from 3--6 seconds. We evaluate some machine learning and deep learning models on BCiPS. The CNN-LSTM model achieves the highest performance, over 75{\%}, with four performance metrics: accuracy, recall, precision, and {\$}{\$}F1{\_}{\{}score{\}}{\$}{\$}F1score. Additionally, we will analyze cases where the models fail to identify abnormal behavior to determine the reasons for these fails- ures, identify weaknesses in the dataset, and improve the accuracy of the dataset to create a reliable tool for building an effective warning system in real-life situations.",
isbn="978-3-031-46749-3"
}
```


## Contact
### Authors:
Nguyen Tran Gia The, Do Pham Phuc Tinh,  Cao Dinh Duy Ngoc, Nguyen Huu Minh Tam, Ngo Huynh Truong.

Faculty of Information Science and Engineering, University of Information Technology, Ho Chi Minh City, Vietnam

Vietnam National University, Ho Chi Minh City, Vietnam

{20521940, 20522020, 20521661, 20521871, 20522085}@gm.uit.edu.vn
