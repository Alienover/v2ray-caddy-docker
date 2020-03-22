
# v2ray-caddy-docker
This setting is based on [ws-tls-web] which using the [caddy] as the web server and all the server are running in docker.

### Variables
|Variable|Description|
|---|---|
|DOMAIN|Website domain for TLS certificate authority|
|PROXY_PORT|The exposed port to receive websocket request|
|UUID|The universally unique identifier for v2ray server. Get from `https://www.uuidgenerator.net/` or use command `uuidgen`|

All you need to do is to modify the variables above to your specified info.

### Related Command
```shell
# Build (Will start at default after building)
$ docker-compose up --build -d

# Start
$ docker-compose start

# stop
$ docker-compose stop

# Show logs
$ docker-compose logs -f
```

### Referrences:

[Caddy Server][caddy]

[Docker Compose][docker-compose]

[Websocket-TLS-Web][ws-tls-web]

[ws-tls-web]: https://toutyrater.github.io/advanced/wss_and_web.html
[caddy]: https://caddyserver.com/
[docker-compose]: https://docs.docker.com/compose/reference/overview/
