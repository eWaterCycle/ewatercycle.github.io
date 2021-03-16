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
1. Install ruby.
    On Linux:
    ```
    sudo apt-get install ruby-full
    ```
    NB: on Mac, version 2.6 may be necessary. You can install a specific version
    with [rbenv](https://github.com/rbenv/rbenv).
    ```
1. Install the required gems
    ```
    sudo gem install bundler
    sudo bundle install
    ```
1. Run the website locally
    ```
    bundle exec jekyll serve
    ```