---
parent: Setting up Cardano
layout: default
title: Air Gapped Machine
nav_order: 3
---

# Set up the air gapped environment

1. Never connect to the internet!

2. Remove Network Manager

```
# Ubuntu 21.04 Desktop
sudo apt-get remove --purge network-manager network-manager-gnome network-manager-pptp network-manager-pptp-gnome
```

3. Remove Bluetooth for good measure

```
# Ubuntu 21.04 Desktop
sudo apt-get remove --purge blueman bluez-utils bluez bluetooth
```

4. Have `cardano-cli` and `cardano-node` compatible binaries on the air gapped machine

5. Have a cardano wallet generator on the air gapped machine

