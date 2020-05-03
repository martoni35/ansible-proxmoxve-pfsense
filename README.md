# ansible-proxmoxve-pfsense

## Objectifs du projet (à compléter et/ou modifier)

Déploiement et configuration d'un serveur proxmox avec un firwall virtuel pfsense.
Proxmox sera ensuite disponible par accès VPN + SSH.

### Prérequis (à compléter et/ou modifier)

* Avoir un serveur dédié avec une IP public + son accès root
* Avoir créé un domaine DNS et aassocié ce nom avec l'IP public du serveur dédié
* Avoir installé proxmox depuis l'image proposée par votre provider ou installé debian + proxmox

## Liste des étapes (à compléter et/ou modifier)

Plusieurs rôles composeront ce playbook et permettront de distinguer les différentes étapes :

* rôle pour la configuration de proxmox:
  hostname, partitionnement, cartes réseaux physiques, compte system et compte proxmox
* rôle pour la configuration des services sur le serveur proxmox:
  service ssh, ajout de fail2ban, service smtp, service iptables et son template, template des routes...
* rôle pour la création d'une VM (récupération fichier vpn-client par exemple)
* rôle pour la création et configuration de pfsense
  déploiement depuis une image, configuration, création des réseaux, créations des rules..
* rôle pour le service VPN de pfsense

