# HDFS with Docker

Docker image for single HDFS node.

**Only for development purpose.**

License: **MIT**

## Local build
```sh
$ docker build -t mdouchement/hdfs .
```

## Running HDFS container

```sh
# Running and get a Bash interpreter
$ docker run -p 22022:22 -p 8020:8020 -p 50010:50010 -p 50020:50020 -p 50070:50070 -p 50075:50075 -it mdouchement/hdfs

# Running as daemon
$ docker run -p 22022:22 -p 8020:8020 -p 50010:50010 -p 50020:50020 -p 50070:50070 -p 50075:50075 -d mdouchement/hdfs
```

- Ports
  - HDFS namenode -> `8020` (hdfs://localhost:8020)
  - HDFS datanode -> `50010`
  - HDFS datanode (ipc) -> `50020`
  - HDFS Web browser -> `50070`
  - HDFS datanode (http) -> `50075`
  - HDFS secondary namenode -> `50090`
  - SSH -> `22`


## Contributing

All PRs are welcome.

1. Fork it ( https://github.com/[my-github-username]/gemsupport/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
