# RAIN Seminar Website

Website for the RAIN seminar series. Originally forked from [jekyll-now](https://github.com/barryclark/jekyll-now) and Stanford SysML Seminar.

Feel free to clone this template, but please include a shoutout to the MLSys
Seminars website (uncomment the part at the bottom of `index.md`)!

## Validate changes locally

The public site is built by GitHub Pages from the repository's `main` branch.
Before opening a pull request, use Ruby 3.3 and Bundler to run the same supported
Jekyll stack locally:

```sh
bundle config set --local path vendor/bundle
bundle install
JEKYLL_GITHUB_TOKEN="$(gh auth token)" bundle exec jekyll build --strict_front_matter
```

The build uses the token only to let `jekyll-github-metadata` read repository
details without anonymous API limits. The generated site is written to `_site/`,
which is ignored by Git.
