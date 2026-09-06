# RAG Local GPU - 100% Offline na RTX 5060 Ti

ChatGPT que lê PDF 100% offline. Sem API, sem custo.

### Setup testado
- GPU: RTX 5060 Ti 16GB (616.64 / CUDA 13.4)
- Modelo: qwen2.5:14b (11GB VRAM) ou qwen2.5:7b (6GB VRAM)

### Como rodar
ollama pull qwen2.5:14b
pip install fastapi uvicorn PyPDF2 requests python-multipart
ollama run qwen2.5:14b
uvicorn main:app --reload

Acesse: http://127.0.0.1:8000

### Features V3
- Drag and drop PDF
- Multi-PDF
- Chat com histórico
- Exportar conversa
