# Stories
## AI Finance Assistant - Contextual Response Generator

## Overview
This project implements an AI-powered finance assistant that retrieves and processes textual and visual data from PDFs, stores them in a vector database, and uses a language model to generate context-aware responses. The assistant also creates a knowledge graph to visualize relationships between retrieved content and presents all results through an interactive UI in Google Colab.

## Features
- **Text and Image Extraction**: Uses PyMuPDF to extract text and images from uploaded PDFs.
- **Embedding Generation**:
  - OpenAI's `text-embedding-3-large` for textual data.
  - OpenAI's CLIP (`clip-vit-base-patch32`) for image embeddings.
- **Vector Database Storage**: Stores embeddings in ChromaDB for efficient retrieval.
- **Similarity Search**: Enables retrieval of the most relevant text and images using vector similarity search.
- **Knowledge Graph Generation**: Uses `llmgraph` to create a visual representation of the relationships between retrieved content.
- **Contextual Response Generation**: Uses OpenAI's `gpt-4o` to generate well-structured responses based on retrieved data.
- **Interactive UI**: Built with Gradio, featuring:
  - Query input field
  - AI-generated response display
  - Relevant images gallery
  - Knowledge graph visualization

## Installation & Setup
### Prerequisites
Ensure you have the following installed in your Google Colab environment:
- Python 3
- Required Libraries:
  ```python
  !pip install pymupdf openai open_clip_torch chromadb llmgraph gradio torch torchvision matplotlib networkx
  ```

### API Keys Setup
Ensure you have an OpenAI API key for embedding generation and GPT-4o response generation. Replace `your_openai_api_key` in the code with your actual API key.

## How It Works
1. **Upload PDFs**: The user uploads a PDF file.
2. **Extract & Process Data**:
   - The system extracts text and images.
   - Text is chunked into groups of three sentences.
   - Embeddings are generated and stored in ChromaDB.
3. **Query Handling**:
   - User submits a query.
   - The system retrieves similar text and image embeddings.
   - A knowledge graph is created to visualize relationships.
   - The AI generates a context-aware response.
4. **Display Results**:
   - The UI presents the AI's response.
   - Relevant images are shown in a gallery.
   - The knowledge graph is displayed on the right side.

## Running the Project in Google Colab
1. Open a new Google Colab notebook.
2. Upload and run the provided Python script.
3. Click the `Upload` button to add PDFs.
4. Input a query into the text box.
5. View the AI-generated response, relevant images, and knowledge graph in the UI.

## Potential Enhancements
- Support for multiple file uploads.
- Integration with a financial news API for real-time data enrichment.
- Improved UI with interactive graph visualization.
- Fine-tuned models for domain-specific accuracy.

## License
This project is licensed under the MIT License.

## Contributors
Aryan Tomar  
Anshumaan Singh  
Naman Sharma  


