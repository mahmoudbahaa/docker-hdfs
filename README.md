# HDFS with Docker

Docker image for single HDFS node.

License: **MIT**

## Local build
```sh
$ docker build -t mdouchement/hdfs .
```

## Running HDFS container

```sh
# Running and get a Bash interpreter
$ docker run -p 9000:9000 -p 50020:50020 -p 50070:50070 -p 50075:50075 -it mdouchement/hdfs

# Running as daemon
$ docker run -p 9000:9000 -p 50020:50020 -p 50070:50070 -p 50075:50075 -d mdouchement/hdfs
```

- Ports
  - hdfs://localhost:9000 -> `9000`
  - HDFS namenode -> `50020`
  - HDFS Web browser -> `50070`
  - HDFS datanodes -> `50075`
  - HDFS secondary namenode -> `50075`


## Contributing

All PRs are welcome.

1. Fork it ( https://github.com/[my-github-username]/gemsupport/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
