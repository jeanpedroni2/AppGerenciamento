# .devcontainer/Dockerfile

FROM ruby:3.2

RUN apt-get update -qq && \
    apt-get install -y nodejs yarn postgresql-client

RUN gem install rails

WORKDIR /workspace

COPY Gemfile Gemfile.lock ./

RUN gem install bundler && \
    bundle install || true

EXPOSE 3000
