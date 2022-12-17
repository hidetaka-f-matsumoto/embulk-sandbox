# Embulk Sandbox

## Run query in postgres, output to csv

```
docker-compose run --rm \
    -e EMBULK_CONFIG=pg_to_csv \
    -e PG_QUERY='SELECT id, body::text FROM json_samples' \
    embulk
```
