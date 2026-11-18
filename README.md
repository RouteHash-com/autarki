<p align="center">
  <img src="icon.svg" alt="Autarki" width="128">
</p>

# Autarki

No platform. Just the sale.

A self-custodial wallet and a shop. You keep the 24 words. You pay the person. Autarki does not hold the coins, clear the sale, or take a cut of the catalog price. Details are at [autarki.app](https://autarki.app/).

- Look through shops before you make a wallet. Sending an order needs the wallet open.
- Shop, receive, and send for XBT and BTC. Pay with XBT or Pay with BTC. Each payment stays in the coin you chose.
- Until you connect your own node, ordinary addresses use Autarki's servers. A silent-payment code appears after your own node is connected.
- Lightning for XBT and BTC is in the AMD and Intel StartOS package, the Ubuntu image, the Umbrel amd64 image file, and Android. You do not install a second Lightning app. The Umbrel community store, Raspberry Pi, and Umbrel arm64 omit the Lightning programs, so Lightning stays off there. On-chain still works on those packages.
- On a package that starts Lightning, a Lightning invoice in the other coin spends the coin this wallet already holds. Nothing is sent until a channel from this wallet can pay. Each install asks for its own code. There is nothing to paste.
- Use other Autarki Lightning nodes is under Settings, then Coin Nodes. Leave it off on AMD and Intel to use the built-in nodes. Turn it on only for another Autarki that stays on. An open channel keeps the built-in nodes running. iPhone and Raspberry Pi keep that choice on.
- Use Autarki's pool is one channel you confirm, so a later sale can use it. Routing stays within 1,000 sats. The pool does not hold a shipment.
- The stall is public. The order is a private note. The relay that carries the order cannot read it.
- A shipment holds the coins on the seller's node until it is marked received. Not received asks a named referee. The referee does not hold the coins. With no decision, the window still sends the coins back.
- Classifieds stay on unless Enable Classifieds is turned off. Pick up can pay on-chain or with Lightning. Ship pays with Lightning. A giveaway, a personal, or a job hire can be posted with no coin node. Goods, a service, a rental, or a job offered for a price needs your own XBT node or Bitcoin node, because that ad publishes a silent-payment code.
- Pay Counter records cash, card, coupon, store credit, or coin. The card machine is the clerk's. This page does not charge the card.
- A private note goes to one person. It does not become an order and it does not move coins. There is no public chat.
- Hire a listed rig. Rewards come back to this wallet. Nothing is spent until you click Mine, or until the hours are confirmed. This computer does not mine.
- Completed shipments write the delivery count. Nobody types a star.
- The 24 words restore the funds. They do not restore the shop book or a Lightning channel. A saved copy of the shop book leaves the words out. The same 99 digits do not rebuild a wallet. That device adds its own randomness. A blank password stores the 24 words unencrypted on that device.
- Bugs go to [Discord #autarki](https://discord.gg/VBxvzQXvt).

## Install

Release [0.1.0](https://github.com/RouteHash-com/autarki/releases/tag/0.1.0). The AMD and Intel StartOS package inside that tag is 0.1.0:47, built on 17 November 2026. The Ubuntu image, the Umbrel amd64 image, Android 0.1.0 (40), and the Raspberry Pi package are that same page. The on-chain balance keeps what remains after a transfer into Lightning, once that send has at least one confirmation in the coin record. Used Lightning addresses and Lightning transactions use Show and Hide and start closed. Receive and Send tables start closed. Classifieds stays on unless it was turned off. The extra password asks only when sending funds. Receive, contacts, Settings, and Classifieds do not ask it. Settings has a Security tab with Lock the wallet. Price hint is under Other. Questions is under Backup. A message shows the full name and Close. Send and Add to contacts show a spinner until they finish. A new contact is checked for a nostr name and a Discord name. Moving coins from the on-chain wallet into Lightning sits under the Lightning card. The From line stays hidden, because the on-chain card already shows that balance. After Prepare the transfer, Send opens on the summary. A pencil beside the amount returns to the amount field. The pace control says Adjust the fee rate. A fee already sent stays on its own card. Check again reads this wallet and does not send another fee. While a channel to Autarki's pool is opening, the Lightning card shows a spinner. Watch only asks for the account public key from the other wallet. Find a referee can be turned on from Settings, then Nostr, then Profile. A Discord username is optional. One Discord link shows that username. Otherwise the site shows the nostr name, or a shortened public name. Watch only, on Create a wallet, pastes an account public key. The words stay on the other wallet. This computer cannot sign. A public key with no path is refused. After the wallet is restored without its Lightning seeds, each chain still offers Restore this Lightning backup while the new seed is on screen. Open channels do not return. Coins still in that node's wallet come back after the scan. On a package that starts Lightning, a Lightning invoice in the other coin spends the coin this wallet already holds. Nothing is sent until a channel from this wallet can pay. Lightning stays off on the Umbrel community store, Raspberry Pi, and Umbrel arm64. The Umbrel listing is 0.1.30.

- **StartOS.** `autarki_x86_64.s9pk` for AMD or Intel. `autarki_aarch64.s9pk` for Raspberry Pi.
- **Umbrel.** Add the [RouteHash community store](https://github.com/RouteHash-com/umbrel-store), then install Autarki.
- **Ubuntu.** `autarki_ubuntu_amd64.tar`. Steps are on the [Ubuntu page](https://github.com/RouteHash-com/autarki/blob/main/ubuntu/README.md).
- **Docker images on this release.** `autarki_0.1.0_amd64.tar` and `autarki_0.1.0_arm64.tar`. Umbrel uses the community store. The arm64 image leaves Lightning off.

Server install steps are on [autarki.app/install](https://autarki.app/install).

## Android beta

Version 0.1.0 (40). The same program. The phone keeps its own wallet file. Restoring the 24 words makes a second copy. The same 99 digits do not rebuild a wallet. This phone adds its own randomness. The 24 words shown once are the only backup. Lightning for Blake2b XBT bitcoin and SHA-256 BTC bitcoin is in this package. A Lightning invoice in the other coin spends the coin this wallet already holds. Nothing is sent until a channel from this wallet can pay. This file installs over the previous signed 0.1.0 package. A phone that already has 0.1.0 (1), or a copy installed by Play, has to uninstall that copy before this one will install.

- [Request access](https://appdistribution.firebase.dev/i/2ae8a6c81ce866a4). Sign in with a Google account. Firebase emails the install.
- Or download [autarki-android.apk](https://github.com/RouteHash-com/autarki/releases/download/0.1.0/autarki-android.apk) and allow the install. A 64-bit phone, Android 8 or newer.

## iPhone beta

Version 0.1.0, build 15. The same wallet and shop. This build does not start Lightning. Use other Autarki Lightning nodes stays on, for another Autarki that stays running. It is not an App Store listing. Request an invite on the [install page](https://autarki.app/install#iphone).

## Check the download

Download `SHA256SUMS` into the same directory as the files, then run:

```
sha256sum -c SHA256SUMS --ignore-missing
```

A matching file prints OK.

```
6c7baeaa0f42a06231fb6e755e7cc9ec3c8802e518f97f26eb86346a4ac6f312  autarki_x86_64.s9pk
00556f2d2e7657406bae04d08f78775593f22dfe265a0bddd5d32903b0c07f76  autarki_aarch64.s9pk
b79a6ec0f82e1c778ef148a9ba79c393987f44843741f7680c3dbe2e67c83971  autarki_0.1.0_amd64.tar
f25d2a114dcf0bd7bb7fafd9e321b8b0a2b67d707aa9a06effe3ba843221a8a0  autarki_0.1.0_arm64.tar
6366c9b6817fbf7b06c722954583a511960e2ddf535979c6a49f9090751b7783  autarki_ubuntu_amd64.tar
5fe2955c26c9352ff6537928299b6d6a387083c150fc9b8e7681341e30ed26dd  autarki-android.apk
```
