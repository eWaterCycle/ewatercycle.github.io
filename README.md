# eWaterCycle II Project Website

The eWaterCycle II project envisions a collaborative environment containing
many local and global hydrological models, allowing hydrologists to run
experiments on high performance computing infrastructure, with multiple
models, without having to be an expert in computer science. This will all
contribute to further advance our knowledge of the global hydrological
cycle.

# Install and run the website locally (for development)

1. Clone the repository, move to its directory
    ```
    git clone git@github.com:eWaterCycle/ewatercycle.github.io.git
    cd ewatercycle.github.io
    ```
1. Run with docker (recommended) or install Ruby and run locally

## Install and run with Docker

1. Ensure Docker is running.

1. Run from the command line:
```
docker run --rm -it \
  --volume="$PWD:/srv/jekyll" \
  --volume="$PWD/vendor/bundle:/usr/local/bundle" \
  -p 4000:4000 jekyll/jekyll:3.8 \
  jekyll serve
```

## Install and run locally

_NB: The following instructions are for Linux.
On Mac, Ruby version 2.6 may be necessary. You can install a specific version
with [rbenv](https://github.com/rbenv/rbenv)._

1. Install ruby.
    ```
    apt-get install ruby-full
    ```
1. Install the required gems
    ```
    gem install bundler
    bundle install
    ```
1. Run the website locally
    ```
    bundle exec jekyll serve
    ```
