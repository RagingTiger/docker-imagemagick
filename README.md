# About
`Dockerized` version of [imagemagick](https://imagemagick.org/script/index.php).

# Multi-arch Image
The below commands reference a
[Docker Manifest List](https://docs.docker.com/engine/reference/commandline/manifest/)
at [`tigerj/imagemagick`](https://hub.docker.com/r/tigerj/imagemagick)
built using Docker's
[BuildKit](https://docs.docker.com/develop/develop-images/build_enhancements/).
Simply running commands using this image will pull the matching image
architecture (e.g. `amd64`, `arm32v7`, or `arm64`) based on the hosts
architecture. Hence, if you are on a **Raspberry Pi** the below commands will
work the same as if you were on a traditional `amd64` desktop/laptop computer.

## Usage: Example
Here is an example usage where we convert an image to a different
size:
```
$ docker run --rm \
             -v /you/image/path:/tmp \
             -it tigerj/imagemagick \
             convert your_image.jpg \
             -resize 100x100 your_image-resize.jpg
```
