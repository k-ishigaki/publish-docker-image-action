# publish-docker-image-action
A simple GitHub composite action for a Docker repository.

### Example

```yaml
name: Docker Image CI

on:
  push:
    branches:
      - 'main'
    tags:
      - 'v*.*.*'

jobs:
  docker:
    runs-on: ubuntu-latest
    steps:
      -
        name: Publish Docker image
        uses: k-ishigaki/publish-docker-image-action@main
        with:
        token: ${{ secrets.GITHUB_TOKEN }}
```
