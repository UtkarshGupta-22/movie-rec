# Movie Recommender System

![Python](https://img.shields.io/badge/Python-3.11-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-green)
![Streamlit](https://img.shields.io/badge/Streamlit-Frontend-red)
![Render](https://img.shields.io/badge/Render-Deployed-purple)
![TMDB](https://img.shields.io/badge/TMDB-API-orange)
![Status](https://img.shields.io/badge/Status-Live-success)

An AI-powered full-stack Movie Recommendation Platform that combines content-based filtering, genre-based recommendations, TMDB integration, and a modern interactive user experience.

The system allows users to discover movies, search titles in real time, explore detailed movie information, and receive intelligent recommendations using TF-IDF and cosine similarity.

---

# Live Deployment

### Frontend (Streamlit)

https://movie-rec-kj6vaxp3m6pgwvvwzmqver.streamlit.app/

### Backend (FastAPI + Render)

https://movie-rec-e45h.onrender.com

### API Documentation

https://movie-rec-e45h.onrender.com/docs

---

# Project Overview

This project was built as a complete production-ready movie recommendation system demonstrating:

- Machine Learning Integration
- Recommendation Systems
- FastAPI Backend Development
- Streamlit Frontend Development
- REST API Design
- Cloud Deployment
- Third-Party API Integration

The application combines:

### TF-IDF Content-Based Recommendations

Movies are recommended based on textual similarity.

### Genre-Based Recommendations

Movies with similar genres are recommended as a secondary recommendation layer.

### TMDB Enrichment

All movie posters, metadata, backdrops, and discovery feeds are dynamically fetched using TMDB APIs.

---

# Features

## Dynamic Home Feed

Browse movies across:

- Trending
- Popular
- Top Rated
- Now Playing
- Upcoming

---

## Real-Time Movie Search

Features:

- Dynamic Search
- Keyword Matching
- Autocomplete Suggestions
- TMDB Search Integration
- Poster-Based Results

Example:

```text
Batman
Thor
Avenger
Spider-Man
Interstellar
```

---

## Detailed Movie Pages

Each movie page contains:

- Poster
- Backdrop
- Genres
- Release Date
- Overview
- TMDB Metadata

---

## TF-IDF Recommendation Engine

Uses:

```text
TF-IDF Vectorization
+
Cosine Similarity
```

Workflow:

```text
Selected Movie
      ↓
Vectorization
      ↓
Cosine Similarity
      ↓
Most Similar Movies
      ↓
TMDB Metadata Enrichment
      ↓
Poster Recommendation Display
```

---

## Genre Recommendations

Additional recommendation layer based on movie genres.

Benefits:

- Better recommendation coverage
- Improved movie discovery
- Fallback recommendation support

---

## Fully Cloud Deployed

Frontend:

```text
Streamlit Community Cloud
```

Backend:

```text
Render
```

The application runs completely in the cloud and does not require local execution.

---

# Architecture

```text
User
 │
 ▼
Streamlit Frontend
 │
 ▼
FastAPI Backend
 │
 ├── TF-IDF Recommendation Engine
 │
 ├── Genre Recommendation Engine
 │
 └── TMDB API Integration
 │
 ▼
Movie Recommendations
```

---

# Tech Stack

## Frontend

- Streamlit
- Requests

## Backend

- FastAPI
- Uvicorn
- HTTPX

## Machine Learning

- Scikit-Learn
- TF-IDF Vectorizer
- Cosine Similarity

## Data Processing

- Pandas
- NumPy
- SciPy

## APIs

- TMDB API

## Deployment

- Streamlit Cloud
- Render

---

# Recommendation System

The recommendation engine combines:

## Content-Based Filtering

Uses TF-IDF vectorization on movie metadata and computes similarity using cosine similarity.

## Genre-Based Filtering

Identifies movies sharing similar genres.

## Hybrid Recommendation Strategy

```text
TF-IDF Recommendations
            +
Genre Recommendations
```

This improves recommendation quality and coverage.

---

# Project Structure

```text
movie-rec/
│
├── app.py
├── main.py
├── movies.pkl
├── similarity.pkl
├── requirements.txt
├── runtime.txt
├── README.md
│
└── __pycache__/
```

---

# API Endpoints

## Health Check

```http
GET /health
```

---

## Home Feed

```http
GET /home
```

Parameters:

```text
category
limit
```

---

## Movie Search

```http
GET /tmdb/search
```

Parameters:

```text
query
```

---

## Movie Details

```http
GET /movie/id/{tmdb_id}
```

---

## Genre Recommendations

```http
GET /recommend/genre
```

---

## TF-IDF Recommendations

```http
GET /recommend/tfidf
```

---

## Recommendation Bundle

```http
GET /movie/search
```

Returns:

```text
Movie Details
+
TF-IDF Recommendations
+
Genre Recommendations
```

---

# Deployment

## Frontend

Hosted on Streamlit Cloud.

Responsibilities:

- User Interface
- Search Experience
- Recommendation Display

---

## Backend

Hosted on Render.

Responsibilities:

- Recommendation Logic
- TMDB Communication
- API Processing
- Data Handling

---

# Screenshots

## Home Feed

Add screenshot here.

---

## Search Results

Add screenshot here.

---

## Movie Details

Add screenshot here.

---

## Recommendations

Add screenshot here.

---

# Future Improvements

Planned enhancements:

- User Authentication
- Watchlists
- Favorite Movies
- Collaborative Filtering
- Deep Learning Recommendations
- LLM-Powered Movie Assistant
- Actor & Director Search
- Personalized User Profiles
- Recommendation Analytics

---

# Learning Outcomes

This project demonstrates practical experience in:

- Software Engineering
- Machine Learning
- Recommendation Systems
- FastAPI Development
- REST API Design
- Streamlit Development
- Cloud Deployment
- API Integration
- Production Systems

---

# 👨‍💻 Author

## Utkarsh Gupta

B.Tech Computer Science (Data Science)

PSIT Kanpur

GitHub:

https://github.com/UtkarshGupta-22

LinkedIn:

Add your LinkedIn profile link here.

---

# License

This project is intended for educational, research, and portfolio purposes.

Movie metadata, posters, and related content are provided through TMDB APIs and remain subject to TMDB licensing policies.

---

# Project Status

| Component | Status |
|------------|---------|
| Frontend Deployment | Live |
| Backend Deployment | Live |
| TMDB Integration | Operational |
| Search System | Operational |
| Recommendation Engine | Operational |
| API Documentation | Available |
| Genre Recommendations | Operational |
| TF-IDF Recommendations | Operational |
