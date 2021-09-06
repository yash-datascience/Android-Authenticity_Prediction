# Android-Authenticity_Prediction
## Project Summary
This project classifies whether an app you install on your phone is malware or benign. The Dataset has 30k records with 185 columns with the binary class column as malware(1) and benign(0). We have handled missing values for textual columns such as app name and description manually as there are just 1 or 2 missing columns. And we have imputed numerical columns and removed the duplicates. We processed textual columns as NLP tasks of text cleaning and vectorization and came up with a derived column, replace related apps with the count, and removed those permission columns which are all zeros as well as those which are not contributing to the target. After we derived some features and encoded the category with target encoding we are left with 163 columns and 27k approx records. After trying 5 different algorithms we settled on using XGboost for our classification task due to its high accuracy score and how it handled multicollinearity in our data along with some other features such as built-in regularization which generalizes our model well and prevent overfitting. Finally, we were able to classify 82% of benign apps and 92% of malware apps on the given dataset.