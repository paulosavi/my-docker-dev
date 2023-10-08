# Configurações para o ambiente linux

### Alterar necessidade de password no docker
``` bash
sudo visudo
```

### Adicionar a linha abaixo no final do arquivo
``` bash
<user> ALL=(ALL) NOPASSWD: ALL
```

### Remover necessidade do sudo para o docker
``` bash
sudo usermod -aG docker $USER
```

### Adicionar UID e GID do usuário docker sempre que uma sessão for iniciada
``` bash
echo "export DOCKER_UID=$(id -u)" >> ~/.bashrc
echo "export DOCKER_GID=$(id -g)" >> ~/.bashrc
```

### Depois de adicionar, aplique as mudanças com:
``` bash
source ~/.bashrc
```

### Comando para iniciar container com o build
``` bash
docker-compose up -d --build
```
