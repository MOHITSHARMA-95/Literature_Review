Literature Review:

1. we evaluate the performance of the models with respect to well-established fairness measures and detect a significant decrease of discriminatory biases for the subset of data 
with missing values. 
2. Martínez-Plumed et al. [9] present the first comprehensive analysis of the relationship between missing data on fairness. Their study of three scientific datasets indicates that 
the subsets containing missing data are fairer when compared to their complete counterparts.
3. The implementations of mitigation and fairness evaluation methods reveals a strong preference for eliminating partial observations. This practice worsens the quality of statistical 
analyses performed on the data, extending beyond just the predictive capability of the models as all parts of the modern data pipeline are affected.  

****************************************************************** 
The aim of this thesis is to locate and analyze a novel dataset relating to the current fairness discussion, and to verify the main findings of Martínez-Plumedet al. [9] — records 
containing missing values are usually fairer than the rest. This study contains a brief review of algorithmic fairness, including fairness definitions and measures, and its relationship 
to missingness in datasets. We pay close attention to missingness patterns and how missing values are treated using various methods, such as imputation. While the main objective is not 
necessarily to provide the most accurate classifier possible, we deem it imperative to investigate optimal model performance on differently treated subsets of data. Furthermore, we 
separately analyze the unfairness contribution of each chosen predictor along with its information gain. Our main research question relates to the effect of missing values on a 
particular fairness measure.  How does the application of imputation methods on a sparse dataset effect the discriminatory bias of machine learning models? 
******************************************************************
4. Another example of unfairness relates to the equal treatment of unequal subpopulations. When a majority and a minority population show different distributions in the data, training
a group-blind classifier to minimize the overall error, but it is not able to fit both optimally, it will fit the majority one. Consequently, the minority population will suffer a 
larger amount of errors.
5. The accidental absence of information is just as much a concern as the intentional removal of data due to various reasons.
**The different causes of missingness:**  
**a. Partial completion:** During the process of collecting data over time, user fatigue, or object-related problems may fail to provide useful data after a certain point in the study. The resulting ordinal dependency of attributes can be used as a basis for treating the missing values.
**b. Missing by design:**  In this scenario the missingness mechanism is known and intentional, thus statistically treatable in the analysis. We differentiate between contingency attributes, when not all characteristics are equally applicable to all objects, and attribute sampling.
 **c. Item non-response:** Some variables are missing for some observations. In user-related studies, we further consider these categories of missingness: not provided, intentionally left out for various reasons; useless, provided data yields no information due to suitability, legibility or otherwise; lost,

## We identify 4 sensitive, protected attributes, namely african_american, lgbt, minority and sex. 
These are automatically disqualified as potential modeling attributes and are utilized for the discrimination analysis below. Ad- ditionally, we dismiss scholarship as a predictor due to its strongly correlated with the positive class of our target label, detailed in the correlation plot below.
