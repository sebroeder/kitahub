# kitahub
The kitahub app.

# Prerequisites
On macOS use [Homebrew](http://brew.sh) to install the latest Ruby and PostgreSQL

``` shell
brew update
brew install ruby postgresql
brew link --overwrite ruby
```

Install [Docker for Mac](https://docs.docker.com/docker-for-mac/) to launch the database via docker-compose.

It is recommended to use editorconfig support in your text editor. Plugins can be found here: http://editorconfig.org/#download

# Usage
Get the source code

``` shell
git clone https://github.com/jehrhardt/kitahub.git
cd kitahub
```

Install the dependencies

``` shell
bundle install
```

Launch the database in the background

``` shell
docker-compose up -d db
```

Create and migrate the database

``` shell
rake db:setup
rake db:migrate
```

Run the app

``` shell
rails server
```

Open the app in your browser [localhost:3000](http://localhost:3000).

# Development
Run the tests

``` shell
rake db:test:prepare
rails spec
```
