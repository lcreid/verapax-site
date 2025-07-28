# verapax-site

## Development

With Docker, use my Rails app and the included `compose.yml` file:

```bash
docker compose up -d
docker compose exec jekyll jekyll server -H 0.0.0.0 --livereload
```

To see draft blog posts, too:

```bash
docker compose up -d
docker compose exec jekyll jekyll server -H 0.0.0.0 --livereload --drafts
```

I thought I needed `foreman` and a `Procfile` for a while, but Jekyll does all the SASS itself. I suppose one could figure out a more complicated build pipeline if one had to, but later for that.

I used to use a standard Docker Jekyll container, but this doesn't seem to work well anymore:

```bash
JEKYLL_VERSION=4.2.2 # Or whichever version you want
docker run -p 4000:4000 --volume="$PWD:/srv/jekyll" -it jekyll/jekyll:$JEKYLL_VERSION jekyll serve -H 0.0.0.0 -w
```
