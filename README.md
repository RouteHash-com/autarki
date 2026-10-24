# Autarki

No platform. Just the sale.

Release 0.1.0 has the StartOS package and the Umbrel image tars:

https://github.com/RouteHash-com/autarki/releases/tag/0.1.0

Download `SHA256SUMS` into the same directory as the files, then run:

```
sha256sum -c SHA256SUMS --ignore-missing
```

A matching file prints `OK`.

`autarki_x86_64.s9pk` is the StartOS sideload. `autarki_0.1.0_amd64.tar` and `autarki_0.1.0_arm64.tar` are the Umbrel images. Load the tar that matches the machine. The community store is https://github.com/RouteHash-com/umbrel-store
