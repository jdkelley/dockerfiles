## jq

[jq][1] in a container. This is useful if you do not want to depend on having installed dependencies to your CI node or if you are unable to install dependencies.

On how to use jq, see the [manual][1] and [source code][2]. To test your filters and expressions use [jq playground][3].

### Usage

```
$ curl -s 'https://api.github.com/repos/jdkelley/dockerfiles/commits?per_page=1' | docker run --rm -i jdkelley/jq .[0].commit.verification
{
  "verified": false,
  "reason": "unsigned",
  "signature": null,
  "payload": null
}
```

If you want to use jq in a container on your local system but do not want to type out the long `docker run` command every time you want to use it, you may wish to add a bash alias like:

```
alias jq="docker run --rm -i jdkelley/jq"
```

NB: Since the `-i` flag is hard coded into this alias, this alias will only work with content that is piped to it. If you try to use it directly, you would need to call the container directly with `-it` or add another alias like: 

```
alias jqit="docker run --rm -it jdkelley/jq"
```

### Deployed

This is deployed on [Docker Hub][4] and [GitHub Package Registry][5].

[//]: # "LINKS"

[1]: https://stedolan.github.io/jq/       "jq"
[2]: https://github.com/stedolan/jq       "jq Source Code (GitHub)"
[3]: https://jqplay.org/                  "jq Playground"
[4]: https://hub.docker.com/r/jdkelley/jq "jdkelley/jq"
[5]: https://github.com/jdkelley/dockerfiles/packages/39805 "Deployed on GitHub Package Registry"
