<p align="center">
  <img src="icon.svg" alt="Autarki" width="128">
</p>

# Autarki

No platform. Just the sale.

A self-custodial wallet and a shop. You keep the 24 words. Details are at [autarki.app](https://autarki.app/).

- Shop, receive, and send for XBT, BTC, and XBTC.
- Lightning for XBT and BTC starts with the wallet on AMD and Intel. Raspberry Pi and Umbrel arm64 leave Lightning off.
- Use other Autarki Lightning nodes is under Settings, then Coin Nodes. Leave it off on AMD and Intel to use the built-in nodes. Turn it on only for another Autarki that stays on. An open channel keeps the built-in nodes running. iPhone and Raspberry Pi keep that choice on.
- The stall is public. The order is a private note.
- Classifieds stay off until Enable Classifieds.
- Pay Counter records cash, card, coupon, store credit, or coin. The card machine is the clerk's.
- Hire a listed rig. Nothing is spent until you click Mine, or until the hours are confirmed.
- A blank password stores the 24 words unencrypted on that device.
- Bugs go to [Discord #autarki](https://discord.gg/VBxvzQXvt).

## Install

Release [0.1.0](https://github.com/RouteHash-com/autarki/releases/tag/0.1.0). The StartOS package inside that tag is 0.1.0:31. The Umbrel listing is 0.1.19. The Raspberry Pi StartOS package and the Umbrel arm64 image are still the previous page.

- **StartOS.** `autarki_x86_64.s9pk` for AMD or Intel. `autarki_aarch64.s9pk` for Raspberry Pi.
- **Umbrel.** Add the [RouteHash community store](https://github.com/RouteHash-com/umbrel-store), then install Autarki.
- **Ubuntu.** `autarki_ubuntu_amd64.tar`. Steps are on the [Ubuntu page](https://github.com/RouteHash-com/autarki/blob/main/ubuntu/README.md).
- **Docker images on this release.** `autarki_0.1.0_amd64.tar` and `autarki_0.1.0_arm64.tar`. Umbrel uses the community store. The arm64 image leaves Lightning off.

Server install steps are on [autarki.app/install](https://autarki.app/install).

## Android beta

Version 0.1.0 (17). The same program. The phone keeps its own wallet file. Restoring the 24 words makes a second copy. The same 99 digits do not rebuild a wallet. This phone adds its own randomness. The 24 words shown once are the only backup. Lightning for Blake2b XBT bitcoin and SHA-256 BTC bitcoin is in this package. This file installs over the previous signed 0.1.0 package. A phone that already has 0.1.0 (1) has to uninstall that copy before this one will install.

- [Request access](https://appdistribution.firebase.dev/i/2ae8a6c81ce866a4). Sign in with a Google account. Firebase emails the install.
- Or download [autarki-android.apk](https://github.com/RouteHash-com/autarki/releases/download/0.1.0/autarki-android.apk) and allow the install. A 64-bit phone, Android 8 or newer.

## Check the download

Download `SHA256SUMS` into the same directory as the files, then run:

```
sha256sum -c SHA256SUMS --ignore-missing
```

A matching file prints OK.

```
50dc81cb111fc73a318dae3be6b317ae8846cf2864a1fe1078931369aed67e27  autarki_x86_64.s9pk
c7e896f86106f29835a4b51eaac350480fd55f89e8cee7e87aa7f1bbfb2a8265  autarki_aarch64.s9pk
86f9ff8e10792d05707f146f51de9f4ad1a973792f260bc920fde5e5a37874e6  autarki_0.1.0_amd64.tar
2bfc6369d9825d4daf2e3087c97ea17bc79a661ac7976a545ca5d635cda0e87d  autarki_0.1.0_arm64.tar
28bcdb2d7f4c00f9e20780e0479e2714aa54401229e524917a8b89b95ed2a4ff  autarki_ubuntu_amd64.tar
c92bdb0507185a9cda5c4356f2446a5e1babfa19a21360cabfb882349d9a78d2  autarki-android.apk
```
