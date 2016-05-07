# Ruby Node on Alpine

This will build the base image needed to run any rails app that uses

+ Postgres Database
+ Ruby 2.3.0
+ Node JS from Alpine Packages

## How to Use

Very simple simply do this in your rails app

### Create Dockerfile

Create a `Dockerfile` with the following content

```
FROM codemy/ruby:latest
MAINTAINER Zack Siri <zack@codemy.net>

COPY . /usr/src/app

RUN bundle install --path vendor/bundle --without development test doc --deployment --jobs=4
RUN DB_ADAPTER=nulldb bundle exec rake assets:precompile
```

### Build the docker image

Once you've added the docker file you can build the base image of your app using