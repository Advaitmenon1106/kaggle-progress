# J045-NNDL-M1-Kaggle

## Table of Contents

| File                         | Link                                         | Description                                                      |
| ---------------------------- | -------------------------------------------- | ---------------------------------------------------------------- |
| naive_approach.ipynb         | [Click Here](./naive_approach.ipynb)         | Naive approach by dropping NA values                             |
| J045_Naive_Imputation        | [Click Here](./J045_NNDL_M1.ipynb)           | Approach by imputing NA values with measures of central tendency |
| J045_Better_Imputation.ipynb | [Click Here](./J045_Better_Imputation.ipynb) | A relatively better approach to immputation using KMeans Imputer |
| submission.csv               | [Click Here](./submission.csv)               | Submissions for the first method(naive imputation)               |
| submission2.csv              | [Click Here](./submission2.csv)              | Submissions for the second method (KMeans Imputer)               |

### Steps taken:-

#### Data Dictionary:-

![Data Dictionary](https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F2003977%2F4465d9311ccae2f9ccb057fc7e14f26f%2FScreenshot%20from%202023-10-18%2009-42-52.png?generation=1697586187040332&alt=media)

#### Naive approach:-

- Drop the NA values
- Convert categorical columns to One-Hot Encoded vectors
- Label-Encode the y (Status) values
- Run a stratified train-test split operation
- Run an SVM to check the base accuracy that can be obtained with the approach. An accuracy of ~70-72% was achieved on both training and testing data
- **Shortcomings of this approach :-**
  - Loss of a large amount of data (42.3%)
  - Lesser data left for a train-test approach
  - Information about specific targets are lost (Status, in this case)

#### Naive imputation :-

- Fill missing continuous values with mean/median
- Fill missing categorical values with mode

#### Better imputation :-

- Fill continuous values "naively"
- Fill categorical values using sklearn's KMeans imputer
- Did not yield better results in the final model
