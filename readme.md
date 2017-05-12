# Mushtaq Welfare Trust

Source code for [Mushtaq Welfare Trust website](http://mwt.org.uk/).

## Getting started
The site is built using [Jekyll](http://jekyllrb.com/).

### macOS Prerequisites Native:
* Install Ruby from https://www.ruby-lang.org/en/downloads/
* Install Bundler gem from http://bundler.io/
* Install Node.js from https://nodejs.org/en/download/

Steps to setup development machine.
* `git clone git@github.com:mushtaq-welfare-trust/mushtaq-welfare-trust.github.io.git`
* `cd mushtaq-welfare-trust.github.io`
* `bundle install`
* `npm i bower -g`
* `bower install`

### macOS Prerequisites via Docker:
* Install [Docker for Mac](https://docs.docker.com/docker-for-mac/). You can use the Beta/Stable channel.
* Follow the [Getting Started with Docker for Windows](https://docs.docker.com/docker-for-windows/) from Step 1 to Step 4 to check your setup.

### Windows Prerequisites:
For development on Windows should be done inside a Docker container as setting up requirements is a very painful process on Windwos OS.

* Install [Docker for Windows](https://docs.docker.com/docker-for-windows/). You can use the Beta/Stable channel.
* Follow the [Getting Started with Docker for Windows](https://docs.docker.com/docker-for-windows/) from Step 1 to Step 4 to check your setup.

## Development
Run the project locally:
```
rm -rf _site; jekyll serve --trace
```

```
rm -rf _site; bundle exe jekyll serve --trace
```

Using Docker:
```
rm -rf _site; docker run --rm --label=jekyll --volume=$(pwd):/srv/jekyll -it -p 127.0.0.1:4000:4000 jekyll/jekyll npm i bower -g; bower install; bundle exe jekyll serve --trace
```

## Production build
Before you upload the site you'll need to be build the site in production mode.

Locally:
```
rm -rf _site; JEKYLL_ENV=production jekyll build
```

Using Docker:
```
rm -rf _site; docker run --rm --label=jekyll --volume=$(pwd):/srv/jekyll -it -p 127.0.0.1:4000:4000 --env JEKYLL_ENV=production jekyll/jekyll npm i bower -g; bower install; bundle exe jekyll build --trace
```

Once the command finish upload the content of `_site` directory to root of your web server.

## Fonts and Icons:
* [Font Awesome](https://fortawesome.github.io/Font-Awesome) - used for icons
* [Signika](https://www.google.com/fonts/specimen/Signika) - used for headings including company name
* [Open Sans](https://www.google.com/fonts/specimen/Open+Sans) - used for body text
