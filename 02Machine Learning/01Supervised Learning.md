<img src='./Images/Supervised Learning.png'>

# Supervised Learning Introduction

## What is Supervised Learning?

Supervised learning is a type of machine learning where a computer learns from labeled data. This means that for every input, we already have the correct output, and the model tries to learn the relationship between them.

Real-Life Example:

    Imagine you're a teacher grading student essays. You have past essays with grades (A, B, C, etc.), and you learn patterns to predict the grades of new essays. This is how supervised learning works!

## Types of Learning

Machine learning has three main types:

    1️⃣ Supervised Learning - Learns from labeled data.
    2️⃣ Unsupervised Learning - Learns from unlabeled data (e.g., grouping similar customers based on shopping habits).
    3️⃣ Reinforcement Learning - Learns by trial and error (e.g., a robot learning to walk).

## Applications of Supervised Learning

    Spam Detection (Gmail classifies emails as spam or not based on past examples).
    Medical Diagnosis (Predicting if a patient has a disease based on symptoms).
    Fraud Detection (Banks use it to detect fraudulent transactions).
    Speech Recognition (Google Assistant understands your voice).

# Supervised Learning Algorithms

## 1️⃣ Linear Regression Model

Used for predicting continuous values (like temperature, house prices).

📌 Example:

    You want to predict house prices based on square footage. If larger houses are more expensive, the relationship between size and price is a straight line.

Formula: 

        y = mx + c
    
    Where:
     y = predicted value (house price)
     x = input (house size)
     m= slope (rate of increase in price per sq ft)
     c = intercept (starting price)
    
`Graph: The model finds a straight line that best fits the data points.`

### How it Works:

    1️⃣ Collect Data - We gather data with input feature (e.g., house size) and an output (house price).
    2️⃣ Plot the Data - We visualize the data points on a graph.
    3️⃣ Find the Best Fit Line - The algorithm finds the straight line that minimizes the difference between actual and predicted values.
    4️⃣ Make Predictions - Once trained, we can use the equation to predict new values.

👉 Mathematical Formula:

        y = mx + c

    y = Predicted output
    x = Input feature
    m = Slope (how fast y changes with x)
    c = Intercept (starting value of y)

📌 Example:

    If the equation is Price = 5000 × (House Size) + 50,000,
        A house of 1000 sq ft will cost:
            5000 × 1000 + 50,000 = 5,050,000

✔️ Optimization:

    The model adjusts m and c to minimize errors using a technique called Gradient Descent.

## 2️⃣ Naive Bayes Classifier

A simpel but powerful algorithm used to text classification (like spam filtering).

📌 Example:

    Imagine you receive an email, and you want to classify it as spam or not spam. The Naive Bayes algorithm calculates the probability of words appearing in spam vs. non-spam emails and makes decision.

👉 Formula:

        P(A∣B)= P(B∣A)P(A)/P(B)

    Where:

    P(A∣B) = Probability of email being spam given certain words
    P(B∣A) = Probability of words appearing in spam emails
    P(A) = Prior probability of spam emails
    P(B) = Probability of words appearing in any email  

💡 ​Why "Naïve"?

    Because it assumes that all words in an email contribute independently to the classification, which is often not true but works well in practice.

### How it Works:

    1️⃣ Calculate Probability of Words - It learns how often words appear in each cateory (spam or not spam).
    2️⃣ Multiply Probabilities - It calculates the probability that a new email belongs to each category.
    3️⃣ Choose the Highest Probability - It classifies the email based on the highest probability.

📌 Example:
    If an email contains "Win lottery now!", the model calculates:
        P(Spam | "Win lottery now!")
        P(Not Spam | "Win lottery now!")
    If P(Spam) > P(NotSpam), the email is marked as spam.

## Decision Tree

A tree-like structure used for classification (like deciding if a person is eligible for a loan) and decision making.

📌 Example:

    Imagine you're bank manager approving loans. You can create a decision tree like:

        If salary > 50,000 → Approve loan
        Else, if credit score > 700 → Approve loan
        Otherwise → Reject loan

The tree splits at each decision point, and we reach the final decision at the leaves.

### How it Works:

    1️⃣ Start with the Root Node - The root is the most important feature (e.g., salary for loan approval).
    2️⃣ Create Decision Nodes - The data is split based on different conditions.
    3️⃣ Continue Splitting - The tree keeps dividing until it reaches a final decision (leaf node).
    4️⃣ Make a Prediction - For a new input, follow the tree's path to find the result.

📌 Example:

    Predicting if a loan will be approved:
        Root Node: Income
            If Income > ₹50,000, loan is approved.
            Else, check credit score.
                If Credit Score > 700, loan is approved.
                Else, rejected.

✔️ Optimization:

    The tree selects the best features using Gini Index or Entropy (Information Gain). 

## 4️⃣ K-Nearest Neighbors (KNN)

A simple algorithm that classifies new data points based on their nearest neighbors.

📌 Example:
     
     Imagine you open a new restaurant and want to know if it should be classified as fast food or fine dining.
        If most nearby restaurants are fast food, your restaurant is also classified as fast food.
        If most are fine dining, your restaurant is fine dining.

### How it Works:

    1️⃣ Store All Data Points - The algorithm saves all past examples.
    2️⃣ Choose K (number of neighbors) - A number is chosen, like K = 3 or K = 5.
    3️⃣ Find Nearest Neighbors - When a new input is given, it finds the closest K points.
    4️⃣ Majority Voting - It assigns the class that appears the most among the K neighbors.

✔️ Optimization:

    Choosing the right K value is crucial.
    Distance is calculated using Euclidean distance:

        d= sqrt( sq(x2 −x1) + sq(y2 −y1) )
 
​
## 5️⃣ Logistic Regression

Used for binary classification `(Yes/No, True/False)`

📌 Example:

    Predicting if a student will pass or fail based on study hours.

    Unlike LInear Regression, which gives continuous values, Logistic Regression gives probabilities between 0 and 1.

👉 Formula:

            P = 1/ ( 1 + e-(mx+c))  this is e to the power

    Where
    P is the probability (between 0 and 1)
    e is a mathematical constant

If P > 0.5, we classify it as Pass.
If P < 0.5, we classify it as Fail

### How it WOrks:

    1️⃣ Transform Linear Regression Output - Instead of predicting values, it gives a probability.
    2️⃣ Apply the Sigmoid Function - That is already written above
    3️⃣ Threshold the Output
            If P > 0.5, classify as 1(Pass, Yes, Spam, etc.).
            If P < 0.5, classify as 0(Fail, No, Not Spam, etc.). 

✔️ Optimization:

    Uses Gradient Descent to adjust weights.     

## 6️⃣ Support Vector Machine (SVM)

Used for classification by drawing the best boundary (hyperlane) between classes.

📌 Example:
    Imagine a basketball coach classifying players as tall or short based on height and weight.
    SVM draws a line that best separates the two classes.

### How it works:

    1️⃣ Find the Hyperlane - It searches for the line/plane that best seperates two classes.
    2️⃣ MAximize Margin - The algorithm ensures the gap between classes is as wide as possible.
    3️⃣ Classify New Data - A new point is classified based on which side of the hyperplane it falls on.

✔️ Optimization:

    If data is not linearly separable, SVM applies kernel tricks to map data into higher dimensions.

## 7️⃣ Random Forest Algorithm

A collection of multiple decision trees that improves accuracy.
Used for classification and regression by combining multiple decision trees.

📌 Example: 

    Imagine you ask 10 different doctors about a diagnosis. Instead of relying on just one, you take the majority vote.

### How it works:

    1️⃣ Create Multiple Decision Trees - It generates many trees using random subsets of data.
    2️⃣ Aggregate Results:
        For classification, take the majority vote.
        For regression, take the average prediction.
    3️⃣ Reduce Overfitting - More trees lead to a stable and accurate model.

📌 Example:

    Predicting if a customer will buy a product:
        Decision Tree 1: Yes
        Decision Tree 2: No
        Decision Tree 3: Yes
        Final Prediction (majority vote): Yes
    
Optimization:

    Uses Bootstrap Aggregation (Bagging) for better performance.

