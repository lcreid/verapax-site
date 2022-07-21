# verapax-site

## Development

With Docker, just use a standard Docker Jekyll container:

```bash
JEKYLL_VERSION=4.1.0 # Or whichever version you want
docker run -p 4000:4000 --volume="$PWD:/srv/jekyll" -it jekyll/jekyll:$JEKYLL_VERSION jekyll serve
```
