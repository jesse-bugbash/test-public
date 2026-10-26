FROM ruby:3.3-slim

RUN apt-get update -qq \
 && apt-get install -y --no-install-recommends build-essential libpq-dev \
 && rm -rf /var/lib/apt/lists/*

WORKDIR /app
COPY Gemfile Gemfile.lock ./
RUN bundle config set --local without 'development test' \
 && bundle install --jobs 4

COPY . .
ENV RAILS_ENV=production
CMD ["bundle", "exec", "sidekiq", "-C", "config/sidekiq.yml"]
