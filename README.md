# rofi-prowlet

<a href="./LICENSE.md"><img src="https://img.shields.io/badge/license-MIT-blue.svg"></a>
<a href="https://aur.archlinux.org/packages/rofi-cuff-git/"><img src="https://img.shields.io/aur/version/rofi-prowlet-git"></a>

[`rofi`](https://github.com/davatorium/rofi) wrapper for [`prowlet`](https://github.com/loiccoyle/prowlet). Use the [`Prowlarr`](https://github.com/prowlarr/prowlarr) search API to find torrents.

![rofi-prowlet](https://i.imgur.com/Fb2wh45.png)

[See it in action](https://imgur.com/7roVMqQ)

# Installation

### Dependencies

- [`rofi`](https://github.com/davatorium/rofi)
- [`prowlet`](https://github.com/loiccoyle/prowlet)
- [`jq`](https://github.com/stedolan/jq)

Optional:

- [webtorrent](https://github.com/webtorrent/webtorrent): for torrent streaming.

Of course you'll also need access to a `Prowlarr` server.

### Manual

You'll need to git clone this repository and place the script somewhere in your `$PATH`.

```
git clone https://github.com/loiccoyle/rofi-prowlet
cd rofi-prowlet
cp rofi-prowlet /somewhere/in/your/PATH/
```

### Arch linux

Using your prefered AUR helper:

```
paru -S rofi-prowlet-git
```

# Usage

`rofi-prowlet` is just wrapping [`prowlet`](https://github.com/loiccoyle/prowlet), any options will be passed on to `prowlet`.

```
$ rofi-prowlet -h
Use "-" to read the json Prowlarr response from stdin e.g.:

$ cuff search big buck bunny | rofi-cuff -

Otherwise, rofi-cuff passes any provided options to the main cuff command:

Query the Prowlarr search API from the command line.

Usage:
    cuff [OPTIONS] {search, config, indexers, categories, open}
        -h                        Show this message and exit.
        -r                        Raw output, no coloring.
        -v                        Verbosisty, up to -vv.
        -s                        Start Prowlarr service if not running.
        -k                        Stop Prowlarr service before exiting.
        -u JACKETT_URL            Prowlarr URL.
        -a API_KEY                Prowlarr API key, will query Prowlarr if not provided.
        -p PASSWORD               Prowlarr password.
```

# Contributing

Please feel free to open a PR, especially to add common torrent related actions.
