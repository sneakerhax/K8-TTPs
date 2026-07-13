# Inspecting container images

**Description:** This entry describes how to inspect images for secrets or other details

**Requirements:** docker

**Optional:** dfimage, dive

**MSID:** MS-TA9001, MS-TA9004

## Inspecting an image using Docker

```
docker history <image>
```

Prints the build steps for an image

```
docker inspect <image>
```

Prints the full build manifest (secrets can be found in environment variables)

## Inspecting an image using external tools

```
docker run -v /var/run/docker.sock:/var/run/docker.sock ghcr.io/laniksj/dfimage <image>
```

Prints contents of Dockerfile

```
docker run --rm -it -v /var/run/docker.sock:/var/run/docker.sock -v $(pwd):/output wagoodman/dive <image>
```

Runs the dive tool on an image to interactively explore layer contents and identify wasted space or sensitive files
  
## References
* [Docker image history](https://docs.docker.com/reference/cli/docker/image/history/)
* [Docker inspect](https://docs.docker.com/reference/cli/docker/inspect/)
* [Github - dfimage](https://github.com/LanikSJ/dfimage)
* [Github - Dive](https://github.com/wagoodman/dive)
