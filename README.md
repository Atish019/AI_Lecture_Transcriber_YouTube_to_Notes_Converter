
# AI Lecture Transcriber: YouTube to Notes Converter
This project is designed to make learning from YouTube lectures easier and more effective. With just a video link, it extracts the transcript and converts it into clear, subject-specific notes using Google Gemini (Generative AI).

Whether the lecture is about Physics, Mathematics, Generative AI, or Data Science & Statistics, this tool helps you turn raw video content into organized, easy-to-read notes — great for quick reviews or deep study sessions.

Built using Python, Streamlit, and the YouTube Transcript API, this app is simple to use, fast, and flexible for different academic topics.

## Demo Screenshots

### App Interface

![App Screenshot](./Screenshot%202025-08-05%20203715.png)

### Generated Notes

![Notes Screenshot](./Screenshot%202025-08-05%20203728.png)


---

## Features

-  Extract transcript directly from YouTube video link
-  Generate subject-specific notes using Generative AI (Gemini)
-  Supports subjects: Physics, Chemistry, Mathematics, Generative AI, Data Science & Statistics
-  Fast response via `gemini-1.5-flash` model
-  Automatically shows YouTube video thumbnail for context
-  Clean UI built with **Streamlit**
-  API key management with `.env` and `dotenv`

---

##  File Descriptions

### `app.py`
Main Streamlit frontend that:
- Takes YouTube video link + subject input
- Extracts transcript using `extract_transcript()` function
- Generates detailed notes using Gemini model and subject-specific prompt

### `youtube_transcript.py`
- Uses `youtube_transcript_api` to fetch transcript text from video ID

### `.env`
Contains your API key securely like:
```
GOOGLE_API_KEY=your_api_key_here
```

### `requirements.txt`
Install all dependencies with:
```
pip install -r requirements.txt
```

---

## Prompt Design (LLM Engineering)

Each subject uses a **custom-designed prompt** to instruct Gemini to generate **detailed, structured notes**.

### Example: Prompt for Generative AI

```
Title: Comprehensive Generative AI Notes from YouTube Video Transcript

As an expert in Generative AI, your task is to generate **detailed and structured notes** based on the transcript of a YouTube video. The goal is to make these notes student-friendly and informative, covering both theoretical foundations and real-world applications.

Your notes should include:
- Introduction to Generative AI and its importance in modern AI systems.
- Explanation of key concepts like:
    - Generative Models vs Discriminative Models
    - Latent Space
    - Sampling Methods
- Overview of popular architectures:
    - GANs, VAEs, Transformers (GPT, BERT, etc.)
- Applications in:
    - Image, Text, Audio Generation
    - Drug discovery, gaming, education, etc.
- Ethical concerns: Deepfakes, AI bias, copyright issues
- Latest tools: OpenAI, Gemini, HuggingFace, etc.

Use clear examples, analogies, or diagrams where helpful.
```

Each subject (Physics, Maths, Chemistry, etc.) has its own **tailored prompt** to ensure domain-specific depth.

---

##  How to Run

1. Clone this repo
2. Create virtual environment and activate
3. Install dependencies:  
```bash
pip install -r requirements.txt
```
4. Add your Google Gemini API key to `.env` file
5. Run the Streamlit app:
```bash
streamlit run app.py
```

---

##  Example Output

The app generates **well-structured notes** with clear headings, subpoints, bullet lists, and explanations, ideal for students and learners.

---

##  Requirements

- Python 3.8+
- `streamlit`, `google-generativeai`, `youtube-transcript-api`, `python-dotenv`, etc.

---

##  Coming Soon

- Download notes as PDF/Doc
- Add voice summarizer (Speech-to-text)
- Multilingual support

---

## Author

Made with  by Atish Kr. Sharma  
Feel free to contribute, fork, or connect with me!

