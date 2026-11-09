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

Release [0.1.0](https://github.com/RouteHash-com/autarki/releases/tag/0.1.0). The StartOS package inside that tag is 0.1.0:29. The Umbrel listing is 0.1.18.

- **StartOS.** `autarki_x86_64.s9pk` for AMD or Intel. `autarki_aarch64.s9pk` for Raspberry Pi.
- **Umbrel.** Add the [RouteHash community store](https://github.com/RouteHash-com/umbrel-store), then install Autarki.
- **Ubuntu.** `autarki_ubuntu_amd64.tar`. Steps are on the [Ubuntu page](https://github.com/RouteHash-com/autarki/blob/main/ubuntu/README.md).
- **Docker images on this release.** `autarki_0.1.0_amd64.tar` and `autarki_0.1.0_arm64.tar`. Umbrel uses the community store. The arm64 image leaves Lightning off.

Server install steps are on [autarki.app/install](https://autarki.app/install).

## Android beta

Version 0.1.0 (16). The same program. The phone keeps its own wallet file. Restoring the 24 words makes a second copy. The same 99 digits do not rebuild a wallet. This phone adds its own randomness. The 24 words shown once are the only backup. Lightning for Blake2b XBT bitcoin and SHA-256 BTC bitcoin is in this package. This file installs over the previous signed 0.1.0 package. A phone that already has 0.1.0 (1) has to uninstall that copy before this one will install.

- [Request access](https://appdistribution.firebase.dev/i/2ae8a6c81ce866a4). Sign in with a Google account. Firebase emails the install.
- Or download [autarki-android.apk](https://github.com/RouteHash-com/autarki/releases/download/0.1.0/autarki-android.apk) and allow the install. A 64-bit phone, Android 8 or newer.

## Check the download

Download `SHA256SUMS` into the same directory as the files, then run:

```
sha256sum -c SHA256SUMS --ignore-missing
```

A matching file prints OK.

```
5bc9d2dce8cf6d26fd8c4e8dbb8feec29f6092ee1ec65a13376b6445cb6f39c8  autarki_x86_64.s9pk
c7e896f86106f29835a4b51eaac350480fd55f89e8cee7e87aa7f1bbfb2a8265  autarki_aarch64.s9pk
1ac3c9ad47285b1cecd1220fcabed1f1166b485e750243ca02b4600e34e91a45  autarki_0.1.0_amd64.tar
2bfc6369d9825d4daf2e3087c97ea17bc79a661ac7976a545ca5d635cda0e87d  autarki_0.1.0_arm64.tar
62736f2e1b985c8b1b58ff5e9970a16b70a97afd83245740c649c73b8e3649f1  autarki_ubuntu_amd64.tar
85ee63fdeb5be7ac2feb5f8a231294e61b43123b4b390ac7b7c7405b26b09c29  autarki-android.apk
```
