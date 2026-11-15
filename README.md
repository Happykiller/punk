# Punk

Le **wiki** du cluster Happykiller : un MediaWiki en Docker, exposé sur le port 8082 et servi sous
`wiki.happykiller.net` par le reverse proxy (`nami`).

## Ce qui n'est pas versionné

`LocalSettings.php` (la configuration du wiki, avec ses secrets) et `images/` (les fichiers téléversés) restent sur
le serveur : ils sont montés dans le conteneur mais ignorés par git. Les perdre, c'est perdre le wiki — ils relèvent
des sauvegardes du serveur.

## Commandes

| Commande | Effet |
|---|---|
| `make start` | démarre le wiki |
| `make startall` | reconstruit et démarre |
| `make down` | arrête le conteneur |
| `make reset` | arrête puis supprime le conteneur |
