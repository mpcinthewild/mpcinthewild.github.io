Jekyll-enabled site (minimal)

This folder contains a minimal Jekyll setup so you can write Markdown pages (`.md`) and have them rendered by Jekyll (useful for GitHub Pages).

Local preview (Docker, no Ruby install required):

```bash
cd /path/to/mpc-in-the-wild
docker run --rm -it -v "$PWD:/srv/jekyll" -p 4000:4000 jekyll/jekyll \
	jekyll serve --watch --force_polling --baseurl "" --host 0.0.0.0
# open http://localhost:4000
```

Or install Jekyll locally and run:

```bash
gem install bundler jekyll
# bundle install (if you add a Gemfile)
jekyll serve --livereload --baseurl ""
```

Place Markdown files at the repository root (or `docs/` if you prefer) and include YAML front matter (e.g., `layout: default`) so Jekyll processes them.
# mpc-in-the-wild