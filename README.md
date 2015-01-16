## Tup (Optional)

`build.sh` builds its own copy of Tup if it can't find it. If you want to be more efficient, install Tup using your distro's package manager, or build it yourself and add the `tup` binary to your `PATH`.

## Get Source

    git clone https://github.com/cablelabs/rui-http-server.git --recursive
    cd rui-http-server

If you previously downloaded without `--recursive`, you can checkout the submodule with:

    git submodule init
    git submodule update

## Build

    ./build.sh

This will also install or build dependencies as needed.

### Auto-rebuilding (Optional)

While developing, it can be useful to leave `tup` running in the background, autocompiling every time anything changes:

    tup monitor -a
    # stop with 'tup stop'

## Run

To start the HTTP server on port 8080, do:

    ./src/server -p 8080

If you want a random point, you can do:

    ./src/server

And, the server output will say something like:

> Starting HTTP server on http://localhost:37229

Visit that page in your browser to see the discovered remote UIs.
