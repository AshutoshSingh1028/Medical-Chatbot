# Medical-Chatbot

An AI-powered medical chatbot that leverages advanced language models to answer medical queries, provide information, and assist users with healthcare-related questions. The chatbot uses a custom knowledge base built from medical literature and is designed for educational and informational purposes only.

## Features

- **Conversational AI**: Interact with users in natural language.
- **Medical Knowledge Base**: Answers are generated using information from a curated medical PDF (e.g., `Medical_book.pdf`).
- **Web Interface**: User-friendly chat interface built with Flask and HTML/CSS.
- **Extensible**: Modular codebase for easy updates and improvements.

## Project Structure

```
Medical-Chatbot/
├── app.py                  # Main Flask application
├── requirements.txt        # Python dependencies
├── setup.py                # Package setup
├── store_index.py          # Indexing script for knowledge base
├── data/                   # Contains medical PDF(s)
├── src/                    # Source code (helpers, prompts)
├── static/                 # Static files (CSS)
├── templates/              # HTML templates
├── research/               # Notebooks and experiments
└── ...
```

## Setup Instructions

1. **Clone the repository**
	```sh
	git clone https://github.com/AshutoshSingh1028/Medical-Chatbot.git
	cd Medical-Chatbot
	```

2. **Create a virtual environment (recommended)**
	```sh
    conda create -n medchatbot python=3.10
    conda activate medchatbot
    ```

3. **Install dependencies**
	```sh
	pip install -r requirements.txt
	```

4. **Add your medical PDF**
	- Place your medical reference PDF in the `data/` directory (default: `Medical_book.pdf`).

5. **Set up environment variables**
	- Create a `.env` file in the project root with the following content (replace with your own API keys):
      ```
      PINECONE_API_KEY="your-pinecone-api-key"
      OPENAI_API_KEY="your-openai-api-key"
      ```

6. **Run the application**
	```sh
	python app.py
	```
	The chatbot will be available at [http://localhost:8080](http://localhost:8080).

## Usage

1. Open your browser and go to [http://localhost:8080](http://localhost:8080).
2. Type your medical question in the chat interface.
3. The chatbot will respond with information based on the medical knowledge base.

**Note:** This chatbot is for informational and educational purposes only. It is not a substitute for professional medical advice, diagnosis, or treatment.

## Customization

- To update the knowledge base, replace or add PDFs in the `data/` folder and re-run `store_index.py`.
- Modify prompts or helper functions in `src/` as needed.

## License

This project is licensed under the MIT License.

