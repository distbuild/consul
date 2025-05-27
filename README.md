# consul

Consul docker

## Deploy

```bash
docker run \
    -d \
    -p 8500:8500 \
    -p 8600:8600/udp \
    -v /path/to/consul/config:/consul/config \
    -v /path/to/consul/data:/consul/data \
    --name=consul \
    consul agent -server -ui -node=server-1 -bootstrap-expect=1 -client=0.0.0.0
```

## Reference

- [consul-docker](https://developer.hashicorp.com/consul/docs/deploy/server/docker)
