## csvkit

[csvkit][1] in a container. This is useful if you do not want to depend on having installed dependencies to your CI node or if you are unable to install dependencies.

For full usage visit the [source code][2] and the [latest release documentation][3].

### Usage | Pipes

```
curl -L -s https://raw.githubusercontent.com/wireservice/csvkit/master/examples/realdata/acs2012_5yr_population.csv | \
    docker run --rm \
    -i \
    jdkelley/csvkit \
    csvlook
```

To use this instead of the local version of csvkit, create an alias:

```
alias csvkit="docker run --rm -i jdkelley/csvkit"
```

### Usage | Local Files

There may be times when you want to use a directory of files inside your csvkit container. Map in the directory as a volume:

```
docker run --rm \
    -v <scripts-directory>:/scripts \
    -it \
    jdkelley/csvkit
```

To map your current directory, use:

```
docker run --rm \
    -v ${PWD}:/scripts \
    -it \
    jdkelley/csvkit
```

### Deployed

This is deployed on Docker Hub using their autobuilds tool: [jdkelley/bash][4]

[//]: # "LINKS"

[1]: https://csvkit.readthedocs.io/en/1.0.3/                    "csvkit docs"
[2]: https://github.com/wireservice/csvkit                      "csvkit Source Code (GitHub)"
[3]: https://media.readthedocs.org/pdf/csvkit/latest/csvkit.pdf "Latest Release Documentation"
[4]: https://hub.docker.com/r/jdkelley/csvkit                   "jdkelley/csvkit on Docker Hub"
