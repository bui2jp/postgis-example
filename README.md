# postgis

docker pull postgis/postgis:11-3.1

docker run --name some-postgis -e POSTGRES_PASSWORD=mysecretpassword -d postgis/postgis

docker run -it --link some-postgis:postgres --rm postgres \
    sh -c 'exec psql -h "$POSTGRES_PORT_5432_TCP_ADDR" -p "$POSTGRES_PORT_5432_TCP_PORT" -U postgres'

