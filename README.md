# 2rpdesafio
INSTALAÇÃO DOCKER:
sudo yum install -y docker
sudo systemctl start docker
sudo systemctl enable docker
 
TESTE:
sudo docker run hello-world 

CRIAÇÃO DA VARIÁVEL:
Criar uma variável:
TWORPTESTE="true100%"

Ver a variável:
echo $TWORPTEST

Exportar a variável para o ambiente:
export TWORPTEST="true100%"

Deletar a variável:
unset TWORPTEST="true100%"


CRIAR APLICAÇÃO:
for i in 1 2 3: do env | grep TERM; date ; sleep 20; done


COMO INICIAR UM CONTAINER:
Comando para puxar a imagem:
docker pull Ubuntu 

Comando para rodar uma imagem:
docker run ubuntu

Para iniciar o container:
docker run --name MeuContainer -it ubuntu bash

Ver o container rodando:
sudo docker ps -a 


CRIAR UM DOCKERFILE:
FROM ruby:2.6-alpine

COPY . /app
WORKDIR /app

CMD ["ruby", "app.rb"]

Fazer o build da imagem e enviar para o Docker Hub:
docker build . -t <sarahalvim>/dummy-logger:1.0
docher push <sarahalvim>/dummy-logger:1.0

CRIAR CLUSTER KUBERNETES
(é necessário fazer a instalação do k3d) 
curl -s https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash
k3d cluster create sarah-cluster

CRIAR SERVICE
vide manifesto service.yaml

CRIAR SECRET
vide manifesto secret.yaml

CRIAR DEPLOYMENT
vide manifesto deployment.yaml
