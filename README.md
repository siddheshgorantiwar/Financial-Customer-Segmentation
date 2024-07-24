# Financial Customer Segmentation Using Clustering and Classification

## 📊 Overview
This project aims to perform market segmentation on a financial customer dataset using clustering techniques and subsequently build a classification model to predict customer segments. Market segmentation helps businesses tailor their marketing strategies and improve customer satisfaction by understanding distinct customer groups.

## 📂 Dataset Description
The dataset includes various features related to customer transactions and behaviors:

- **💳 BALANCE:** The balance amount left in the account to make purchases
- **📈 BALANCE_FREQUENCY:** The frequency of balance updates
- **🛒 PURCHASES:** The total amount of purchases made
- **🛍️ ONEOFF_PURCHASES:** The total amount of one-time purchases
- **📆 INSTALLMENTS_PURCHASES:** The total amount of purchases made in installments
- **💵 CASH_ADVANCE:** The total amount of cash advances taken
- **🔄 PURCHASES_FREQUENCY:** The frequency of purchases
- **📊 ONEOFF_PURCHASES_FREQUENCY:** The frequency of one-time purchases
- **🔄 PURCHASES_INSTALLMENTS_FREQUENCY:** The frequency of installment purchases
- **💳 CASH_ADVANCE_FREQUENCY:** The frequency of cash advances
- **💳 CASH_ADVANCE_TRX:** The number of cash advance transactions
- **🛒 PURCHASES_TRX:** The number of purchase transactions
- **💳 CREDIT_LIMIT:** The credit limit of the account
- **💰 PAYMENTS:** The total amount of payments made
- **💳 MINIMUM_PAYMENTS:** The total amount of minimum payments due
- **🔢 PRC_FULL_PAYMENT:** The percentage of months with full payment
- **📅 TENURE:** The tenure of the account in months

## 🔍 Project Steps

### 1. 🧹 Data Preprocessing
- **Handling Missing Values:** Imputed missing values using the mean of respective columns.
- **Feature Scaling:** Applied standardization to ensure all features contribute equally to the clustering process.
- **Feature Selection:** Ensured all selected features were relevant and contributed to the clustering process.

### 2. 📈 Clustering
Performed clustering to identify distinct customer segments using the K-Means++.

- **Elbow Method:** Used to determine the optimal number of clusters (k) by plotting the within-cluster sum of squares (WCSS) against the number of clusters to find the elbow point.
- **K-Means Clustering:** Applied K-Means with the chosen number of clusters to segment the customers. Each customer was assigned a cluster label representing their segment.

### 3. 🧐 Cluster Analysis
- Calculated the mean values of features within each cluster to understand the typical customer profile in each segment.
- Visualized clusters using PCA (Principal Component Analysis) to reduce dimensionality and plot the data in a 2D space.

### 4. 🤖 Classification
Built a predictive model for customer segmentation using the cluster labels from K-Means as the target variable.

- **Labeling:** Used the cluster labels as the target variable for the classification model.
- **Model Selection:** Chose  Random Forest as classification model.
- **Training and Evaluation:** Split the data into training and test sets. Trained the model on the training set and evaluated its performance on the test set using metrics like accuracy, precision, recall, and F1-score.
- **Hyperparameter Tuning:** Applied techniques like Grid Search to optimize model parameters and improve performance.

## 🎯 Outcomes and Insights
- Successfully identified distinct customer segments with meaningful differences in their transaction behaviors.
- The classification model provided a reliable way to predict the segment of new customers based on their transaction features with an cross val accuracy of 93%.
- The insights gained from cluster analysis helped tailor marketing strategies to different customer segments, potentially improving customer satisfaction and business performance.

## 🚀 Challenges and Learnings
- **Handling Imbalanced Data:** Some clusters had significantly more customers than others, requiring careful handling during the classification phase.
- **Feature Engineering:** Creating new features or combining existing ones was crucial to improve model performance.
- **Interpretability:** Ensuring the model was interpretable and the results were actionable for business stakeholders.

## 🏁 Conclusion
This project demonstrated the application of clustering for market segmentation and the use of classification techniques to build predictive models, providing valuable insights for business decision-making.

