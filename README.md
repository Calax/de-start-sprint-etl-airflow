# Тренажер для спринта

## Для настройки airflow выполните команду:

```bash
docker compose up airflow-init
```
Эту команду достаточно выполнить один раз.

## Для запуска Airflow и выполнения заданий выполните команду в терминале:

```bash
docker compose up -d airflow-webserver airflow-scheduler airflow-worker airflow-triggerer vsc
```

тренажер доступен по адресу [http://localhost:7090](http://localhost:7090),

airflow по  [http://localhost:8080](http://localhost:8080),

для запуска сервисов понадобится какое-то время.

База данных PostgreSQL:

```json
"host": "localhost",
"port": 15432,
"database": "student",
"username": "student",
"password": "student-de"
```

## Для запуска metabase и выполнения заданий выполните:

```bash
docker compose up -d metabase
```

metabase доступен по адресу [http://localhost:13000](http://localhost:13000)

## Остановка и удаление

Для остановки тренажера выполните docker compose down
Для возобновления повторите команды из предыдущих пунктов.

По окончании спринта остановите контейнеры и удалите образы с системы (будут удалены все сохраненные данные - БД, решения в заданиях и ДАГи): `docker compose down --volumes --rmi all`
