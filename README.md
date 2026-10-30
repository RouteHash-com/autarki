<p align="center">
  <img src="icon.svg" alt="Autarki" width="128">
</p>

# Autarki - Wallet / Nostr Shop

No platform. Just the sale.

Autarki is the wallet and the Nostr shop. It runs on an AMD or Intel server and on a Raspberry Pi. On StartOS, a Raspberry Pi uses `autarki_aarch64.s9pk`. On Umbrel, including Umbrel Home and a Raspberry Pi, install from the RouteHash community store. That listing installs on umbrelOS 1.x and on umbrelOS 2.0. This page has no umbrelOS file to download. A merchant builds the order on the page. Use it as an in-person point of sale, or set the shop to Online and take the order over Nostr. The same page hires a listed rig, posts a classified, and an online order can be shipped. The words, the shop book, and the sale stay on that server.

Ordinary XBT and SHA-256d use Autarki's servers until you connect your own node under Settings, then Coin Nodes. XBTC uses Autarki's public node until you connect your own. The StartOS package and the Umbrel package do not include that node. A customer can pay at the counter or send the order from their own wallet.

<p align="center">
  <img src="shop.png" alt="Autarki shop page for Sunrise Coffee Shop, with one bagel on the order and the Check-Out button" width="440">
</p>

## What you get

One page: Shop, Receive, Send, Balance, Ledger, Store, Mining, Classifieds, and Settings. Settings is the gear on the first row. Classifieds stays hidden until you turn on Enable Classifieds under Settings. Mining stays hidden until you save a RouteHash account under Settings. Open Mining Invoices on Balance follows that same account.

The first screen creates the wallet. Write the 24 words on paper before you leave that screen. A password for this copy is optional. Leave both password fields blank and the 24 words are stored unencrypted on this device. A backup of this service is then the seed. Restore the 24 words is on that same screen. It shows the first XBT address and does not show the words again. A shorter phrase uses Import a BIP39 phrase. A native SegWit phrase can be imported on that same screen. After that import you can set a password, or leave the copy unlocked.

Settings, then Nostr Node, then A copy of the shop, saves the catalog, the orders, the coin journal, and the classifieds to a file on this computer or a drive. Bring a copy back replaces that book. The file leaves out the 24 words, the wallet file, a secret key, a macaroon, and a node password. The Lightning channel stays on the Lightning node. The stall, each product, and each classified are already notes on the Nostr node. Anyone can read those notes. This wallet does not send the shop book to that shared node. A shop that runs its own Nostr node keeps those public notes on that machine. Autarki's node is the shared board until then.

The shop opens as a point of sale. A guest at the counter uses Pay Counter, and the clerk ticket shows the last four characters of the order. Set the shop to Online when the sale is not at the counter. Online hides Pay Counter and that ticket. Publish announces the choice. Until you publish, customers still see the counter.

Nostr is how a shop is found, and how an order reaches that shop, without a website of your own. Publish announces the shop name, the products for sale, and which nodes should receive an order. Check for orders brings a new order onto Check Outs. Paying is still a coin, cash, a card, or Lightning. The order itself does not move the money. When the clerk marks a counter sale paid, the customer's page shows that order under Ledger, then Receipts.

The three chains are ordinary XBT, SHA-256d, and XBTC. XBTC is the third chain. Ordinary XBT and SHA-256d use Autarki's servers until you connect your own node under Settings, then Coin Nodes. A silent-payment code for an address of yours is used only after that node is connected. Until then the page gives a normal address. Paying a shop order uses the stall's silent-payment code from that order. A code you type on Send uses your own node. XBTC uses Autarki's public node until you connect your own. Where this copy includes Autarki's XBTC node, that node is used until you connect your own. The StartOS package and the Umbrel package do not include that node. Nostr uses Autarki's public node until you add another. Blake2b Lightning and SHA-256 Lightning are your own nodes. The seed stays in this wallet. The longer notes on those cards stay closed until you open them. The address, the certificate, and the channel amount stay on the page.

On Receive, Send, Balance, and the till, the ordinary Bitcoin chip says BTC. Under Settings, then SHA-256 Lightning, the save button says Save BTC Lightning. Remove this node, under Settings, then Coin Nodes, hides that chain on those screens, on checkout, and on Check Outs. Use this node brings it back. The choice stays in this browser. A saved connection stays on this computer.

On Umbrel you can run Knots for XBT, Knots for XBTC, or Bitcoin Core for SHA-256. XBT Knots and Bitcoin Core do not run on the same computer. XBTC Knots can run on the same computer as XBT Knots. This package does not treat Bitcoin Core as the XBT node. Blake2b Lightning is Lightning Fork, which PaulsCode made for XBT Knots. SHA-256 Lightning is LND, for Bitcoin Core. A giveaway, a personal, or a job you are hiring for can be posted with no coin node. A store catalog can be saved and announced too. Goods, a service, a rental, or a job offered for a price needs the XBT node or the Bitcoin node. One is enough. That ad can carry a payment code for each connected node. Buyers pay that shop on-chain after a coin node is connected and you publish the shop again.

## Ship an online order

An online shop asks Ship or Pick up before the order is sent. There is no default. Pick up pays the shop directly, the same as a counter sale. A shipment pays with Lightning. The shop marks it shipped. The customer marks it received. The shop's node holds the coins until the customer marks the order received. Tracking is a note on the order. If the customer does not mark it received, the hold ends and the coins return to the customer. The shop's node has to stay on for that window.

Each open order shows Ordered by and a short public name. On a customer wallet, Balance keeps See open orders and opens Shop. On the shop's wallet, an order that is still open opens Ledger, then Check Outs.

The stall card shows the shop's short public name, the day the stall note was signed, and the payment codes. It shows how many shipments this wallet has marked received, and how many are still unfinished. After a completed shipment, the stall can show how many receipts both keys signed.

Pick up on a classified offers Pay with XBT and Pay with BTC, with Lightning under the chain you press. Ship offers XBT Lightning and BTC Lightning. On-chain is not offered for a shipment. When this wallet is the seller, that Lightning payment request comes back on the click. The customer ledger names the order, the store, and the store owner. The coin download includes the product, the store, the date, and the charges on that order.

## Classifieds

Classifieds stays hidden until you turn on Enable Classifieds under Settings. A new wallet leaves it off. Turning it off hides the tab. A draft stays on this computer.

The categories are Goods, Services, Jobs, Rentals, Giveaways, and Personals. Goods, a service, and a rental ask for a price. A job asks Offer or Hire. A giveaway and a personal do not ask for a price. An ad can carry up to four image addresses. A map link is an https address from OpenStreetMap, Google Maps, or Apple Maps. What is a map link? tells you to copy that address and paste it into Map. Use my location copies the shop's saved country, province or state, city, neighbourhood, and map link. It does not open that explanation.

Search sits to the left of the keyword. Post and Check for orders are icons on the same row as Show Ignored and View blocked. My Ads, beside Post, shows the ads saved on this computer. Opening Post hides the ads. Edit is on your own classified card. Cancel on the ad form leaves it without saving. Save and Publish return to the board when they succeed. One buyer and one listing stay one unpaid order. With the store off, a classified sale still shows on Check Outs until it is paid, and on Sales after that. A classified ad and a store listing are saved to the same Nostr account on the relay(s); they use the same key. A Discord username can be shown beside the shop. The shop and the classified stay public. The link is not required to buy or sell. Publishing an ad does not require a store listing. Place notes sit on the Country row. Each connected coin node gets a silent-payment code, so a buyer can pay that chain. The buyer pay card uses the same code picture as a shop order, with the chain name in the center.

Classifieds use their own node list. Kind 30402 is the classified. The stall and the products stay kinds 30017 and 30018. The nodes that receive an order are kind 10050. The private order is kind 1059. The order is a private note. The node that carries it cannot read it. If Shop or Classifieds comes back empty, check the node. If it allows every kind, leave it that way. If it only allows some kinds, allow 30402, 30017, 30018, 10050, and 1059. A whitelist that should check the receipt count also allows 38383 and 38384. A whitelist that should show the Discord link also allows 10011.

A price line reads Price in sats, then an approximate dollar amount, then now at market price. The word price opens the Neoxa market for BTCB2 and USDC:

https://neoxa.exchange/trade/BTCB2_USDC

A name on a post or an order is the display name that person published, or their name when they published no display name. A click copies the public name. A missing profile leaves the short public name. That name is what they wrote. It is not a checked website name. Kind 0 is a profile. A whitelist that should show a name also allows kind 0.

## Hire a listed rig

Save a RouteHash account under Settings. The account is the one on https://routehash.com. That account unlocks Mining. Hire a listed Blake2b rig with XBT, or a listed SHA-256 rig with BTC.

Mine writes a Lightning invoice for accepted shares and waits until you click Pay. Paying it starts that rig only. The button says Pay to start on the first invoice, and Pay to keep on a later invoice for a rig that is already hashing. Add Hash puts another rig on the same card. Blake2b is one card. SHA-256 is the other card.

Hours from balance uses the confirmed balance on that account for the rig's minimum time. The first click quotes the hire. The second click spends it. Nothing is spent until you click Mine or confirm those hours.

The card shows the work still paid for. The countdown starts when the rig is hashing. Before payment the card shows the time you bought. The payout address is on the card while a hire is running or waiting for payment. You can remove a hire that is still waiting, or stop one that is hashing.

Balance lists Open Shop Orders. Once the RouteHash account is saved, it also lists Open Mining Invoices for a hire that is running or waiting for payment.

## Install on Umbrel

This page does not give you an umbrelOS file. umbrelOS 1.x and umbrelOS 2.0 use the same listing. It is version 0.1.12. A wallet from 0.1.11 stays. If the store still shows 0.1.11, remove this community store and add the same address again.

1. In Umbrel, open Settings, then App stores, then Add a community app store.
2. Paste this address:

```
https://github.com/RouteHash-com/umbrel-store
```

3. Install **Autarki - Wallet / Nostr Shop**.

That store is the RouteHash community store. It is not the official Umbrel App Store. If the store is already added, or an install fails after you update to umbrelOS 2.0, remove this community store and add the same address again. Umbrel keeps the copy it already downloaded.

Umbrel builds the app on the machine. A PC, Umbrel Home, and Umbrel Pro use the amd64 program. A Raspberry Pi uses the arm64 program.

To check those programs yourself, open the `routehash-autarki` folder in the store and run:

```
sha256sum -c SHA256SUMS
```

| Program | SHA-256 |
| --- | --- |
| `bin/autarki-amd64` | `b72e326e5610b66be4a0e76f19647b36ad02e39fd80c404fde09c2c64b574a04` |
| `bin/autarki-arm64` | `4a2cf899cda76f1c1a5145a5dc0338173b725917d3237e1f139deccdf696d751` |

## Which file to download

StartOS uses a file from release 0.1.0. Umbrel does not. `x86_64` is the 64-bit build for an AMD PC and for an Intel PC. `aarch64` is the build for a Raspberry Pi. StartOS does not use a separate file named amd64.

| Install on | Machine | File |
| --- | --- | --- |
| StartOS | AMD or Intel, 64-bit | `autarki_x86_64.s9pk` |
| StartOS | Raspberry Pi | `autarki_aarch64.s9pk` |

Download the StartOS package:

https://github.com/RouteHash-com/autarki/releases/tag/0.1.0

The same release also attaches `autarki_0.1.0_amd64.tar` and `autarki_0.1.0_arm64.tar`. Those are Docker images from this build. They are not an umbrelOS 2.0 install, and the community store does not use them. An Ubuntu server uses `autarki_ubuntu_amd64.tar`. The steps are on the Ubuntu page. Sizes and checksums for every file on the release:

| File | Bytes | SHA-256 |
| --- | ---: | --- |
| `autarki_x86_64.s9pk` | 30724450 | `5e3e527870212841a2ef128e271ee42d5e00e9c469d3f17113093a584135a823` |
| `autarki_aarch64.s9pk` | 29360485 | `d246a33d005f0b4226472a8fcb18b54056906245a0f4e23b0a22b5dd42057fd2` |
| `autarki_0.1.0_amd64.tar` | 111381504 | `d9f65f34e4b7501265d056f7f6bcdcbec8757507795fce65ac174c6111bc6d7a` |
| `autarki_0.1.0_arm64.tar` | 132101632 | `1d5e1f3839fb272873ebcfac406779c0fb9a84dd50b69db4e8f9cae08f0ac203` |
| `autarki_ubuntu_amd64.tar` | 111381504 | `8f46dfc55179effbb5b7f72df1198be07eb726dd1ddf1239d5cc3a9c5aed4bc3` |

The package version inside each StartOS file is 0.1.0:10. Sideloading it replaces 0.1.0:9, and the wallet stays.

## Check the download

Put `SHA256SUMS` from the release in the same folder as the file you downloaded. Then run:

```
sha256sum -c SHA256SUMS --ignore-missing
```

The line for your file ends in `OK` when the download matches. A partial download does not.

## Install on Ubuntu

An Ubuntu server with Docker, and without StartOS or Umbrel, uses `autarki_ubuntu_amd64.tar` from the same release. The steps and the compose file are on the Ubuntu page:

https://github.com/RouteHash-com/autarki/blob/main/ubuntu/README.md

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
