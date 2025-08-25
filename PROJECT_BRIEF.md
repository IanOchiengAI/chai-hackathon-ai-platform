# AI Engine: Project Brief & System Architecture

## 1. The High-Level Vision

Our goal is to build the "brain" for the Youth Educated mentorship platform. This brain will accomplish two critical tasks:
1.  **Make intelligent decisions** to match individual mentees with the best possible mentors.
2.  **Generate high-level insights** from all platform data to help the YE staff make strategic, data-driven decisions.

To do this, we are building two distinct but connected components.

---

## 2. The Core Components

### Component A: The Matching Engine ("The Decision-Maker")

*   **Purpose:** To be the smart matchmaker of the platform. This is the core AI feature that users will experience directly.

*   **How it Works:**
    *   **Input:** It takes the ID of a single mentee.
    *   **Process:** It uses a content-based filtering algorithm (Cosine Similarity) to compare that mentee's profile (their skills, goals, and interests) against every available mentor in the system.
    *   **Output:** It produces a simple, ranked list of the top 3-5 most compatible mentor IDs.

*   **Technology:** This will be a Python script (`matching_engine/engine.py`) using the `Pandas` and `Scikit-learn` libraries. It has no user interface; it's a pure logic engine.

### Component B: The Impact Dashboard ("The Insight-Generator")

*   **Purpose:** To be the mission control center for the YE staff. It provides a real-time, bird's-eye view of the entire mentorship program's health and performance.

*   **How it Works:**
    *   **Input:** It takes the *entire* user database as its input.
    *   **Process:** It analyzes and aggregates all user data to find patterns and calculate key metrics. It answers questions like, "What skills are most in-demand?" and "Where are our mentor supply gaps?".
    *   **Output:** It produces a visual, interactive web page with charts, graphs, and key numbers that are easy to understand at a glance.

*   **Technology:** This will be a Python script (`dashboard/app.py`) using the `Streamlit` library, which automatically generates a web interface.

---

## 3. How They Work Together: The Data Flow

The two components are separate, but they are connected by a **Single Source of Truth**: the main user database.

Here is the step-by-step data journey:

1.  **Data Collection:** A new user (mentor or mentee) signs up on the main website (built by Dylan).
2.  **Central Database:** Their profile information is saved to a central user database. For our MVP, this can be our `data/users.csv` file.
3.  **The Connection:**
    *   When a mentee logs in to their dashboard, the website **calls the Matching Engine**. The Matching Engine reads from the Central Database, performs its calculation, and returns the top mentor IDs to the website.
    *   When a YE staff member wants to see program performance, they open the **Impact Dashboard**. The Impact Dashboard reads from the same Central Database, performs its analysis, and displays the insights as a webpage.

**In short: Both "brains" read from the same central data source. The Matching Engine works on a micro-level (one user at a time) to make decisions, while the Impact Dashboard works on a macro-level (all users at once) to generate insights.**
