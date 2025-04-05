# API de Usuários (Flask)

Esta é uma API simples construída com **Flask** que simula operações básicas de CRUD (Create, Read) para usuários. Os dados são armazenados em um dicionário em memória, sem persistência em banco de dados.

## 🚀 Tecnologias

- Python 3.x
- Flask

Comandos para rodar o Docker: https://github.com/JoaoTrevisam/Tabalho-Cloud.git

cd Trabalho-Cloud

cd API_Flask

docker build -t flask-api .  

docker run -p 5000:5000 flask-api

📚 Endpoints

URL: /usuario/

Método: GET

Resposta de sucesso: 200 OK

{
  "1": {"nome": "João da Silva", "email": "joao@exemplo.com", "senha": "senha123"},
  ...
}

🔍 Obter um usuário específico
URL: /usuario/<id_usuario>

Método: GET

Resposta de sucesso: 200 OK

Resposta de erro: 404 Not Found

➕ Criar um novo usuário
URL: /usuario

Método: POST

Body (JSON):

{
  "nome": "Novo Usuário",
  "email": "novo@exemplo.com",
  "senha": "minhasenha"
}

📤 Requisição POST para criar um novo usuário
{
  "nome": "Naruto Uzumaki",
  "email": "naruto@exemplo.com",
  "senha": "rasengan123"
}
Resposta esperada:
{
  "id_usuario": "4"
}

Resposta da rota GET /usuario/ (listar todos os usuários)
{
  "1": {
    "nome": "João da Silva",
    "email": "joao@exemplo.com",
    "senha": "senha123"
  },
  "2": {
    "nome": "Maria do Bairro",
    "email": "maria@exemplo.com",
    "senha": "senha456"
  },
  "3": {
    "nome": "Goku Super Saiyajin 3",
    "email": "goku@exemplo.com",
    "senha": "senha789"
  },
  "4": {
    "nome": "Naruto Uzumaki",
    "email": "naruto@exemplo.com",
    "senha": "rasengan123"
  }
}

Resposta da rota GET /usuario/2 (usuário existente)
{
  "nome": "Maria do Bairro",
  "email": "maria@exemplo.com",
  "senha": "senha456"
}
