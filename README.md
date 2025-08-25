# AI Mentorship Platform for Youth Educated (CHAI Hackathon)

This repository contains the AI components for the Youth Educated mentorship matching platform, built for the 2025 CHAI Hackathon.

## 🚀 Project Goal

To build a web-based platform that uses an AI recommendation engine to intelligently match mentees with suitable mentors, and provides a dashboard to track the program's impact.

## AI Components

This repository contains two core AI components:

1.  **The Matching Engine (`/src/matching_engine`):** A Python script that uses content-based filtering (Cosine Similarity) to recommend mentors to mentees based on their profiles.
2.  **The Impact Dashboard (`/src/dashboard`):** A Streamlit application that provides a real-time, visual overview of the platform's data and key metrics.

## 🛠️ Setup & Installation

To run this project locally, please follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/YourUsername/chai-hackathon-ai-platform.git
    cd chai-hackathon-ai-platform
    ```

2.  **Create and activate a virtual environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required libraries:**
    ```bash
    pip install -r requirements.txt
    ```

## 🏃‍♀️ How to Run

### Matching Engine (Test)

To run the test script for the matching engine:
```bash
python src/matching_engine/matcher.py
