# Movie Recommender System

An AI-powered full-stack Movie Recommendation Platform that combines content-based filtering, genre-based recommendations, TMDB integration, and an interactive modern user interface.

The platform enables users to discover movies, search titles in real-time, explore detailed movie information, and receive intelligent recommendations using Natural Language Processing (TF-IDF) and genre similarity analysis.

---

## Live Deployment

### Frontend (Streamlit)

https://movie-rec-kj6vaxp3m6pgwvvwzmqver.streamlit.app/

### Backend API (FastAPI + Render)

https://movie-rec-e45h.onrender.com

### API Documentation (Swagger UI)

https://movie-rec-e45h.onrender.com/docs

---

# Overview

This project was designed and deployed as a complete production-ready movie recommendation platform.

The application combines:

- Machine Learning
- Recommendation Systems
- FastAPI Backend Development
- Streamlit Frontend Development
- REST APIs
- Cloud Deployment
- TMDB API Integration

The recommendation engine uses a hybrid strategy consisting of:

### 1. TF-IDF Content-Based Recommendations

Movies are recommended based on textual similarity using:

- Movie titles
- Content descriptions
- TF-IDF Vectorization
- Cosine Similarity

### 2. Genre-Based Recommendations

Movies sharing similar genres are recommended as an additional recommendation layer.

This hybrid approach improves recommendation coverage and user experience.

---

# Features

## Home Feed

Browse dynamically generated movie collections:

- Trending Movies
- Popular Movies
- Top Rated Movies
- Now Playing
- Upcoming Movies

All data is fetched directly from TMDB.

---

## Real-Time Movie Search

Search movies using title keywords.

Features include:

- Live Search
- Autocomplete Suggestions
- Dynamic Filtering
- Poster Preview
- TMDB Search Integration

Example:

```text
Avenger
Batman
Thor
Interstellar
Spider-Man
```

---

## Detailed Movie Information

Each movie page displays:

- Movie Poster
- Backdrop Image
- Release Date
- Genres
- Overview
- TMDB Metadata

---

## TF-IDF Recommendation Engine

The recommendation system uses:

```text
TF-IDF Vectorization
+
Cosine Similarity
```

Pipeline:

```text
Selected Movie
      ↓
Text Vectorization
      ↓
Cosine Similarity
      ↓
Top Similar Movies
      ↓
TMDB Enrichment
      ↓
Poster-Based Display
```

---

## Genre Recommendation Engine

A secondary recommendation system generates movies belonging to similar genres.

Benefits:

- Better recommendation coverage
- Fallback recommendation support
- Enhanced movie discovery

---

## Fully Interactive Interface

Features:

- Responsive Layout
- Sidebar Controls
- Movie Cards
- Poster-Based Navigation
- Dynamic Recommendations
- Query-Based Routing

---

# System Architecture

```text
┌─────────────────────────┐
│      User Browser       │
└────────────┬────────────┘
             │
             ▼
┌─────────────────────────┐
│ Streamlit Frontend      │
│ User Interface Layer    │
└────────────┬────────────┘
             │
             │ REST API Calls
             ▼
┌─────────────────────────┐
│ FastAPI Backend         │
│ Recommendation Engine   │
└────────────┬────────────┘
             │
             ▼
┌─────────────────────────┐
│ TF-IDF + Genre Logic    │
└────────────┬────────────┘
             │
             ▼
┌─────────────────────────┐
│ TMDB API Integration    │
└─────────────────────────┘
```

---

# Recommendation Workflow

```text
User Selects Movie
            │
            ▼
Fetch Movie Details
            │
            ▼
Generate TF-IDF Recommendations
            │
            ▼
Generate Genre Recommendations
            │
            ▼
TMDB Metadata Enrichment
            │
            ▼
Display Recommendations
```

---

# Technology Stack

## Frontend

- Streamlit
- Requests
- Python

---

## Backend

- FastAPI
- Uvicorn
- HTTPX
- Python

---

## Machine Learning

- Scikit-Learn
- TF-IDF Vectorizer
- Cosine Similarity
- Pandas
- NumPy
- SciPy

---

## External APIs

### TMDB API

Used for:

- Movie Search
- Posters
- Backdrops
- Metadata
- Trending Movies
- Popular Movies
- Top Rated Movies
- Upcoming Movies

---

# Project Structure

```text
movie-rec/
│
├── app.py
├── main.py
├── requirements.txt
├── movies.pkl
├── similarity.pkl
├── .env
│
├── __pycache__/
│
└── deployment/
    ├── Streamlit Cloud
    └── Render
```

---

# API Endpoints

## Health Check

```http
GET /health
```

Response:

```json
{
  "status": "ok"
}
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

Supported Categories:

```text
trending
popular
top_rated
now_playing
upcoming
```

---

## Search Movies

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

Returns:

- Poster
- Backdrop
- Genres
- Release Date
- Overview

---

## Genre Recommendations

```http
GET /recommend/genre
```

Parameters:

```text
tmdb_id
limit
```

---

## TF-IDF Recommendations

```http
GET /recommend/tfidf
```

Parameters:

```text
title
top_n
```

---

## Combined Recommendation Endpoint

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

in a single API response.

---

# ☁️ Deployment Architecture

## Frontend Deployment

Platform:

```text
Streamlit Community Cloud
```

Responsibilities:

- User Interface
- Search Experience
- Recommendation Display
- Navigation

---

## Backend Deployment

Platform:

```text
Render
```

Responsibilities:

- Recommendation Logic
- TMDB Communication
- API Processing
- Data Handling

---

# Performance Highlights

- Full Cloud Deployment
- FastAPI-Based Backend
- Modular Architecture
- TMDB Integration
- Real-Time Search
- Hybrid Recommendation Engine
- Interactive Movie Exploration
- Scalable API Design
- Production-Ready Deployment

---

# Future Enhancements

Planned improvements include:

### User Features

- User Accounts
- Watchlists
- Favorites
- Recently Viewed Movies

### Recommendation Improvements

- Collaborative Filtering
- Deep Learning Recommendations
- Personalized User Preferences

### Advanced Search

- Actor Search
- Director Search
- Genre Filters
- Year Filters

### AI Integration

- Natural Language Movie Search
- AI Movie Assistant
- LLM-Based Movie Suggestions

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
- Data Processing
- Production Systems

---

# Author

### Utkarsh Gupta

B.Tech Computer Science (Data Science)

PSIT Kanpur

### GitHub

https://github.com/UtkarshGupta-22

---

# License

This project is intended for educational, research, and portfolio purposes.

Movie metadata, posters, and related content are provided by TMDB and remain subject to TMDB licensing and usage policies.

---

# Project Status

| Component | Status |
|------------|---------|
| Frontend Deployment | Live |
| Backend Deployment | Live |
| TMDB Integration | Operational |
| Search System | Operational |
| Recommendation Engine | Operational |
| Swagger Documentation | Available |
| Genre Recommendations | Operational |
| TF-IDF Recommendations | Operational |
