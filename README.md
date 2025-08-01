### Repurchase Predicting

**Jianan Wu**

#### Executive summary
This project develops a predictive model to forecast user repurchase behavior using e-commerce browsing and purchase data. Leveraging advanced feature engineering and Gradient Boosting models, it seeks to enhance ad targeting precision for DSP platforms, improving marketing ROI by identifying users likely to repurchase.

#### Rationale
In the competitive field of digital advertising, identifying potential repurchasers is crucial for DSP (Demand-Side Platform) effectiveness. High-quality retargeting campaigns significantly reduce ad spend waste and maximize returns by accurately predicting user behaviors. Understanding and modeling repurchase patterns empowers advertisers to strategically focus on high-value prospects.

#### Research Question
Can we accurately predict whether a user will repurchase within a given future window based on historical browsing, carting, and purchase behaviors?

#### Data Sources
The dataset used in this project is sourced from Kaggle and can be accessed at https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store?resource=download. 

#### Methodology
Data Aggregation: Aggregated user-level behavioral features including Recency, Frequency, and Monetary (RFM) metrics.
Feature Engineering: Derived additional meaningful metrics such as event type spans, conversion rates, and purchase lag times.
Modeling: compare three models(LogisticRegression,RandomForest,LightGBM) to classify users based on future repurchase likelihood.
Evaluation: Assessed model performance primarily through Recall, Precision, F1-score, and ROC-AUC.

#### Results
The optimized lightGBM model achieved:
- Accuracy: 0.37
- ROC AUC: 0.7430
- Average Precision (AP): 0.1526
- Weighted F1-score: 0.51
- Macro F1-score: 0.31

#### Limitations:
The data and thus the model is highly biased toward class 0. Precision for class 1 (positive class) is very low – indicating many false positives.
However, recall for class 1 is high – the model is catching most of the true positives.

In real world, as a retargeting dsp, we would like to make recall high, since we want to catch payers as much as possible and at the same time spend advertisers' money in full. If precision is too high, the model would be too conserverative and spend very less. But because we only get a 1/10th sample of the 1 month data. There is a lot of room to improve if given larger data. 

#### Next steps
To further enhance the model's performance, next steps include:
Session Embedding: Incorporate GRU-based session embedding features to capture dynamic user behavior patterns.
Attention Mechanism: Explore attention-based models to better weight significant user actions within sessions.
Class Weighting or Resampling: Apply positive class weighting or SMOTE to better handle class imbalance and enhance recall.
Expanded Feature Set: Integrate deeper user-interest and intent features such as product affinity and category-level behaviors.

#### Project Link

- https://github.com/JiananWuu/Repurchase-Predicting/blob/main/Capstone_Project_Repurchase_final.ipynb 


##### Contact and Further Information
Jianan Wu
Email: wjn0301@outlook.com
