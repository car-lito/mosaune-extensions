# Mosaune — extensions

Catalogue officiel des premiers paquets du **Projet Mosaune**, un serveur multimédia personnel en développement.

## Utiliser ce catalogue

Dans Mosaune **0.0.21**, ouvrez **Réglages → Extensions → À télécharger**, puis **Charger le catalogue officiel**. Son adresse est déjà intégrée.

Dans Mosaune **0.0.20**, ouvrez **Gérer les dépôts GitHub** et ajoutez **https://github.com/car-lito/mosaune-extensions** en laissant la branche vide.

Ouvrez une carte, vérifiez le paquet et ses accès, puis installez-le. La première installation reste désactivée jusqu’à votre choix. L’actualisation recherche les nouvelles versions sans les installer automatiquement. Le catalogue reste conservé en cas de panne réseau.

## Paquets

| Paquet | Versions | Fonction |
|---|---|---|
| Ambre | 2.0.0 | Thème clair/sombre déclaratif aux tons papier, ambre et brun. |
| TMDB | 0.4.0 et 0.4.1 | Recherche et fiches de films, séries et épisodes. |

Les deux versions TMDB offrent les mêmes fonctions : elles servent à tester la mise à jour indépendante et la restauration. Si la 0.4.1 est déjà installée, aucune réinstallation n’est nécessaire. TMDB nécessite votre propre clé ou jeton, à saisir dans les réglages de votre serveur. Aucun identifiant de connexion n’est fourni ici.

## Vérifications

`mosaune-repository.json` annonce chaque ZIP, sa version et son SHA-256. Mosaune vérifie les octets et leur manifeste avant installation. Les thèmes ne contiennent pas de programme exécutable. Ce pilote n’accepte que les fournisseurs TMDB portant la signature reconnue du projet ; ajouter un dépôt n’accorde aucun droit à de nouvelles clés.

`provider-package-key.pub` est uniquement la clé publique de vérification. La clé privée n’est pas distribuée. Une signature établit la provenance reconnue du paquet, pas l’absence de bogues. Le dépôt contient les paquets d’extensions, pas le serveur ni les bibliothèques de médias. Mosaune est encore expérimental.

## Composants tiers

Les programmes TMDB sont compilés en WebAssembly avec Go et incluent son runtime et sa bibliothèque standard. Leur notice est conservée dans [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt). Les données et images TMDB ne sont pas incluses ici. La licence générale du Projet Mosaune sera précisée lors de la publication de son code source. La licence Go ne s’applique pas à l’ensemble de ce projet.
