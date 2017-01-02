# rural - User-friendly command-line HTTP tool in Rust

## Installation

Assuming you have a reasonably recent version of Rust/Cargo installed, simply run `cargo install rural`.

## Usage

Rural currently supports making GET and POST requests. To make a request, invoke rural with the request method (in lowercase) and the URL:

```sh
rural get http://example.com
rural post http://example.com
```

Rural supports HTTPS requests if OpenSSL is installed:

```sh
rural get https://example.com
```

To see the response headers returned, use the `--headers` flag (`-d` for short):

```sh
rural --headers get http://example.com
rural -d get http://example.com
```

Rural supports supplying GET parameters in the querystring or by using the syntax `key=value`:

```sh
rural get 'http://example.com?bass=john&drums=keith'
rural get http://example.com bass=john drums=keith
```

To supply form parameters, use the syntax `key==value`:

```sh
rural post http://example.com bass==john drums==keith
```
