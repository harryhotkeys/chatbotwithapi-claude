ChatbotAPIClaude

A simple desktop chatbot application built with Python, Tkinter, and Anthropic Claude API. The application provides a graphical chat interface with real-time streaming responses from Claude.

Features
Simple and clean Tkinter GUI
Real-time streaming responses from Claude
Multi-turn conversation memory
Scrollable chat history
Clear chat functionality
Background threading to prevent UI freezing
Customizable system prompt
Screenshot

The application includes:

Chat display area
User input field
Send button
Clear Chat button
Streaming AI responses
Requirements
Python 3.9+
Anthropic Python SDK

Install dependencies:

pip install anthropic
Setup
1. Install the Anthropic SDK
pip install anthropic
2. Set Your API Key
Windows (PowerShell)
$env:ANTHROPIC_API_KEY="your-api-key"
Linux / macOS
export ANTHROPIC_API_KEY="your-api-key"

Or configure it permanently in your environment variables.

Running the Application
python ChatbotAPIClaude.py
Project Structure
ChatbotAPIClaude.py

Main components:

Component	Description
ChatbotUI	Main GUI class
send_message()	Handles user messages
stream_response()	Streams Claude responses
append_text()	Updates chat window
finish_response()	Restores UI after response
clear_chat()	Clears chat history
Configuration
System Prompt

Modify the chatbot behavior by changing:

SYSTEM_PROMPT = "you are a helpful assistant"

Examples:

SYSTEM_PROMPT = "You are a Python programming tutor."
SYSTEM_PROMPT = "You are an expert cybersecurity assistant."
Claude Model

Currently configured to use:

model="claude-sonnet-4-6"

You can replace this with another Claude model supported by your Anthropic account.

How It Works
User enters a message.
Message is added to conversation history.
A background thread sends the conversation to Claude.
Claude streams tokens back in real time.
The GUI updates as the response arrives.
The assistant response is stored for future context.
Example Conversation
You: What is Python?

Bot: Python is a high-level programming language known for its readability and versatility...
Known Limitations
No API key validation in the GUI
No error handling for network/API failures
Conversation history is not saved between sessions
No support for images or file uploads
Clear Chat removes all conversation context
Possible Improvements
Add dark/light themes
Save chat history to disk
Add markdown rendering
Support multiple Claude models
Add typing indicators
Add token usage statistics
Add settings menu
Add retry button for failed requests
Add API key configuration inside the application


<img width="502" height="628" alt="image" src="https://github.com/user-attachments/assets/77f6fe7b-07c3-422a-846a-190cc0a2ed89" />

Author
Created by harryhotkeys.

License

This project is open-source. Feel free to modify and distribute it according to your preferred license.
