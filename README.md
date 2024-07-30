# Project Name
go-memcached

## Description

This project is a [Go](https://golang.org/) implementation of a memcached server.

The purpose of this project is to implement a simple go application that uses memcached, all within a dev container environment.

## Features

- Reliable deployment running in VSCode Dev Containers
- Support for GitHub Codespaces (TODO: browser connectivity)
- High performance caching
- Simple and easy to use API

## Installation

To install and run this project locally, follow these steps:

1. Copy the URL to the repo, but do not clone it: `https://github.com/your-username/go-memcached.git`
2. Ensure Docker is installed and running on your machine
3. Enable [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) extension in VSCode 
4. From the Command Palatte (CTRL/Command+Shift+P), type and select `Dev Containers: Clone Repository in Container Volume...`
5. Choose Remote Source GitHub, and supply/choose the `go-memcached` repo
6. Once all containers are built and running, use `go run .` to start the app

## Usage

Once the server is running, you can interact with it using a memcached client library or the [telnet](https://en.wikipedia.org/wiki/Telnet) command.

Here's an example of how to set a key-value pair using telnet:

```
$ telnet localhost 11211
set mykey 0 3600 5
value
STORED
```

To retrieve the value:

```
$ telnet localhost 11211
get mykey
VALUE mykey 0 5
value
END
```

For more information on the available commands, refer to the [memcached protocol documentation](https://github.com/memcached/memcached/blob/master/doc/protocol.txt).

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
