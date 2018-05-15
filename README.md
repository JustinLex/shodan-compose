# shodan-compose

My docker-compose files for all the services running on my home server, SHODAN.
SHODAN is designed for complete fire-and-forget ease-of-use, it can be fully replicated on any Docker server using these compose files, and the local data stored in /services and /mnt/storage. Any service on the machine can be managed through docker-compose, and will remember their configuration independent of their container instance.

## Services
As of now, SHODAN runs 3 services and 1 gameserver.

### Services:
* Home-Assistant for home automation
* Samba filesharing for Windows filesharing and Windows backups
* Unifi AP controller for managing my Unifi access point (with more coming)

### Gameservers:
* Factorio

### Services waiting to be implemented:
 * wiki.js - My old documentation wiki used gollum, but it's not very powerful, and doesn't have any Docker containers on Docker Hub. I'd rather not "maintain" my own Dockerfile or integrate it with docker-compose, and wiki.js seems to be the new, upcoming wiki package.
 * Emby - It has taken me 2 years to get around to implementing a media server on my home network...
 * Transmission with OpenVPN buddy container - Should be an obvious companion to emby.
 * automated offsite backup container - Still need to set up offsite backups...
 * OpenSSH - My latest plan for a self hosted "cloud drive" involves a hardened sshfs that my laptop automatically mounts to.

## etc
Note: The plaintext passwords within the Samba config are an unfortunate limitation of dperson's Samba container, but since that service (and most others) are only accessible on the wired network or through VPN, they don't pose a major security hole. As long as my roommate doesn't get any ideas.
