# bayesian-inferences-multivariate-normal-distribution

In statistics, especially in multivariate analysis, there are many applications in which multivariate normal distribution plays an important role, such as discriminant analysis, multivariate analysis of variance, and canonical correlation analysis. 

In the demonstration, we focus on obtaining the probabilities of class/labels and assuming a multivariate normal distribution of data. 

An organization is given an overall rating based on different factors, such as its innovation leadership, regulatory leadership and so on. Moreover, the ratings are given on a scale between 1-9 which implies that we have 9 different class labels.  

Dataset can be found at- 
https://docs.google.com/spreadsheets/d/1-erQeB3Ga5WnAs-Sw7zJuSjO06v4Cs_O/edit?usp=sharing&ouid=108266723122050992017&rtpof=true&sd=true

We subset the survey data for each class and obtain the distribution using `multivariate_normal()` from `scipy.stats` module in python. The input to the function is mean and variance parameters of a particular class subset which defines a multivariate normal distribution.

It is important to note that `multivariate_normal.pdf()` takes in an data array, mean and variance values. It assigns the probability to each observation in input array based on the input multivariate distribution parameters. Multiplying the likelihood values With the prior probabilities of each class renders the probability of a observation in each class. That is to say, we have 9 probability values corresponding a particular observation which gives us information about the presence of a observation in which class is maximum. 
