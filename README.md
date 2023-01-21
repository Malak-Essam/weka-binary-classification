# weka-binary-classification
using weka workbench to  build a model on binary classification problem

# dataset
Pima Indians Onset of Diabetes dataset
There are 768 instances in the dataset. If we evaluate models using 10-fold cross validation
then each fold will have about 76 instances, which is fine.
There are 9 attributes, 8 input and one output attributes.
The input attributes are all numerical and have differing scales. We may see some benefit
from either normalizing or standardizing the data.
There are no missing values marked.
There are values for some attributes that do not seem sensible, specifically: plas, pres,
skin, insu, and mass have values of 0. These are probably missing data that could be
marked.
The class attribute is unbalanced, 1 positive outcome to 1.8 negative outcomes, nearly
double the number of negative cases. We may benefit from balancing the class values.
 Some attributes have a Gaussian-like distribution such as plas, pres, skin and mass,
suggesting methods that make this assumption could achieve good results, like Logistic
Regression and Naive Bayes.
 We see a lot of overlap between the classes across the attribute values. The classes do not
seem easily separable.

so we going to create 3 different views of data
Normalized View
The first view we will create is of all the input attributes normalized to the range 0 to 1. This
may benefit multiple algorithms that can be influenced by the scale of the attributes, like
regression and instance-based methods.

Standardized View
We noted in the previous section that some of the attribute have a Gaussian-like distribution.
We can rescale the data and take this distribution into account by using a standardizing filter.
This will create a copy of the dataset where each attribute has a mean value of 0 and a standard
deviation (mean variance) of 1. This may benefit algorithms in the next section that assume a
Gaussian distribution in the input attributes, like Logistic Regression and Naive Bayes

missing values 
some values are non sense and they seem that they are have zero value and that would be mistake so we could consider them missing
so we apply a fither to detect missing and them apply another filter to replace missing with mean

# experment
![Annotation 2023-01-21 153148](https://user-images.githubusercontent.com/63660283/213869134-4162d1de-709e-473e-b614-9682ccc021cb.png)

result
We can see that the estimated accuracy of the model on unseen data is 77.47% with a
standard deviation of 4.39%.



