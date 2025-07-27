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
Feature Engineering: Derived additional meaningful metrics such as session counts, event type spans, conversion rates, and purchase lag times.
Modeling: Applied Gradient Boosting (with hyperparameter tuning and threshold optimization) to classify users based on future repurchase likelihood.
Evaluation: Assessed model performance primarily through Recall, Precision, F1-score, and ROC-AUC.

#### Results
The optimized Gradient Boosting model achieved:
ROC AUC: ~0.805
Recall: Approximately 24%
Precision: Approximately 18%
F1-score: Approximately 21%
While the model showed a moderate level of accuracy and decent ROC AUC, the recall rate (critical for advertising applications) indicated significant room for improvement.

#### Next steps
To further enhance the model's performance, particularly recall, suggested next steps include:
Session Embedding: Incorporate GRU-based session embedding features to capture dynamic user behavior patterns.
Attention Mechanism: Explore attention-based models to better weight significant user actions within sessions.
Class Weighting or Resampling: Apply positive class weighting or SMOTE to better handle class imbalance and enhance recall.
Expanded Feature Set: Integrate deeper user-interest and intent features such as product affinity and category-level behaviors.

#### Outline of project

- [Link to notebook 1]()
- [Link to notebook 2]()
- [Link to notebook 3]()


##### Contact and Further Information
Jianan Wu
Email: wjn0301@outlook.com
