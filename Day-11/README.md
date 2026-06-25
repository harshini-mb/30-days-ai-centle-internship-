# 📅 Day 11 – Displaying Chat History

## 🎯 Objective
Enhance the chatbot by adding conversation history, welcome messages, sidebar statistics, and a clear history feature.

## 🛠️ What I Learned
- Managing chat history with Session State
- Displaying previous messages automatically
- Creating sidebar statistics
- Counting user and assistant messages
- Using `st.spinner()` for better user experience
- Using `st.rerun()` to instantly update the interface
- Passing conversation history to the AI for context

## 🚀 Features
- Welcome message on startup
- Persistent conversation history
- Conversation statistics sidebar
- Clear History button
- AI remembers previous messages
- Loading indicator while generating responses

## 📚 Key Concepts
- `st.session_state`
- `st.sidebar`
- `st.metric()`
- `st.spinner()`
- `st.rerun()`
- Context-aware AI conversations
- Conversation memory

## 💡 How It Works
1. Initialize the chatbot with a welcome message.
2. Store all user and assistant messages in Session State.
3. Display chat history every time the app reruns.
4. Show conversation statistics in the sidebar.
5. Build the full conversation history before sending it to the AI.
6. Generate context-aware responses.
7. Allow users to clear the conversation and start fresh.

## 🏆 Outcome
Successfully built a chatbot that remembers previous conversations, displays chat statistics, and provides a more polished user experience.

## 📸 Screenshot
[Displaying Chat History.webm](https://github.com/user-attachments/assets/9ff63900-bd42-4b90-b8f2-cfa2cb329beb)

## 🔗 Skills Practiced
- Python
- Streamlit
- Session State
- Chatbot Development
- UI/UX Design
- Context Management
- AI Applications

---
#30DaysOfAI #Streamlit #Python #ArtificialIntelligence #Chatbot #SessionState #LearningInPublic #WomenInTech #BuildInPublic
