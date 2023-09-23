# FreeBSD Jail Manual Implementation

This repository contains configuration files for a FreeBSD Jail Manual Implementation. It includes the following configuration files:

- [jail.conf](#jailconf)
- [pf.conf](#pfconf)
- [rc.conf](#rcconf)

## jail.conf

The `jail.conf` file defines the configuration for FreeBSD jails. It includes pre-start, start, pre-stop, and post-stop instructions for each jail. Here are some of the notable sections:

- **shinsha**: Configuration for the "shinsha" jail, which includes hostname, IP address, and MAC address settings.

- **deskjail**: Configuration for the "deskjail" jail, which includes hostname, devfs_ruleset, IP address, and MAC address settings.

- **bot**: Configuration for the "bot" jail, which includes hostname, IP address, and MAC address settings.

- **webserver**: Configuration for the "webserver" jail, which includes hostname, IP address, and MAC address settings.

- **mamad**: Configuration for the "mamad" jail, which includes hostname, devfs_ruleset, IP address, and MAC address settings.

## pf.conf

The `pf.conf` file contains the configuration for the PF (Packet Filter) firewall. It defines rules for network address translation (NAT), port forwarding, and general packet filtering. Notable rules include:

- NAT and port forwarding rules for redirecting traffic to specific jails.

- Rules to allow all traffic in and out.

## rc.conf

The `rc.conf` file is the system configuration file for FreeBSD. It includes various system-wide settings, including network interfaces and service enablement. Notable configurations include:

- Configuration of the bridge interface (`bridge0`) with an IP address (`192.168.100.2/24`) and the addition of the `ena0` interface.

- Enabling of FreeBSD jails (`jail_enable`) and the PF firewall (`pf_enable`).

Please make sure to review and adjust these configuration files as needed for your specific setup. Ensure that the network settings, IP addresses, and MAC addresses match your environment.

Feel free to contribute or provide feedback on this repository's configuration files!

## License
Copyright (c) 2023 Palguno Wicaksono

The copyright holders grant the freedom to copy, modify, convey, adapt, and/or redistribute this work under the terms of the BSD 3-Clause "New" or "Revised" License.
A copy of that license is available at [`LICENSE`](https://github.com/icaksh/shinsha-jail/blob/master/LICENSE)
