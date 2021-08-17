---
parent: Setting up Cardano
layout: default
title: Journal
nav_order: 4
---

# Journal
`journalctl` logs all the connections `cardano-node` makes, this file can get big.
 
Save space by only keeping the last 7 days of logging.
```
sudo nano /etc/systemd/journald.conf
```
```
# /etc/systemd/journald.conf
MaxRetentionSec=7d
```

Load the new config
```
service systemd-journald restart
```

