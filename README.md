# Projeto kube-news

### Objetivo
O projeto Kube-news é uma aplicação escrita em NodeJS e tem como objetivo ser uma aplicação de exemplo pra trabalhar com o uso de containers.

### Configuração
Pra configurar a aplicação, é preciso ter um banco de dados Postgre e pra definir o acesso ao banco, configure as variáveis de ambiente abaixo:

DB_DATABASE => Nome do banco de dados que vai ser usado.

DB_USERNAME => Usuário do banco de dados.

DB_PASSWORD => Senha do usuário do banco de dados.

DB_HOST => Endereço do banco de dados.

Kubernetes
1-Criar Dockerfile e fazer o build
docker build -t jonathanabrantes/kube-news:v1 .    ->corrente onde está o dockerfile

2-Fazer o docker push para o repositório do dockerhub
docker push jonathanabrantes/kube-news:v1

3-criar o cluster em k3s
k3d cluster create meucluster -p "80:30000@loadbalancer"

4-criar o deployment do manifesto
kubectl create -f .\deployment.yaml

5-update do deployment do manifesto
kubectl apply -f .\deployment.yaml

6-deletar o deployment do manifesto
kubectl delete -f .\deployment.yaml
