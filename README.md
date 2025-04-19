# DSC 550 Data Mining -- Sentiment Analysis of Customer Reviews

## Overview
This project is part of the DSC 550 Data Mining course. It aims to apply various data mining techniques, such as classification, clustering, or regression, to a real-world dataset. The project explores different approaches to data preprocessing, model building, and performance evaluation.

## Dataset
- **Dataset Name**: Amazon Reviews dataset from 2023
- **Source**: [Amazon Reviews 2023 dataset](https://amazon-reviews-2023.github.io/#grouped-by-category)
- **Description**: 
  - This dataset contains 48.19 million items and 571.54 million reviews. 
  - The Appliances category includes:
  - 1.8 million unique users who have left reviews.
  - 94.3K unique items in the Appliances category.
  - 2.1 million customer reviews.
  - 92.8 million ratings given for these products.
  - 95.3 million total feedback entries.
  
## Project Goal (Solving)
The goal is to identify factors driving customer satisfaction or dissatisfaction across various product categories. 

## Project Structure

- `README.md`: This file.
- `data/`: Contains the dataset files.
  - `raw/`: Original dataset files.
  - `cleaned/`: Preprocessed dataset (if applicable).
- `src/`: Contains the Python scripts for the project.
  - `preprocessing.py`: Script for data cleaning and preprocessing.
  - `modeling.py`: Script for training and testing the model.
  - `evaluation.py`: Script for evaluating the model.
- `notebooks/`: Jupyter notebooks for exploratory data analysis (EDA) and model building.
- `results/`: Contains model performance metrics and visualizations (e.g., confusion matrix, feature importance).
- `models/`: Stores trained model files (e.g., `model.pkl`).
- `requirements.txt`: A file listing the required Python libraries for this project.

---

**Introducing the Problem**

***How can we implement a machine learning model to accurately classify appliance
reviews, ensuring strong performance for both positive and negative feedback?***

For this project, we will be analyzing a large-scale Amazon Reviews dataset from 2023,
which contains 48.19 million items and 571.54 million reviews. Our primary focus will be
on the Appliances category within this dataset.

The goal is to identify factors driving customer satisfaction or dissatisfaction across various
product categories. Using NLP techniques like TextBlob and VADER, sentiment polarity
scores will be extracted from reviews and categorized into positive (satisfied) or negative
(dissatisfied).

A classification model, such as Logistic Regression, will be trained to predict sentiment
based on review text. The target of the model is the binary sentiment (positive or negative)
derived from polarity scores as well as the rating scale.


**Why It Is Important/Useful to Solve This Problem**

Solving this problem is crucial for several reasons. First, it will lead to improved customer
satisfaction insights, allowing manufacturers and retailers to adjust their product
strategies. Second, addressing this issue will result in better-targeted marketing and
product development. Lastly, finding a solution to this problem will pave the way for future
advancements in sentiment analysis and NLP applications within e-commerce.


**Pitch to Stakeholders**

To gain buy-in from stakeholders, I emphasized the potential benefits of solving this
problem. By accurately classifying sentiment in appliance reviews, we can expect to see
improved customer experience through targeted product improvements and more effective
marketing strategies. Furthermore, the solution will position our organization as a leader in
utilizing advanced data science techniques to drive innovation and growth.


**Data Acquisition**

The data for this project was obtained from:
• Amazon Reviews 2023 dataset
This source offers comprehensive details, including product ratings, review texts, and
timestamps, providing a rich foundation for analysis. Its extensive nature and reliability
make it an ideal resource for uncovering trends and patterns that can drive improvements
in both customer satisfaction and business performance.

**Conclusion**

Model Evaluation and Insights
The model achieved an accuracy of 0.91, with a detailed report below highlighting the F1
scores for both negative and positive reviews.

![image](https://github.com/user-attachments/assets/a84a1043-e317-461b-8e70-0b33c6b05c8f)

An F1 score of 94% for positive reviews and 74% for negative reviews indicates a
performance imbalance. As previously mentioned, the model is biased due to most
reviews being positive.

A confusion matrix representation to showcase where my model did well and bad.

![image](https://github.com/user-attachments/assets/1703b372-dc47-4dd8-825d-d771822d70a5)

- True Negative (Top-Left): 50,643 reviews were correctly classified as negative.
- False Positive (Top-Right): 23,785 negative reviews were misclassified as positive.
- False Negative (Bottom-Left): 12,234 positive reviews were misclassified as
negative.
- True Positive (Bottom-Right): 303,338 reviews were correctly classified as positive.

The model performs well, particularly in identifying positive reviews, but has some
misclassification of negative reviews.


![image](https://github.com/user-attachments/assets/f87341c1-da83-44cf-b5dc-c1ccc2bde08a)

The logistic regression model has 91% accuracy, performing well overall. It excels at
identifying positive reviews but shows moderate performance with negative reviews (80%
precision, 67% recall). The weighted averages for precision, recall, and F1-score are all
0.90, reflecting strong overall performance. The Area Under the Curve (AUC) is 0.94,
indicating a strong classifier.

After completing the project, the Logistic Regression model performed well on classifying
appliance review sentiments. The evaluation metrics showed that the model was able to
distinguish between positive and negative sentiments with reasonable accuracy (91%).

**Deployment Readiness**

The model isn't fully ready for deployment yet. To improve these topics can be addressed:
- Addressing Bias: Adjust class weights or resample the data to handle class
imbalance, especially for negative reviews.
- Training on More Data: Add more labeled negative reviews to improve recall.
- Threshold Adjustment: Adjust classification thresholds to improve recall for
negative reviews.

**Recommendations for Future Work**

In the future, I recommend exploring more advanced NLP techniques such as BERT, which
can capture contextual meaning in the reviews better than simpler models. I also suggest
applying the model to different product categories and continuously updating it to handle
new data and evolving language patterns.


**Challenges and Opportunities**

A significant challenge I faced was handling the imbalance between positive and negative
sentiment in the dataset. However, this project provides an opportunity to explore deeper
into NLP and build models that can address more nuanced sentiment categories or multiclass classifications



