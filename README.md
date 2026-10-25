<p align="center">
  <img src="icon.svg" alt="Autarki" width="128">
</p>

# Autarki

No platform. Just the sale.

Autarki is the wallet and the shop on the server you already run. A merchant builds the order on the page. Use it as an in-person point of sale, or set the shop to Online and take the order over Nostr. The words, the shop book, and the sale stay on that server.

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

## Which file to download

StartOS has two packages in this release. `x86_64` is the 64-bit build for an AMD PC and for an Intel PC. `aarch64` is the build for a Raspberry Pi. StartOS does not use a separate file named amd64.

Umbrel has two images. A PC uses amd64. Umbrel Home and a Raspberry Pi use arm64. That Raspberry Pi image is already in this release. The RouteHash community store installs the matching one for the machine.

| Install on | Machine | File |
| --- | --- | --- |
| StartOS | AMD or Intel, 64-bit | `autarki_x86_64.s9pk` |
| StartOS | Raspberry Pi | `autarki_aarch64.s9pk` |
| Umbrel | AMD or Intel, 64-bit | `autarki_0.1.0_amd64.tar` |
| Umbrel Home or Raspberry Pi | ARM, 64-bit | `autarki_0.1.0_arm64.tar` |

Download the release:

https://github.com/RouteHash-com/autarki/releases/tag/0.1.0

| File | Bytes | SHA-256 |
| --- | ---: | --- |
| `autarki_x86_64.s9pk` | 30370587 | `321dc0c9fd3ce926bb93cb2d30f21a0968361dccd712968884e14856ffe97e7a` |
| `autarki_aarch64.s9pk` | 29018910 | `514d71444db53e7667336c658ef84d74b60b4bfd305865ceb1eef65854d28c5c` |
| `autarki_0.1.0_amd64.tar` | 109023232 | `b1404af28a5124092ba5a9495659e9ad736c25f40c138edbb68a99eedf5a83f6` |
| `autarki_0.1.0_arm64.tar` | 130007552 | `1555fb86afe0493fd90456b69078beb7eaa2366148189618c2030c71d989508a` |

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

## Install on Umbrel from the community store

This is the path that picks amd64 or arm64 for you.

1. In Umbrel, open Settings, then App stores, then Add a community app store.
2. Paste this address:

```
https://github.com/RouteHash-com/umbrel-store
```

3. Install Autarki.

That store is the RouteHash community store. It is not the official Umbrel App Store. The Autarki listing there is version 0.1.1. Umbrel uses that version to offer this update. Umbrel builds the app from the program in `routehash-autarki/bin`. On a PC it uses `autarki-amd64`. On Umbrel Home or a Raspberry Pi it uses `autarki-arm64`.

To check those programs yourself, open the `routehash-autarki` folder in the store and run:

```
sha256sum -c SHA256SUMS
```

| Program | SHA-256 |
| --- | --- |
| `bin/autarki-amd64` | `4e6620b3e1620db2941d31d7c33a09f40b960d2f2c42bee674b69dcf6dccb774` |
| `bin/autarki-arm64` | `46b92c8ad95d39fa1a40d4697e4617f1b6b1e62db56c8b264e7351ba6387ffb8` |

## Install on Umbrel from a downloaded image

Use this when you want to load the image yourself. Check the tar first.

On an AMD or Intel Umbrel:

```
docker load -i autarki_0.1.0_amd64.tar
```

On Umbrel Home or a Raspberry Pi:

```
docker load -i autarki_0.1.0_arm64.tar
docker tag autarki:0.1.0-arm64 autarki:0.1.0
```

The loaded image is named `autarki:0.1.0`. An install that tries to pull that name from the internet fails until this load has been done on that machine.

## First sale

Open Shop. Add the items. Read the tax lines and the estimated total. Write a note if the guest asked for one.

At the counter, press Check-Out. For an online order, publish the shop under Store, then Nostr, and press Check for orders when a customer has sent one.

The guide on the server is under Settings, then Read the guide.
