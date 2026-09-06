# RAG Local GPU - 100% Offline na RTX 5060 Ti

> ChatGPT que lê PDF 100% offline. Sem API, sem custo, privado.

Chat com seus documentos rodando 100% local na sua máquina. Nenhum dado sai do seu PC.

### 🚀 Setup Testado
- **GPU:** RTX 5060 Ti 16GB (Driver 616.64 / CUDA 13.4)
- **Modelo:** qwen2.5:14b (11GB VRAM) ou qwen2.5:7b (6GB VRAM)
- **RAM:** 16GB DDR4

### 🛠️ Stack
Python, FastAPI, Ollama, PyPDF2, Uvicorn

### 📦 Como Rodar

```bash
# 1. Instalar modelo
ollama pull qwen2.5:14b

# 2. Instalar dependências
pip install fastapi uvicorn PyPDF2 requests python-multipart ollama

# 3. Rodar API
uvicorn main:app --host 0.0.0.0 --port 8000

# 4. Testar
# Abra http://localhost:8000/docs
