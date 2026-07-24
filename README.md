# 🎬 Movie Recommendation System

An end-to-end **content-based Movie Recommendation System** built using **Natural Language Processing (NLP)** and machine learning techniques.

The system analyzes movie metadata using **TF-IDF Vectorization** and **Cosine Similarity** to recommend movies that are similar to a user's selected title. The project combines a machine learning recommendation engine with a **FastAPI backend**, **Streamlit frontend**, and **TMDB API integration** to provide an interactive movie discovery experience.

---

## 🚀 Features

* Content-based movie recommendation
* Movie search functionality
* TF-IDF-based text feature extraction
* Cosine Similarity-based recommendation ranking
* REST API built with FastAPI
* Interactive web interface using Streamlit
* Movie posters and metadata fetched from TMDB
* Separation of ML, backend, and frontend components
* Deployment-ready project structure

---

## 🧠 Recommendation System

The recommendation engine uses a **content-based filtering approach**.

Movie metadata is cleaned and transformed into textual features representing each movie. These features are converted into numerical vectors using **TF-IDF (Term Frequency–Inverse Document Frequency)**.

Cosine Similarity is then calculated between movie vectors to determine how closely movies are related.

### Recommendation Pipeline

```text
Movie Dataset
      │
      ▼
Data Cleaning & Preprocessing
      │
      ▼
Feature Engineering
      │
      ▼
TF-IDF Vectorization
      │
      ▼
Cosine Similarity
      │
      ▼
Similarity Ranking
      │
      ▼
Top Movie Recommendations
```

When a user selects a movie, the system retrieves its similarity scores and returns the movies with the highest similarity values.

---

## 🏗️ Application Architecture

```text
                    ┌─────────────────────┐
                    │     Movie Dataset   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Recommendation      │
                    │ Engine (NLP + ML)   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      FastAPI        │
                    │      Backend        │
                    └──────────┬──────────┘
                               │
                     REST API  │
                               ▼
                    ┌─────────────────────┐
                    │     Streamlit       │
                    │      Frontend       │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      TMDB API       │
                    │ Posters & Metadata  │
                    └─────────────────────┘
```

---

## 🛠️ Tech Stack

| Technology       | Purpose                               |
| ---------------- | ------------------------------------- |
| **Python**       | Core programming language             |
| **Pandas**       | Data preprocessing and manipulation   |
| **NumPy**        | Numerical operations                  |
| **Scikit-learn** | TF-IDF and Cosine Similarity          |
| **FastAPI**      | Backend REST API                      |
| **Streamlit**    | Interactive frontend                  |
| **TMDB API**     | Movie posters and additional metadata |
| **Uvicorn**      | FastAPI ASGI server                   |

---

## 📁 Project Structure

```text
movie-recommendation-system/
│
├── app.py
├── main.py
├── requirements.txt
├── .gitignore
│
├── df.pkl
├── indices.pkl
│
└── README.md
```

> The project structure can be updated as additional deployment or configuration files are introduced.

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd movie-recommendation-system
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

### 3. Activate the Environment

**Windows**

```bash
venv\Scripts\activate
```

**macOS / Linux**

```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Application

### Start the FastAPI Backend

```bash
uvicorn main:app --reload
```

The backend will start locally, and FastAPI's interactive API documentation can be used to test the available endpoints.

### Start the Streamlit Frontend

Open another terminal and run:

```bash
streamlit run app.py
```

The Streamlit application will then be available in your browser.

---

## 🔌 API Functionality

The FastAPI backend is responsible for exposing the recommendation engine to the frontend.

Core functionality includes:

* Searching for movies
* Retrieving movie recommendations
* Returning recommendation results to the Streamlit application

The API architecture keeps the recommendation logic separated from the user interface, making the project easier to maintain and extend.

---

## 🎞️ TMDB Integration

The application integrates with **The Movie Database (TMDB) API** to enrich recommendation results.

TMDB is used to retrieve information such as:

* Movie posters
* Movie details
* Additional metadata

This allows the recommendation engine to focus on generating relevant results while TMDB improves the presentation of those results.

---

## 📸 Application Preview

Add screenshots of the application here once the UI is finalized.

```text
screenshots/
├── home.png
├── search.png
└── recommendations.png
```

Screenshots are particularly useful for recruiters because they can understand the application without having to run the project locally.

---

## 🔮 Future Improvements

Potential improvements include:

* Add collaborative filtering
* Build a hybrid recommendation system
* Add user authentication
* Store user preferences and recommendation history
* Add ratings and popularity-based recommendations
* Improve movie search and filtering
* Add caching for external API requests
* Containerize the application using Docker
* Deploy the frontend and backend to cloud services

---

## 🎯 Learning Outcomes

This project provided hands-on experience with:

* Building recommendation systems
* Natural Language Processing
* Content-based filtering
* TF-IDF Vectorization
* Cosine Similarity
* Data preprocessing and feature engineering
* REST API development with FastAPI
* Frontend development with Streamlit
* Third-party API integration
* Connecting ML models with production-style applications
* Structuring an end-to-end machine learning project

---

## 👨‍💻 Author

**Arth Patel**

Computer Engineering Graduate | AI & Data Science

---

⭐ If you found this project useful, consider giving the repository a star.
