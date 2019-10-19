## bash

[Bash][1] in a container. This is useful if the system you are on does not have an up to date version of bash and you are unable to upgrade. Examples of this might be a shared CI node, a build server that must provide multiple versions of bash, or a Mac.

### Usage

```
docker run --rm \
    -it \
    jdkelley/bash
```

To use this instead of the local version of bash, create an alias:

```
alias bash="docker run --rm -it jdkelley/bash"
```

### Using scripts on your local filesystem.

There may be times when you want to use a directory of files inside your bash container. Map in the directory as a volume:

```
docker run --rm \
    -v <scripts-directory>:/scripts \
    -it \
    jdkelley/bash
```

To map your current directory, use:

```
docker run --rm \
    -v ${PWD}:/scripts \
    -it \
    jdkelley/bash
```

### Deployed

This is deployed on [Docker Hub][2] and [GitHub Package Registry][3].

[//]: # "LINKS"

[1]: https://www.gnu.org/software/bash/     "GNU Bash"
[2]: https://hub.docker.com/r/jdkelley/bash "jdkelley/bash"
[3]: https://github.com/jdkelley/dockerfiles/packages/39804 "On GitHub Package Registry"
