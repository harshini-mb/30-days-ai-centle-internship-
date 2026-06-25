# Day 3 – Write Streams

## Overview

For Day 3 of the 30 Days of AI Challenge, I built a Streamlit application that interacts with Large Language Models 
using an OpenAI-compatible API and supports both standard responses and real-time streaming responses.

The application allows users to select an AI model, enter a prompt, and choose between receiving the complete
response at once or watching the response stream in real-time.

---

## Technologies Used

* Python
* Streamlit
* OpenAI Python Client
* Snowflake Cortex API
* REST API

---

## What I Learned

* Connecting to AI models using OpenAI-compatible APIs
* Working with multiple LLM models
* Creating model selection interfaces in Streamlit
* Understanding streaming vs non-streaming responses
* Using `st.write_stream()` for real-time output
* Handling AI-generated responses efficiently

---

## Features

* Multiple AI model selection
* User prompt input
* Direct response generation
* Real-time streaming responses
* Interactive Streamlit interface
* Loading indicators with Streamlit Spinner

---

## Challenges Faced

* Understanding how streaming responses work
* Learning the OpenAI chat completion format
* Configuring API connections correctly
* Comparing direct and streaming response methods

---

## Outcome

Successfully built a Streamlit application capable of generating AI responses using multiple models 
and displaying them through both traditional and streaming methods.

---

## Screenshot

[Write streams.webm](https://github.com/user-attachments/assets/b9fe1c5b-56c6-44f3-84c9-bda017e456e7)



## Key Takeaway

Today I learned how modern AI chat applications generate responses in real time using streaming, creating a faster and more interactive user experience.
