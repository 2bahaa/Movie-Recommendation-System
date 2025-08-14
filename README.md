# 🎬 Movie Recommendation System – MovieLens 100K

## 📌 Project Overview
This project implements a **collaborative filtering-based movie recommendation system** using the [MovieLens 100K dataset](https://grouplens.org/datasets/movielens/100k/).  
The system recommends movies to a target user based on **user similarity** and evaluates its performance using **Precision@K**.

It also includes **dataset exploration and visualization** to gain insights into user preferences, movie popularity, and rating distributions.

---

## 📂 Dataset Description
The MovieLens 100K dataset contains:
- **100,000 ratings** (1–5) from 943 users on 1,682 movies.
- Each user has rated at least 20 movies.
- Additional metadata such as:
  - Movie titles, release years, genres
  - User demographic info (age, gender, occupation, zip code)

**Main Files Used:**
- `u.data` → user–item ratings
- `u.item` → movie details (title, genres, release year)
- `u.user` → user demographic information

---

## ⚙️ Features Implemented
### 1. **Data Loading & Preprocessing**
- Reads and merges ratings, movie metadata, and user demographics.
- Creates a **user–item rating matrix** for collaborative filtering.

### 2. **Exploratory Data Analysis (EDA)**
- Ratings distribution
- Most popular movies
- Genre frequency
- Active users with the most ratings

### 3. **User-Based Collaborative Filtering**
- Calculates **cosine similarity** between users.
- Recommends top-N **unseen movies** for a given user.
- Avoids recommending movies already rated by the user.

### 4. **Evaluation**
- Uses **Precision@K** to measure performance.
- Optionally supports:
  - Item-based collaborative filtering
  - Matrix factorization (SVD)

---

## 📊 Example Insights
- **Most Popular Genres**: Drama, Comedy, Action
- **Most Rated Movies**: *Star Wars (1977)*, *Contact (1997)*
- Ratings are slightly **skewed towards higher values**.

---

## 🛠 Tech Stack
- **Python**
- **Pandas** – Data handling
- **NumPy** – Matrix operations
- **Matplotlib / Seaborn** – Data visualization
- **Scikit-learn** – Similarity computation & evaluation metrics

---

## 🚀 Installation & Usage
### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/movie-recommendation-system.git
cd movie-recommendation-system
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Place the Dataset
Download [MovieLens 100K dataset](https://grouplens.org/datasets/movielens/100k/)  
Extract and place files (`u.data`, `u.item`, `u.user`) in the `data/` folder.

### 4. Run the Jupyter Notebook
```bash
jupyter notebook Movie_Recommendation_System.ipynb
```

---

## 📈 Evaluation Metric
We use **Precision@K** to measure how many of the recommended movies are actually relevant (rated positively in the test set).

Example:
```
Average Precision@5: 0.0437
```
A higher score means better recommendation accuracy.

---

## 🔮 Future Improvements
- Implement **hybrid filtering** (combine user and item similarity).
- Add **content-based recommendations** using genres & tags.
- Use **matrix factorization** (SVD, ALS) for better scalability.
- Deploy as a **web application** using Flask or Streamlit.

---

## 📜 License
This project is licensed under the **MIT License** – see the LICENSE file for details.
