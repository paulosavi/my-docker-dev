# Configurações para o ambiente linux

## Alterar necessidade de password no docker
```sudo visudo```

## Adicionar a linha abaixo no arquivo aberto
```<user> ALL=(ALL) NOPASSWD: ALL```

## Remover necessidade do sudo para o docker
```sudo usermod -aG docker $USER``

## Adicionar UID e GID do usuário docker sempre que uma sessão for iniciada
```echo "export DOCKER_UID=$(id -u)" >> ~/.bashrc```
```echo "export DOCKER_GID=$(id -g)" >> ~/.bashrc```

## Depois de adicionar, aplique as mudanças com:
```source ~/.bashrc```

## Comando para iniciar container com o build
```docker-compose up -d --build```
