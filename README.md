# Multi-Model RAG with Gemini, LangChain, and Google AI Studio

This project implements a Retrieval-Augmented Generation (RAG) pipeline utilizing Google's Gemini models, LangChain, and Google AI Studio to process both text and image data. The system leverages vector databases (FAISS) and Google Generative AI embeddings to enhance retrieval-based answering.

## Features
- Multi-Modal AI Integration: Uses Gemini models to handle text and image inputs.
- Document Processing: Loads and splits text for better retrieval.
- Vector Search with FAISS: Implements an efficient document retrieval system.
- LangChain RAG Pipeline: Builds a retrieval-augmented generation workflow.
- Google AI Studio API: Uses Generative AI models from Google.

## Installation
To install the required dependencies, run:

## Usage

1. **Set Up Google API Key**  
   Make sure to set up your Google AI Studio API key:

2. **Load a Gemini Model**  

3. **Text Processing with LangChain**  

4. **FAISS Vector Store for Retrieval**  


5. **Multi-Modal AI Processing**  
- Image Retrieval and Summarization  
  ```
  import requests
  from PIL import Image
  import matplotlib.pyplot as plt

  def get_image(url, filename, extension):
      content = requests.get(url).content
      with open(f"{filename}.{extension}", 'wb') as f:
          f.write(content)
      image = Image.open(f"{filename}.{extension}")
      return image

  image = get_image("https://example.com/sample_image.png", "nike_shoes", "png")
  plt.imshow(image)
  plt.show()
  ```

- Process Image with Gemini  
  ```
  message = [
      {"type": "text", "text": "Summarize this image in 5 words"},
      {"type": "image_url", "image_url": image}
  ]
  vision_model = load_model("gemini-pro-vision")
  print(vision_model.invoke(message).content)
  ```

## Project Structure


## Dependencies
- LangChain
- Google Generative AI
- FAISS
- Matplotlib
- Pillow
- Requests

## License
This project is open-source under the MIT License.
