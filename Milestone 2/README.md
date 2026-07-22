# Employee Wellness Management Analytics – NLP Module

## Overview

The Employee Wellness Management Analytics system is designed to analyze employee feedback using Natural Language Processing (NLP). It accepts text from multiple input sources, preprocesses the content through a comprehensive NLP pipeline, and provides detailed intermediate outputs to help understand each stage of text transformation.

The application currently supports multilingual text preprocessing and language detection for uploaded files. The integrated wellness chat assistant is available for conversational interaction, but multilingual conversations are currently under development and are primarily optimized for English.

---

# Objectives

* Accept employee feedback through direct text input.
* Support file uploads in **.txt** and **.csv** formats.
* Automatically detect the language of the uploaded text.
* Perform comprehensive text preprocessing.
* Display every preprocessing stage for transparency.
* Support multilingual text preprocessing using language-aware NLP techniques.
* Generate clean text suitable for sentiment and emotion analysis.

---

# Features

## 1. Text Input Module

The system accepts textual data from multiple sources:

* Text (.txt) files
* CSV (.csv) files

Uploaded files are automatically read and prepared for preprocessing.

---

## 2. Language Detection

Before preprocessing begins, the application automatically detects the language of the input text.

The detected language is displayed to the user before the preprocessing pipeline starts.

---

## 3. Text Preprocessing Pipeline

The following preprocessing operations are performed sequentially:

* Unicode Text Normalization
* Text Cleaning
* URL Removal
* Email Address Removal
* HTML Tag Removal
* Emoji Extraction
* Emoji Removal
* Punctuation Removal
* Number Removal
* Lowercase Conversion (where applicable)
* Tokenization
* Language-aware Stop-word Removal
* Lemmatization
* Noise Filtering

Each stage improves the quality of the text for downstream NLP tasks.

---

## 4. Multilingual Support

The preprocessing pipeline supports multiple languages by integrating language detection and language-aware NLP libraries.

The application attempts to apply appropriate preprocessing for the detected language. If a language is not fully supported by the available NLP resources, the system continues processing gracefully without crashing.

**Current Status**

* Multilingual preprocessing: Supported
* Language detection: Supported
* Language-aware stop-word removal: Supported (where resources are available)
* Multilingual chat conversations: Currently optimized for English and under development for broader multilingual support.

---

## 5. Intermediate Processing Outputs

For better transparency and debugging, the application displays the output after every major preprocessing step.

Displayed outputs include:

* Original Text
* Detected Language
* Cleaned Text
* Extracted Emojis
* Tokens
* Tokens after Stop-word Removal
* Lemmatized Tokens
* Final Preprocessed Text

These intermediate results help users understand how the raw input is transformed throughout the NLP pipeline.

---

# Technologies Used

* Python
* Streamlit
* FastAPI
* spaCy
* NLTK
* langdetect
* ftfy
* emoji
* pandas

---

# Current Limitations

* The conversational wellness chatbot currently performs best with English interactions.
* Multilingual preprocessing is supported for uploaded text, but multilingual conversational responses are still being enhanced.
* Language-specific lemmatization depends on the availability of NLP models for the detected language.


