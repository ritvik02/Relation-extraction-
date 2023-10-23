# Relation-extraction-
At the start of my internship, I was provided with a clinical dataset which had 2 columns which corresponded to 2 concepts and another column which corresponds to the relation between the 2 concepts. The task was to build a model that could extract the relation between any 2 concepts. So I basically treated it as a next word prediction problem where the 2 concepts are given to the model and the model predicts the corresponding relation. However, after doing EDA, I found out that the data was highly imbalanced which hampered the ability to achieve great performance on this data.

Overview of my approach to tackle imbalance

To tackle the problem of this imbalanced data I used sampling techniques to give
equal representation to each of the classes. I did Oversampling, Undersampling,
Synthetic minority oversampling (SMOTE) and Machine Translation. With
oversampling I was able to increase the number of samples of the minority classes
and with undersampling I reduced the number of samples of the majority classes.
By applying SMOTE I was able to generate synthetic samples of the minority
classes to make the number of samples of the minority classes equal to the majority
classes. While these techniques helped, I decided to go a step further and try
Machine translation to generate more samples of the minority classes. In this
approach I converted a datapoint corresponding to the minority classes to French or
any other language and then converted these back to English. This text was then
appended as an additional datapoint to the dataset. Similarly, it was carried out for
all datapoints corresponding to the minority class.
