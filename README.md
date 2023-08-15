
## NLP-Hotel-Review: Sentiment Analysis
**Project Objective:** Assist Hotel Management Inc. in understanding which hotel qualities contribute to customer satisfaction and higher ratings.

### Data Description:
The dataset encompasses hotel reviews with both positive and negative text comments. Along with these reviews, other details like hotel location, duration of the stay, and more are included. The primary target is the `Reviewer_Score` column, marking positive sentiment as `1` and negative as `0`.

[**Download the Dataset Here**](your_link_here)

### Workflow:

#### 1. Exploratory Data Analysis (EDA):
   - **Task:** Load the data and familiarize yourself with its structure.
   - **Goal:** Extract 3-4 key observations to gain actionable insights.
   - **Actions:** 
     - Create a data dictionary.
     - Conduct basic statistical analysis.
     - Visualize the data.
     - Preprocess and clean data for modeling.

#### 2. Preprocessing:
   - **Task:** Process text data for modeling.
   - **Goal:** Ready the data for modeling.
   - **Actions:** 
     - Split the dataset into training and testing sets.
     - Transform `positive` and `negative` review columns using `CountVectorizer`.
     - Set a max feature limit of `500` and omit tokens used `<10` times.
     - Merge the processed arrays with original numeric data to produce final train and test data frames. Prefix column names to differentiate between positive (`pos_`) and negative (`neg_`) reviews.

#### 3. Modeling:
   - **Tasks & Goals:** 
     1. **Logistic Regression:** 
        - Fit the data.
        - Analyze training and testing accuracy.
        - Identify the top 20 words from both positive and negative reviews that are most indicative of the respective sentiments.
        - Derive actionable insights from the findings.
     
     2. **Decision Tree Classifier with PCA:** 
        - Utilize a pipeline to combine PCA with a decision tree classifier.
        - Optimize hyperparameters: maximum tree depth, minimum data points required at leaf nodes, etc.
        - Utilize 20 principal components.
        - Determine the best parameters via 5-fold cross-validation.
        - Compare outcomes with the logistic regression model.

#### 4. Evaluation:
   - **Task:** Delve deeper into the performance of your best model.
   - **Goal:** Understand the model's strengths and weaknesses.
   - **Actions:** 
     - Examine the confusion matrix.
     - Comment on model errors.
     - Evaluate metrics such as precision and recall.

