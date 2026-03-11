# NetForge

a network automation project I built to learn and demonstrate real-world skills used by network engineers at companies like Cisco, AT&T, and Juniper.

The idea was simple - instead of manually SSHing into every router and typing the same commands over and over, why not automate the whole thing? that's exactly what this project does.

## Tech Used

- **Ansible** - for pushing configs to routers and switches
- **Python + NAPALM** - for pulling device facts and building reports
- **GNS3** - to simulate the whole network on my laptop
- **Cisco IOSv** - virtual routers/switches inside GNS3
- **WSL2** - to run Linux tools on Windows

## Things I Learned Along the Way

Getting Ansible to talk to cisco devices over SSH was trickier than expected - you need to set `ansible_connection=network_cli` and make sure legacy SSH algorithms are enabled on the router side. Spent a good few hours on that one.

NAPALM made pulling device facts surprisingly clean once the connection was stable. The reports it generates are good enough to drop straight into documentation.