## bash


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

This is deployed on Docker Hub using their autobuilds tool:

* <https://hub.docker.com/r/jdkelley/bash>
