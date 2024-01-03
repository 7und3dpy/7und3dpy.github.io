# Introduction to Weka

Sample article demonstrating basic Markdown syntax and HTML element formatting.

<!--More-->

# Building a Basic Classification Machine Learning Model with Weka

![](https://datamahadev.com/wp-content/uploads/2020/09/Classification-in-Machine-Learning-datamahadev.com_.jpeg)

Don't think that Machine Learning is only for experts. If you're a learner or a non-expert looking to dive into Machine Learning, Weka is a great choice.

Weka is a collection of machine learning algorithms for data mining tasks. It includes tools for data preparation, classification, regression, clustering, association rules, and visualization.

Weka is open-source software distributed under the GNU General Public License. The product is developed by the Machine Learning research group at the University of Waikato, New Zealand.

Notably, Weka also supports deep learning.

You can explore more about Weka [here](https://www.cs.waikato.ac.nz/ml/weka/index.html).

## Why Choose Weka?

A significant benefit of using Weka is its extensive support for various machine learning algorithms. The more algorithms, the better for understanding your problem and comparing different algorithms easily.

One of the highlights is that Weka already has algorithms that allow us to approach the Titanic Case Study more visually. In this context, we'll explore three basic classification algorithms: K-Nearest Neighbor, Naive Bayes, and Decision Tree.

## Understanding the Titanic Case Study

![](https://media.nationalgeographic.org/assets/photos/000/273/27302.jpg)

On April 15, 1912, on its maiden voyage, the Titanic sank after colliding with an iceberg, claiming 1502 out of 2224 passengers and crew. This tragic event shocked the international community and led to improved safety regulations for ships.

While luck played a role in survival after the Titanic disaster, certain groups, such as women, children, and the upper class, had higher survival chances.

In this case study, we will analyze the types of people likely to survive. Specifically, we will use machine learning tools to predict which passengers survived the disaster.

You can learn more about this case study and get the data [here](https://www.kaggle.com/c/titanic/overview).

#### **Input**
From the original data, I will simplify it. I filtered out some important attributes and modified attribute names that affect the survival (**survived**) of passengers on the Titanic.
My input attributes will include:

| Attribute   |      Definition      | Explanation |
|----------|:-------------:|------:|
| class | Ticket class - First, Second, or Third class. | 1 = 1st, 2 = 2nd, 3 = 3rd |
| gender | Gender | Standardized as 0 - Female and 1 - Male |
| age | Age | 1 - Adult and 0 - Children |
| survived | Survival probability | 0 - No and 1 - Yes |

If you want to test the normalized dataset from me, you can download it [here](https://drive.google.com/file/d/13ycO_k8erbZrS-cxa-F8RlWlfitF57Kv/view?usp=sharing).

#### **Output**
The output data is straightforward, providing predictions about the likelihood of survival for the remaining passengers based on known factors such as name, age, gender, the number of accompanying people, cabin location, etc.

#### **Significance**
This problem allows us to predict the survival chances of a person based on a disaster, enabling us to draw lessons for future journeys. This information can be used for designing safer ships, improving services, issuing warnings, and more.

#### **Analysis**
It's evident that this is a Two-Class Classification problem with the output being **survived** or not.

## How to Use Weka?

I personally think using Weka is straightforward. You just need to install it and select a CSV file.
![](https://i.imgur.com/uYRi4yL.png)
Next, go to the "Classify" tab:
![](https://i.imgur.com/koui4zN.png)
Under "Classifier," choose the algorithm you want to test. I will start with the K-Nearest Neighbor algorithm.

In the test options, you can choose:

- Use training set: Use the entire dataset to train the model.
- Supplied test set: Provide an additional test set to evaluate the model.
- Cross-validation: Split the data into k subsets of equal size. In each iteration, one subset is used as the test set, and the rest are used for training. The value of k is usually set to 10. You can use either:
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; + Leave-one-out: k equals the number of samples in the dataset (suitable for small datasets).
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; + Stratified cross-validation: Uses sampling methods to ensure that class distribution is similar across all subsets.
- Percentage split: Split the data into training and test sets based on the percentage you want.

Similarly, continue with the Decision Tree ID3 and Naive Bayes algorithms.
![](https://i.imgur.com/Ixx08sl.png)
![](https://i.imgur.com/e87Sxzd.png)

I hope everyone has some interesting experiences with Weka. Before using it, don't forget to appreciate the Computer Science Department at the University of Waikato, New Zealand, for bringing us such an excellent product!

## More Information About Weka

- Details about the tool (including download links, documentation, and courses): [https://www.cs.waikato.ac.nz/ml/weka/index.html](https://www.cs.waikato.ac.nz/ml/weka/index.html)
- To add ID3 Decision Tree to Weka: \
[https://stackoverflow.com/questions/48888463/weka-3-8-package-installation-what-are-the-steps-to-add-id3](https://stackoverflow.com/questions/48888463/weka-3-8-package-installation-what-are-the-steps-to-add-id3)
- If you don't see KNN in Lazy, choose the IBk classifier.
- An interesting article on model evaluation for those who are not familiar: [https://ongxuanhong.wordpress.com/2015/08/25/danh-gia-mo-hinh-model-evaluation/](https://ongxuanhong.wordpress.com/2015/08/25/danh-gia-mo-hinh-model-evaluation/)

