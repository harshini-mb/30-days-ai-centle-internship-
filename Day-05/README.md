# Day 5 – Build a LinkedIn Post Generator App

## Overview

Today I built a LinkedIn Post Generator using Streamlit and AI.

The application allows users to generate professional LinkedIn posts by providing a content URL, selecting a tone, and choosing the desired post length. The AI then creates a customized LinkedIn post based on the user's preferences.

## Key Concepts Learned

* Building interactive Streamlit applications
* Using input widgets in Streamlit
* Prompt Engineering
* AI-powered content generation
* Using caching for better performance
* Creating dynamic user experiences

## Features

* Content URL input
* Tone selection (Professional, Casual, Funny)
* Adjustable word count slider
* AI-generated LinkedIn posts
* Fast response using caching

## Streamlit Components Used

### Text Input

```python
content = st.text_input("Content URL:")
```

Allows users to provide a URL or topic for generating content.

### Select Box

```python
tone = st.selectbox(
    "Tone:",
    ["Professional", "Casual", "Funny"]
)
```

Lets users choose the writing style.

### Slider

```python
word_count = st.slider(
    "Approximate word count:",
    50,
    300,
    100
)
```

Controls the length of the generated post.

### Button

```python
if st.button("Generate Post"):
```

Triggers the AI content generation process.

## What I Learned

* How to collect user inputs using Streamlit widgets.
* How prompt engineering influences AI responses.
* How to build practical AI-powered applications.
* How caching improves app performance.
* How AI can assist in content creation and social media management.

## Screenshot

[linkdin post generator.webm](https://github.com/user-attachments/assets/28dca611-0fe3-4b2f-8f97-20a42b6b88df)

![Day 5 Screenshot](screenshot.png)

## Tech Stack

* Python
* Streamlit
* AI/LLM Integration

## Challenge

30 Days of AI – Day 5
