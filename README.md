# Lateral-Movement-Detection-using-AutoEncoder
Lateral movement refers to a group of methods cyber criminals use to explore a network after initial access, to find vulnerabilities, escalate access privileges, and reach their ultimate target.  In this Project we used AutoEncoders to detect such attacks in LMD-2023 Dataset, which can be found here https://github.com/ChristosSmiliotopoulos/Lateral-Movement-Dataset--LMD_Collections.

The AE(AutoEncoder) was trained using the stratified k-fold Cross Validation, with a k=10. Precisely, each fold divided the total of the LMD-2023 dataset into 1,314,668 (75%) and 438,223 (25%) subcategories related to the training and testing tests, respectively.
An autoencoder is a type of artificial neural network used to learn efficient codings of unlabeled data (unsupervised learning). An autoencoder learns two functions: an encoding function that transforms the input data, and a decoding function that recreates the input data from the encoded representation. The autoencoder learns an efficient representation (encoding) for a set of data, typically for dimensionality reduction, to generate lower-dimensional embeddings for subsequent use by other machine learning algorithms. Stacked-autoencoder is a set of few autoencoders stacked together. In anomaly detection, AE is trained only on Normal data, and outliers are detected when its reconstructed error is big then a certain threshold.
![alt text](http://url/to/img.png)



























My code was based on this tutorial : [Analytics Vidhya](https://www.analyticsvidhya.com/blog/2022/01/complete-guide-to-anomaly-detection-with-autoencoders-using-tensorflow/) , using TensorFlow.

The ML technique training and testing details: 
Special reference should be made to the highly imbalanced nature of LMD-2023, as denoted here: 



Due to imbalance cause, the stratified k-fold Cross Validation, with a k=10 was applied to each model. Precisely, each fold divided the total of the LMD-2023 dataset into 1.314.668 and 438.223 subcategories related to the training and testing tests, respectively. This helps evaluate model performance more reliably than a single train or test split.
![alt text](http://url/to/img.png)


Results:
We the following results:
AUC	Accuracy	Precision	Recall	F1 Score
0.9940
	0.9919	0.9629	0.9392
	0.9482



