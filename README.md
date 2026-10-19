# Root-Me — CTF & challenges résolus

> Vitrine des challenges [Root-Me](https://www.root-me.org) travaillés dans le cadre de ma formation en cybersécurité (BUT R&T, parcours Cybersécurité — IUT d'Auxerre).
>
> **Dylan Mehadi** · **TryHackMe :** [tryhackme.com/p/Dylanlpb](https://tryhackme.com/p/Dylanlpb)

Certains challenges ont été travaillés en binôme avec **Amin Cherif**.

> ⚠️ **Pas de solutions ici.** La charte Root-Me interdit la publication des solutions de ses challenges. Ce dépôt ne liste donc que les challenges résolus et la **notion de sécurité** associée — jamais la méthode d'exploitation ni les flags. L'objectif est de montrer les domaines couverts, pas de divulguer les réponses.

---

## Challenges résolus

### Web — Client & Serveur

| Challenge | Notion travaillée | Difficulté |
|---|---|---|
| API – Broken Access / MongoDB | Contrôle d'accès défaillant, identifiants prévisibles utilisés comme jetons | Intermédiaire |
| SQL Injection – Philoquote | Injection SQL via requête `UNION`, contournement de filtre | Intermédiaire |
| SQL Injection – En aveugle | Injection SQL aveugle (blind), extraction par inférence | Intermédiaire |
| XSS – DOM based | Cross-Site Scripting côté client, manipulation non sécurisée du DOM | Intermédiaire |
| HTTP – Totemus-QCode | Analyse de requêtes/réponses HTTP, logique applicative | Intermédiaire |
| File Upload – Double extensions | Upload de fichier, contournement de filtrage d'extension | Facile |
| EDU-B – File Upload Introduction | Bases du contrôle de téléversement de fichiers | Facile |

### Système & Élévation de privilèges

| Challenge | Notion travaillée | Difficulté |
|---|---|---|
| Linux Privesc – CVE | Élévation de privilèges via une vulnérabilité connue (CVE) | Facile |

### Objets connectés (BLE)

| Challenge | Notion travaillée | Difficulté |
|---|---|---|
| BLE – Authentification strip | Analyse de communications Bluetooth Low Energy | Intermédiaire |
| BLE – Entrée utilisateur 2 | Interaction avec un périphérique BLE | Facile |
| BLE – Contrôles incohérents | Vérifications de sécurité incohérentes côté objet | Facile |

### Forensic & SOC

| Challenge | Notion travaillée | Difficulté |
|---|---|---|
| SOC Réseau – Scan de ports | Détection d'un scan de ports dans des logs réseau | Intermédiaire |
| SOC AD – Authentification | Analyse d'événements d'authentification Active Directory | Intermédiaire |
| EDU-B – SOC Windows / Pilotes | Investigation d'événements système Windows | Facile |
| EXIF – Christmas House | Analyse de métadonnées EXIF d'une image | Facile |

---

## Domaines couverts

- **Sécurité Web** — injections SQL, XSS, contrôle d'accès, upload de fichiers
- **Système** — élévation de privilèges Linux, exploitation de CVE
- **Objets connectés** — analyse de protocoles BLE
- **Blue team / SOC** — analyse de logs réseau, Windows et Active Directory
- **Forensic** — métadonnées, investigation

## Outils utilisés

`Burp Suite` · `nmap` · `Wireshark` · analyse de logs · outils BLE · lecture de métadonnées (EXIF)

---

*Formation cybersécurité — BUT R&T, IUT d'Auxerre. Les write-ups détaillés restent privés, conformément à la charte Root-Me.*
