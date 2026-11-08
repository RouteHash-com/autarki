<p align="center">
  <img src="icon.svg" alt="Autarki" width="128">
</p>

# Autarki

No platform. Just the sale.

A self-custodial wallet and a shop. You keep the 24 words. Details are at [autarki.app](https://autarki.app/).

- Shop, receive, and send for XBT, BTC, and XBTC.
- Lightning for XBT and BTC starts with the wallet on AMD and Intel. Raspberry Pi and Umbrel arm64 leave Lightning off.
- The stall is public. The order is a private note.
- Classifieds stay off until Enable Classifieds.
- Pay Counter records cash, card, coupon, store credit, or coin. The card machine is the clerk's.
- Hire a listed rig. Nothing is spent until you click Mine, or until the hours are confirmed.
- A blank password stores the 24 words unencrypted on that device.
- Bugs go to [Discord #autarki](https://discord.gg/VBxvzQXvt).

## Install

Release [0.1.0](https://github.com/RouteHash-com/autarki/releases/tag/0.1.0). The StartOS package inside that tag is 0.1.0:27.

- **StartOS.** `autarki_x86_64.s9pk` for AMD or Intel. `autarki_aarch64.s9pk` for Raspberry Pi.
- **Umbrel.** Add the [RouteHash community store](https://github.com/RouteHash-com/umbrel-store), then install Autarki.
- **Ubuntu.** `autarki_ubuntu_amd64.tar`. Steps are on the [Ubuntu page](https://github.com/RouteHash-com/autarki/blob/main/ubuntu/README.md).
- **Docker images on this release.** `autarki_0.1.0_amd64.tar` and `autarki_0.1.0_arm64.tar`. Umbrel uses the community store. The arm64 image leaves Lightning off.

Server install steps are on [autarki.app/install](https://autarki.app/install).

## Android beta

Version 0.1.0 (3). The same program. The phone keeps its own wallet file. Restoring the 24 words makes a second copy. This package leaves the Lightning programs out. The page still offers Lightning and stays closed until a node is connected. A phone that already has 0.1.0 (1) has to uninstall that copy before this one will install.

- [Request access](https://appdistribution.firebase.dev/i/2ae8a6c81ce866a4). Sign in with a Google account. Firebase emails the install.
- Or download [autarki-android.apk](https://github.com/RouteHash-com/autarki/releases/download/0.1.0/autarki-android.apk) and allow the install. A 64-bit phone, Android 8 or newer.

## Check the download

Download `SHA256SUMS` into the same directory as the files, then run:

```
sha256sum -c SHA256SUMS --ignore-missing
```

A matching file prints OK.

```
d2f6ce500c06313cf1a410a4cc87152c82688b5d72d07606fcbef549ceb7297c  autarki_x86_64.s9pk
294a545aea04500fcbc6403168fbc4582ccacc404c93631471fd833055c49bb9  autarki_aarch64.s9pk
8ecd7a157f323e57a3e51cb5cf8090dede7f0a08ac344540704e884e23643615  autarki_0.1.0_amd64.tar
d8b03f5ddd8358b2c9efd07e3588a65379b2064d161ff10ebd56425f022a0a53  autarki_0.1.0_arm64.tar
5d83221e88b19bdcc85b69f7a1e6b51281ed5fb9ac57466315b496c046553ae5  autarki_ubuntu_amd64.tar
d363de41ca136611cb3dc5c5614029b815b9b1affbbbbb34cb3c0401a9a15976  autarki-android.apk
```
