
# Deep Learning Challenge Report: Predicting Alphabet Soup Success

## **1. Overview of the Analysis**
Alphabet Soup is a nonprofit foundation that provides funding to organizations. The goal of this project is to build a deep learning model that predicts whether an applicant will successfully use the funding provided by Alphabet Soup. 

I use **machine learning and neural networks** to classify funding applicants based on historical data. The dataset contains over **34,000** organizations and includes categorical and numerical features related to the applicants.

---

## **2. Data Preprocessing**
To prepare the dataset for training, the following steps were performed:

- **Loaded the dataset** and explored its structure.
- **Dropped unnecessary columns:** The `EIN` and `NAME` columns, as they do not contribute to the prediction.
- **Categorical Encoding:**
  - Replaced rare categories (less than a certain threshold) in `APPLICATION_TYPE` and `CLASSIFICATION` with "Other."
  - Applied **one-hot encoding** to categorical variables.
- **Feature Selection:**
  - Extracted features (`X`) and target variable (`y`).
  - Split the dataset into **training (75%)** and **testing (25%)** sets.
- **Feature Scaling:**
  - Used **StandardScaler** to normalize numerical values.

---

## **3. Model Architecture and Accuracy**
We implemented a **deep neural network (DNN)** using TensorFlow and Keras. The model structure is as follows:

- **Input Layer:** `43` features
- **Hidden Layer 1:** 80 neurons, **ReLU** activation
- **Hidden Layer 2:** 30 neurons, **ReLU** activation
- **Output Layer:** 1 neuron, **Sigmoid** activation

### **Model Training Results**
After training the model for **100 epochs**, we obtained the following results:

- **Loss:** 0.5569
- **Accuracy:** 72.47%

---

## **4. Optimization Attempts**
To improve model performance beyond **75% accuracy**, we made the following modifications:

1. **Increased the number of neurons per layer** (from 80 → 100, 30 → 50).
2. **Added an additional hidden layer** to improve feature extraction.
3. **Tried different activation functions** (ReLU, Sigmoid, Tanh).
4. **Extended training epochs** from 100 to 150.

The best-performing model achieved an accuracy of **72.47%**, which is < 75%.

---

## **5. Conclusion**
- The final model provides a reasonable prediction accuracy of **72.47%**.
- Further improvements can be made by:
  - Experimenting with **hyperparameter tuning**.
  - Using **dropout layers** to prevent overfitting.
  - Exploring different **machine learning models (e.g., Random Forest, XGBoost)** as alternatives to deep learning.

The deep learning approach demonstrates **strong potential** for predicting successful funding applicants for Alphabet Soup. 🚀
