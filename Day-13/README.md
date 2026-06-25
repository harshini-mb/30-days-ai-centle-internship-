DAY 13: ADDING A SYSTEM PROMPT

OBJECTIVE:
Build a customizable chatbot with different personalities using System Prompts. Users can choose personas like Pirate, Teacher, Comedian, or Robot, and the chatbot will respond according to that character.

--------------------------------------------------
1. WHAT IS A SYSTEM PROMPT?
--------------------------------------------------

A System Prompt is a special instruction given to the AI before the conversation starts.

It tells the AI:

- Who it should be
- How it should behave
- What tone it should use
- What personality it should follow

Example:

"You are a helpful pirate assistant named Captain Starlight. Speak using pirate slang and nautical metaphors."

The AI will then answer all questions as a pirate.

--------------------------------------------------
2. INITIALIZING THE SYSTEM PROMPT
--------------------------------------------------

if "system_prompt" not in st.session_state:
    st.session_state.system_prompt = "You are a helpful pirate assistant..."

Purpose:
- Creates a default personality.
- Stores it in Session State.
- Keeps the personality even after app reruns.

--------------------------------------------------
3. INITIALIZING CHAT HISTORY
--------------------------------------------------

if "messages" not in st.session_state:
    st.session_state.messages = [
        {
            "role":"assistant",
            "content":"Ahoy! Captain Starlight here..."
        }
    ]

Purpose:
- Starts the chatbot with a welcome message.
- Matches the default Pirate personality.

--------------------------------------------------
4. PERSONALITY PRESET BUTTONS
--------------------------------------------------

The sidebar contains four quick preset buttons:

Pirate
Teacher
Comedian
Robot

Example:

if st.button("Pirate"):
    st.session_state.system_prompt = "You are a pirate assistant..."
    st.rerun()

Purpose:
- Instantly changes the chatbot's personality.
- Updates the System Prompt.
- Refreshes the app.

--------------------------------------------------
5. CUSTOM SYSTEM PROMPT EDITOR
--------------------------------------------------

st.text_area(
    "System Prompt",
    height=200,
    key="system_prompt"
)

Purpose:
- Lets users create their own personalities.
- Can modify existing presets.
- Automatically saves changes to Session State.

Example:

You are a fitness coach.
You provide short motivational advice.

The chatbot will behave like a fitness coach.

--------------------------------------------------
6. CONVERSATION STATISTICS
--------------------------------------------------

user_msgs = len([
    m for m in st.session_state.messages
    if m["role"] == "user"
])

assistant_msgs = len([
    m for m in st.session_state.messages
    if m["role"] == "assistant"
])

Displayed using:

st.metric()

Purpose:
- Tracks conversation activity.
- Shows number of user messages.
- Shows number of AI responses.

--------------------------------------------------
7. CLEAR HISTORY BUTTON
--------------------------------------------------

if st.button("Clear History"):
    st.session_state.messages = [
        {
            "role":"assistant",
            "content":"Ahoy! Captain Starlight here..."
        }
    ]
    st.rerun()

Purpose:
- Removes old messages.
- Resets chat to initial state.
- Keeps chatbot clean.

--------------------------------------------------
8. DISPLAYING CHAT HISTORY
--------------------------------------------------

for message in st.session_state.messages:
    with st.chat_message(message["role"]):
        st.markdown(message["content"])

Purpose:
- Displays all previous messages.
- Maintains chat history.
- Shows messages after every rerun.

--------------------------------------------------
9. BUILDING CONVERSATION CONTEXT
--------------------------------------------------

conversation = "\n\n".join([
    f"{'User' if msg['role']=='user' else 'Assistant'}:
    {msg['content']}"
    for msg in st.session_state.messages
])

Purpose:
- Converts chat history into a single text block.
- Gives the AI memory of previous messages.

--------------------------------------------------
10. COMBINING SYSTEM PROMPT + HISTORY
--------------------------------------------------

full_prompt = f"""
{st.session_state.system_prompt}

Here is the conversation so far:

{conversation}

Respond to the user's latest message while staying in character.
"""

Purpose:
- Personality instruction goes first.
- Conversation history comes next.
- AI maintains character and context.

--------------------------------------------------
11. STREAMING RESPONSES
--------------------------------------------------

def stream_generator():
    response_text = call_llm(full_prompt)

    for word in response_text.split(" "):
        yield word + " "
        time.sleep(0.02)

Purpose:
- Simulates real-time typing.
- Makes chatbot feel modern.
- Improves user experience.

--------------------------------------------------
12. DISPLAY STREAMING OUTPUT
--------------------------------------------------

with st.spinner("Processing"):
    response = st.write_stream(stream_generator)

Purpose:
- Shows loading indicator.
- Streams text word-by-word.
- Returns final response.

--------------------------------------------------
13. SAVE AI RESPONSE
--------------------------------------------------

st.session_state.messages.append({
    "role":"assistant",
    "content":response
})

Purpose:
- Stores AI reply in chat history.
- Allows future context-aware conversations.

--------------------------------------------------
KEY CONCEPTS LEARNED
--------------------------------------------------

✓ System Prompts
✓ Chat Personalities
✓ Session State
✓ Sidebar Controls
✓ Conversation Memory
✓ Streaming Responses
✓ Custom Prompt Engineering
✓ Chat History Management

OUTPUT:


https://github.com/user-attachments/assets/e3fc4ba6-f1d0-4499-a832-8944914898c7




A fully functional chatbot with customizable personalities, conversation memory, 
streaming responses, statistics tracking, and chat history management.
