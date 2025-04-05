# Imagem base
FROM python:3.10-slim

# Define o diretório de trabalho dentro do container
WORKDIR /app

# Copia os arquivos da API para o container
COPY . .

# Instala as dependências
RUN pip install --no-cache-dir -r requirements.txt

# Expõe a porta padrão do Flask
EXPOSE 5000

CMD ["python", "api_v1.py"]
