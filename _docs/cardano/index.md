---
layout: default
title: Setting up Cardano
nav_order: 2
has_children: true
---

# Setting up Cardano

1. Set LLVM up for raspberry pi (allows cardano-cli to compile successfully)
2. Start a `tmux` session so we can detach with `C-b d`, 
3. `cardano-cli` and `cardano-node` compilation will take a while, 4+ hours.
*nb. Raspberry Pi will limit the CPU if the temperature exceeds 80°C*
 
4. Start using [Coin Cashew's Guide][cc]{:target="_blank"}

[cc]: https://www.coincashew.com/coins/overview-ada/guide-how-to-build-a-haskell-stakepool-node
