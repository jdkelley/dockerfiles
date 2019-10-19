## Apache Benchmark

[ab][1] in a container. This is useful if you are on a system you are unable to upgrade. Examples of this might be a shared CI node, a build server that must provide multiple versions of ab, or a Mac.

### Usage

```
docker run --rm \
    -it \
    jdkelley/ab <url>
```

To use this instead of the local version of ab, create an alias:

```
alias ab="docker run --rm -it jdkelley/ab"
```

### Deployed

This is deployed on [Docker Hub][2] and [GitHub Package Registry][3].

[//]: # "LINKS"

[1]: https://httpd.apache.org/docs/2.4/programs/ab.html     "ab"
[2]: https://hub.docker.com/r/jdkelley/ab                   "jdkelley/ab"
[3]: https://github.com/jdkelley/dockerfiles/packages/39806 "Deployed on GitHub Package Registry"
