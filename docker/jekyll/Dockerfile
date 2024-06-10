FROM ruby:3.3.1

WORKDIR /app

COPY \
  Gemfile \
  Gemfile.lock \
  /app/
RUN bundle config set path '/bundle' &&
  bundle install --jobs=4 --path=/bundle
