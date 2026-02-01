# RedM Egg – Pterodactyl

Cet **egg RedM** pour **Pterodactyl** permet d’héberger un serveur **Red Dead Redemption 2 (RedM)** en utilisant les dernières versions du serveur **CFX**.  
Il est basé sur l’egg officiel maintenu par **parkervcp** et a été adapté pour prendre en compte les changements récents de RedM.

---

## Fonctionnalités

- Support des **dernières versions RedM / CFX**
- Téléchargement automatique de l’artifact RedM
- Support de **versions spécifiques ou latest**
- Installation automatique des ressources par défaut
- Compatible avec **txAdmin**
- Configuration automatique de `server.cfg`
- Gestion simple via le panel Pterodactyl

---

## Prérequis

- Une **clé CFX valide** (obligatoire)
- Un **serveur Pterodactyl** fonctionnel
- Un port ouvert pour le jeu (par défaut `30120`)
- Optionnel : une clé Steam Web API

---

## Installation

1. Importer l’egg **RedM** dans le panel Pterodactyl.
2. Créer un nouveau serveur avec cet egg.
3. Renseigner les variables obligatoires (voir ci-dessous).
4. Démarrer le serveur.

---

## Fonctionnement de l’installation

- Télécharge automatiquement les **ressources officielles CFX**
- Télécharge l’artifact RedM :
  - dernière version recommandée
  - version spécifique
  - URL personnalisée
- Extrait les fichiers dans le dossier `alpine`
- Génère un `server.cfg` par défaut si absent

---

## Variables de configuration

### Obligatoires

| Variable | Description |
|--------|------------|
| `CFX_LICENSE` | Clé CFX (obligatoire) |
| `SERVER_HOSTNAME` | Nom du serveur affiché |
| `MAX_PLAYERS` | Nombre maximum de joueurs (1–128) |
| `CFX_VERSION` | Version du serveur (`latest` ou précise) |

---

### Optionnelles

| Variable | Description |
|--------|------------|
| `STEAM_WEBAPIKEY` | Clé Steam Web API ou `none` |
| `DOWNLOAD_URL` | Lien direct vers un artifact RedM |
| `TXADMIN_ENABLE` | Activer txAdmin (`1` / `0`) |
| `TXADMIN_PORT` | Port txAdmin |

---

## txAdmin

### Activation

```env
TXADMIN_ENABLE=1
TXADMIN_PORT=40120
```
Modification de RedM pour le panel Pterodactyl. Vous pouvez désormais utiliser txAdmin.

## Auteur
- MaEvA  
  - [page GitHub](https://github.com/Maeva31)
  - [Discord](https://discord.gg/bJ4UjhjUDP)
  - [Site Personnel](https://maevakonnect.fr)
