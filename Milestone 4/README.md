# Employee Wellness Management Analytics

## MoodMentor – AI-Powered Emotional Wellness System

MoodMentor is an AI-powered employee wellness application designed to help employees understand and monitor their emotional well-being through **mood tracking, journal analysis, sentiment analysis, emotion detection, personalized recommendations, wellness chat, and historical analytics**.

The project integrates a **Streamlit frontend, Python backend, NLP/ML pipeline, PostgreSQL database, authentication system, recommendation engine, and reporting functionality** into a single application.

---

##  Project Overview

Employee well-being can have a significant impact on productivity, engagement, and overall workplace experience. MoodMentor provides employees with a private platform where they can record their moods or describe their feelings through text.

The system processes the user's input using NLP techniques and determines:

* Sentiment
* Detected emotion
* Emotion confidence
* Mood classification
* Personalized wellness recommendation

The analysis results are stored in the database and can later be used for **historical analysis, mood trends, dashboards, and reports**.

---

## Milestone 4 – Final Integration, Testing & Enhancement

Milestone 4 focuses on integrating and validating the complete MoodMentor application.

### Main objectives completed

* Integrated frontend and backend components
* Integrated authentication and session handling
* Integrated NLP and emotion analysis
* Integrated sentiment analysis
* Integrated recommendation system
* Integrated PostgreSQL database
* Implemented direct text analysis
* Implemented CSV/TXT file analysis
* Implemented mood history
* Implemented mood calendar
* Implemented dashboard analytics
* Implemented historical mood trends
* Implemented emotion visualizations
* Implemented PDF report generation
* Added wellness chat functionality
---

#  Complete System Workflow

```text
                    USER
                     │
                     ▼
             ┌─────────────────┐
             │   Streamlit UI  │
             └────────┬────────┘
                      │
          ┌───────────┴───────────┐
          │                       │
          ▼                       ▼
    Direct Text Input       CSV / TXT Upload
          │                       │
          └───────────┬───────────┘
                      ▼
             ┌─────────────────┐
             │   Backend API   │
             └────────┬────────┘
                      ▼
             ┌─────────────────┐
             │ Text Processing │
             │ & Preprocessing │
             └────────┬────────┘
                      ▼
             ┌─────────────────┐
             │ Sentiment       │
             │ Analysis        │
             │ (VADER)         │
             └────────┬────────┘
                      ▼
             ┌─────────────────┐
             │ NLP / Emotion   │
             │ Classification  │
             │ (Transformer)   │
             └────────┬────────┘
                      ▼
             ┌─────────────────┐
             │ Final Emotion & │
             │ Sentiment       │
             └────────┬────────┘
                      ▼
             ┌─────────────────┐
             │ Recommendation  │
             │ Engine          │
             └────────┬────────┘
                      ▼
             ┌─────────────────┐
             │ PostgreSQL DB   │
             │    (Neon)       │
             └────────┬────────┘
                      ▼
             ┌─────────────────┐
             │ Dashboard /     │
             │ History /       │
             │ Reports         │
             └─────────────────┘
```

---

#  Key Features

## 1. User Authentication

MoodMentor provides secure authentication functionality.

### Features

* User registration
* Email verification using OTP
* Login
* Password hashing
* Forgot password
* Password reset using OTP
* JWT-based authentication
* Employee and Manager roles
* Session management
* Logout

Passwords and authentication information are not stored as plain text.

---

## 2. Mood Tracking

Employees can manually select their current mood.

Supported mood categories include:

*  Happy
*  Neutral
*  Sad
*  Stress
*  Angry
*  Fear

The selected mood is stored in the database and used for historical analysis.

---

## 3. Journal-Based Emotion Analysis

Employees can write about their feelings using the Journal section.

Example:

```text
I had a very stressful day because of multiple deadlines,
but I managed to complete my work successfully.
```

The text is sent to the backend for NLP processing.

The system returns:

* Sentiment
* Emotion
* Confidence score
* Emotion probability scores
* Recommendation

The result is then stored in the database.

---

#  NLP & Machine Learning Pipeline

MoodMentor uses multiple NLP techniques to understand employee text.

## Text Preprocessing

The input text is processed before analysis.

The preprocessing pipeline handles elements such as:

* Text normalization
* Tokenization
* Cleaning
* Special characters
* Numbers
* Emojis
* Punctuation
* Multilingual text handling

---

## Sentiment Analysis – VADER

**VADER (Valence Aware Dictionary and sEntiment Reasoner)** is used for sentiment analysis.

It generates sentiment scores including:

* Positive
* Negative
* Neutral
* Compound score

The compound sentiment score is used as part of the overall sentiment analysis.

---

## Emotion Detection – BERT Transformer Model

A transformer-based NLP model is used to identify the emotional context of the user's text.

The model analyzes contextual relationships between words rather than relying only on individual keywords.

The system generates emotion probabilities and identifies the emotion with the highest confidence.

---

## spaCy

spaCy is used as part of the NLP processing pipeline for text processing and linguistic analysis.

It assists with preprocessing and understanding the structure of the input text.

---

#  Recommendation System

After detecting the user's sentiment and emotion, MoodMentor generates a wellness recommendation.

Recommendations are based on the detected emotional state.

For example:

```text
Detected Emotion → Stress

Recommendation:
Take a short break, practice deep breathing,
and divide your workload into smaller manageable tasks.
```

The recommendation engine is integrated with the analysis workflow so that recommendations are generated from actual analysis results.

---

#  Wellness Chat

MoodMentor includes a wellness chat interface where employees can communicate with an AI-powered assistant.

The chat provides a supportive space for users to discuss their feelings.

The chat maintains recent conversation history during the session.

> The wellness chat is intended for general emotional support and is not a substitute for professional medical or psychological care.

---

#  Employee Dashboard

The employee dashboard provides an overview of historical emotional data.

### Dashboard features

* Mood distribution
* Mood trend over time
* Detected emotion statistics
* Recent activity
* Confidence scores
* Historical mood information
* Date-range selection
* PDF report generation

---

# Mood Calendar

The Home section contains a calendar that displays mood information for different dates.

Each day can display:

* Date
* Mood emoji
* Mood category
* Entry time

Users can navigate between previous and upcoming months.

---

# Mood Analytics

MoodMentor converts mood categories into numerical values for trend analysis.

```text
Happy     →  2
Neutral   →  0
Sad       → -1
Stress    → -1
Angry     → -2
Fear      → -2
```

These values are used to visualize emotional trends over time.

The dashboard provides:

* Mood distribution
* Mood trend
* Emotion frequency
* Recent activity

---

#  PDF Report Generation

Users can generate a PDF wellness report from their historical mood data.

The report contains:

* Username
* Selected date range
* Number of entries
* Mood summary
* Recommendation
* Mood
* Emotion
* Confidence
* Entry time
* Source of entry

The generated report can be downloaded from the application.

---

#  File-Based Analysis

MoodMentor supports file-based NLP analysis.

Supported formats:

```text
.csv
.txt
```

The uploaded file is sent to the backend NLP endpoint for processing.

The system then:

1. Reads the uploaded content
2. Preprocesses the text
3. Performs sentiment analysis
4. Performs emotion classification
5. Generates recommendation
6. Stores the result
7. Displays the analysis to the user

---

#  Database

The application uses a PostgreSQL database hosted using **Neon PostgreSQL**.

The database stores application information such as:

* User accounts
* User roles
* Authentication information
* OTP information
* Mood logs
* Journal entries
* Sentiment results
* Emotion results
* Confidence scores
* Analysis source
* Dates and timestamps

Sensitive database credentials are stored using environment variables and are **not included in the repository**.

---

#  Security

Security was considered during the development and integration of the application.

Implemented security-related features include:

* Password hashing
* JWT authentication
* OTP verification
* Protected backend endpoints
* Role-based access
* Session handling
* Environment variables for sensitive configuration

The repository does not contain:

* Database passwords
* API keys
* JWT secrets
* Email passwords
* Other confidential credentials

---

#  Testing

The final milestone included integration and functional testing of the major application components.

## Input Testing

The NLP pipeline was tested using:

* Valid text
* Empty input
* Invalid input
* Short text
* Long text
* Text containing emojis
* Text containing numbers
* Text containing punctuation
* Text containing special characters
* Multilingual text
* CSV files
* TXT files

---

## Authentication Testing

The authentication workflow was tested for:

* New user registration
* Existing username
* Existing email
* Password validation
* OTP verification
* Invalid OTP
* Expired/invalid verification code
* Login with valid credentials
* Login with invalid credentials
* Forgot password
* Password reset
* Logout

---

## API Testing

The backend APIs were tested for:

* Valid requests
* Invalid requests
* Authentication headers
* Missing authentication
* Backend availability
* NLP analysis
* File analysis
* Wellness chat
* Error responses

---

## Database Testing

Database operations were tested for:

* User creation
* User retrieval
* Mood insertion
* Journal entry storage
* Mood history retrieval
* Monthly mood retrieval
* Employee mood retrieval
* Latest mood retrieval

---

# 🧩 Technology Stack

## Frontend

* Python
* Streamlit
* HTML/CSS
* Matplotlib

## Backend

* Python
* FastAPI
* REST APIs

## NLP / Machine Learning

* Transformer-based NLP model
* BERT-based architecture
* VADER Sentiment Analysis
* spaCy

## Database

* PostgreSQL
* Neon PostgreSQL

## Authentication

* JWT
* bcrypt/password hashing
* OTP
* SMTP

## Reporting

* PDF generation

## Development Environment

* Google Colab
* GitHub



#  Application Workflow

### Employee Workflow

```text
Register
   ↓
Email OTP Verification
   ↓
Login
   ↓
Home Dashboard
   ↓
Select Mood / Write Journal
   ↓
NLP Analysis
   ↓
Sentiment + Emotion
   ↓
Recommendation
   ↓
Save to PostgreSQL
   ↓
View History
   ↓
Dashboard Analytics
   ↓
Generate PDF Report


---

#  API Integration

The Streamlit frontend communicates with the backend through REST APIs.

Important endpoints include:

```text
POST /analyze-text
POST /analyze
POST /chat
```

### `/analyze-text`

Used for direct journal/text analysis.

### `/analyze`

Used for uploaded file analysis.

### `/chat`

Used for the wellness chat functionality.

Authentication tokens are included in protected API requests.

---

#  Expected Output

For a text such as:

```text
I am feeling stressed because I have several deadlines,
but I am trying my best to complete everything.
```

The system performs:

```text
Input Text
    ↓
Preprocessing
    ↓
VADER Sentiment Analysis
    ↓
Transformer Emotion Analysis
    ↓
Final Sentiment
    ↓
Final Emotion
    ↓
Confidence Score
    ↓
Recommendation
    ↓
Database Storage
```

The result is then displayed in the Streamlit interface.



# Future Enhancements

* Voice-based emotion analysis
* Real-time wellness monitoring
* More advanced multilingual emotion models
* Personalized recommendation learning
* Advanced employee/team analytics
* Improved visualization and reporting
* Notification and reminder system
* Anonymous employee wellness surveys
* More comprehensive feedback-based recommendation evaluation




