# Autarki on Ubuntu

An Ubuntu server with Docker, and without StartOS or Umbrel, runs this image. It is the same wallet as the StartOS package for an AMD or Intel server. A Raspberry Pi does not use this file.

The first screen creates the wallet. Write the 24 words on paper before you leave that screen. Leave both password fields blank and the 24 words are stored unencrypted on this device. A backup of this service is then the seed. Restore the 24 words is on that screen. Settings, then Nostr Node, can save a copy of the shop book. That file does not hold the 24 words.

Ordinary XBT and SHA-256d use Autarki's servers until you connect your own node under Settings, then Coin Nodes. XBTC uses Autarki's public node until you connect your own. This image does not include that node.

The page is on this computer only, at port 4173.

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
| `autarki_ubuntu_amd64.tar` | 111381504 | `8f46dfc55179effbb5b7f72df1198be07eb726dd1ddf1239d5cc3a9c5aed4bc3` |

## Start

From that folder:

```
docker load -i autarki_ubuntu_amd64.tar
docker compose up -d
```

Open `http://127.0.0.1:4173` on this computer. Compose uses the image id from this release and does not pull another image. The first start prepares `data` for the wallet. An existing `data` directory is kept.

From another computer, open a tunnel, then open `http://127.0.0.1:4173` there:

```
ssh -L 4173:127.0.0.1:4173 user@this-server
```

The `data` directory beside the compose file is the wallet. Back that directory up. Do not send it to anyone.

To stop the page and keep the wallet:

```
docker compose down
```

That leaves `data` in place. Removing the `data` directory removes the wallet.
