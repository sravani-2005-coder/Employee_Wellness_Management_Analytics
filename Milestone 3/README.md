#  Employee Wellness Management Analytics

##  Project Objective

Employee Wellness Management Analytics is an AI-powered web application developed to analyze employees' journal entries and textual feedback for emotional well-being. The system supports multilingual text, performs advanced Natural Language Processing (NLP), predicts emotions using a transformer-based model, computes sentiment scores, and provides personalized wellness recommendations.

The application enables secure user authentication, journal management, multilingual text preprocessing, emotion detection, sentiment analysis, and AI-assisted wellness support through an interactive chatbot.

---

#  Features

- Secure User Authentication (JWT)
- User Registration with Email OTP Verification
- Password Reset via Email OTP
- Dashboard
- Daily Journal Module
- Direct Text Analysis
- File Upload (.txt and .csv)
- Multilingual Language Detection
- Text Preprocessing Pipeline
- Transformer-based Emotion Detection
- Sentiment Analysis using VADER
- Confidence Score Prediction
- Wellness Recommendation
- AI Wellness Chatbot
- Interactive Streamlit Interface

---

#  Model Used

## Emotion Detection

Model:

```
bhadresh-savani/bert-base-go-emotion
```

Framework:

- Hugging Face Transformers
- PyTorch

The model predicts emotions from the processed journal text and returns:

- Dominant Emotion
- Confidence Score
- Emotion Probability Distribution

---

## Sentiment Analysis

Library:

```
VADER Sentiment Analyzer
```

Generated Scores:

- Positive
- Negative
- Neutral
- Compound Score

---

# Multilingual NLP Pipeline

The application supports multilingual employee feedback and journal entries.

Pipeline Steps:

1. Original Text
2. Unicode Normalization
3. Language Detection
4. URL Removal
5. Email Removal
6. HTML Tag Removal
7. Emoji Extraction
8. Emoji Removal
9. Text Cleaning
10. Lowercase Conversion
11. Tokenization
12. Stop-word Removal
13. Lemmatization
14. Noise Filtering
15. Translation to English (when required)
16. Emotion Detection
17. Sentiment Analysis
18. Wellness Recommendation

---

#  Emotion Detection Pipeline

```
Journal Entry
      │
      ▼
Language Detection
      │
      ▼
Text Preprocessing
      │
      ▼
Translation (if required)
      │
      ▼
BERT GoEmotion Model
      │
      ▼
Predicted Emotion
      │
      ▼
Confidence Score
      │
      ▼
Sentiment Analysis
      │
      ▼
Wellness Recommendation
```

---

#  Confidence Score Calculation

The BERT emotion classifier returns probability scores for all supported emotions.

The emotion with the highest probability is selected as the predicted emotion.

Example:

| Emotion | Probability |
|----------|------------|
| Happy | 0.91 |
| Sad | 0.03 |
| Fear | 0.02 |
| Stress | 0.02 |
| Angry | 0.01 |
| Neutral | 0.01 |

Predicted Emotion:

```
Happy
```

Confidence Score:

```
91%
```

---

#  Sentiment Analysis

The VADER Sentiment Analyzer computes:

- Positive Score
- Negative Score
- Neutral Score
- Compound Score

Example:

Positive : 0.71

Negative : 0.05

Neutral : 0.24

Compound : 0.88

---

# Journal Module

The Journal Module allows employees to:

- Write daily journal entries
- Submit entries for emotion analysis
- Detect the language automatically
- View preprocessing outputs
- View predicted emotion
- View confidence score
- View sentiment scores
- Receive wellness recommendations

---

# 💬 Wellness Chatbot

The AI Wellness Chatbot provides:

- Emotional support
- Stress management suggestions
- Positive encouragement
- General wellness guidance

The chatbot is powered using:

```
Qwen2.5-0.5B-Instruct
```

---

# 💾 Database Schema

## Users

| Field | Description |
|--------|-------------|
| id | User ID |
| username | Username |
| email | Email Address |
| password_hash | Encrypted Password |
| is_verified | Email Verification Status |

---

## OTP

| Field | Description |
|--------|-------------|
| email | User Email |
| otp | Generated OTP |
| purpose | Signup / Password Reset |
| expiry | Expiration Time |

---

# 🔗 API Endpoints

## Authentication

```
POST /signup
```

```
POST /login
```

```
POST /verify
```

```
POST /forgot
```

```
POST /reset
```

---

## NLP

```
POST /upload
```

Upload CSV/TXT files.

```
POST /analyze
```

Analyze uploaded files.

```
POST /analyze-text
```

Analyze direct journal text.

---

-

#  Sample Input

```
Today I felt stressed because I had many deadlines. After taking a short walk and speaking with my teammates, I felt much better.
```

---

#  Sample Output

Detected Language

```
English
```

Emotion

```
Stress 😫
```

Confidence Score

```
87%
```

Sentiment

```
Positive : 0.24

Negative : 0.38

Neutral : 0.38

Compound : -0.19
```


---

# 🔍 Observations

- Successfully detects multiple languages before preprocessing.
- Performs complete multilingual NLP preprocessing.
- Emotion prediction is generated using a transformer-based BERT model.
- Confidence scores improve result interpretability.
- VADER provides detailed sentiment analysis.
- Journal entries are analyzed to support employee wellness monitoring.
- AI chatbot offers supportive wellness guidance.
- Secure authentication is implemented using JWT and OTP verification.

---

# 🛠️ Technologies Used

## Frontend

- Streamlit

## Backend

- FastAPI

## NLP

- spaCy
- langdetect
- stopwordsiso
- ftfy
- emoji
- deep-translator

## Machine Learning

- Hugging Face Transformers
- PyTorch
- BERT GoEmotions
- Qwen2.5

## Sentiment Analysis

- VADER

## Database

- PostgreSQL (Neon)

## Authentication

- JWT
- bcrypt
- Email OTP

---

```


# 👩‍💻 Developed By

**Sravani Darsi**

B.Tech – Computer Science and Engineering

Employee Wellness Management Analytics Project
