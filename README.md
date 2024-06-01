# Detection-Report-Generation-of-Brain-Tumors-using-Deep-Learning

# Problem Statement
The primary objective of this project is to develop a computer-aided diagnosis (CAD) system capable of automatically detecting the presence of brain tumors in medical images, such as MRI scans. The system can differentiate between tumor and non-tumor regions with high accuracy and also highlights the specific image regions critical for its diagnosis.

# Objectives
The main objectives of the project include:
- To explore and implement traditional machine learning algorithms, such as Support Vector Machines (SVM) and Random Forest, for brain tumor detection.
- To develop a Convolutional Neural Network (CNN) architecture tailored for brain tumor detection, leveraging deep learning techniques.
- To compare the performance of traditional machine learning algorithms and neural networks in terms of accuracy, sensitivity, specificity, and computational efficiency.
- To provide insights into the strengths and limitations of each approach and identify areas for further improvement.

# Model Development
- Support Vector Machine (SVM):
SVM is very useful since it can capture complex correlations between characteristics and tumor types because it can handle both linear and non-linear classification problems. We utilize the SVM algorithm for brain tumor classification based on the extracted features from MRI images.
- Random Forest Tree Algorithm:
Given that noisy and correlated characteristics are frequently found in medical imaging datasets like MRI pictures, Random Forest is especially useful. We employ the Random Forest algorithm for brain tumor classification based on the extracted features from MRI images.
- Convolutional Neural Network:
CNNs have proven to perform better in a variety of image identification tasks, which makes them a good option for classifying brain tumors from MRI scans. For brain tumor classification, we use a CNN architecture based on the EfficientNetB0 model in our implementation.

# Results and Analysis:
- Support Vector Machine:  
The performance of SVM was evaluated using accuracy, precision, recall, F1-score, and other relevant metrics. The overall accuracy of the model is 76% and it is fairly effective in detecting pituitary, glioma and no tumor with the precision at 82%. While it is less precise while detecting meningioma tumors with precision at 61%. Confusion matrices generated for SVM show high accuracy in detecting ‘notumor’ cases but it is showing confusion while differentiating between ‘glioma’ and ‘meningioma’ cases. ROC curves were used to check the effectiveness of the model in detecting the classes of brain tumors. The area under each class are glioma (0.83), meningioma (0.72), notumor (0.89) and pituitary (0.88), which indicate that there are still improvements required in the model for accurate detection of tumor categories.
- Random Forest:  
After evaluating the performance of the random forest model, we can observe that the overall accuracy of the model is 89% for detecting brain tumors. It shows high accuracy while detecting ‘notumor’ cases with the precision of 94%. It also shows high accuracy in detecting ‘pituitary’ tumors with the precision of 92%. But the model can still be improved for ‘glioma’ and ‘meningioma’ classes with precision of 89%
and 80% respectively. The confusion matrix for random forest also exhibits confusion between ‘glioma’ and ‘meningioma’ tumors as support vector machine. The ROC curve for random forest has also exhibited impressive results while distinguishing between different classes of tumor. The results of the random forest model shows that this is an accurate model for detecting the tumor and its types.
- Convolutional Neural Network:  
The performance of the Convolutional Neural Network was evaluated using accuracy and loss. Comparison between training and validation losses, and comparison between training and validation accuracies were conducted to gain further insights into the neural network's performance and behavior. The model showed a steady increase in training accuracy with each epoch, reaching a high of 0.95 by the final epoch. Training loss decreased significantly from 0.7136 in the first epoch to 0.1179 in the fifth epoch indicating effective learning and convergence of the model. Validation accuracy remained consistently high throughout training, peaking at 92.12% in the fourth epoch. Validation loss shows a decreasing trend over epochs reflecting the model’s ability to generalize well to unseen data. The confusion matrix for CNN also exhibits a high confusion between ‘glioma’ and ‘meningioma’ tumors.  
In addition to assessing the Convolutional Neural Network (CNN), Grad-CAM was utilized to highlight the important regions of the image helping in the detection process.
![image](https://github.com/SanchiSatam/Detection-Report-Generation-of-Brain-Tumors-using-Deep-Learning/assets/68892516/e8a01f9b-bef1-4fe1-8671-d0fc386773ad)  
Here, is it highlighting the important region of the image indicating that this part is responsible for the detection of a particular disease.
The CNN model along with Grad-CAM is highly effective in detecting brain tumor detection, considering its high accuracy and the ability to generalize from the training data to validation data. It can provide visualizations for the predicted results with explanations which makes it the most efficient model for medical diagnosis. The random forest model also exhibits high accuracy when it comes to accurate classification problems. While the SVM model can be useful, it still requires few improvements for accurate results.
