<p align="center">
  <img src="icon.svg" alt="Autarki" width="128">
</p>

# Autarki - Wallet / Nostr Shop

No platform. Just the sale.

Autarki is the wallet and the Nostr shop. It runs on an AMD or Intel server and on a Raspberry Pi. On StartOS, a Raspberry Pi uses `autarki_aarch64.s9pk`. On Umbrel, including Umbrel Home and a Raspberry Pi, install from the RouteHash community store. That listing installs on umbrelOS 1.x and on umbrelOS 2.0. This page has no umbrelOS file to download. A merchant builds the order on the page. Use it as an in-person point of sale, or set the shop to Online and take the order over Nostr. The words, the shop book, and the sale stay on that server.

Ordinary XBT and SHA-256d use Autarki's servers until you connect your own node under Settings, then Coin Nodes. XBTC uses Autarki's public node until you connect your own. The StartOS package and the Umbrel package do not include that node. A customer can pay at the counter or send the order from their own wallet.

<p align="center">
  <img src="shop.png" alt="Autarki shop page for Sunrise Coffee Shop, with one bagel on the order and the Check-Out button" width="440">
</p>

## What you get

One page: Shop, Receive, Send, Balance, Ledger, and Settings.

The first screen creates the wallet. Write the 24 words on paper before you leave that screen. A password for this copy is optional. Leave it blank and the 24 words stay in the clear, so a backup of this server is then the seed. A native SegWit phrase can be imported on that same screen. After that import you can set a password, or leave the copy unlocked.

The shop opens as a point of sale. A guest at the counter uses Pay Counter, and the clerk ticket shows the last four characters of the order. Set the shop to Online when the sale is not at the counter. Online hides Pay Counter and that ticket. Publish announces the choice. Until you publish, customers still see the counter.

Nostr is how a shop is found, and how an order reaches that shop, without a website of your own. Publish announces the shop name, the products for sale, and which nodes should receive an order. Check for orders brings a new order onto Check Outs. Paying is still a coin, cash, a card, or Lightning. The order itself does not move the money. When the clerk marks a counter sale paid, the customer's page shows that order under Ledger, then Receipts.

The three chains are ordinary XBT, SHA-256d, and XBTC. XBTC is the third chain. Ordinary XBT and SHA-256d use Autarki's servers until you connect your own node under Settings, then Coin Nodes. A silent-payment code is used only after that node is connected. Until then the page gives a normal address. XBTC uses Autarki's public node until you connect your own. Where this copy includes Autarki's XBTC node, that node is used until you connect your own. The StartOS package and the Umbrel package do not include that node. Nostr uses Autarki's public node until you add another.

Umbrel's Bitcoin app is Bitcoin Core. Autarki does not use it as the XBT node.

## Install on Umbrel

This page does not give you an umbrelOS file. umbrelOS 1.x and umbrelOS 2.0 use the same listing. It is version 0.1.4. A wallet from 0.1.3 stays.

1. In Umbrel, open Settings, then App stores, then Add a community app store.
2. Paste this address:

```
https://github.com/RouteHash-com/umbrel-store
```

3. Install **Autarki - Wallet / Nostr Shop**.

That store is the RouteHash community store. It is not the official Umbrel App Store. If the store is already added, or an install fails after you update to umbrelOS 2.0, remove this community store and add the same address again. Umbrel keeps the copy it already downloaded.

Umbrel builds the app on the machine. On a PC it uses `autarki-amd64`. On Umbrel Home or a Raspberry Pi it uses `autarki-arm64`.

To check those programs yourself, open the `routehash-autarki` folder in the store and run:

```
sha256sum -c SHA256SUMS
```

| Program | SHA-256 |
| --- | --- |
| `bin/autarki-amd64` | `aa4f193b7cc348791b4949726354f4ed83c496e31e41ae3f9fc84279d7415297` |
| `bin/autarki-arm64` | `519b11d2c9f3a5f56888d250fb1794e5f44aaf08ad868df74370b8ad3fa9fc1b` |

## Which file to download

StartOS uses a file from release 0.1.0. Umbrel does not. `x86_64` is the 64-bit build for an AMD PC and for an Intel PC. `aarch64` is the build for a Raspberry Pi. StartOS does not use a separate file named amd64.

| Install on | Machine | File |
| --- | --- | --- |
| StartOS | AMD or Intel, 64-bit | `autarki_x86_64.s9pk` |
| StartOS | Raspberry Pi | `autarki_aarch64.s9pk` |

Download the StartOS package:

https://github.com/RouteHash-com/autarki/releases/tag/0.1.0

The same release also attaches `autarki_0.1.0_amd64.tar` and `autarki_0.1.0_arm64.tar`. Those are Docker images from this build. They are not an umbrelOS 2.0 install, and the community store does not use them. Sizes and checksums for every file on the release:

| File | Bytes | SHA-256 |
| --- | ---: | --- |
| `autarki_x86_64.s9pk` | 30403722 | `3ade87baf4d866ba594318abffcb62f60a99ed812838d46e0ede46f8c1c4d10c` |
| `autarki_aarch64.s9pk` | 29035661 | `1d0e75a466474f6faf844be556a4abb049567fde2725d27ad86dce98d7826c03` |
| `autarki_0.1.0_amd64.tar` | 109133824 | `b575762dcf20ae05f5f87d0079f5c9b1fffb2fd0cbde0ec47c99b6c6e2f36acb` |
| `autarki_0.1.0_arm64.tar` | 130140672 | `6a71894c1c1d76b87e5fc0c69f308550a610a928ba18ca6afa1244633ae934f6` |

The package version inside each StartOS file is 0.1.0:2. Sideloading it replaces 0.1.0:1, and the wallet stays.

## Check the download

Put `SHA256SUMS` from the release in the same folder as the file you downloaded. Then run:

```
sha256sum -c SHA256SUMS --ignore-missing
```

The line for your file ends in `OK` when the download matches. A partial download does not.

## Install on StartOS

1. Download the package that matches the server. An AMD or Intel server uses `autarki_x86_64.s9pk`. A Raspberry Pi uses `autarki_aarch64.s9pk`. Check it with the command above.
2. In StartOS, sideload that file and install Autarki. Install does not ask for Bitcoin Knots or Bitcoin Core.
3. Open Autarki.
4. Create the wallet. Write the 24 words on paper before you leave the screen.

The shop opens first, until the wallet exists. After that, the page opens on Receive.

## First sale

Open Shop. Add the items. Read the tax lines and the estimated total. Write a note if the guest asked for one.

At the counter, press Check-Out. For an online order, publish the shop under Store, then Nostr, and press Check for orders when a customer has sent one.

The guide on the server is under Settings, then Read the guide.
