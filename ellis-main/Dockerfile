# Imagem base do Python 3.10 (conforme pré-requisitos no readme)
FROM python:3.10-slim

# Define o diretório de trabalho
WORKDIR /app

# Copia o arquivo de requisitos e instala as dependências
COPY requirements.txt .
RUN pip install --no-cache-dir --upgrade pip && pip install --no-cache-dir -r requirements.txt

# Copia o restante do código da aplicação
COPY . .

# Expõe a porta 8000 (padrão do Uvicorn/FastAPI)
EXPOSE 8000

# Comando para iniciar a aplicação ouvindo em todas as interfaces de rede
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "8000"]