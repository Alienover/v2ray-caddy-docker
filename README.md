
# v2ray-caddy-docker
This setting is based on [ws-tls-web] which using the [caddy] as the web server and all the server are running in docker.

Leave a star if you like it or issue me if there're questions.

### Variables
|Variable|Type|Description|
|---|---|---|
|DOMAIN|**String**|Website domain for TLS certificate authority|
|PROXY_PORT|**Number**|The exposed port to receive websocket request|
|UUID|**String**|The universally unique identifier for v2ray server. Get from `https://www.uuidgenerator.net/` or use command `uuidgen`|
|WS_PATH|**String**|Path to connect websocket. Format like `/:ws-path`. *ps. `/:path` isn't equal to `/:path/`*

All you need to do is to modify the variables above to your specified info in the following files
* *Caddyfile* Replace **DOMAIN**, **WS_PATH** and **PROXY_PORT**
* *server_config.json* Replace **PROXY_PORT**, **UUID** and **WS_PATCH**
* *client_config.json* Replace **DOMAIN**, **PROXY_PORT**, **UUID** and **WS_PATCH**
* *docker-compose.yml* Replace **PROXY_PORT**

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

[UUID Generator][uuid-generator]

[ws-tls-web]: https://toutyrater.github.io/advanced/wss_and_web.html
[caddy]: https://caddyserver.com/
[docker-compose]: https://docs.docker.com/compose/reference/overview/
[uuid-generator]: https://www.uuidgenerator.net/
