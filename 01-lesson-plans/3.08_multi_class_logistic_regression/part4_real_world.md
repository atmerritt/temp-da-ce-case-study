# Real-world case study

## Learning goals and implementation
In this last section, the goal is for the students to put everything they've learned together (multi-class classification and imbalanced datasets) and apply it to
a messy, real-world dataset. Working in pairs, students will be able to apply their SQL and exploratory data analysis skills to collect, clean and process the data 
before training a classification model.

The ideal structure here is: 
1. Lab (exploratory data analysis and feature selection)
2. Discussion #1 (progress and questions so far)
3. Lab (training and evaluating the model)
4. Discussion #2 (results and remaining challenges)

---
### Lab

The following notebook is meant to guide the students through multi-class classification:

XXXXX LINK TO NOTEBOOK XXXXX

#### DATA
For continuity with the rest of the unit (and with the previous unit) they can work with the 
[Sakila Sample Database](https://dev.mysql.com/doc/sakila/en/sakila-structure.html) representing DVD rentals.

#### GOALS
Students will attempt to train a logistic regression model to classify the genre of a movie based on available information about it. 
They can choose whether to model each available genre on its own or to combine some (for example "family" and "children" or etc), and can also
decide which extension to multi-class classification to apply.

---

### Discussion #1
1. What do you think about the data? Did you find anything interesting and/or unusual about it, or was all as-expected?
2. Which features are you planning to use for your models, and why?
3. Which target variables are you predicting? Did you combine any genres? Why or why not?
4. Which logistic regression approach are you planning to use and why?
5. Any questions or issues so far?

### Discussion #2
1. How are your results looking? Which evaluation metric(s) did you use to assess your model's performance?
2. What challenges remain? Is anything unclear?
3. Imagine that we had unlimited time to work on this problem. What steps would you take next? 
