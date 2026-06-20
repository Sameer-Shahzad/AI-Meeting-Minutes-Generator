# AI Meeting Minutes Generator

An end-to-end AI product that automates the process of transcribing meeting audio and generating structured, professional meeting minutes. The system uses high-speed cloud APIs for transcription and a highly optimized, quantized Large Language Model (LLM) locally for text analysis.

---

## Features

* **Fast Audio Transcription:** Utilizes the Groq API powered by the `whisper-large-v3` model for near-instantaneous and highly accurate speech-to-text conversion.
* **Local LLM Processing:** Runs `Llama-3.1-8B-Instruct` locally on a T4 GPU.
* **4-Bit Quantization:** Implements `BitsAndBytesConfig` (NF4 quantization with double quantization) to dramatically reduce memory footprint, allowing large models to run efficiently on free-tier cloud hardware.
* **Structured Output:** Automatically extracts summaries, attendee lists, core discussion points, takeaways, and action items with owners in standard Markdown.
* **Live Streaming:** Uses `TextStreamer` to display the model's response word-by-word in real-time.

---

## Tech Stack & Tools

* **Language:** Python
* **Speech-to-Text:** Groq API (`whisper-large-v3`), Hugging Face Pipelines (`whisper-medium.en`)
* **LLM:** Meta Llama-3.1-8B-Instruct
* **Model Optimization:** BitsAndBytes (4-bit Quantization)
* **Frameworks:** Transformers, Accelerate, Torch

---

## Setup & Environment Variables

To run this project locally or in Google Colab, you need to set up the following environment variable:

```text
GROQ_API_KEY=your_groq_api_key_here
HF_TOKEN="your_huggingface_token_here"
