# Diving into multi-class classification via logistic regression



## Learning goals and implementation
In this part of the lesson, the goal is for the students to understand what multi-class classification is, 
and the differences between binary and multi-class classification. This will be a combination of a brief lecture and a guided project.



---

### Mini Lecture
Briefly recap for the students what logistic regression is, including a refresher on its loss function:

L(y<sub>pred</sub>, y<sub>true</sub>) = -[y<sub>true</sub>log(y<sub>pred</sub>) + (1-y<sub>true</sub>)log(1-y<sub>pred</sub>)] 

Which is a combination of two individual cases, namely:

If `y=1`:  
L(y<sub>pred</sub>, 1) = -log(y<sub>pred</sub>), 

and if `y=0`:  
L(y<sub>pred</sub>, 0) = -log(1-y<sub>pred</sub>).

When we combine these we ensure that our cost function (which is the average loss over all data points) is convex (a key requirement for efficient training). 
However, as we can see, it is constructed explicitly from *two* classes (0 and 1). In other words it is designed exclusively for the binary classification case.
So what do we do if we have more than 2 classes? [**can solicit input from students here**]

#### Extensions of binary classification for logistic regression

**One-vs-Rest (OVR):** in this case, we convert the multi-class classification with *N* classes into *N* binary classification problems. 
For example, if we are classifying "cat" vs "dog" vs "bird", we would first do "cat vs not-cat", then "dog vs not-dog", then "bird vs not-bird". 
This means that for every data sample that we classify, we actually end up with *N* different probabilities (one per class), and the final classification is
made based on which probability was highest. 

**One-vs-One (OVO):** once again we convert the multi-class classification problem into binary classification problems, but now we fit one model per *pair* of classes;
i.e., "cat vs dog", "cat vs bird", "dog vs bird". In this particular example, we end up with the same number of models as we did in OVR, but the number of models goes as N(N-1)/2, 
so for cases with higher numbers of classes this quickly becomes less efficient.

#### Multinomial logistic regression

A third option is to perform multinomial logistic regression. This is a generalization of binary logistic regression, and involves changes to the 
loss (and therefore cost) function to account for additional classes. 


---

### Guided Project

The following notebook is meant to guide the students through multi-class classification:

`./ipynb/multiclass_cls_instructor.ipynb`

#### DATA
In this part of the lesson we'll use the classic [Iris Dataset](https://archive.ics.uci.edu/ml/datasets/Iris/). The dataset 
can be read in easily with `sklearn`'s built-in function `load_iris()`, which also serves to highlight the collection of 
datasets that `sklearn` provides access to (these are generally simple and over-used datasets, but they can be a very useful learning tool).

#### Notes to instructor:
* For the exploratory data analysis, you can walk the students through creating a histogram and a boxplot for one of the features (in case a refresher on these visualization methods is useful), and then have them explore the rest on their own. 
* The instructor's version of the lab has a complete EDA for your reference.

---

### Wrap-up discussion
1. What do you think about the differences between OVR and multinomial logistic regression?
2. Why do you think OVO isn't one of the multi-class options in `sklearn`'s logistic regression classifier?
