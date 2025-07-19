
# Supervised Learning with Support Vector Machines (SVM)

## 🧠 What is SVM?
Support Vector Machines (SVM) are supervised learning algorithms used for both classification and regression tasks. They work by mapping data into a multidimensional space and finding a hyperplane that best separates two classes.

---

## 📌 Key Concepts

- **Hyperplane**: Decision boundary that separates classes.
- **Margin**: Distance between the hyperplane and the nearest data points from each class.
- **Support Vectors**: Closest data points that define the margin.
- **Soft Margin**: Allows misclassification, controlled by parameter **C** (smaller C = more tolerance).
- **Hard Margin**: Less tolerance for misclassification (larger C).

---

## 🔄 Linear vs. Nonlinear Data

- **Linear SVM**: Works when classes are linearly separable.
- **Nonlinear SVM**: Uses **kernel trick** to map data into higher-dimensional space for separation.

---

## 🧰 Kernel Functions (via Scikit-learn)

- **Linear** (default)
- **Polynomial**
- **RBF (Radial Basis Function)**
- **Sigmoid**

---

## 📈 Support Vector Regression (SVR)

- Uses SVM for regression problems.
- Employs an **epsilon-tube** around the prediction curve to distinguish signal from noise.
- Controlled by the **epsilon** parameter.

---

## ✅ Advantages

- Effective in high-dimensional spaces.
- Robust to overfitting.
- Works well for linearly and weakly non-linearly separable data.

---

## ⚠️ Limitations

- Slow training on large datasets.
- Sensitive to:
  - Noise
  - Overlapping classes
  - Choice of kernel and regularization parameters

---

## 💡 Applications

- Image classification and handwritten digit recognition
- Spam filtering, sentiment analysis
- Speech recognition, anomaly detection, noise reduction

---

## 📌 Summary

SVM is a powerful supervised learning method used to find the optimal decision boundary between classes. It can be extended using kernels to solve nonlinear problems, and used for regression with SVR. It's well-suited for many ML problems, though computationally expensive and sensitive to tuning.

