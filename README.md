# Chatbot Generative AI - Winter School : Generative AI

**Design of a simple RAG (Retrieval-Augmented Generation) system that answers user questions based on a set of Wikipedia pages on generative AI as part of my Winter School on Generative AI organised by DataScientist.fr and CYU.**  
The aim is to put the document retrieval and text generation pipeline into practice using popular tools.

## Technical specifications

- Languages : Python (Library : LangChain)
- AI model : GPT-4-o
- GUI framework : Streamlit
- Deployment : Docker, Railway

## Installation process

1. Create the .env file
   
   Create the `.env` file from the `.env.template` file :
     
     ```
      cp .env.template .env
     ```
     
   Then edit the `.env` file to add the necessary information.
3. Run the application

   ```
    pip install -r requirements.txt

    streamlit run app.py
   ```

## Containerisation process (with Docker)

1. Build the Docker image

   ```
    docker build -t chatbot-gen-ai .
   ```
   
2. Launch the Docker container

   ```
    docker run --env-file=.env -p 8501:8501 chatbot-gen-ai
   ```
   
   Use a persistent volume to store model data :

   ```
    docker run --env-file=.env -p 8501:8501 -v /vectorstore chatbot-gen-ai
   ```
   
## Author

Kévin BERNARD
