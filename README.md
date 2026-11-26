# RAG Multi Modal Agentique

Application RAG multimodale et agentique sur l'article « Attention is all you need ».

## Pipeline
1. Extraction texte et images du PDF (PyMuPDF)
2. Embeddings CLIP ViT-B-32 (open_clip), vecteurs normalisés
3. Indexation dans ChromaDB (métadonnées : type, page, chemin image)
4. Recherche par similarité cosinus (texte ou image)
5. Retriever encapsulé en outil (`retriever_tool`)
6. Agent ReAct avec LangGraph et Qwen3 (Ollama)
7. Tests de l'agent

## Installation
    uv sync
    ollama pull qwen3:8b
Placer le PDF dans `pdfs/`, puis exécuter `rag_multimodal.ipynb`.