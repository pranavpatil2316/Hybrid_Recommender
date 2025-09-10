---

# Hybrid Recommender System

This project implements a **Hybrid Recommender System** that combines **Collaborative Filtering (CF)** and **Content-Based Filtering (CBF)** to generate personalized recommendations.
The system is demonstrated on the **MovieLens dataset** and extended with hybrid scoring and visualization features.

---

## 📌 Features

* **Collaborative Filtering (CF):**
  Uses **Matrix Factorization (SVD)** to predict user-item ratings.

* **Content-Based Filtering (CBF):**
  Uses **TF-IDF vectorization** of movie genres/tags combined with cosine similarity.

* **Hybrid Model:**
  Combines CF and CBF scores with a tunable parameter `alpha`.

  * `alpha=1.0` → pure CF
  * `alpha=0.0` → pure CBF
  * `0 < alpha < 1` → hybrid of both

* **Top-N Recommendations:**
  For each user, the system outputs the **Top-10 recommended movies** with scores, titles, and genres.

* **Visualizations:**

  * **Bar chart** of Top-10 recommendations for a sample user.
  * **Comparison chart** of CF vs Hybrid performance.
  * **Rating distribution histogram** for dataset insights.

---

## 📂 Files

* **`hybrid_recommender.ipynb`** → Jupyter Notebook with full implementation.
* **MovieLens dataset** (used inside notebook).

---

## 🚀 How to Run

1. Clone/download this repository.
2. Open the notebook:

   ```bash
   jupyter notebook hybrid_recommender.ipynb
   ```
3. Run all cells step by step.
4. Try changing `alpha` in the `hybrid_recommend()` function to see how recommendations shift.

---

## ⚙️ Example Output

Top-10 recommendations for a user:

```
movieId | Score   | Title                          | Genres
------------------------------------------------------------
  2571  | 0.9821  | The Matrix (1999)              | Action|Sci-Fi
  1196  | 0.9654  | Star Wars: Episode V (1980)    | Action|Adventure|Sci-Fi
  1210  | 0.9523  | Star Wars: Episode VI (1983)   | Action|Adventure|Sci-Fi
  2858  | 0.9456  | American Beauty (1999)         | Drama
  593   | 0.9321  | Silence of the Lambs (1991)    | Thriller
   ...  |   ...   | ...                            | ...
```

---

## 🛠️ Requirements

* Python 3.8+
* Libraries:

  ```
  numpy
  pandas
  scikit-learn
  matplotlib
  scipy
  ```

---
