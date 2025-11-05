# 🎬 Movie Metadata Analysis & Recommendation System (Django)

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-4.2-green.svg)](https://www.djangoproject.com/)
[![Machine Learning](https://img.shields.io/badge/ML-Recommendation_System-orange.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> 🎥 A full-fledged **Movie Recommendation Web App** built with **Django**, combining both **Content-Based** and **Collaborative Filtering** techniques to deliver smart and personalized movie suggestions.

---

## 🧠 Overview

This project bridges **Data Science** and **Web Development**, integrating ML-based recommendation algorithms with a Django web interface.
Users can search for movies, get similar recommendations, and receive personalized movie suggestions — all within an interactive and lightweight web app.

---

## ✨ Features

✅ **Content-Based Filtering** – Uses TF-IDF and cosine similarity on movie overviews
✅ **Collaborative Filtering** – Uses user–user similarity for personalized suggestions
✅ **Django Web UI** – Clean and easy-to-use web interface
✅ **Data Cleaning & Visualization** – Handles missing data and visualizes rating distributions
✅ **Customizable Dataset** – Works with your own movie and rating CSVs
✅ **Scalable Design** – Easily extendable for future ML model upgrades

---

## 🧩 Tech Stack

| Category             | Technologies                 |
| -------------------- | ---------------------------- |
| **Backend**          | Django 4.2                   |
| **Machine Learning** | scikit-learn, pandas, numpy  |
| **Visualization**    | matplotlib, seaborn          |
| **Frontend**         | HTML, CSS (Django Templates) |
| **Database**         | SQLite (default Django DB)   |

---

## 📂 Project Structure

```
movie_recommender_django/
│
├── manage.py
├── requirements.txt
├── README.md
├── data/
│   ├── movies_metadata.csv
│   └── ratings.csv
│
├── movie_site/
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
└── recommender/
    ├── utils.py         # Core ML logic (TF-IDF + Collaborative Filtering)
    ├── views.py         # Django views
    ├── urls.py          # URL routing
    ├── templates/       # HTML templates (UI)
    └── static/          # Optional CSS/JS files
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/movie-recommender-django.git
cd movie-recommender-django
```

### 2️⃣ Create a Virtual Environment

```bash
python -m venv venv
```

Activate it:

* **Windows:** `venv\Scripts\activate`
* **Mac/Linux:** `source venv/bin/activate`

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Add Dataset

Place your datasets inside the `data/` folder:

* `movies_metadata.csv`
* `ratings.csv`

📊 Download dataset from [The Movies Dataset – Kaggle](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset)

### 5️⃣ Apply Migrations

```bash
python manage.py migrate
```

### 6️⃣ Run the Server

```bash
python manage.py runserver
```

Now open your browser and visit 👉 [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

---

## 🌐 Web Pages

| Route               | Description                                    |
| ------------------- | ---------------------------------------------- |
| `/`                 | Homepage                                       |
| `/recommend/title/` | Get content-based movie recommendations        |
| `/recommend/user/`  | Get collaborative (user-based) recommendations |

---

## 🧠 How It Works

### 🎯 Content-Based Recommendation

* Extracts **movie overviews**
* Converts text to **TF-IDF vectors**
* Computes **cosine similarity** between movies
* Returns top 10 similar movies

### 👥 Collaborative Filtering

* Builds a **user–movie rating matrix**
* Computes **user–user similarity** using cosine distance
* Suggests movies rated by similar users

---

## 📈 Example Workflow

1. User enters a movie title like *Inception* 🎞️
2. App computes similarity scores using TF-IDF
3. Displays top 10 similar movies
4. Users can also enter a user ID for personalized recommendations

---

## 🛠️ Future Enhancements

* 🔍 Fuzzy title matching (autocomplete + typo tolerance)
* 💾 Precompute TF-IDF vectors with `joblib` for faster startup
* 🎨 Enhanced UI with TailwindCSS or Bootstrap
* 🐳 Dockerfile and CI/CD integration
* ☁️ Deployment to Render / Vercel / Railway
* 📊 Analytics dashboard for data visualization

---

## 🧑‍💻 Author

**Dharanish**
🎓 Student | 💡 Developer | 🔬 Hardware Research Enthusiast
Passionate about **AI, Data Science, and Embedded Systems**


## 🏷️ License

This project is licensed under the **MIT License** — you’re free to use, modify, and distribute it with proper attribution.

---

