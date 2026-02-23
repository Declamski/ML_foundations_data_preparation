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

Note: This is my percieved ordering at the moment. However, there is clearly a "Task Ordering" task which means that after exploring the data I may change the ordering of my tasks. This reordering would be based on research/studying resources from the class. I just wanted to get started with something so I can start working.

### Identifying the Prediction Target

**The Prediction target is y**
Besides the fact that it's labelled as "target" on the uci website, it is what we're looking for. We want to see if a client will subscribe to a term deposit, therefore, we should train our data on the target of subscribing to a term deposit which is what **y** is.

Two variables which could have been percieved as the target variable are:
- **poutcome**: This shows the outcome of the previous marketing campaign, however the data that we have is focused on **y** not **poutcome** so we'd be training our data on the wrong target. It also holds Categorial data while we're looking for a binary output
- **default**: Simply because I didn't know what it meant until this task, otherwise I don't feel as though there are any other features what would be reasonably mistaken as the target.

### Data Loading and Exploration

