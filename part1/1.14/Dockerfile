FROM ruby:2.6.0

WORKDIR /mydir
RUN apt-get update && apt-get install -y git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get update && apt-get install -y nodejs
RUN git clone https://github.com/docker-hy/rails-example-project

EXPOSE 3000
WORKDIR /mydir/rails-example-project

RUN gem install bundler
RUN bundle install
RUN rails db:migrate
CMD rails s