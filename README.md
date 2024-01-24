# Diabetic-Retinopathy-Detection
Diabetic Retinopathy, a vision-threatening condition in diabetes, requires early detection. The task involves predicting severity classes (Normal to Proliferative) from fundus photographs. Developing an accurate model is crucial for timely intervention and vision preservation.

![image](https://github.com/b-kashyap/Diabetic-Retinopathy-Detection/assets/155677382/2d5bfb2b-2515-477b-8271-883ca38c3b40)

## Technologies and Libraries Used:
1. PyTorch: PyTorch is chosen for its flexibility and ease of use in building and training neural network models for image classification tasks.<br>
2. Torchvision: Utilized for pre-trained models and image transformation utilities.<br>
3. Matplotlib: Employed for visualizing data distributions and training/validation loss graphs.<br>
4. Pandas and NumPy: Used for data manipulation and handling.<br>
5. PIL (Python Imaging Library): Utilized for working with image files.<br>

## Dataset:
The dataset is sourced from Kaggle, specifically from the APTOS 2019 Blindness Detection competition.It consists of fundus photographs used for diagnosing diabetic retinopathy.
The dataset is split into training and testing sets, with labels representing the severity of diabetic retinopathy.

## Model Architecture:
Transfer learning is employed using a pre-trained ResNet-34 model.
The final layer of ResNet-34 is replaced with four new layers for predicting five severity classes (Normal, Mild, Moderate, Severe, Proliferative).

## Training and Evaluation:
1. The dataset is preprocessed using data augmentation techniques, and class weights are calculated to address imbalances. <br>
2. The model is trained using Stochastic Gradient Descent (SGD) with CrossEntropyLoss and class weights. <br>
3. Training and validation are conducted for 30 epochs, with periodic evaluation of losses and accuracies. <br>
4. The training and validation losses are plotted against the number of epochs. <br>

## Results:
The model achieves increasing accuracy on both the training and validation sets over epochs.
Validation accuracy reaches approximately 82.22% after 30 epochs.
The trained model is used to predict labels for the test set, completing the testing phase.

## Future Scope

Further improvement can be achieved by increasing the dataset size, exploring more complex model architectures, or utilizing ensemble models.
Hyperparameter tuning and fine-tuning the model on additional diabetic retinopathy datasets can enhance performance.
Continuous monitoring and updating of the model with new data can improve its generalization to diverse cases.
