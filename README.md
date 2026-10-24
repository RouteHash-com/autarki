<p align="center">
  <img src="icon.svg" alt="Autarki" width="128">
</p>

# Autarki

No platform. Just the sale.

Autarki is the wallet and the shop on the server you already run. A merchant builds the order on the page. The guest pays at check-out. The words, the shop book, and the sale stay on that server.

Bitcoin Knots operators can keep the node they trust and put the register beside it. On StartOS, Autarki reads XBT from the Bitcoin Knots service on that server. The same page also takes a normal SHA-256d payment and, when you connect the node, XBTC.

<p align="center">
  <img src="shop.png" alt="Autarki shop page for Sunrise Coffee Shop, with one bagel on the order and the Check-Out button" width="440">
</p>

## What you get

One page: Shop, Receive, Send, Balance, Ledger, and Settings.

The first screen creates the wallet. Write the 24 words on paper before you leave that screen. A password for this copy is optional. Leave it blank and the 24 words stay in the clear, so a backup of this server is then the seed. A native SegWit phrase can be imported on that same screen. After that import you can set a password, or leave the copy unlocked.

XBT comes from Bitcoin Knots when that service is on the server. A normal SHA-256d address can be paid through Autarki's server until you connect your own node under Settings, then Coin Nodes. A silent-payment code is used only after that node is connected. XBTC has no public server in these packages. Connect that node under Settings, then Coin Nodes, when you use it.

Umbrel's Bitcoin app is Bitcoin Core. Autarki does not use it as the XBT node.

## Which file to download

StartOS has one package in this release. Its name is `x86_64`. That is the 64-bit build for an AMD PC and for an Intel PC. StartOS does not use a separate file named amd64.

Umbrel has two images. A PC uses amd64. Umbrel Home and a Raspberry Pi use arm64. The RouteHash community store installs the matching one for the machine.

| Install on | Machine | File |
| --- | --- | --- |
| StartOS | AMD or Intel, 64-bit | `autarki_x86_64.s9pk` |
| Umbrel | AMD or Intel, 64-bit | `autarki_0.1.0_amd64.tar` |
| Umbrel Home or Raspberry Pi | ARM, 64-bit | `autarki_0.1.0_arm64.tar` |

Download the release:

https://github.com/RouteHash-com/autarki/releases/tag/0.1.0

| File | Bytes | SHA-256 |
| --- | ---: | --- |
| `autarki_x86_64.s9pk` | 30408775 | `46fba7ea4e4b9098dd4d23c76d8b50a733cbba11b44b8e1e289c059bab355429` |
| `autarki_0.1.0_amd64.tar` | 108975104 | `fbd1ae4dbb36ebbd5ad73b6a4b387306b8f89c72f7b65fef170da2208d9db08b` |
| `autarki_0.1.0_arm64.tar` | 129971712 | `3c9ddbedcdc4e2c4ec616ed0b1fd808f4055284223512764b3ca370aa6e389ac` |

## Check the download

Put `SHA256SUMS` from the release in the same folder as the file you downloaded. Then run:

```
sha256sum -c SHA256SUMS --ignore-missing
```

The line for your file ends in `OK` when the download matches. A partial download does not.

## Install on StartOS

Use this on a 64-bit AMD or Intel computer running StartOS.

1. Download `autarki_x86_64.s9pk` and check it with the command above.
2. In StartOS, sideload that file and install Autarki.
3. Install Bitcoin Knots on the same server when you want Autarki to read XBT from Knots. If the Knots companion is installed, Autarki uses that service.
4. Open Autarki.
5. Create the wallet. Write the 24 words on paper before you leave the screen.

The shop opens first, until the wallet exists. After that, the page opens on Receive.

## Install on Umbrel from the community store

This is the path that picks amd64 or arm64 for you.

1. In Umbrel, open Settings, then App stores, then Add a community app store.
2. Paste this address:

```
https://github.com/RouteHash-com/umbrel-store
```

3. Install Autarki.

That store is the RouteHash community store. It is not the official Umbrel App Store. Umbrel builds the app from the program in `autarki/bin`. On a PC it uses `autarki-amd64`. On Umbrel Home or a Raspberry Pi it uses `autarki-arm64`.

To check those programs yourself, open the `autarki` folder in the store and run:

```
sha256sum -c SHA256SUMS
```

| Program | SHA-256 |
| --- | --- |
| `bin/autarki-amd64` | `494b1d7b75739f231fbda82960c05ea9f6b596e5aed3d99b6f68fa1571034444` |
| `bin/autarki-arm64` | `549e0f13e90d4e7b16c88654d663687fe145aa27dbdfd9a67b1f2dd79b1760f6` |

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

Open Shop. Add the items. Read the tax lines and the estimated total. Write a note if the guest asked for one. Press Check-Out. The guide on the server is under Settings, then Read the guide.
