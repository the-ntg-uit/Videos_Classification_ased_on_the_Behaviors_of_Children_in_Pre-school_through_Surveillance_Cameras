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

## Cite

Nguyen, T.G.T., Do, P.P.T., Cao, D.D.N., Nguyen, H.M.T., Ngo, H.T., Do, TH. (2023). Video Classification Based on the Behaviors of Children in Pre-school Through Surveillance Cameras. In: Dao, NN., Thinh, T.N., Nguyen, N.T. (eds) Intelligence of Things: Technologies and Applications. ICIT 2023. Lecture Notes on Data Engineering and Communications Technologies, vol 188. Springer, Cham. https://doi.org/10.1007/978-3-031-46749-3_5


## Contact
### Authors:
Nguyen Tran Gia The, Do Pham Phuc Tinh,  Cao Dinh Duy Ngoc, Nguyen Huu Minh Tam, Ngo Huynh Truong.

Faculty of Information Science and Engineering, University of Information Technology, Ho Chi Minh City, Vietnam

Vietnam National University, Ho Chi Minh City, Vietnam

{20521940, 20522020, 20521661, 20521871, 20522085}@gm.uit.edu.vn
