# test-spring-boot

# O Contexto
A Tecnobooks é um Market Place de livros de tecnologia (fictícia) onde escritores independentes
conseguem fazer suas publicações de forma rápida e barata e leitores interessados nesse tema
encontram livros por preços acessíveis.
O sistema da Tecnobooks é dividido em vários pequenos componentes de software distribuídos em
um cluster do Kubernetes hospedado na nuvem. A implantação de cada componente é feita
manualmente por um analista de operações.

Percebendo a grande dificuldade de manter a implantação dos sistemas de forma manual, a empresa
decidiu automatizar esse processo.



# Premissas

  - Dar permissão ao Jenkins par que possua os devidos acessos ao registry de imagens Docker e ao
Kubernete. Por enquanto, dispensar a autenticação nesses ambientes;
  - Considerar que qualquer imagem com a tag no formato tecnobooks/<app-name>:<version>
será publicada no registry correto;
  - Pode-se utilizar o helm e, se for esse o caso, 
  - Considerar a implantação apenas em ambiente de desenvolvimento. Futuramente implantar em teste, homologação e produção.

![image](https://user-images.githubusercontent.com/22057957/111466720-663ead00-8702-11eb-83b3-4ee1481e1a46.png)



# Jenkins no Google Kubernetes Engine

# Objetivos

  - Criar um cluster do Kubernetes com o GKE.
  - Instalar o Jenkins usando o Helm.
  - Conectar ao Jenkins.
  - Pipeline declarativo no formato de um Jenkinsfile
  - Imagem Docker da aplicação
  - Publicar a imagem em um registry privado;
  - Atualizar o Kubernetes com a nova versão da imagem publicada.

![image](https://user-images.githubusercontent.com/22057957/111410051-c871c080-86b6-11eb-9ddf-9bd6fae05c9c.png)

# Dados da máquina no Googlecloud

O Jenkins está roandando no endereço: http://35.199.64.97:8080/login?from=%2F

