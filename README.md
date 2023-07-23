# Facial-Expression-Recognition
---
## Introduction:
The project aimed to develop an accurate model for accurately classifying images into emotion categories. This report outlines the approach taken, the dataset used, the methodology employed, and the results obtained.

## Dataset:
The dataset used for this project consisted of images categorized into multiple classes. Upon analysis, it was observed that the dataset was imbalanced, with some classes having significantly fewer samples than others. To address this issue, data augmentation techniques were applied to generate additional images for the underrepresented classes. This resulted in a balanced dataset with an equal number of samples per class (8989). The augmented dataset was then saved in a CSV file for further use.
Counts of images corresponding to each class – 

<table>
 <thead>
  <th>Class</th>
  <th>Counts</th>
 </thead>
 <tbody>
  <tr>
   <td>
    0 : anger
   </td>
   <td>
   	 4953
   </td>
  </tr>
 <tr>
   <td>
    1 : disgust
   </td>
  <td>
    	547
   </td>
 </tr>
 <tr>
   <td>
    2 : fear
   </td>
  <td>
    5121
   </td>
 </tr>
 <tr>
   <td>
    3 : happiness

   </td>
   <td>
    8989
   </td>
 </tr>
 <tr>
   <td>
    4 : sadness
   </td>
  <td>
    6077
   </td>
 </tr>
  <tr>
   <td>
    5 : surprise
   </td>
    <td>
    4002
   </td>
 </tr>
  <tr>
   <td>
      6 : neutral
   </td>
    <td>
      6198
   </td>
 </tr>
 </tbody>
</table>

## Methodology:
Three machine learning models were selected for evaluation: VGG19 with transfer learning, a deep convolutional neural network (CNN), and the Vision Transformer (ViTb16) model. These models were chosen based on extensive research and their proven effectiveness in image classification tasks.

### Model 1: VGG19 with Transfer Learning:
The VGG19 model was utilized with transfer learning, leveraging pre-trained weights from the ImageNet dataset. The top layers of the model were fine-tuned to adapt to this specific classification task. Hyperparameter tuning techniques were applied to optimize the performance of the model. The resulting model achieved an overall testing accuracy of 69%.

#### VGG19  (Without Hyperparameter Tuning):

##### 1. Accuracy and Loss Graphs
![VGG19](https://github.com/sharma-prerna/Facial-Expression-Recognition/blob/main/vgg19_without_hyperparameter_tuning_loss_acc_graph.png)

##### 2. Confusion Matrix
![VGG19](https://github.com/sharma-prerna/Facial-Expression-Recognition/blob/main/vgg19_without_hyperparameter_tuning_conf_mat.png)

#### VGG19 ( With Hyperparameter Tuning):

##### 1. Accuracy and Loss Graphs
![VGG19](https://github.com/sharma-prerna/Facial-Expression-Recognition/blob/main/vgg19_with_hyperparameter_tuning_loss_acc_graph.png)
 
##### 2. Confusion Matrix
![VGG19](https://github.com/sharma-prerna/Facial-Expression-Recognition/blob/main/vgg19_with_hyperparameter_tuning_conf_mat.png)

### Model 2: Deep Convolutional Neural Network (CNN):
A deep CNN architecture with 8 layers was designed and implemented. The model was trained on the balanced dataset, both with and without hyperparameter tuning. Surprisingly, the model without hyperparameter tuning performed better, achieving an overall testing accuracy of 70%. 

#### Deep Convolutional Neural Network ( Without Hyperparameter Tuning):

##### 1. Accuracy and Loss Graphs
![CNN](https://github.com/sharma-prerna/Facial-Expression-Recognition/blob/main/cnn_without_hyperparameter_tuning_loss_acc_graph.png)
 
##### 2. Confusion Matrix
![CNN](https://github.com/sharma-prerna/Facial-Expression-Recognition/blob/main/cnn_without_hyperparameter_tuning_conf_mat.png)

#### Deep Convolutional Neural Network ( With Hyperparameter Tuning):
 
##### 1. Accuracy and Loss Graphs
![CNN](https://github.com/sharma-prerna/Facial-Expression-Recognition/blob/main/cnn_with_hyperparameter_tuning_loss_acc_graph.png)

##### 2. Confusion Matrix
![CNN](https://github.com/sharma-prerna/Facial-Expression-Recognition/blob/main/cnn_with_hyperparameter_tuning_conf_mat.png)

### Model 3: Vision Transformer (ViTb16):
The Vision Transformer model, with pre-trained weights from the ViTb16 architecture, was employed for face expression classification. However, due to time constraints, hyperparameter tuning was not performed on this model. As a result, the testing accuracy achieved was relatively lower at 62%.

#### Vision Transformer - ViTB16:

##### 1. Accuracy and Loss Graphs
![Vit](https://github.com/sharma-prerna/Facial-Expression-Recognition/blob/main/vit_without_hyperparameter_tuning_loss_acc_graph.png)
 
##### 2. Confusion Matrix
![Vit](https://github.com/sharma-prerna/Facial-Expression-Recognition/blob/main/vit_without_hyperparameter_tuning_conf_mat.png)

## Conclusion:
In conclusion, this project successfully addressed the issue of data imbalance by applying data augmentation techniques. Through the implementation and evaluation of three different models, including VGG19 with transfer learning, a deep CNN, and the Vision Transformer, valuable insights were gained. The best-performing models were VGG19 with hyperparameter tuning (69% accuracy) and the deep CNN without hyperparameter tuning (70% accuracy). 

## Future Work:
Future work may involve further exploration of hyperparameter tuning for the Vision Transformer model, as well as the investigation of other advanced architectures and techniques in image classification. Additionally, ensemble methods or model stacking could be explored to further boost the performance and generalization of the models.






