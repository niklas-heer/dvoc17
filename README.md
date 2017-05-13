



[DevOps Camp 2017](http://www.devops-camp.de/)
========================

# Session Caddy

This repo contains the session notes for the session "Caddy" at the [#dvoc17](https://twitter.com/search?q=%23dvoc17)

## Links

- Caddy: https://caddyserver.com/
- Let's Encrypt: https://letsencrypt.org/
- Caddy Docs: https://caddyserver.com/docs
- Caddy Build service: https://caddyserver.com/download
- Caddy on Dockerhub: https://hub.docker.com/r/abiosoft/caddy/
- What's new in caddy: https://caddyserver.com/blog/caddy-0_10-released
- Caddy & QUIC: https://github.com/mholt/caddy/wiki/QUIC
- Caddy Syntax Support for Sublimetext: https://github.com/caddyserver/sublimetext
- Caddy Examples: https://github.com/caddyserver/examples

## Log

```
$ docker run -d \
    -e "CADDYPATH=/etc/caddycerts" \
    -v $(pwd)/.caddy:/etc/caddycerts \
    -v $(pwd):/srv \
    -v $(pwd)/Caddyfile:/etc/Caddyfile \
    -p 80:80 -p 443:443 \
    abiosoft/caddy
```

```
$ git clone https://github.com/abiosoft/caddy-docker.git
$ cd caddy-docker/
$ docker build --build-arg plugins=http.git -t caddy-plugins .
```

## More Stuff

see also: https://github.com/niklas-heer/dvocc16
