# A collection of any notes, thoughts, etc so I can keep them in an organized place.

## Order

**Ordering tasks so I can work on them one by one as I go**

- Identifying the Prediction Target
- Data Loading and Exploration
- Task Ordering
- Data Splitting
- Addressing Class Imbalance
- Managing Missing Values
- Encoding Categorial Variables
- Feature Selection
- Feature Scaling
- Training a Logistic Regression Model

Note: This is my percieved ordering at the start. However, there is clearly a "Task Ordering" task which means that after exploring the data I may change the ordering of my tasks. This reordering would be based on research/studying resources from the class. I just wanted to get started with something so I can start working.

### Identifying the Prediction Target

**The Prediction target is y**
Besides the fact that it's labelled as "target" on the uci website, it is what we're looking for. We want to see if a client will subscribe to a term deposit, therefore, we should train our data on the target of subscribing to a term deposit which is what **y** is.

Two variables which could have been percieved as the target variable are:
- **poutcome**: This shows the outcome of the previous marketing campaign, however the data that we have is focused on **y** not **poutcome** so we'd be training our data on the wrong target. It also holds Categorial data while we're looking for a binary output
- **default**: Simply because I didn't know what it meant until this task, otherwise I don't feel as though there are any other features what would be reasonably mistaken as the target.

### Data Loading and Exploration

**Explicit and Implicit missing values**
In the kaggle website for the data set, there is a .txt file called "bank.additional-names.txt". There it tells us what values are in each feature, it also explains any implicit missing data such as in the feature **pdays** if the value is **999** it means that the client was not previously contacted meaning it is a missing value.

**pdays** woul require dealing with the skew of **999** values, especially as they are representing a missing value.

**Try PCA, suggested by PEAD prof**

### Task Ordering

- Data Splitting
- Managing Missing Values
- Encoding Categorial Values
- Feature Selection
- Feature Scaling
- Addressing Class Imbalance
- Training a Logistic Regression Model


**LMM prompts:**
- **Prompt:** how do i go about detecting which features have "unknown" values in them. Don't do the code, just explain how. **Result:** Suggested iterating through features and searching for "unknown" in them.
- **Prompt:** so I've done it manually, but I'm only looking for "unknown" instead of general explicit and implicit missing values, is exploring data and looking for specific values representing missing values the best way to go about it or is there another, better, way **Result:** Suggested manual looking at the authors notes of the dataset, this lead me to finding "bank.additional-names.txt" which had a written explanation of each feature.
- **Prompt:** Can you help me create a pandas DF for an analysis of the missing values **Result:** Gave me the code to visualize the missing values that I assigned to the features that had missing values.
- **Prompt:** I want to visualize the distributions of some of the features, how do I go about this. When do I know what visualization to use for each data type/feature. **Result:** Gave me a guide of when certain specific distributions are used depending on what the data types are and a decision framework.
- **Prompt:** For my job distribution I can't read the labels, can you help me make it clearer **Result:** Added a few lines to make it readable.
- **Prompt:** Can I see how each type of value of the job feature correlated to the output of y? **Result:** Gave me code of sideways bar chart representing subscription rate per job.
- **Prompt:** so right now I (mostly) just have basic statistical distributions on the data, are there any observations I can make that can give me more insight on how data interacts with each other or the target or anything else? **Result:** Suggested different plots that could give me insight, namely: Box plots of key numerical features vs target,cCorrelation heatmaps, temporal patterns and outlier analysis.
- I had chat re-organize the notebook as it was messy