# Employee Wellness Management Analytics - Milestone 1

## Project Objective

This milestone focuses on building a secure **User Authentication Module** using Streamlit. The application provides user registration, login, password recovery through OTP, secure session management using JWT, and stores user data securely in a Neon PostgreSQL database.

## Features

*  Home Page
*  User Registration (Sign Up)
*  Secure Login
*  Forgot Password with OTP Verification
*  OTP Delivery using Google SMTP
*  Password Encryption using bcrypt
*  JWT-based User Authentication
*  Neon PostgreSQL Database Integration
*  Dashboard / CSV Upload Page after Successful Login

## Technologies Used

* Python
* Streamlit
* Neon PostgreSQL
* JWT (JSON Web Token)
* Google SMTP
* Google Colab

## Google Colab Setup Instructions

1. Open `Authentication.ipynb` in Google Colab.
2. Install the required Python libraries.
3. Configure the Neon PostgreSQL database credentials.
4. Configure the Google SMTP email credentials.
5. Run all notebook cells in order.
6. Launch the Streamlit application and access it through the generated public URL.

## Authentication Workflow

1. Create a new account using the **Sign Up** page.
2. Verify the registered email using the OTP sent via Google SMTP.
3. Log in using the registered email and password.
4. A JWT token is generated for secure session management.
5. If the password is forgotten, use the **Forgot Password** page to receive an OTP and reset the password.
6. After successful login, the user is redirected to the Dashboard/CSV Upload page.

## Screenshots

The `screenshots` folder contains images of:

* Home Page
* Sign Up Page
* Login Page
* Forgot Password Page
* Dashboard / CSV Upload Page
* Neon PostgreSQL Database

## Author

**Sravani Darsi**
