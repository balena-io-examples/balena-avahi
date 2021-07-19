# mDNS/.local resolution with Avahi within a container

This example project demonstrates how to install Avahi and nss-mdns in order to resolve *.local hostnames via mDNS within a container.

The motivation behind this example project is that while it is already possible to resolve *.local hostnames from within this balena host OS, currently it is not possible to do that within a container without installing a separate mDNS resolver there.

The part with setting up systemd is taken directly from the [Balena Services Masterclass](https://www.balena.io/docs/learn/more/masterclasses/services-masterclass/#5-running-systemd-in-a-service). On top of that the only necessary step is to install Avahi and nss-mdns.

_Note: While systemd-resolved provides .local resolution capabilities as well, we recommend using Avahi. The reason is that systemd-resolved depends on systemd-networkd or NetworkManager for its configuration, while Avahi can be used in standalone mode._
