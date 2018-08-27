FROM ruby:2.5.1-alpine


# Minimal requirements to run a Rails app
RUN apk add --no-cache --update build-base \
                                linux-headers \
                                git \
                                postgresql-dev \
                                nodejs \
                                tzdata

ENV APP_PATH /usr/src/app

# Different layer for gems installation
WORKDIR $APP_PATH
RUN gem install rails -v 5.2.1
# Copy the application into the container

EXPOSE 3000
CMD sh
