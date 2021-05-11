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

#### DATA
In this part of the lesson we'll build our own datasets using `sklearn`'s `make_classification`. This is a very useful function that will allow students
to easily explore the effects of various dataset properties on the problem of class imbalance (they can change the dataset size, number of features and classes, 
usefulness of features, distinctness of classes, how noisy the class assignments are, how imbalanced the data are, etc etc). Playing around with the different
settings and creating a variety of increasingly complex datasets will help solidify the issue of class imbalance and also serve as a hopefully-smooth transition 
to the real-world dataset that they'll use in the next part of the lesson.

#### Flow of the lab
The first two sections - building and modeling balanced vs imbalanced datasets - are meant to be completed relatively quickly. The goal is mainly to set up a direct comparison between the types of datasets, and to provide some coding snippets that will be useful. To this end, most of the code has been provided and the students should spend more time thinking/discussing than coding.

The final section is the main one, where students will build their own imbalanced datasets and explore the many ways in which things can become more complicated. This will involve more coding on their part, but they can copy/paste relevant lines as needed from the previous sections.

---

### Wrap-up discussion
1. As classes become *more* imbalanced, describe how the challenge of modeling a dataset evolves 
(i.e., does increasing class imbalance make things more or less difficult?)
2. What about as the classes become more similar (in feature space)? Does the size of the dataset matter? What about the relevance of the features?
3. Aside from various optimization choices, what else do you think could be done? 

**Note to instructors:** The last question is meant to lead into a (brief) discussion of techniques to upsample smaller classes or downsample larger classes. Recommendation is to just mention various options and students can look into these on their own time.
