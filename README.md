# rofi-prowlet

<a href="./LICENSE.md"><img src="https://img.shields.io/badge/license-MIT-blue.svg"></a>
<a href="https://aur.archlinux.org/packages/rofi-prowlet-git/"><img src="https://img.shields.io/aur/version/rofi-prowlet-git"></a>

[`rofi`](https://github.com/davatorium/rofi) wrapper for [`prowlet`](https://github.com/loiccoyle/prowlet), a cli utility to query `Prowlarr`.

> Use the [`Prowlarr`](https://github.com/prowlarr/prowlarr) search API to find torrents.

![rofi-prowlet](https://i.imgur.com/RudooO4.png)

## 📦 Installation

### Dependencies

- [`rofi`](https://github.com/davatorium/rofi)
- [`prowlet`](https://github.com/loiccoyle/prowlet)
- [`jq`](https://github.com/stedolan/jq)

Optional:

- [webtorrent](https://github.com/webtorrent/webtorrent): for torrent streaming.

You'll need to have `Prowlarr` running locally or have access to a `Prowlarr` server.

### Manual

You'll need to git clone this repository and place the script somewhere in your `$PATH`.

```console
git clone https://github.com/loiccoyle/rofi-prowlet
cd rofi-prowlet
cp rofi-prowlet /somewhere/in/your/PATH/
```

### Arch linux

Using your prefered AUR helper:

```console
paru -S rofi-prowlet-git
```

## 📋 Usage

`rofi-prowlet` is just wrapping [`prowlet`](https://github.com/loiccoyle/prowlet), any options will be passed on to `prowlet`.

```console
$ rofi-prowlet -h
Use "-" to read the json Prowlarr response from stdin e.g.:

$ prowlet search big buck bunny | rofi-prowlet -

Otherwise, rofi-prowlet passes any provided options to the prowlet command:

Query the Prowlarr search API from the command line.

Usage:
    prowlet [OPTIONS] {search, config, indexers, categories, open}
        -h                        Show this message and exit.
        -r                        Raw output, no coloring.
        -v                        Verbosisty, up to -vv.
        -s                        Start prowlarr.service if not running.
        -k                        Stop prowlarr.service before exiting.
        -u PROWLARR_URL           Prowlarr URL.
        -a API_KEY                Prowlarr API key, will query prowlarr if not provided.
```

## 🥳 Contributing

Please feel free to open a PR, especially to add common torrent related actions.
