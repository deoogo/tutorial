<h1> Conteiners </h1>

### Build Dockerfile

```bash
* docker image build -t userDockerHub/nome:TAG.
* docker images ls
* docker container run -d userDockerHub/nome:TAG
* docker container ls
```

### Registry docker

```bash
* docker images tag IDconteiner userDockerHub/nome:TAG
* docker login registry.com
* docker push userDockerHub/nome:TAG
* docker pul userDockerHub/nome:TAG
```
### Comandos docker 

```bash
* docker container run -it IMAGE
* docker run -d -p 0:0
* docker exec -it conteiner /bash ou sh
```

### Volume

```bash
* docker run -ti --mount type=bind.src=caminhoHost.dist=/caminhoConteiner IMAGEM
* docker volume ls
* docker volume create **nome**
* docker volume inspect **nome**
* docker run -ti --mount type=**volume**.src=**nome**.dist=/caminhoConteiner IMAGEM
* docker volume prune
```