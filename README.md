PDF-Chatbot-RAG
Welcome to PDF-Chatbot-RAG! 🎉 This is a simple yet powerful chatbot that allows you to chat with the content of your PDFs. It uses advanced techniques to extract text from your PDF documents, create a vector-based database, and then generate answers to your questions using an intelligent language model.

What’s This About?
With this project, you can:

Upload any PDF file, and it will extract and process the text from it.
Ask the bot questions about the content, and it will respond based on what’s inside the PDF.
It’s all done using state-of-the-art machine learning models and fast search algorithms to make sure you get quick and accurate answers.

Key Features
PDF Text Extraction: We use pdfminer.six to extract text from your PDFs.
Smart Text Chunking & Embedding: The text is split into smaller, more manageable chunks, which are then turned into meaningful vector embeddings.
Efficient Retrieval: Embeddings are stored in a FAISS database, allowing for fast retrieval of relevant information.
AI-Powered Answers: The bot uses a pre-trained language model to provide you with contextually relevant answers based on the extracted content.

How To Get It Running
1. Clone the Repo
Start by cloning this repository to your local machine:

bash
Copy code
git clone https://github.com/Sumanth8913/PDF-Chatbot-RAG.git
cd PDF-Chatbot-RAG
2. Install the Dependencies
You’ll need a few libraries to get everything running. Just use pip to install them:

bash
Copy code
pip install pdfminer.six streamlit pickle5 langchain langchain-groq faiss-cpu huggingface_hub
3. Run the Program
Once everything is installed, you can run the program like this:

bash
Copy code
python main.py
It will ask you to upload a PDF file, and once that’s done, you can start asking questions!

How It Works
Upload Your PDF:

Upload a PDF file, and we’ll extract all the text from it.
Text Processing:

The extracted text is split into chunks, and these chunks are converted into embeddings (a fancy word for numerical representations) using Hugging Face models.
Saving Embeddings:

These embeddings are saved in a FAISS database, so we can quickly look them up when you ask a question.
Ask Away:

You can then ask questions about the content in the PDF. The chatbot will look through the database, find the most relevant text, and use that to generate an answer for you!
Example Questions
Once you upload your PDF and the system is ready, you can ask questions like:

vbnet
Copy code
Ask a Question: What is the unemployment rate for Computer Science graduates?
Answer:
The unemployment rate for Computer Science graduates is 4.2%.
Project Files
main.py: This is where all the magic happens! It handles everything from uploading PDFs to answering questions.
faiss_store_openai.pkl: This file stores all the vector embeddings generated from the PDFs you upload.
