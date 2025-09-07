<!DOCTYPE html>
<html>
<head>

</head>
<body>

<h1><strong>Neural Network-Based Bank Customer Churn Prediction</strong></h1>
<p>The notebook focuses on predicting customer churn using a neural network, combining data preprocessing, model training, and evaluation.</p>

<h2><strong>Project Structure:</strong></h2>

 <h2>1. Libraries used:</h2>
      <ul>
        <li>Python</li>
        <li>NumPy, Pandas</li>
        <li>Scikit-learn (preprocessing, SMOTE, metrics)</li>
        <li>TensorFlow / Keras (modeling)</li>
        <li>Matplotlib (visualization)</li>
      </ul>

<h2>2. Data Collection and Preprocessing</h2>
<ul>
    <li>The dataset is loaded (<code>Churn_Modelling.csv</code>) and features (<code>X</code>) and target (<code>y</code>) are extracted.</li>
    <li>Initial exploration includes viewing the first few rows and checking the dataset shape.</li>
    <li>The target variable <code>Exited</code> is analyzed to understand the class distribution.</li>
</ul>

<h2>3. Handling Class Imbalance</h2>
<ul>
    <li>The dataset is imbalanced, with fewer churned customers compared to non-churners.</li>
    <li><strong>SMOTE (Synthetic Minority Oversampling Technique)</strong> is applied to generate synthetic samples for the minority class.</li>
    <li>This oversampling balances the classes, ensuring the neural network does not bias toward the majority class and improves recall for churners.</li>
</ul>

<h2>4. Encoding Categorical Data</h2>
<p>Categorical variables are properly encoded into numerical values to make them suitable for the neural network.</p>

<h2>5. Model Building and Training</h2>
<ul>
    <li>A neural network model is constructed with multiple dense layers.</li>
    <li>The model is compiled with an appropriate optimizer and loss function.</li>
    <li><strong>Early stopping</strong> is implemented to prevent overfitting during training.</li>
</ul>

<h2>6. Model Evaluation</h2>
<ul>
    <li>Predictions are made on the test data.</li>
    <li>Evaluation metrics such as <strong>precision, recall, f1-score, and Average Precision (AP)</strong> are calculated.</li>
    <li>Model performance is visualized using precision-recall curves to analyze ranking effectiveness.</li>
</ul>

<h2>7. Key Results and Benchmark Comparison</h2>
<ul>
    <li><strong>Recall for churned customers:</strong> 76% — higher than typical real-world benchmarks (60–70%), indicating strong detection of actual churners.</li>
    <li><strong>Average Precision (AP) score:</strong> nearly 70% — reflects effective ranking of high-risk churners.</li>
</ul>

<p><strong>Key Insights:</strong></p>
<ul>
    <li>Achieving <strong>76% recall</strong> means the model successfully captures the majority of churners, reducing the risk of losing valuable customers.</li>
    <li>An <strong>AP close to 70%</strong> shows robust prioritization of high-risk customers, making this model well-suited for real-world bank churn prediction applications.</li>
    <li>Handling class imbalance with <strong>SMOTE</strong> contributed significantly to improving recall and AP, ensuring the model treats minority churn cases appropriately.</li>
</ul>
<section>
      <p>Notes:</p>
      <p>
        This README summarizes the notebook workflow and main findings. For code,
        notebooks, figures, and exact hyperparameters, see the notebook file
        (<code>ANN.ipynb</code>) and the scripts in the repository.
      </p>
</section>

</body>
</html>
