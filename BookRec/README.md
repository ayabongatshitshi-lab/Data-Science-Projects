# Book Recommendation Engine (K-Nearest Neighbors)

### Project Overview
This project implements a **Book Recommendation System** using the **K-Nearest Neighbors (KNN)** algorithm. Analyzing the Book-Crossings dataset—which includes 1.1 million ratings for over 270,000 books—the model identifies and suggests books that are "closest" in similarity to a given title based on user rating patterns.

### Machine Learning Highlights
*   **Algorithm:** Utilized `sklearn.neighbors.NearestNeighbors` to calculate the cosine similarity between book vectors.
*   **Sparse Data Management:** Handled a large, sparse matrix of user-item interactions to find meaningful clusters of similar books.
*   **Statistical Filtering:** Implemented rigorous data cleaning to ensure recommendation quality, filtering out infrequent raters and unpopular books.

---

### Technical Methodology

#### **1. Data Pre-processing & Cleaning**
*   **Filtering for Significance:** To improve model reliability and reduce noise, I removed:
    *   **Users** with fewer than 200 total ratings.
    *   **Books** with fewer than 100 total ratings.
*   **Pivoting:** Transformed the long-format dataset into a **2D Pivot Table** (User-Item Matrix), filling missing values with zeros to prepare for distance calculations.

#### **2. Model Implementation**
*   **KNN Configuration:** Trained the `NearestNeighbors` model using the **Cosine Similarity** metric, which is highly effective for recommendation systems where the magnitude of ratings matters less than the pattern of the ratings.
*   **Recommendation Function:** Developed a `get_recommends` function that:
    1.  Locates the vector for a specific book title.
    2.  Calculates the "distance" to all other books in the vector space.
    3.  Returns the top 5 most similar titles along with their calculated distance scores.

#### **3. Performance Testing**
*   Verified the model using the "Vampire Chronicles" series, successfully identifying other Anne Rice titles and related supernatural fiction with high accuracy (low distance scores).

---

### View the Analysis: **[View the Book Recommendation Notebook](./fcc_book_recommendation_knn.ipynb)**

### Stack
*   **Library:** Scikit-Learn
*   **Data Handling:** Pandas, NumPy, Scipy (Sparse Matrices)

*   **Algorithm:** K-Nearest Neighbors (Unsupervised)
