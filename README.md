# AI Chatbot (DialoGPT + Gradio)

A simple conversational chatbot built with Hugging Face's `DialoGPT-medium` model and deployed through a Gradio web interface.

## What it does

- Loads a pre-trained conversational model (`microsoft/DialoGPT-medium`) via the Hugging Face `transformers` pipeline
- Takes user text input and generates a chatbot reply
- Strips the echoed input prompt from the generated output to return just the reply
- Serves the chatbot through a Gradio interface for easy interaction in the browser

## Setup

1. Clone the repo and install dependencies:

   ```bash
   pip install transformers gradio
   ```

2. Run the app:

   ```bash
   python app.py
   ```

3. Gradio will print a local URL (and optionally a public share link) — open it in your browser to chat.

## Notes

- This is a stateless chatbot: each message is generated independently, so it won't remember earlier turns in the conversation.
- `DialoGPT-medium` can produce repetitive or generic responses; tuning generation parameters (e.g. `temperature`, `top_p`, `do_sample=True`) can help improve response variety.
- The first run will download the model weights from Hugging Face, which may take a few minutes depending on your connection.

## Author

**B S Lakshmi Prerana**
B.Tech AIML, UVCE (2024–2028)

## License

MIT
