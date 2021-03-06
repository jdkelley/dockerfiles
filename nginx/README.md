## nginx

Currently the alpine based [Nginx][1] container on Docker Hub has two security vulnerabilities ([CVE-2019-1549][2] and [CVE-2019-1563][3]) around OpenSSL. There is a [Github ticket][4] to resolve these CVEs but there is no telling when this will be shipped in the docker-alpine repo.  

This container is a convenience image I am using so I know I am using a patched nginx container. 

### Usage

In your Dockerfile:

```dockerfile
FROM jdkelley/nginx:latest
...
```

### Deployed

This is deployed on [Docker Hub][5] and [GitHub Package Registry][6].

[//]: # "LINKS"

[1]: https://hub.docker.com/_/nginx                                "Nginx Container"
[2]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-1549  "CVE-2019-1549"
[3]: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-1563  "CVE-2019-1563"
[4]: https://github.com/alpinelinux/docker-alpine/issues/39        "docker-alpine Issue #39"
[5]: https://hub.docker.com/r/jdkelley/nginx                       "jdkelley/nginx"
[6]: https://github.com/jdkelley/dockerfiles/packages/39809 "Deployed on GitHub Package Registry"
