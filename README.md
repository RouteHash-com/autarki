<p align="center">
  <img src="icon.svg" alt="Autarki" width="128">
</p>

# Autarki

No platform. Just the sale.

A self-custodial wallet and a shop. You keep the 24 words. You pay the person. Autarki does not hold the coins, clear the sale, or take a cut of the catalog price. Details are at [autarki.app](https://autarki.app/).

- Look through shops before you make a wallet. Sending an order needs the wallet open.
- Shop, receive, and send for XBT and BTC. Pay with XBT or Pay with BTC. Each payment stays in the coin you chose.
- Until you connect your own node, ordinary addresses use Autarki's servers. A silent-payment code appears after your own node is connected.
- Lightning for XBT and BTC starts with the wallet on AMD and Intel. You do not install a second Lightning app. Raspberry Pi and Umbrel arm64 omit the Lightning programs, so Lightning stays off there. On-chain still works on those packages.
- Use other Autarki Lightning nodes is under Settings, then Coin Nodes. Leave it off on AMD and Intel to use the built-in nodes. Turn it on only for another Autarki that stays on. An open channel keeps the built-in nodes running. iPhone and Raspberry Pi keep that choice on.
- Use Autarki's pool is one channel you confirm, so a later sale can use it. Routing stays within 1,000 sats. The pool does not hold a shipment.
- The stall is public. The order is a private note. The relay that carries the order cannot read it.
- A shipment holds the coins on the seller's node until it is marked received. Not received asks a named referee. The referee does not hold the coins. With no decision, the window still sends the coins back.
- Classifieds stay off until Enable Classifieds. Pick up can pay on-chain or with Lightning. Ship pays with Lightning. A giveaway, a personal, or a job hire can be posted with no coin node. Goods, a service, a rental, or a job offered for a price needs your own XBT node or Bitcoin node, because that ad publishes a silent-payment code.
- Pay Counter records cash, card, coupon, store credit, or coin. The card machine is the clerk's. This page does not charge the card.
- A private note goes to one person. It does not become an order and it does not move coins. There is no public chat.
- Hire a listed rig. Rewards come back to this wallet. Nothing is spent until you click Mine, or until the hours are confirmed. This computer does not mine.
- Completed shipments write the delivery count. Nobody types a star.
- The 24 words restore the funds. They do not restore the shop book or a Lightning channel. A saved copy of the shop book leaves the words out. The same 99 digits do not rebuild a wallet. That device adds its own randomness. A blank password stores the 24 words unencrypted on that device.
- Bugs go to [Discord #autarki](https://discord.gg/VBxvzQXvt).

## Install

Release [0.1.0](https://github.com/RouteHash-com/autarki/releases/tag/0.1.0). The AMD and Intel StartOS package inside that tag is 0.1.0:35, built on 11 November 2026. The Ubuntu image, the Umbrel amd64 image, Android 0.1.0 (26), and the Raspberry Pi packages are that same page. Lightning stays off on Raspberry Pi and Umbrel arm64. The Umbrel listing is 0.1.21.

- **StartOS.** `autarki_x86_64.s9pk` for AMD or Intel. `autarki_aarch64.s9pk` for Raspberry Pi.
- **Umbrel.** Add the [RouteHash community store](https://github.com/RouteHash-com/umbrel-store), then install Autarki.
- **Ubuntu.** `autarki_ubuntu_amd64.tar`. Steps are on the [Ubuntu page](https://github.com/RouteHash-com/autarki/blob/main/ubuntu/README.md).
- **Docker images on this release.** `autarki_0.1.0_amd64.tar` and `autarki_0.1.0_arm64.tar`. Umbrel uses the community store. The arm64 image leaves Lightning off.

Server install steps are on [autarki.app/install](https://autarki.app/install).

## Android beta

Version 0.1.0 (26). The same program. The phone keeps its own wallet file. Restoring the 24 words makes a second copy. The same 99 digits do not rebuild a wallet. This phone adds its own randomness. The 24 words shown once are the only backup. Lightning for Blake2b XBT bitcoin and SHA-256 BTC bitcoin is in this package. This file installs over the previous signed 0.1.0 package. A phone that already has 0.1.0 (1) has to uninstall that copy before this one will install.

- [Request access](https://appdistribution.firebase.dev/i/2ae8a6c81ce866a4). Sign in with a Google account. Firebase emails the install.
- Or download [autarki-android.apk](https://github.com/RouteHash-com/autarki/releases/download/0.1.0/autarki-android.apk) and allow the install. A 64-bit phone, Android 8 or newer.

## iPhone beta

Version 0.1.0, build 5. The same wallet and shop. This build does not start Lightning. Use other Autarki Lightning nodes stays on, for another Autarki that stays running. It is not an App Store listing. Request an invite on the [install page](https://autarki.app/install#iphone).

## Check the download

Download `SHA256SUMS` into the same directory as the files, then run:

```
sha256sum -c SHA256SUMS --ignore-missing
```

A matching file prints OK.

```
e0df9b4c5246dda2df8a47d415e6c6612dcc22ed404b3ae1f6803ebf2dcc784a  autarki_x86_64.s9pk
b8752be9eae318a67b7ee71d9f973c24eb4c14c9ad8d1baaac98677703b4a8c8  autarki_aarch64.s9pk
b0d256b5ad0af4e390973534cef4b23c2a44facba3548875ec031e994483daec  autarki_0.1.0_amd64.tar
08902083cfe0fa11f33ab69b2d6beae6ea6c998eea5afd0fe543f6b69c46f870  autarki_0.1.0_arm64.tar
b049217556e1790a26750641e51104742571783c9cf9a807b6205784e6200393  autarki_ubuntu_amd64.tar
d4767bd6fcd6c5929bcc5a4bac04a402526d5fe500e702831fdeff2c4f54fedb  autarki-android.apk
```
