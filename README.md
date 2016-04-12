# Notibot, a simple Discord bot

[![Build Status](https://travis-ci.org/dhedegaard/notibot.svg?branch=master)](https://travis-ci.org/dhedegaard/notibot)
[![Docker Pulls](https://img.shields.io/docker/pulls/dhedegaard/notibot.svg)](https://hub.docker.com/r/dhedegaard/notibot/)

It sends messages to a text channel whenever someone is leaving/joining the
server or creating/changing/deleting channels.

## Running standalone ##

Install dependency

`$ go get -v .`

Run the program

`$ go run notibot.go [email] [password]`

Or for a BOT-user

`$ go run notibot.go [app bot user token]`

## Running through Docker ##

Pull the image from the [Docker Hub](https://hub.docker.com/r/dhedegaard/notibot/):

`$ docker pull dhedegaard/notibot`

Run the image

`$ docker run -d --name notibot dhedegaard/notibot app [email] [password]`

Or for a BOT-user

`$ docker run -d --name notibot dhedegaard/notibot app [app bot user token]`

You might also want to add `--restart always` as parameter for the container
to automatically restart it if/when the process crashes.