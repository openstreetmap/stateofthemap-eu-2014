# State of the Map Europe 2014

Static archive of the State of the Map Europe 2014 conference in Karlsruhe,
available at [2014.stateofthemap.eu](https://2014.stateofthemap.eu/).

## Running locally

This is a fully static export of the original Rails site. All internal links
point to explicit `.html` files, so no URL rewriting is required.

The site is served by nginx using the included
[`Dockerfile`](./Dockerfile) and [`docker-compose.yml`](./docker-compose.yml):

```sh
docker compose up
```

Then open <http://localhost:8080/>.

## Media compression

Large downloads in [`slides/`](./slides/) and [`postercom/`](./postercom/) have
been recompressed:

- PDF images are downsampled to 150 dpi for slides and 200 dpi for posters.
- Large PNG posters are palette-quantised.
- `slides/94-4.mov` was re-encoded as `slides/94-4.mp4` using H.264.
- `postercom/sotm2014.tiff` was converted to PNG.

No published file exceeds 100 MB.
