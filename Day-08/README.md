# Day 8 – Meet the Chat Elements

## Overview

On Day 8 of the 30 Days of AI Challenge, I explored Streamlit's chat components and built the visual foundation of a chatbot.

Unlike previous applications that followed a simple Input → Process → Output workflow, today's project introduced a conversational interface using chat elements. The goal was to understand how chat messages are displayed before implementing memory and AI integrations.

## What I Learned

* Using `st.chat_message()`
* Using `st.chat_input()`
* Building a chatbot user interface
* Displaying user and assistant messages
* Adding rich content inside chat messages
* Understanding the need for Session State

## Features Implemented

### Static Chat Messages

Created sample user and assistant conversation bubbles using:

```python
with st.chat_message("user"):
    st.write("Hello!")

with st.chat_message("assistant"):
    st.write("Hi! How can I help you?")
```

### Rich Content in Chat

Learned that chat messages can contain more than text.

Example:

* Charts
* Images
* Tables
* Dataframes

### Chat Input Box

Implemented a chat input field using:

```python
prompt = st.chat_input("Type a message here...")
```

This creates a modern chat-style input box fixed at the bottom of the application.

### Dynamic Responses

When the user enters a message:

* The message is displayed in a user bubble.
* A mock assistant response is generated and displayed.

## Key Observation

The chatbot looked functional, but previous messages disappeared whenever a new message was sent.

This happens because Streamlit reruns the entire application after every interaction.

Without storing messages in Session State, the application cannot remember previous conversations.

## Technologies Used

* Python
* Streamlit

## Key Takeaway

A chatbot is more than a text box and response. To create real conversations, applications must remember previous messages. Today's lesson provided the visual chatbot structure that will later be enhanced with memory and AI capabilities.

## Outcome

Successfully built the visual skeleton of a chatbot using Streamlit Chat Elements and prepared the foundation for conversation memory in future projects.
[Meet the Chat Elements.webm](https://github.com/user-attachments/assets/4aec5321-0f72-4833-8448-f0bd32646bd8)
