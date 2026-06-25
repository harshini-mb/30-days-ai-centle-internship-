# Day 4 – Caching Your App

## Overview

Today I learned how caching works in Streamlit and why it is important for improving application performance.

Caching helps avoid repeating expensive operations such as API calls, database queries, or complex calculations. Instead of running the same function again and again, Streamlit stores the result and instantly returns it when the same input is used.

## Key Concepts Learned

* Understanding Streamlit caching
* Using `@st.cache_data`
* Improving app performance
* Reducing response time
* Measuring execution time with Python's `time` module

## Example Workflow

1. User enters a prompt.
2. App processes the request.
3. Result is stored in cache.
4. If the same prompt is entered again, the cached result is returned instantly.
5. Faster user experience and reduced computation.

## Code Concept

```python
@st.cache_data
def process_data(prompt):
    return f"Processing: {prompt}"
```

The first execution runs normally and stores the result.

Future executions with the same input use the cached version.

## What I Learned

* How caching improves performance.
* When to use `@st.cache_data`.
* Difference between cached and non-cached execution.
* How caching creates a smoother user experience.

## Screenshot

[caching the app.webm](https://github.com/user-attachments/assets/9e1b3720-d63b-491c-8f6e-1b98c6c794a8)


## Tech Stack

* Python
* Streamlit

## Challenge

30 Days of AI – Day 4
