## jq


### Usage

```
curl -s 'https://api.github.com/repos/jdkelley/dockerfiles/commits?per_page=1' | docker run --rm -i jdkelley/jq .[0].commit.verification
```

