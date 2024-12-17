# SITHAPALTASK1
Chat with PDF Using RAG Pipeline

# PDF Semantic Search Toolkit

## Overview
This Python toolkit provides a powerful solution for extracting, processing, and semantically searching PDF documents. It combines advanced natural language processing techniques with efficient vector search to enable intelligent document analysis.

## Features
- 🔍 Comprehensive PDF Extraction
  - Full text extraction
  - Table extraction
  - Image extraction
- 🧠 Semantic Search Capabilities
- 📄 Intelligent Document Chunking
- 💾 Persistent Vector Store Storage

## Prerequisites

### Installation
Install required dependencies:
```bash
pip install -r requirements.txt
```

#### Required Libraries
- PyMuPDF (fitz)
- pdfplumber
- sentence-transformers
- faiss-cpu
- numpy
- Pillow
- opencv-python

### Dependencies
```
# requirements.txt
fitz
pdfplumber
sentence-transformers
faiss-cpu
numpy
Pillow
opencv-python
google-colab
```

## Key Components

### 1. DocumentChunker
Breaks down text into semantically meaningful chunks
- Customizable chunk size
- Overlap between chunks to preserve context

### 2. VectorStore
- Converts text to semantic embeddings
- Performs similarity search
- Supports saving and loading vector stores

### 3. PDF Extraction
Extracts multiple content types:
- Text
- Tables
- Images

## Usage Example

```python
# Process a PDF and create vector store
vector_store = process_pdf_complete('document.pdf', 'output_directory')

# Perform semantic search
results = vector_store.search("Your query here", k=5)
```

## Configuration Options

### Chunking
- `chunk_size`: Default 500 characters
- `chunk_overlap`: Default 50 characters

### Vector Store
- Default embedding model: 'all-MiniLM-L6-v2'
- Customizable search depth

## Advanced Usage

### Custom Embedding
```python
# Use a different embedding model
vector_store = VectorStore(model_name='your-custom-model')
```

### Saving and Loading
```python
# Save vector store
vector_store.save('path/to/store')

# Load vector store
loaded_store = VectorStore.load('path/to/store')
```

## Potential Applications
- Academic Research
- Legal Document Analysis
- Knowledge Management
- Intelligent Document Search

## Limitations
- Requires structured PDFs
- Performance depends on document complexity
- Limited to text-based semantic search

## Contributing
1. Fork the repository
2. Create your feature branch
3. Commit changes
4. Push to the branch
5. Create a Pull Request

## License
[Specify your license - e.g., MIT, Apache 2.0]

## Contact
[Your Contact Information]

## Troubleshooting
- Ensure all dependencies are correctly installed
- Check PDF file integrity
- Verify Python version compatibility (3.7+)

## Performance Tips
- For large documents, increase chunk size
- Use powerful embedding models for better results
- Leverage GPU for faster processing

## Future Roadmap
- Support more document formats
- Improve multi-language support
- Enhance image extraction capabilities
```

## Disclaimer
This toolkit is designed for research and educational purposes. Always respect copyright and usage rights of source documents.
