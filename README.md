Primeiramente, instalei o ambiente Docker na minha distro Ubuntu 20.04.4 LTS do Linux. 

Em seguida, loguei como root utilizando:
   ~$ sudo su

E baixei a imagem do WordPress do Docker Hub:
    docker pull wordpress

Se usarmos o comando "docker images", conseguimos ver
as imagens baixadas disponíveis.

Para executarmos a imagem do WordPress, precisamos especificar o nome do container, uma porta para o seviço rodar, e qual a imagem base que será executada.
Assim:
    docker run --name litle_wordpress -p 8080:80 -d wordpress

Para visualizar os container que estão rodando no docker, basta usar:
    docker ps

No comando "docker ps" é inicado a o endereço e a porta onde a aplicação do wordpress está rodando. Assim, se acessarmos o endereço + porta iremos usar e interagir com a instância do wordpress normalmente.

Para mostrar todos os containers, executados ou parados, basta usar:
    docker ps -a

Assim, se quisermos remover um container precisamos parar sua execução com o comando:
    docker stop ID_DO_CONTAINER

De forma trivial, os comando para iniciar, reiniciar e remover são:
    docker start ID_DO_CONTAINER
    docker restart ID_DO_CONTAINER
    docker rm ID_DO_CONTAINER

Já para remover a imagem base, basta usar o comando:
    docker rmi NOME_DA_IMAGEM

ps: Para remover a imagem, primeiro tem que remover sua instância 


Isso é apena a ponta da ponta de um enorme iceberg que é o Docker. A ideia é adicionar a este repositório alguma aplicação específica usando esta tecnologia de mini virtualizações.
