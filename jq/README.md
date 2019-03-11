## jq


### Usage

```
curl -s 'https://api.github.com/repos/jdkelley/dockerfiles/commits?per_page=1' | docker run --rm -i jdkelley/jq .[0].commit.verification
```

### Deployed

This is deployed on Docker Hub using their autobuilds tool:

* <https://hub.docker.com/r/jdkelley/jq>
