## About
`Dockerized` version of `imagemagick`.

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
