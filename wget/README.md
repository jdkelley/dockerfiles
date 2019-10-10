## wget

[wget][1] in a container. This is useful if the system you are on does not have an up to date version of wget and you are unable to upgrade. Examples of this might be a shared CI node, a build server that must provide multiple versions of bash, or a Mac.

I also use this and a derivitive container to spin up multiple containers making requests to a service.

### Usage

```sh
docker run --rm \
    -it \
    jdkelley/wget <wget options>
```

### Downloading resources

Most use-cases of `wget` involve downloading a resource from the internet. To do that, map in the directory as a volume:

```sh
docker run --rm \
    -v <scripts-directory>:/scripts \
    -it \
    jdkelley/wget <wget options and parameters>
```

Here is an example:

```sh
docker run --rm \
    -it \
    -v `pwd`:/downloads \
    jdkelley/wget https://github.com/alpinelinux/docker-alpine/blob/da78fcf5c5da55092aa82a97095274b3df648866/x86_64/alpine-minirootfs-3.10.2-x86_64.tar.gz?raw=true
```

To use this instead of the local version of wget, create an alias:

```sh
alias wget="docker run --rm -it -v `pwd`:/downloads jdkelley/wget"
```

### Inspect headers

Inspect headers with:

```sh
docker run --rm \
    -it \
    jdkelley/wget --server-response --spider https://google.com
```

### Deployed

This is deployed on Docker Hub using their autobuilds tool: [jdkelley/wget][2]

[//]: # "LINKS"

[1]: https://www.gnu.org/software/wget/manual/     "GNU Wget"
[2]: https://hub.docker.com/r/jdkelley/wget        "jdkelley/wget on Docker Hub"
