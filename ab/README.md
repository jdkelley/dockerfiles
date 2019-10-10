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

This is deployed on Docker Hub using their autobuilds tool: [jdkelley/ab][2]

[//]: # "LINKS"

[1]: https://httpd.apache.org/docs/2.4/programs/ab.html     "ab"
[2]: https://hub.docker.com/r/jdkelley/ab                   "jdkelley/ab on Docker Hub"
