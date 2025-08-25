# CHAI Hackathon: AI Engine

This repository contains the core AI and Machine Learning components for the Youth Educated mentorship platform, built for the CHAI Hackathon.

## Overview

This project is the "brain" of the platform and consists of two main parts:
1.  **The Matching Engine:** A Python script that uses a content-based recommendation algorithm to match mentees with suitable mentors.
2.  **The Impact Dashboard:** A Streamlit web app that provides real-time analytics and insights on the platform's data.

---

## Getting Started

Follow these steps to set up your local development environment.

### Prerequisites
- Python 3.8+

### Setup

1.  **Clone the repository:**
    `git clone https://github.com/YOUR_USERNAME/chai-hackathon-ai-engine.git`
    `cd chai-hackathon-ai-engine`

2.  **Create and activate a virtual environment:**
    `python3 -m venv venv`
    `source venv/bin/activate`

3.  **Install the required libraries:**
    `pip install -r requirements.txt`

---

## How to Run

### Matching Engine (Test)
To test the matching algorithm with the sample data, run:
`python matching_engine/engine.py`

### Impact Dashboard
To launch the Streamlit analytics dashboard locally, run:
`streamlit run dashboard/app.py`

---

## My Initial To-Do List
- [x] Set up GitHub repository and file structure
- [ ] Finalize the data schema (skills, interests, goals) with Sheila
- [ ] Populate `data/users.csv` with realistic test data
- [ ] Build the first prototype of the matching algorithm in `engine.py`
- [ ] Build the first prototype of the dashboard in `app.py`
