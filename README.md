# Mes challenges Root-Me

Je m'entraîne régulièrement sur [Root-Me](https://www.root-me.org) dans le cadre de ma formation en cybersécurité (BUT Réseaux & Télécoms, parcours Cybersécurité à l'IUT d'Auxerre). Ce dépôt recense les challenges que j'ai résolus et les notions qu'ils m'ont fait travailler.

Certains ont été faits en binôme avec Amin Cherif. Je suis aussi actif sur TryHackMe : [tryhackme.com/p/Dylanlpb](https://tryhackme.com/p/Dylanlpb).

**Pourquoi il n'y a pas les solutions ici :** la charte Root-Me interdit de publier les solutions de ses challenges. Je liste donc seulement les challenges et la notion derrière chacun, jamais la méthode ni le flag. Pour moi c'est aussi une question de principe — un bon réflexe quand on fait de la sécurité.

## Sécurité Web

- **API – Broken Access Control (MongoDB)** *(intermédiaire)* — un identifiant prévisible (ObjectId MongoDB) utilisé à tort comme jeton de sécurité. Le genre de faille de contrôle d'accès qu'on retrouve souvent.
- **SQL Injection – Philoquote** *(intermédiaire)* — injection SQL avec contournement d'un filtre de saisie. Toute la logique des requêtes préparées derrière.
- **SQL Injection – En aveugle** *(intermédiaire)* — même principe mais sans retour affiché : on extrait l'info par déduction.
- **XSS – DOM based** *(intermédiaire)* — du JavaScript injecté côté client parce que la page construit le DOM à partir d'une entrée non filtrée.
- **HTTP – Totemus-QCode** *(intermédiaire)* — analyse des requêtes et réponses HTTP et de la logique de l'appli.
- **File Upload – Double extensions** *(facile)* — contournement d'un filtre d'extension à l'upload.
- **EDU-B – File Upload (Introduction)** *(facile)* — les bases du contrôle de téléversement de fichiers.

## Système

- **Linux Privesc – CVE** *(facile)* — élévation de privilèges sous Linux en exploitant une vulnérabilité connue. Ça fait bien comprendre l'importance des mises à jour.

## Objets connectés (Bluetooth LE)

- **BLE – Authentification strip**, **Entrée utilisateur**, **Contrôles incohérents** *(facile à intermédiaire)* — analyse de communications Bluetooth Low Energy et des faiblesses de contrôle côté objet connecté.

## Blue Team — SOC et forensic

- **SOC Réseau – Scan de ports** *(intermédiaire)* — repérer un scan de ports dans des logs réseau.
- **SOC AD – Authentification** *(intermédiaire)* — analyser des événements d'authentification Active Directory pour détecter une activité anormale.
- **EDU-B – SOC Windows (Pilotes)** *(facile)* — investigation d'événements système Windows.
- **EXIF – Christmas House** *(facile)* — récupérer des infos cachées dans les métadonnées EXIF d'une image.

## Les outils que j'utilise

Burp Suite, nmap, Wireshark, de l'analyse de logs (réseau, Windows, AD), des outils d'analyse BLE et de lecture de métadonnées.

Ce qui me plaît dans ces challenges, c'est de voir les deux côtés : comprendre comment une attaque marche pour mieux savoir la détecter et la corriger. Les write-ups détaillés, je les garde pour moi (règle Root-Me).

---
Formation cybersécurité — BUT R&T, IUT d'Auxerre.
