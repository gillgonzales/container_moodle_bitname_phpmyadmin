# Instruções

Renomei o arquivo .env.example para .env e altere as variáveis de configuração de portas, senhas e do moodle conforme a necessidade.

Para iniciar o container execute o seguinte comando na raiz do diretório:

```shell
docker compose up
```

Caso necessite recriar o container, lembre que os volumes não são recriados, portanto, se necessário, exclua os volumes se for o caso.


Para recriar rode o comando
```shell
docker compose up --build
```

Para pausar os serviços rode:
```shell
docker compose stop
```

Para remover os containers rode:
```shell
docker compose down
```

Mas lembre que os volumes não são removidos automaticamente. Para removê-los rode o seguinte comando de acordo com o nome dos volumes criados:
```shell
docker compose down;
docker volume rm moodle_bitnami_phpmyadmin_moodle_data moodle_bitnami_phpmyadmin_mariadb_data moodle_bitnami_phpmyadmin_moodledata_data;
```

Observe que todos os comandos devem ser executados na raiz do projeto, caso não esteja na rais, será necessário passar o parâmetro -p seguido do nome do projeto (atributo **name** no *docker-compose.yml*)

