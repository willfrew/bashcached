# bashcached

> memcached built on [bash] + [ncat]

[bash]: https://www.gnu.org/software/bash/
[ncat]: https://nmap.org/ncat/


## Feature

It is one file script (small, <100 lines!), and it requires only:

  - `bash`
  - `ncat`
  - `lsof`

So, you can use it as soon as you download it.

And, it have been implemented almost all memcached commands:

  - `set`, `add`, `replace`, `append` and `prepend`
  - `get`, `delete` and `touch`
  - `incr` and `decr`
  - `gets` and `cas`
  - `flush_all`
  - `version` and `quit`

## Install

You could install via `brew` if you use macOS:

```console
$ brew install nmap
```

Or, you could install via `apt` if you use Ubuntu:

```console
$ sudo apt install nmap lsof
```

then, download and chmod.

```console
$ curl -LO https://raw.githubusercontent.com/MakeNowJust/bashcached/master/bashcached
$ chmod +x bashcached
```

## Usage

```console
$ ./bashcached --help
bashcached - memcached built on bash + ncat

USAGE: bashcached [--port=PORT] [--maxconn=MAXCONN] [--timeout=TIMEOUT] [--check=CHECK]
$ ./bashcached &
$ telnet localhost 25252
set hello 0 0 11
hello world
STORED
get hello
VALUE hello 0 11
hello world
END
quit
```


## License and Copyright

MIT and [:sushi:](https://github.com/MakeNowJust/sushi-ware)
© TSUYUSATO "[MakeNowJust](https://quine.codes)" Kitsune <<make.just.on@gmail.com>> 2016
