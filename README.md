Light: директории app, traefik и postgres

1.Развернул 2 виртуальные машины с приложением Horilla https://gitlab.com/deusops/classbook/horilla и PostgreSQL. Запустил приложение на одной машине и протестировал его работу с локальной PostgreSQL. 

2.После успешного тестирования работы приложения с локальной базой подготовил базу на второй машине, изменив allowed адреса в файлах /etc/postrgesql/16/main/postgresql.conf и /etc/postrgesql/16/main/pg_hba.conf

3.Пользуясь готовым Dockerfile создал image и запустил его. Написал docker-compose.yml и запустил с помощью него контейнер с приложением.

4.На 3 виртуальной машине развернул контейнер с traefik в режиме обратного прокси для веб-приложения horilla.

