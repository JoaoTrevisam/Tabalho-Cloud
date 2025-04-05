Comandos para rodar o Docker: https://github.com/JoaoTrevisam/Tabalho-Cloud.git

cd Trabalho-Cloud

cd API_Flask

docker build -t flask-api .  

docker run -p 5000:5000 flask-api

