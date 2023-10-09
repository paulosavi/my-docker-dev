## Configurações docker em ambiente Linux WSL

### 1. Alterar necessidade de password no docker
``` bash
sudo visudo
```

### 2. Adicionar a linha abaixo no final do arquivo
``` bash
<user> ALL=(ALL) NOPASSWD: ALL
```

### 3. Remover necessidade do sudo para o docker
``` bash
sudo usermod -aG docker $USER
```

### 4. Adicionar UID e GID do usuário docker sempre que uma sessão for iniciada
``` bash
echo "export DOCKER_UID=$(id -u)" >> ~/.bashrc
echo "export DOCKER_GID=$(id -g)" >> ~/.bashrc
```

### 5. Depois de adicionar, aplique as mudanças com:
``` bash
source ~/.bashrc
```

### 6. Comando para iniciar container com o build
``` bash
docker-compose up -d --build
```
