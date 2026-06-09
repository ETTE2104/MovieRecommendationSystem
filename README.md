# Movie Recommendation System (Full-Stack & Microservices)

A comprehensive Full-Stack Movie Recommendation System that analyzes user behavioral data to deliver highly personalized, real-time movie and TV show suggestions. This project was developed as a graduation thesis for a Bachelor's Degree in Information Technology.

---

## 🚀 Tech Stack & System Architecture

The system is built on a **Microservices Architecture** to separate the user interface, business logic, and heavy AI/Machine Learning computation components.

* **AI Engine (Recommendation Service):** Python, Flask, Pandas, NumPy, Scikit-learn, Surprise.
* **Business Backend:** Node.js, Express.js, JSON Web Token (JWT) for stateless authentication.
* **Frontend (User Interface):** React.js (Single Page Application), Swiper.js, Chart.js.
* **Database:** MongoDB (NoSQL database for flexible user-interaction storage).

---

## 🧠 Recommendation Algorithms Implemented

To deliver accurate and diverse recommendations while handling common industry challenges, the system integrates a **Hybrid Mechanism**:

1.  **Demographic Filtering:** Utilizes TMDB's Weighted Rating formula to display popular/top-rated movies on the homepage, successfully solving the **User Cold-Start problem** for new accounts.
2.  **Content-Based Filtering:** Analyzes movie metadata text (genres, cast, keywords, directors). Implements an expanded NLTK custom stop-words list and a weighted token mechanism, utilizing **TF-IDF Vectorization** and **Cosine Similarity** to match movie content.
3.  **Collaborative Filtering (Item-Based):** Constructs a massive User-Item interaction matrix based on rating histories. Leverages the **SVD (Singular Value Decomposition)** matrix factorization technique via the Surprise library to uncover latent user preferences.
4.  **Hybrid Recommendation System:** Combines Content-Based (50%) and Collaborative Filtering (50%) candidates per liked movie, incorporating a smart backfill (backfill mechanism) and random shuffling to break the "filter bubble" and maximize discovery.

---

## 📁 Repository Structure

```text
├── AI_Engine/                  # Python Flask Server for ML modeling (.pkl files)
├── Backend/                     # Node.js Express Server & MongoDB Schemas
├── Frontend/                    # React.js Client SPA Source Code
├── DATN.docx                    # Complete Graduation Thesis Documentation
└── Slide_ThuyetTrinh.pptx       # Graduation Project Presentation Slides
