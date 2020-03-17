# http-server-v2: a command-line http server with auto-generated ssl

`http-server-v2` is absolutely extending `http-server`, only added one feature => auto-generated ssl

```bash
# For example 
hs2 -p 8080 -S  # will create a https server without cert-undefined error

# hs2 => http-server-v2. Prevent naming conflicts with http-server
# And everything including usage,parameters ... are the same except the installation!
```

## Why I create this?
> I am front-end developer trouble with webrtc, webrtc requires https for audio/video usage, and unsafe https connection is OK.
> But every time https-server requires me to apply -C && -K, I'm going to be sick.

## TODO
* [ ] support detached mode, run in background after quit shell/cmd (using pm2)  

## Installation:

#### Globally via `npm`

    npm install --global http-server-v2


## Usage from http-server(Usage is absolutely the same):

     hs2 [path] [options]

`[path]` defaults to `./public` if the folder exists, and `./` otherwise.

*Now you can visit http://localhost:8080 to view your server*

**Note:** Caching is on by default. Add `-c-1` as an option to disable caching.

## Available Options:

`-p` or `--port` Port to use (defaults to 8080)

`-a` Address to use (defaults to 0.0.0.0)

`-d` Show directory listings (defaults to `true`)

`-i` Display autoIndex (defaults to `true`)

`-g` or `--gzip` When enabled (defaults to `false`) it will serve `./public/some-file.js.gz` in place of `./public/some-file.js` when a gzipped version of the file exists and the request accepts gzip encoding. If brotli is also enabled, it will try to serve brotli first.

`-b` or `--brotli` When enabled (defaults to `false`) it will serve `./public/some-file.js.br` in place of `./public/some-file.js` when a brotli compressed version of the file exists and the request accepts `br` encoding. If gzip is also enabled, it will try to serve brotli first.

`-e` or `--ext` Default file extension if none supplied (defaults to `html`)

`-s` or `--silent` Suppress log messages from output

`--cors` Enable CORS via the `Access-Control-Allow-Origin` header

`-o [path]` Open browser window after starting the server. Optionally provide a URL path to open. e.g.: -o /other/dir/

`-c` Set cache time (in seconds) for cache-control max-age header, e.g. `-c10` for 10 seconds (defaults to `3600`). To disable caching, use `-c-1`.

`-U` or `--utc` Use UTC time format in log messages.

`--log-ip` Enable logging of the client's IP address (default: `false`).

`-P` or `--proxy` Proxies all requests which can't be resolved locally to the given url. e.g.: -P http://someurl.com

`--username` Username for basic authentication [none]

`--password` Password for basic authentication [none]

`-S` or `--ssl` Enable https (if you do not apply -C && -K, http-server-v2 auto generated!)

`-C` or `--cert` Path to ssl cert file (default: `cert.pem`).

`-K` or `--key` Path to ssl key file (default: `key.pem`).

`-r` or `--robots` Provide a /robots.txt (whose content defaults to `User-agent: *\nDisallow: /`)

`--no-dotfiles` Do not show dotfiles

`-h` or `--help` Print this list and exit.

`-v` or `--version` Print the version and exit.


## Author
* 知乎:[霸都丶傲天](https://www.zhihu.com/people/AJLoveChina)
* Github:[霸都丶傲天](https://github.com/ajlovechina)
