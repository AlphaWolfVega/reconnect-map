RECONNECT MAP — DÉPLOIEMENT INFOMANIAK
========================================

Contenu du zip
--------------
- index.html       : la landing complète (single-file vanilla, ~150 Ko)
- .htaccess        : config Apache (HTTPS forcé, gzip, cache, sécurité)
- robots.txt       : noindex/nofollow (la landing reste privée)
- README-deploy.txt: ce fichier

Comment déployer sur Infomaniak
-------------------------------
1. Connecte-toi au Manager Infomaniak (manager.infomaniak.com)
2. Hébergement Web > sélectionne ton domaine
3. Onglet "Gestionnaire FTP" ou "Stockage" > ouvre /web/ (ou /sites/<domaine>/)
4. Upload les 3 fichiers (index.html, .htaccess, robots.txt)
   À la racine du dossier web. PAS dans un sous-dossier.
5. Vérifie que ton domaine pointe sur l'hébergement
6. Active le SSL gratuit Let's Encrypt (Manager > SSL > Let's Encrypt)
   Le .htaccess force déjà la redirection HTTPS, mais sans cert ça donnera
   une erreur — donc active le SSL avant de tester.

Tester
------
- Ouvre https://<ton-domaine>/ en navigation privée
- Vérifie : fond crème, hero "There are 5 kinds of pleasure...", quiz fonctionne

Dépendances externes (rien à uploader, mais à connaître)
--------------------------------------------------------
- Google Fonts (Cormorant Garamond + Lato) — chargé via CDN
- Shopify CDN (Pleasuary) — images bundles + radar
  Domaine : cdn.shopify.com
Si tu veux self-host les images plus tard, il faudra les rapatrier et
modifier la constante SHOPIFY_BASE dans index.html (ligne ~1379).

Mise à jour
-----------
Le repo source est : https://github.com/AlphaWolfVega/reconnect-map
Pour redéployer une nouvelle version, ré-extrais le index.html à jour
depuis ce repo et upload-le par-dessus l'ancien.

Verrous techniques
------------------
- Pas de service worker, pas de PWA — cache navigateur classique
  (le .htaccess limite le cache HTML à 5 min pour les MAJ rapides)
- Pas de backend, pas d'email capture, pas de DB
- Stockage user dans localStorage uniquement (resume du quiz)

Build de référence
------------------
Date export : 2026-05-08
Commit Git  : e71fd23 (Stock modal Variant A inline + 4 benefits)
URL live GH : https://alphawolfvega.github.io/reconnect-map/
