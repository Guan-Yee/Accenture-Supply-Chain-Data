# Accenture-Supply-Chain-Resilience-Data-Challenge


The original datasets are found on Kaggle. However, these datasets have limited access. Nonetheless, the datasets are obtained from the data folder in this repository https://github.com/JNADatathon2022/Datathon.

\textbf{Motivation}
Late Deliveries cause reputation damage and loss of potential revenue for both the logistics companies and the cilents. Hence, this project seeks to investigate the underlying factors that cause the delivery to be delayed and provide preemptive actions for the stakeholders to reduce future instances of late deliveries. \
\textbf{Methodology}
\begin{itemize}
\item Preprocessing the datasets by performing the necessary encoding on the respective variables.
\item Create 2 datasets Stratified and Adasyn to address the imbalanced nature of the dataset.
\item Perform the splitting
\item Perform Mutual Information, Chi square test on the categorical variables
\item Perform Mutual Information and the correlation test on the numerical variables.
\item Remove varaibles with low Mutual information and Chi square test
\item Train them with Random forest, XGBoost and LGBM classifier.
\end{itemize}
\textbf{Evaluation Criterions}
\begin{itemize}
\item Confusion matrix is used to evaluation the performance on the test dataset
\item The ROC score is used to show the overall performance of the classifier as well.
\item Shaply plot for each model will be shown as well
\end{itemize}
\textbf{Datasets Description} \

| Command | Description |
| --- | --- |
| `order_id`(string) | unique identifier of transactional order from port inbound to final destination. Primary key of data set. |
| `origin_port`(string) | location of port where order imports arrives. |
