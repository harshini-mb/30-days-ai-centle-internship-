# Day 9 – Understanding Session State

## Overview

On Day 9 of the 30 Days of AI Challenge, I learned one of the most important concepts in Streamlit development: **Session State**.

The goal was to understand why normal Python variables lose their values whenever a user interacts with the application and how Session State can be used to preserve data across reruns.

## What I Learned

* Why Streamlit reruns the script on every interaction
* The limitations of standard variables
* How Session State works
* Initializing Session State
* Updating values in Session State
* Reading values from Session State
* Building applications with memory

## The Problem: Standard Variables

A normal variable is recreated every time the app reruns.

Example:

```python
count = 0

if st.button("+"):
    count += 1
```

Even after clicking multiple times, the value never truly persists because `count` resets to `0` whenever Streamlit reruns the script.

## The Solution: Session State

Session State acts like a persistent dictionary that survives reruns.

Example:

```python
if "counter" not in st.session_state:
    st.session_state.counter = 0

if st.button("+"):
    st.session_state.counter += 1
```

The value is stored inside Session State and remains available throughout the user's session.

## Features Implemented

### Standard Variable Counter

* Increment button
* Decrement button
* Demonstrated how values reset on every interaction

### Session State Counter

* Increment button
* Decrement button
* Persistent memory across reruns

### Side-by-Side Comparison

Created two columns to compare:

* Standard Variables ❌
* Session State ✅

This made it easy to visualize the difference between temporary and persistent storage.

## Technologies Used

* Python
* Streamlit
* Session State

## Key Takeaway

Session State is the foundation of interactive Streamlit applications.

Without Session State:

* Chatbots forget conversations
* Counters reset
* User data disappears

With Session State:

* Applications remember information
* Conversations can persist
* User experiences become interactive and dynamic

## Outcome

Successfully learned how Streamlit manages state and built a counter application that demonstrates the difference between temporary variables and persistent Session State memory.

This concept prepares the foundation for building chatbots that remember previous messages and maintain conversation history.
[Understanding Session State.webm](https://github.com/user-attachments/assets/50631bc2-35ed-4717-87a4-168609761b11)
