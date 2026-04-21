
# Penggao Yan Academic Website

[![pages-build-deployment](https://github.com/JasonYanxx/JasonYanxx.github.io/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/JasonYanxx/JasonYanxx.github.io/actions/workflows/pages/pages-build-deployment)

This repository powers <https://jasonyanxx.github.io/>. It is based on the Academic Pages Jekyll template and is deployed with GitHub Pages.

## Common Content Files

- Homepage/profile: `_pages/about.md`
- Web CV: `_pages/cv.md`
- Navigation: `_data/navigation.yml`
- Site-wide metadata and SEO defaults: `_config.yml`
- Static files such as PDFs: `files/`

## Running Locally

Local preview is useful before pushing changes to GitHub Pages.

### First-time setup

From the project root, install the Ruby gems into the ignored `local/` folder:

```bash
bundle config set path local/bundle
bundle install
```

This keeps generated dependency files out of the repository. The repo also ignores `.bundle/`, `Gemfile.lock`, `_site/`, and `local/`.

### Start the Jekyll server

```bash
bundle exec jekyll serve --host 127.0.0.1 --port 4000 --livereload
```

Open <http://127.0.0.1:4000/> in the browser.

Press **Ctrl+C** in that terminal to stop the server.

### Static preview fallback

If the Jekyll development server has trouble staying up, build the site and serve the generated `_site/` folder:

```bash
bundle exec jekyll build
python3 -m http.server 4000 --bind 127.0.0.1 --directory _site
```

Then open <http://127.0.0.1:4000/>.

## Troubleshooting

### `bundler: command not found: jekyll`

Run the first-time setup again:

```bash
bundle config set path local/bundle
bundle install
```

### `Faraday::Connection ... without adapter`

This can happen when `jekyll-github-metadata` resolves to Faraday 2 locally. Keep this line in `Gemfile`:

```ruby
gem "faraday", "~> 1.10"
```

Then run:

```bash
bundle install
bundle exec jekyll build
```

### RubyGems warning on macOS system Ruby

macOS may print warnings about RubyGems being old when using the built-in Ruby. If `bundle exec jekyll build` succeeds, those warnings are not blocking local preview.

### Optional newer Ruby on macOS

If you prefer a Homebrew Ruby instead of the macOS system Ruby:

```bash
brew install ruby@3.1
export PATH="/opt/homebrew/opt/ruby@3.1/bin:$PATH"
bundle install
bundle exec jekyll serve --host 127.0.0.1 --port 4000 --livereload
```

## Deployment

Push changes to the GitHub repository. GitHub Pages will build and deploy the site automatically through the Pages workflow.

## Maintenance

Bug reports and feature requests to the template  should be [submitted via GitHub](https://github.com/academicpages/academicpages.github.io/issues/new/choose). For questions concerning how to style the template, please feel free to start a [new discussion on GitHub](https://github.com/academicpages/academicpages.github.io/discussions).

This repository was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License (see LICENSE.md). It is currently being maintained by [Robert Zupko](https://github.com/rjzupkoii) and additional maintainers would be welcomed.

## Bugfixes and enhancements

If you have bugfixes and enhancements that you would like to submit as a pull request, you will need to [fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) this repository as opposed to using it as a template. This will also allow you to [synchronize your copy](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork) of template to your fork as well.

Unfortunately, one logistical issue with a template theme like Academic Pages that makes it a little tricky to get bug fixes and updates to the core theme. If you use this template and customize it, you will probably get merge conflicts if you attempt to synchronize. If you want to save your various .yml configuration files and markdown files, you can delete the repository and fork it again. Or you can manually patch.
