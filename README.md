# Multilable Classification on Patent Application Dataset

This patent application classification has been performed to classify **subclass_labels** in the dataset. The dataset, I am using in this task contains 10,000 samples. The dataset has a wide hirarchy of of labels. E.g. a label **G06K9** has **G** as the section, **G06** as the class **G06K** as subclass and **G06K9** as a group<img src="https://latex.codecogs.com/gif.latex?^1" />. Classification on section would have a large number of labels therefore the task will become more complicated. To keep things simple, after looking at the amount of samples I am using (i. e. 10,000), I am performing the classification on only the sections. Therefore, We have 8 sections (labels) as [A, B, C, D, E, F, G, H]. There could be multiple sections assigned one row, hence the task becomes a **Multilabel Classification**. After chopping of the labels, in few samples, I was left with same labels repeated twice (e.g. [A, A]) for a row and I have removed them. I have made sure that the assigned labels are not repeated in row and all the labels are unique. 

**Baseline Model :** As per the requirement of the task, I have used Glove<img src="https://latex.codecogs.com/gif.latex?^2" /> pretrained embeddings of 100 sequences. 

**Pretrained Model :** I have chosen **BERT_base_uncased**<img src="https://latex.codecogs.com/gif.latex?^3" /> pretrained model. For fine tuning, I am using **keras-bert**<img src="https://latex.codecogs.com/gif.latex?^4" /> wrapper. 

**Dataset :** Dataset<img src="https://latex.codecogs.com/gif.latex?^4" /> was obtained in json format. I have converted the data from JSON to CSV on my local machine and uploaded it to the drive.

<img src="https://latex.codecogs.com/gif.latex?_1" /> [Storm Jr, Bruce H and Schultz, reservoir optimization utilizing neural networks](https://ecmlpkdd2019.org/downloads/paper/619.pdf)

<img src="https://latex.codecogs.com/gif.latex?^2" /> https://nlp.stanford.edu/projects/glove/

<img src="https://latex.codecogs.com/gif.latex?^3" /> https://github.com/google-research/bert



<img src="https://latex.codecogs.com/gif.latex?^4" /> https://pypi.org/project/keras-bert/
