# ~~shodan-compose~~

## This repo has been replaced with [jlh-shodan](https://github.com/JustinLex/jlh-shodan), and the docker-compose files have been moved there.

------

My docker-compose files for all the services running on my home server, SHODAN.
SHODAN is designed for complete fire-and-forget ease-of-use, it can be fully replicated on any Docker server using these compose files, and the local data stored in /services and /mnt/storage. Any service on the machine can be managed through docker-compose, and will remember their configuration independent of their container instance.

## Services
As of now, SHODAN runs 3 services and 1 gameserver.

### Services:
* Home-Assistant for home automation
* Samba filesharing for Windows filesharing and Windows backups
* sftp server for secure filesharing over the internet, can be automounted on Linux and Android with SSHFS.
* Unifi AP controller for managing my Unifi access point (with more coming)
* wiki.js for documentation (being transferred from gollum)

### Gameservers:
* Factorio

### Services waiting to be implemented:
 * Emby - It has taken me 2 years to get around to implementing a media server on my home network...
 * Transmission with OpenVPN buddy container - Should be an obvious companion to emby.
 * Automated offsite backup container - Still need to set up offsite backups...
