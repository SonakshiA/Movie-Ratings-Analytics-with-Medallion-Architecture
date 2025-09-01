## 📊 Movie Ratings Analytics with Medallion Architecture

This project demonstrates the Medallion Architecture (Bronze → Silver → Gold) using the MovieLens Small Dataset
.
It showcases how raw data is ingested, cleaned, and transformed into analytics-ready tables for insights into movie ratings and genre popularity.

## 🏗️ Architecture Overview

**Bronze Layer 🪙**

* Raw ingestion of CSV files (ratings.csv, movies.csv).
* No transformations, schema-on-read.

**Silver Layer 🥈**

* Clean and curated data.
* Data type casting, timestamp conversion, splitting genres.
* Joined ratings + movies into a unified dataset.

**Gold Layer 🥇**

* Aggregated insights for business consumption: 
    * Top 10 movies by average rating (with ≥ 50 ratings).
    * Most popular genres by rating count.
    * Average rating per genre.

## 📂 Dataset

We use the [MovieLens Latest Small Dataset](https://grouplens.org/datasets/movielens/?utm_source=chatgpt.com):

Files used in this project:
* movies.csv → movieId, title, genres
* ratings.csv → userId, movieId, rating, timestamp
