Dice
===

Dice 🎲 is an extremely simple Golang-based in-memory KV store that speaks the Redis dialect.

> This is not production ready

## Story

[Arpit Bhayani](https://arpitbhayani.me) started building Dice DB to understand [Redis](https://redis.io/) better.
He compiled almost all of his learning in a course titled [Redis Internals](https://arpitbhayani.me/redis) that
actually laid the foundation of Dice DB.

## Why should you care?

Building a database from scratch has its own thrill, and you can leverage this to

- build a database from scratch
- learn database internals, starting with Redis
- learn about advanced data structures, algorithms, and event loops
- collaborate with other engineers and contribute back to Open Source

## Tenet

- remain product-first
- remain the easiest to work with

### Highlights

- [planned] Semi-persistent Storage
- [planned] Efficient concurrency using Goroutines

## Setting up

To run DiceDB locally, you will need

1. [Golang](https://go.dev/)
2. Any of the below supported platform environment:
    1. [Linux based environment](https://en.wikipedia.org/wiki/Comparison_of_Linux_distributions)
    2. [OSX (Darwin) based environment](https://en.wikipedia.org/wiki/MacOS)

```
$ git clone https://github.com/dicedb/dice
$ cd dice
$ go run main.go
```

## Dice in action

Because Dice speaks Redis' dialect, you can connect to it with any Redis Client and the simplest way it to use a [Redis CLI](https://redis.io/docs/manual/cli/). Programmatically, depending on the language you prefer, you can use your favourite Redis library to connect.

## Running Tests

To run all the unit tests fire the following command

```sh
$ go test ./...
```

### Running a single test

```sh
$ go test -timeout 30s -run <pattern> <package path>
$ go test -timeout 30s -run ^TestByteList$ ./...
```

## Running Benchmark

```sh
$ go test -test.bench <pattern>
$ go test -test.bench BenchmarkListRedis
```

## Getting Started

To get started with building and contributing to DiceDB, please refer to the [issues](https://github.com/DiceDB/dice/issues) created in this repository.

## The story

DiceDB started as a re-implementation of Redis in Golang and the idea was to - build a DB from scratch and understand the micro-nuances that comes with its implementation. The database does not aim to replace Redis, instead it will fit in and optimize itself for multi-core computations running on a single-threaded event loop.

## How to contribute

The Code Contribution Guidelines are published at [CONTRIBUTING.md](CONTRIBUTING.md); please read them before you start making any changes. This would allow us to have a consistent standard of coding practices and developer experience.

Contributors can join the [Discord Server](https://discord.gg/6r8uXWtXh7) for quick collaboration.

## Contributors

<a href = "https://github.com/dicedb/dice/graphs/contributors">
  <img src = "https://contrib.rocks/image?repo=dicedb/dice"/>
</a>

## License

DiceDB is open-sourced under [Apache License, Version 2.0](LICENSE.md).
