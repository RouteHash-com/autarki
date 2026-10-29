# Autarki on Ubuntu

An Ubuntu server with Docker, and without StartOS or Umbrel, runs this image. It is the same wallet as the StartOS package for an AMD or Intel server. A Raspberry Pi does not use this file.

The first screen creates the wallet. Write the 24 words on paper before you leave that screen. A blank password stores those words in the clear, and a copy of the data directory is then the seed.

Ordinary XBT and SHA-256d use Autarki's servers until you connect your own node under Settings, then Coin Nodes. XBTC uses Autarki's public node until you connect your own. This image does not include that node.

The page listens on port 4173.

## Download

Make a folder. Save these two files into it.

The image:

https://github.com/RouteHash-com/autarki/releases/download/0.1.0/autarki_ubuntu_amd64.tar

The compose file is `docker-compose.yml` in this folder:

https://github.com/RouteHash-com/autarki/raw/main/ubuntu/docker-compose.yml

`SHA256SUMS` on the release lists the image. Download that file into the same folder:

https://github.com/RouteHash-com/autarki/releases/download/0.1.0/SHA256SUMS

Then run:

```
sha256sum -c SHA256SUMS --ignore-missing
```

The line for `autarki_ubuntu_amd64.tar` ends in `OK` when the download matches.

| File | Bytes | SHA-256 |
| --- | ---: | --- |
| `autarki_ubuntu_amd64.tar` | 111319040 | `3b145a0e39f4704cc001267dac35d117a0ecc87f76b52af7b97309dfe9077e4b` |

## Start

From that folder:

```
docker load -i autarki_ubuntu_amd64.tar
docker compose up -d
```

Open `http://this-server:4173`.

The `data` directory beside the compose file is the wallet. Back that directory up. Do not send it to anyone.

To stop the page and keep the wallet:

```
docker compose down
```

That leaves `data` in place. Removing the `data` directory removes the wallet.
