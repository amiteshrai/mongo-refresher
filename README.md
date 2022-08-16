# Mongo Refresher

A refresher on the fundamental concepts of the MongoDB database using Python programming.

## Python Environment Setup

## Installing MongoDB

### Using Docker

For installation of MongoDB, I am using the official Docker [image](https://hub.docker.com/_/mongo).

#### Attach a volume for persistent storage

    mkdir -p data

#### Start a container with network mapping

    docker container run -d --name mongodb --net="host" -v /Users/fintech/Workspaces/Personal/Code/mongo-refresher/data/db:/data/db mongo

#### Check if the container is running

    docker container ls

#### Run commands in the container

    docker exec -t mongodb bash

### Using Homebrew

#### Installing MongoDB and MongoDB Compass

    xcode-select --install
    brew tap mongodb/brew
    brew install mongodb-community@5.0
    brew install --cask mongodb-compass

#### Add PATH

    echo 'export PATH="/opt/homebrew/opt/mongodb-community@5.0/bin:$PATH"' >> ~/.zshrc

#### Start MongoDB

    mongod --dbpath=/Users/fintech/Workspaces/Personal/Code/mongo-refresher/data/db
