---
layout: post
title: "Announcing Mininet 2.2.1rc1 !"
date: 2015-04-16 18:03
comments: true
categories:
---

Mininet 2.2.1 is primarily a performance improvement and bug fix release.

- **Batch startup** has been implemented for Open vSwitch, improving
  startup performance.

- **OVS patch links** have been implemented via OVSLink and `--link ovs`

  Warning! These links have *serious limitations* compared to
  virtual Ethernet pairs: they are not attached to real Linux
  interfaces so you cannot use tcpdump or wireshark with them;
  they also cannot be used in long chains - we don't recommend more
  than 64 OVSLinks, for example `--linear,64`. However, they can offer
  significantly better performance than veth pairs, for certain
  configurations.

- You can now easily **install Mininet on a [Raspberry Pi](http://raspberrypi.org)**
  (simply by using `install.sh -fnv` or `install.sh -a`)  ;-)

- Additional information for this release and previous releases
  may be found in the **[Release Notes](https://github.com/mininet/mininet/wiki/Documentation#mininet-release-notes)**
  on [docs.mininet.org](http://docs.mininet.org).

The easiest way to get started with Mininet is to download a
**VM image**. See [http://mininet.org/download](http://mininet.org/download)
for details.

The latest Mininet **source code** is available on
[github]([http://github.com/mininet/mininet) and also via
[code.mininet.org](http://code.mininet.org).