# eWaterCycle Project Website

The eWaterCycle project envisions a collaborative environment containing
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
1. Run with docker (recommended) or install Ruby and run locally, as follows:

## Install and run with Docker

1. Ensure Docker is installed. You can confirm this with
    ```
    which docker
    ```
1. Run
    ```
    docker run --rm -it \
    --volume="$PWD:/srv/jekyll" \
    --volume="$PWD/vendor/bundle:/usr/local/bundle" \
    -p 127.0.0.1:4000:4000 \
    jekyll/jekyll:3.8 \
    jekyll serve
    ```
1. The page can now be viewed on [localhost:4000](http://localhost:4000/).

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
    bundle config set --local path 'vendor/bundle'  # this avoids the need for sudo
    bundle install
    ```
1. Run the website locally
    ```
    bundle exec jekyll serve
    ```
1. The page can now be viewed on [localhost:4000](http://localhost:4000/).
