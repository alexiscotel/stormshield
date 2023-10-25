# Plan d'adressage IP

## équipements à connecter

- PC persos
- PC pros
- Stormshield
- Routeur TP Link
- Chromecast
- NAS
- VMs proxmox
	- serveur mail
	- serveur web
	- serveur notification


## Adressage

### DHCP Livebox

| infos | IP |
| - | - |
| passerelle par défaut | 10.10.200.254 |
| masque de sous-réseau | 255.255.255.0 |
| Adresse IP de début | 10.10.200.1 |
| Adresse IP de fin | 10.10.200.20 |

#### Baux statiques

| Equipement | IP |
| - | - |
| Stormshield | 10.10.200.10 |
| desktop alex | 10.10.200.2 |
| laptop alex | 10.10.200.3 |
| phone alex | 10.10.200.4 |

#### Baux dynamiques
Equipements :
- laptop Léo
- phone Léo
- laptop Anna
- phone Anna

### DHCP Stormshield

| infos | IP |
| - | - |
| passerelle par défaut | 10.10.200.1 |
| masque de sous-réseau | 255.255.255.0 |
| Adresse IP de début | 10.10.200.100 |
| Adresse IP de fin | 10.10.200.250 |

#### Baux statiques

| Equipement | IP |
| - | - |
| Stormshield | 10.10.200.10 |
| Routeur TP Link | 10.10.200.9 |
| NAS | 10.10.200.101 |
| proxmox | 10.10.200.102 |
| serveur mail | 10.10.200.210 |
| serveur web | 10.10.200.211 |
| serveur notification | 10.10.200.212 |


