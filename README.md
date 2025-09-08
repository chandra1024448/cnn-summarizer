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
   git clone https://github.com/chandra1024448/cnn-summarizer.git
   cd cnn-news-summarizer
* Install dependencies:
   pip install -r requirements.txt
* Run the app:
   python app.py
* Open the local URL (shown in terminal) to use the Gradio interface.

---------------------------------------------------------------------------------------------------------

**Using the Hugging Face Spaces API**

* Endpoint: [https://huggingface.co/spaces/chandra1024/cnn-summarizer]
* Input: JSON object with 'data' field containing:
   1. text – The news article (minimum 5 lines)
   2. lang – 'English' or 'Hindi'
   3. length_choice – 'Short', 'Medium', or 'Detailed'
 
Example Input:

   {
     'data': ['Hurricane Fiona swept through Puerto Rico...', 'Hindi', 'Medium']
   }
* Output Example:
   {
     'data': ['हुरिकेन फियोना ने पोर्टो रिको में रविवार को तूफान की तरह तबाही मचाई...']
   }
  
* Python Example:
import requests

url = 'https://chandra1024.hf.space/api/predict/'
data = {'data': ['Hurricane Fiona swept through Puerto Rico...', 'Hindi', 'Medium']}
response = requests.post(url, json=data)
summary = response.json()['data'][0]
print(summary)

-----------------------------------------------------------------------------------------------------------

**Requirements**

* Python 3.8+
* Libraries: gradio, torch, transformers, sentencepiece
* Install all dependencies with:
   pip install -r requirements.txt
