# docker-haproxy-env
Bare minimum HAProxy docker image that does TCP roundrobin on backends supplied by environment variable.

### How to use?

- Install docker

- `docker run -d --name proxy -p 80:80 -e PORT=80 -e BACKENDS=foo.com,bar.com viranch/haproxy-env`

- Replace following things as desired:
  - `-p 80:80 -e PORT=80` with desired port numbers.
  - `-e BACKENDS=foo.com,bar.com` with actual app server backends.

### What does it contain?

- [HAProxy](https://hub.docker.com/_/haproxy/)
- [dockerize](https://github.com/jwilder/dockerize)

### Customizing

##### haproxy.tmpl config template

This is the template as explained in `jwilder/dockerize` for configuring HAProxy. Customize it to your needs and if you think it will help others, send a pull request :)
