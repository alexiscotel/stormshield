# Stormshield SN200

## Infos étiquette
- PN : **SN200-XA10A-101**
- SN : **SN200A15G5313A7**
- Registration code : **4e0f0784**

## Réinitialisation d'usine

Se connecter en physique au stormshield
- login : admin
- mot de passe : password

Une fois connecter, executer la commande defaultconfig avec les paramètres -f (force) et -r (reboot)
```
defaultconfig -f -r
```


## Première installation / configuration

interface d'installation : [https://10.0.0.254/install](https://10.0.0.254/install)

mot de passe admin : **password**

### Adressage

| infos | IP |
| - | - |
| passerelle par défaut | 10.10.200.10 |
| masque de sous-réseau | 255.255.255.0 |
| Adresse IP de début | 10.10.200.100 |
| Adresse IP de fin | 10.10.200.250 |



### 1. Configuration du réseau

**Définition d''une IP statique**

|  |  |
| - | - |
| Adresse IP | 10.10.200.10 |
| Masque réseau | 255.255.255.0 |
| Passerelle par défaut | 10.10.200.254 |
| Serveur DNS principal | 8.8.8.8 |
| Serveur DNS secondaire | 8.8.4.4 |


### 2. Configuration du réseau interne

Choix du mode : identique au réseau WAN (mode **transparent**)

#### Description des modes
- **transparent** : crée un pont réseau entre l'*interface externe* (port 1) et toutes les *interfaces internes* (port 2)
- **Translaté** : permet de définir un réseau interne, qui s'appliquera à toutes les interfaces à partir du port 2 (donc à l'exclusion de l'interface externe (port 1) )


### 3. Services réseaux

Domaine DNS : *laisser vide*
Attribution d'adresses IP (DHCP)
- Première adresse IP disponible : **10.10.200.100**
- Dernière adresse IP disponible : **10.10.200.250**


### 4. Microsoft Active Directory

*Skip*


### 5. Administration de l'équipement

Mot de passe de l'utilisateur *admin* : **password**

Accès administration WEB :
- **network_internals** (regroupe tous les réseaux internes)

Activer l'accès SSH pour l'utilisateur admin (*accès par mot de passe*)


### 6. Mise à jour des paramètres réseaux

*Mettre à jour et poursuivre la configuration*

Nouvelle adresse pour la suite de la configuration : [https://10.10.200.1](https://10.10.200.1/admin/install.html?lang=fr)


### 7. Enregistrement

#### Produit
- Numéro de série : **SN200A15G5313A7**
- Partenaire : *laisser vide*
- Mot de passe d'enregistrement (WEB) : **4e0f0784** (❗problème d'activation)

#### Société (utilisateur final)
- Nom : NA
- Téléphone : *laisser vide*
- Ville : NA
- Code postal : 44000
- Pays : France
- Adresse : NA

#### Contact (utilisateur final)
- Nom : Ux
- Prénom : Home
- E-mail : noreply@homux.me


### 8. Mise à jour des bases dynamiques

*Récapitulation de l'écran* 
- Antispam : Listes noires DNS (RBL)
- Antispam : moteur heuristique
- Antivirus : signatures antivirales ClamAV
- IPS : signatures de protection
- Base de données d'URL (Stormshield)
- Management des vulnérabilités
- Autorités de certification racine
- Géolocalisation / Réputation IP publiques


### 9. Configuration des serveurs de l'entreprise

*Skip* (*Voir ensuite pour plug le serveur WEB et messagerie de Proxmox*)


### 10. Accès Internet

- Activer l'accès à internet et filtrer en fonction des catégories suivantes
	- *Attendre la mise à jour des catégories de sites Web* (**ou pas !**)
	- Activer la protection antiviral pour l'accès WEB
- Autoriser l'utilisation des logiciels de messagerie instantanée (IM)


### 11. Inspection du trafic

Choix du mode : **IPS**

Liste des modes disponibles :
- IPS (Détecter et bloquer)
- IDS (Détecter)
- Firewall (Ne pas inspecter)


### 12. Appliquer la configuration de la politique de sécurité

*Laisser le transfert des paramètres se faire*
Etapes :
- Création des autres règles de la politique
- Autorisation de la messagerie instantanée
- Activation de la politique de sécurité

### 13. Fin de l'installation

Panneau d'administration disponible à l'adresse : [https://10.10.200.1/admin/admin.html](https://10.10.200.1/admin/admin.html)- identifiant : **admin**
- mot de passe : **password**