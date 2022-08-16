# ktools-docker-fluentd

This is a Fluentd docker image. It can be used to ship logs to a central logging server.

## How to use this image

### Configuration

The fluentd configuration file can be found in `fluent.conf`. You can override any of the settings in this file by creating your own `fluent.conf` in the same directory as the `Dockerfile`.

### Build the image

```
git clone https://github.com/jhonwgo/ktools-docker-fluentd.git
cd ktools-docker-fluentd
docker build -t ktools-docker-fluentd .
```

### Run the container

```
docker run -d -p 24224:24224 -p 24224:24224/udp ktools-docker-fluentd
```
