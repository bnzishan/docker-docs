# Supported tags and respective `Dockerfile` links

-	[`0.12`, `0.12.2` (*0.12/Dockerfile*)](https://github.com/influxdata/influxdb-docker/blob/6d869aa598baf9d23019682ecff42d022a00ce17/0.12/Dockerfile)
-	[`0.13`, `0.13.0`, `latest` (*influxdb/0.13/Dockerfile*)](https://github.com/influxdata/influxdata-docker/blob/a2e36a415b71cd2b0bff87d0eaaf6d5329451c7c/influxdb/0.13/Dockerfile)
-	[`0.13-alpine`, `0.13.0-alpine`, `alpine` (*influxdb/0.13/alpine/Dockerfile*)](https://github.com/influxdata/influxdata-docker/blob/a2e36a415b71cd2b0bff87d0eaaf6d5329451c7c/influxdb/0.13/alpine/Dockerfile)
-	[`1.0.0-beta2` (*influxdb/1.0/Dockerfile*)](https://github.com/influxdata/influxdata-docker/blob/a2e36a415b71cd2b0bff87d0eaaf6d5329451c7c/influxdb/1.0/Dockerfile)
-	[`1.0.0-beta2-alpine` (*influxdb/1.0/alpine/Dockerfile*)](https://github.com/influxdata/influxdata-docker/blob/a2e36a415b71cd2b0bff87d0eaaf6d5329451c7c/influxdb/1.0/alpine/Dockerfile)

[![](https://badge.imagelayers.io/influxdb:latest.svg)](https://imagelayers.io/?images=influxdb:0.12,influxdb:0.13,influxdb:0.13-alpine,influxdb:1.0.0-beta2,influxdb:1.0.0-beta2-alpine)

For more information about this image and its history, please see [the relevant manifest file (`library/influxdb`)](https://github.com/docker-library/official-images/blob/master/library/influxdb). This image is updated via [pull requests to the `docker-library/official-images` GitHub repo](https://github.com/docker-library/official-images/pulls?q=label%3Alibrary%2Finfluxdb).

For detailed information about the virtual/transfer sizes and individual layers of each of the above supported tags, please see [the `influxdb/tag-details.md` file](https://github.com/docker-library/docs/blob/master/influxdb/tag-details.md) in [the `docker-library/docs` GitHub repo](https://github.com/docker-library/docs).

# InfluxDB

InfluxDB is a time series database built from the ground up to handle high write and query loads. InfluxDB is meant to be used as a backing store for any use case involving large amounts of timestamped data, including DevOps monitoring, application metrics, IoT sensor data, and real-time analytics.

[InfluxDB Documentation](https://docs.influxdata.com/influxdb/latest/)

![logo](https://raw.githubusercontent.com/docker-library/docs/43d87118415bb75d7bb107683e79cd6d69186f67/influxdb/logo.png)

## Using this Image

### Running the container

The InfluxDB image exposes a shared volume under `/var/lib/influxdb`, so you can mount a host directory to that point to access persisted container data. A typical invocation of the container might be:

```console
$ docker run -p 8083:8083 -p 8086:8086 \
      -v $PWD:/var/lib/influxdb \
      influxdb
```

Modify `$PWD` to the directory where you want to store data associated with the InfluxDB container.

You can also have Docker control the volume mountpoint by using a named volume.

```console
$ docker run -p 8083:8083 -p 8086:8086 \
      -v influxdb:/var/lib/influxdb \
      influxdb
```

### Exposed Ports

The following ports are important and are used by InfluxDB.

-	8086 HTTP API port
-	8083 Administrator interface port

The HTTP API port will be automatically exposed when using `docker run -P`.

The administrator interface is not automatically exposed when using `docker run -P`. While the administrator interface is run by default, the adminstrator interface requires that the web browser have access to InfluxDB on the same port in the container as from the web browser. Since `-P` exposes the HTTP port to the host on a random port, the administrator interface is not compatible with this setting.

Find more about API Endpoints & Ports [here](https://docs.influxdata.com/influxdb/latest/concepts/api/).

### Configuration

InfluxDB can be either configured from a config file or using environment variables. To mount a configuration file and use it with the server, you can use this command:

Generate the default configuration file:

```console
$ docker run --rm influxdb influxd config > influxdb.conf
```

Modify the default configuration, which will now be available under `$PWD`. Then start the InfluxDB container.

```console
$ docker run -p 8083:8083 -p 8086:8086 \
      -v $PWD/influxdb.conf:/etc/influxdb/influxdb.conf:ro \
      influxdb -config /etc/influxdb/influxdb.conf
```

Modify `$PWD` to the directory where you want to store the configuration file.

For environment variables, the format is `INFLUXDB_$SECTION_$NAME`. All dashes (`-`) are replaced with underscores (`_`). If the variable isn't in a section, then omit that part.

Examples:

```console
INFLUXDB_REPORTING_DISABLED=true
INFLUXDB_META_DIR=/path/to/metadir
INFLUXDB_DATA_QUERY_LOG_ENABLED=false
```

Find more about configuring InfluxDB [here](https://docs.influxdata.com/influxdb/latest/introduction/installation/)

### Graphite

InfluxDB supports the Graphite line protocol, but the service and ports are not exposed by default. To run InfluxDB with Graphite support enabled, you can either use a configuration file or set the appropriate environment variables. Run InfluxDB with the default Graphite configuration:

```console
docker run -p 8083:8083 -p 8086:8086 \
    -e INFLUXDB_GRAPHITE_ENABLED=true \
    influxdb
```

See the [README on GitHub](https://github.com/influxdata/influxdb/blob/master/services/graphite/README.md) for more detailed documentation to set up the Graphite service. In order to take advantage of graphite templates, you should use a configuration file by outputting a default configuration file using the steps above and modifying the `[[graphite]]` section.

### HTTP API

Creating a DB named mydb:

```console
$ curl -G http://localhost:8086/query --data-urlencode "q=CREATE DATABASE mydb"
```

Inserting into the DB:

```console
$ curl -i -XPOST 'http://localhost:8086/write?db=mydb' --data-binary 'cpu_load_short,host=server01,region=us-west value=0.64 1434055562000000000'
```

Read more about this in the [official documentation](https://docs.influxdata.com/influxdb/latest/guides/writing_data/)

### CLI / SHELL

Start the container:

```console
$ docker run --name=influxdb -d -p 8083:8083 -p 8086:8086 influxdb
```

Run the influx client in another container:

```console
$ docker run --rm --net=container:influxdb -it influxdb influx -host influxdb
```

At the moment, you cannot use `docker exec` to run the influx client since `docker exec` will not properly allocate a TTY. This is due to a current bug in Docker that is detailed in [docker/docker#8755](https://github.com/docker/docker/issues/8755).

### Web Administrator Interface

Navigate to [localhost:8083](http://localhost:8083) with your browser while running the container.

See more about using the web administrator interface [here](https://docs.influxdata.com/influxdb/latest/tools/web_admin/).

# License

View [license information](https://github.com/influxdata/influxdb/blob/master/LICENSE) for the software contained in this image.

# Supported Docker versions

This image is officially supported on Docker version 1.11.2.

Support for older versions (down to 1.6) is provided on a best-effort basis.

Please see [the Docker installation documentation](https://docs.docker.com/installation/) for details on how to upgrade your Docker daemon.

# User Feedback

## Documentation

Documentation for this image is stored in the [`influxdb/` directory](https://github.com/docker-library/docs/tree/master/influxdb) of the [`docker-library/docs` GitHub repo](https://github.com/docker-library/docs). Be sure to familiarize yourself with the [repository's `README.md` file](https://github.com/docker-library/docs/blob/master/README.md) before attempting a pull request.

## Issues

If you have any problems with or questions about this image, please contact us through a [GitHub issue](https://github.com/influxdata/influxdata-docker/issues). If the issue is related to a CVE, please check for [a `cve-tracker` issue on the `official-images` repository first](https://github.com/docker-library/official-images/issues?q=label%3Acve-tracker).

You can also reach many of the official image maintainers via the `#docker-library` IRC channel on [Freenode](https://freenode.net).

## Contributing

You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

Before you start to code, we recommend discussing your plans through a [GitHub issue](https://github.com/influxdata/influxdata-docker/issues), especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing.
