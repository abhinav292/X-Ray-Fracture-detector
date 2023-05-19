# X-Ray-Fracture-detector
X-Ray Fracture detector

The proposed model consists of three phases: Phase 1, Phase 2, and Phase 3.

Phase 1:

In this phase, the script performs various image processing operations on a set of input images. It
utilizes the OpenCV library to apply different filters and edge detection techniques to the images.
The processed images are saved in separate output folders. The script also calculates the Peak
Signal-to-Noise Ratio (PSNR) values for different combinations of processed images. PSNR is a
metric used to measure the quality of an image compared to its original version. The PSNR values
are printed as output, and the processed images can be displayed using the OpenCV imshow
function (commented out in the code).

Phase 2:

In this phase, the script focuses on machine learning and deep learning techniques for bone fracture
detection. It assumes the presence of two folders: one containing fractured bone X-rays and another
containing non-fractured bone X-rays. The script uses the scikit-learn library to train a random
forest classifier on features extracted from the images. Additionally, it creates a deep learning
model using the TensorFlow-Keras library, consisting of convolutional and pooling layers. The
deep learning model is trained using the provided dataset. Finally, an AdaBoost classifier is trained
on the combined predictions of the random forest classifier and the deep learning model.

Phase 3:

This phase involves building a graphical user interface (GUI) application using the Tkinter library.
The GUI allows users to upload an image and classifies it as "Fractured" or "Not Fractured" using
the trained ensemble model from Phase 2. The selected image is displayed in the GUI, and the
classification result is shown below the image.
Overall, the proposed model combines image processing techniques, machine learning algorithms,
deep learning models, and a user-friendly GUI to detect bone fractures based on X-ray images.

How our proposed model is better than other models

The proposed approach combines multiple techniques to detect bone fractures, including image
processing techniques and machine learning algorithms. Here are some reasons why this
approach can be beneficial compared to other models used in the industry:
1. Feature extraction: The approach applies various image processing techniques such as
Gaussian blur, median blur, Sobel, Prewitt, Laplace, and Canny edge detection. These
techniques help in extracting relevant features from the bone X-ray images that can indicate
the presence of fractures. By incorporating multiple techniques, the model can capture
different aspects of the fractures, leading to more accurate detection.
2. Ensemble learning: The approach uses ensemble learning, specifically AdaBoost, to
combine the predictions of multiple classifiers. It combines the predictions of base
classifiers, such as Random Forests, with predictions from a deep learning model. Ensemble
learning has been proven to improve classification accuracy by leveraging the strengths of
multiple models. By combining the predictions, the model can make more robust and
accurate fracture predictions.

3. Data augmentation: The approach uses data augmentation techniques during the training
phase, such as rotation, shifting, zooming, and flipping. Data augmentation helps in
increasing the diversity of the training data, which can improve the model's ability to
generalize and make accurate predictions on unseen bone X-ray images. It also helps in
reducing overfitting, which is a common challenge in machine learning models.
4. End-to-end learning: The deep learning model in the approach is trained end-to-end,
meaning it learns the relevant features directly from the raw input images. This eliminates
the need for handcrafted feature extraction, which can be subjective and time-consuming.


The model learns to automatically extract discriminative features from the bone X-ray
images, potentially capturing subtle patterns or characteristics associated with fractures that
may not be easily identifiable by manual feature extraction methods.
5. Flexibility and adaptability: The proposed approach can be easily modified or extended to
incorporate additional techniques or algorithms. For example, if new image processing
techniques or deep learning architectures are developed or discovered, they can be
integrated into the approach to further improve fracture detection. This flexibility allows the
model to adapt to new advancements in the field and potentially achieve better performance
over time.

It's important to note that the effectiveness of any model or approach depends on various
factors, including the quality and size of the dataset, the choice of algorithms and techniques,
and the evaluation metrics used. The proposed approach offers a combination of techniques that
can potentially enhance fracture detection accuracy, but further validation and comparative
studies would be necessary to determine its superiority over other models used in the industry
