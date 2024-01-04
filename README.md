- Create environment file (sample provided)
- Start all services:
```
docker compose -f docker-compose-no-big-data.yml up -d
```
- Insert data into postgres:
```
docker exec -it postgres psql -U app
\i /tmp/sql/init.sql;
```
**Note**: Reserve is currently not updated in the database. It is only stored as an event in Kafka.