# HyperText Transfer Protocol (HTTP)

Discuss the basics of HTTP.

## Introduction

According to Wikipedia:

> Hypertext is structured text that uses logical links (hyperlinks) between nodes containing text. HTTP is the protocol to exchange or transfer hypertext.

> The Hypertext Transfer Protocol (HTTP) is an application protocol for distributed, collaborative, hypermedia information systems. HTTP is the foundation of data communication for the World Wide Web.

## Client-server

Wikipedia:

> The client–server model of computing is a distributed application structure that partitions tasks or workloads between the providers of a resource or service, called servers, and service requesters, called clients.

For our purposes, the client is the user's browser, and the server is an application somewhere on the Internet that serves a website to many clients.

## Create the first HTTP Server

1. Install Node.js environment
    - Mac
        - Install Homebrew, `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
        - Install Node.js, `brew install node`
    - Windows
        - Download the installation package from Node.js website
    - Linux (Ubuntu)
        - Install using apt-get, `sudo apt-get install node`
2. Install the server using `npm install http-server -g`
3. You are now able to run `http-server` to turn any folder into a root of a static website.

## Successful Completion

You are able to install node.js based http-server, run it, and visit `http://localhost:8080/` to show your own site.

## Reference Links

- [HTTP](http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)
- [Web Server](http://en.wikipedia.org/wiki/Web_server)
- [Homebrew for Mac](http://brew.sh/)
- [Node.js](http://nodejs.org/)
- [Why the hell would I use Node.js?](http://www.toptal.com/nodejs/why-the-hell-would-i-use-node-js)
- [NPM](https://www.npmjs.org/)
- [http-server](https://www.npmjs.org/package/http-server)
- [180 websites in 180 days](http://jenniferdewalt.com/)