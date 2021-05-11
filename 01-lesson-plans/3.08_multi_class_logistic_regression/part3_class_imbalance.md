# Introducing class imbalance

## Learning goals and implementation
In this section, we will increase the complexity of multi-class classification by introducing class imbalance. 
Students will learn why accuracy alone is insufficient to evaluate the performance of a classifier, and will become familiar with
other metrics (specifically precision, recall, and F1). 

This will be a combination of a mini lecture, a mini lab, and a discussion.

---

### Mini lecture

---

### Mini lab

The following notebook is meant to guide the students through multi-class classification with class imbalance:

XXXXX LINK TO NOTEBOOK XXXXX

**DATA**
In this part of the lesson we'll build our own datasets using `sklearn`'s `make_classification`. This is a very useful function that will allow students
to easily explore the effects of various dataset properties on the problem of class imbalance (they can change the dataset size, number of features and classes, 
usefulness of features, distinctness of classes, how noisy the class assignments are, how imbalanced the data are, etc etc). Playing around with the different
settings and creating a variety of increasingly complex datasets will help solidify the issue of class imbalance and also serve as a hopefully-smooth transition 
to the real-world dataset that they'll use in the next part of the lesson.

---

### Wrap-up discussion
1. As classes become *more* imbalanced, describe how the challenge of modeling a dataset evolves 
(i.e., does increasing class imbalance make things more or less difficult?)
2. What about as the classes become more similar (in feature space)? Does the size of the dataset matter? What about the relevance of the features?
