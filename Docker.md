Instalação Docker


```
https://docs.docker.com/desktop/install/windows-install/
```

Instalando WSL


```
https://docs.microsoft.com/pt-br/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package
```

Baixando o MySQL

```
docker pull mysql
```

Se você quiser baixar a versão 5.7 do MySQL, basta colocar no fim da tag a versão desejada. Segue o exemplo.

```
docker pull mysql:5.7
```

Se não for passado nenhum parâmetro, por padrão o docker irá baixar a última versão disponível.


Criando o Container


```
 docker run -it mysql -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=root -e MYSQL_USER=root -e MYSQL_PASSWORD=root bomsabor-db
```

Verificando os Containers existentes

```
docker ps -a
```

Ficar atento ao CONTAINER ID que você acabou de criar, copiar esse mesmo CONTAINER ID.

Executando o container

```
docker exec -it container_id bash
```

Entrando no MySQL de forma manual

```
mysql -uroot -p
Enter password: root
```

Executar alguma instrução SQL caso necessário
