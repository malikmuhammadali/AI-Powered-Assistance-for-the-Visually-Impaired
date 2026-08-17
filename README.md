# AI-Powered Assistance for the Visually Impaired

A Streamlit app that helps visually impaired users understand their
surroundings and read text aloud, combining vision, OCR, and
text-to-speech into one workflow.

## What it does

- **Scene understanding** — takes a photo and generates a detailed,
  structured description of what's in it (objects, actions, surroundings,
  colors, context) using Google Gemini
- **Text extraction & reading aloud** — extracts text from an image via
  OCR (Tesseract, with OCR.Space as a fallback API), cleans it up into
  well-formed sentences via an LLM pass, and reads it aloud with
  text-to-speech (gTTS)

## Tech stack

- **Streamlit** for the UI
- **Google Gemini** (`google-generativeai`, `langchain-google-genai`) for
  scene description and text cleanup
- **Tesseract** / **OCR.Space API** for text extraction
- **gTTS** for text-to-speech

## Setup

```bash
pip install -r requirements.txt
cp .env.example .env   # fill in GEMINI_API_KEY; OCR_SPACE_API_KEY is optional
                        # (defaults to OCR.Space's public "helloworld" demo key)
```

## Run

```bash
streamlit run final_project.py
```
