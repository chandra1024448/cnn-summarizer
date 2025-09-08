**CNN News Summarizer (English + Hindi)**

A Gradio web app to summarize news articles in English or Hindi using my trained BART model (chandra1024/bart_cnn). Proper nouns are preserved, and the UI includes GIFs and colorful elements for an interactive experience.

----------------------------------------------------------------------------------------------------------

**Features**

* Summarize news articles in Short, Medium, or Detailed length.
* Support for English and Hindi summaries.
* Proper nouns are preserved in summaries.
* Interactive Gradio UI with GIFs and colors.
* Works for inputs from 5 lines to unlimited text.
* Hugging Face Spaces deployment with ready-to-use API.

---------------------------------------------------------------------------------------------------------

**Getting Started (Local Setup)**

* Clone the repository:
   git clone https://github.com/chandra1024448/cnn-news-summarizer.git
   cd cnn-news-summarizer
* Install dependencies:
   pip install -r requirements.txt
* Run the app:
   python app.py
* Open the local URL (shown in terminal) to use the Gradio interface.

---------------------------------------------------------------------------------------------------------

**Demo/ Try it yourself**

Link - https://chandra1024-cnn-summarizer.hf.space

-----------------------------------------------------------------------------------------------------------

**Technical Details**


	•	Built with PyTorch and Hugging Face Transformers
	•	Optional Helsinki NLP model for English → Hindi translation
	•	Handles large articles by chunking input text
	•	Proper nouns are extracted and restored to avoid translation errors

-----------------------------------------------------------------------------------------------------------

**Requirements**

* Python 3.8+
* Libraries: gradio, torch, transformers, sentencepiece
* Install all dependencies with:
   pip install -r requirements.txt
