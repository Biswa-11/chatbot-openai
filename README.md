# ChatBot with OpenAI (LangChain + Gradio + Play.ht TTS)

A smart chatbot built using **LangChain**, **OpenAI GPT models**, and **Gradio**.  
This project features **conversation memory** and **text-to-speech (TTS)** via **Play.ht**, turning chatbot replies into audio (MP3) in real time.  
It also supports easy deployment to **Hugging Face Spaces**.

---

## Features
-  **Conversational AI** powered by `gpt-3.5-turbo` (via LangChain’s `ChatOpenAI`)
-  **Memory Support** using `ConversationBufferMemory`
-  **Text-to-Speech** with Play.ht (automatic MP3 generation)
-  **User-Friendly Interface** built in Gradio
-  **Deployable** to Hugging Face Spaces with minimal setup


---

##  Setup & API Keys
This project requires the following keys:
- **OPENAI_API_KEY** → for OpenAI GPT models
- **PLAY_HT_API_KEY**, **PLAY_HT_USER_ID**, **PLAY_HT_VOICE_ID** → for Play.ht TTS

## Update the placeholders in the notebook:
- OPENAI_API_KEY = "your-openai-key"
- PLAY_HT_API_KEY = "your-playht-api-key"
- PLAY_HT_USER_ID = "your-playht-user-id"
- PLAY_HT_VOICE_ID = "your-playht-voice-id"

## How It Works
- User enters a query in the Gradio chat.
- LangChain’s ChatOpenAI generates a response (with conversation history).
- The response is sent to Play.ht API, which generates an audio file (MP3).
- Gradio returns both text and downloadable audio.

## Deploying to Hugging Face Spaces
The notebook includes cells to:
- Login with notebook_login()
- Use HfApi().upload_file() to push app.py and requirements.txt
This enables one-click chatbot hosting on Hugging Face Spaces.

## Future Improvements
- Multilingual Support: auto-translate non-English queries before response
- Customizable Voices: add more TTS options & styles
- Streaming Responses: real-time output instead of waiting for full text
- Knowledge Augmentation: connect with external documents (RAG)
- Better Secrets Management: .env + python-dotenv for keys
- Upgrade Models: migrate to GPT-4o mini for faster, cheaper responses

## Example Use Cases
- Personal assistant
- Interactive Q&A bot
- Language learning tutor
- Entertainment chat companion
