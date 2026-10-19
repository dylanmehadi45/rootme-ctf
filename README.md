<div align="center">

# 🚩 Root-Me — Parcours CTF & challenges de sécurité

### Journal des challenges [Root-Me](https://www.root-me.org) résolus en formation cybersécurité

**BUT Réseaux & Télécommunications — RT3, parcours Cybersécurité · IUT d'Auxerre**

![Web](https://img.shields.io/badge/Web-SQLi%20%7C%20XSS%20%7C%20Upload-e34c26)
![Système](https://img.shields.io/badge/Système-Privesc%20Linux-333)
![IoT](https://img.shields.io/badge/IoT-Bluetooth%20LE-005fcc)
![BlueTeam](https://img.shields.io/badge/Blue%20Team-SOC%20%7C%20Forensic-6f42c1)

**Dylan Mehadi** — en binôme sur certains challenges avec **Amin Cherif**
TryHackMe : [tryhackme.com/p/Dylanlpb](https://tryhackme.com/p/Dylanlpb)

</div>

> ### ⚠️ Pas de solutions dans ce dépôt — et c'est volontaire
> La charte Root-Me **interdit la publication des solutions** de ses challenges. Ce dépôt respecte cette règle : il documente **les domaines couverts et les notions de sécurité travaillées**, jamais la méthode d'exploitation ni les flags. L'objectif est de montrer **ce que je sais faire et comprendre**, pas de divulguer les réponses — ce qui est aussi, à mon sens, la bonne posture d'un professionnel de la sécurité.

---

## 📊 Vue d'ensemble

| Domaine | Challenges | Ce que j'y ai travaillé |
|---------|:---------:|-------------------------|
| 🌐 **Sécurité Web** | 7 | Injections SQL, XSS, contrôle d'accès, upload de fichiers |
| 💻 **Système** | 1 | Élévation de privilèges Linux via CVE |
| 📡 **Objets connectés (BLE)** | 3 | Analyse de protocoles Bluetooth Low Energy |
| 🔎 **Blue Team / SOC / Forensic** | 4 | Analyse de logs réseau, Windows, AD, métadonnées |

---

## 🌐 Sécurité Web

<table>
<tr><th>Challenge</th><th>Difficulté</th></tr>

<tr><td>

**API – Broken Access Control (MongoDB)**
Contrôle d'accès défaillant : comprendre pourquoi un identifiant **prévisible** (comme un ObjectId MongoDB, construit sur un timestamp et un compteur) ne doit **jamais** servir de jeton de sécurité. Notion clé : *Insecure Direct Object Reference* et prévisibilité des tokens.

</td><td align="center">🟠<br>Interm.</td></tr>

<tr><td>

**SQL Injection – Philoquote**
Injection SQL classique via requête `UNION` et **contournement d'un filtre** de saisie. Notion clé : la confusion données/instructions, et pourquoi seules les **requêtes préparées** protègent réellement.

</td><td align="center">🟠<br>Interm.</td></tr>

<tr><td>

**SQL Injection – En aveugle (blind)**
Injection SQL **sans retour visible** : extraction d'information par inférence (réponses booléennes / temporelles). Notion clé : une faille reste exploitable même sans message d'erreur affiché.

</td><td align="center">🟠<br>Interm.</td></tr>

<tr><td>

**XSS – DOM based**
Cross-Site Scripting **côté client** : le JavaScript de la page modifie le DOM à partir de données contrôlées par l'utilisateur sans les neutraliser. Notion clé : différence avec le XSS stocké/réfléchi, et l'importance de l'échappement en sortie.

</td><td align="center">🟠<br>Interm.</td></tr>

<tr><td>

**HTTP – Totemus-QCode**
Analyse fine des **requêtes et réponses HTTP** et de la logique applicative. Notion clé : lecture des échanges HTTP (en-têtes, méthodes, codes) à l'aide d'un proxy d'interception.

</td><td align="center">🟠<br>Interm.</td></tr>

<tr><td>

**File Upload – Double extensions**
Contournement d'un **filtrage d'extension** à l'upload. Notion clé : pourquoi valider une extension par liste noire est insuffisant, et comment durcir un upload (type MIME, liste blanche, renommage).

</td><td align="center">🟢<br>Facile</td></tr>

<tr><td>

**EDU-B – File Upload (Introduction)**
Bases du contrôle de **téléversement de fichiers** et des risques associés (exécution de code, stockage non sécurisé).

</td><td align="center">🟢<br>Facile</td></tr>
</table>

---

## 💻 Système & élévation de privilèges

<table>
<tr><th>Challenge</th><th>Difficulté</th></tr>
<tr><td>

**Linux Privesc – CVE**
Élévation de privilèges sous Linux en s'appuyant sur une **vulnérabilité connue (CVE)**. Notion clé : l'importance du **patch management** et de la veille sur les CVE côté défense.

</td><td align="center">🟢<br>Facile</td></tr>
</table>

---

## 📡 Objets connectés — Bluetooth Low Energy

<table>
<tr><th>Challenge</th><th>Difficulté</th></tr>
<tr><td>

**BLE – Authentification strip** · **Entrée utilisateur** · **Contrôles incohérents**
Analyse de communications **Bluetooth Low Energy** et des faiblesses d'authentification / de contrôle côté objet connecté. Notion clé : la sécurité d'un IoT ne doit pas reposer sur des vérifications incohérentes ou contournables côté client.

</td><td align="center">🟢🟠<br>Facile–Interm.</td></tr>
</table>

---

## 🔎 Blue Team — SOC & Forensic

<table>
<tr><th>Challenge</th><th>Difficulté</th></tr>

<tr><td>

**SOC Réseau – Scan de ports**
Détection d'un **scan de ports** dans des logs réseau. Notion clé : reconnaître les signatures d'une phase de reconnaissance côté défenseur.

</td><td align="center">🟠<br>Interm.</td></tr>

<tr><td>

**SOC AD – Authentification**
Analyse d'**événements d'authentification Active Directory**. Notion clé : repérer une activité anormale (échecs en série, horaires, comptes) dans les journaux Windows/AD.

</td><td align="center">🟠<br>Interm.</td></tr>

<tr><td>

**EDU-B – SOC Windows (Pilotes)**
Investigation d'**événements système Windows** (chargement de pilotes). Notion clé : lecture des journaux d'événements pour l'analyse d'incident.

</td><td align="center">🟢<br>Facile</td></tr>

<tr><td>

**EXIF – Christmas House**
Analyse des **métadonnées EXIF** d'une image. Notion clé : une photo transporte des données cachées (appareil, géolocalisation, dates) exploitables en forensic / OSINT.

</td><td align="center">🟢<br>Facile</td></tr>
</table>

---

## 🧰 Outils & méthodes

`Burp Suite` · `nmap` · `Wireshark` · analyse de journaux (réseau / Windows / AD) · outils d'analyse BLE · lecture de métadonnées (EXIF) · manipulation HTTP

## 🎯 Ce que ce parcours démontre

- Une **culture offensive ET défensive** : comprendre une attaque pour mieux la détecter et la corriger
- Une couverture **large** : Web, système, IoT et Blue Team / SOC
- De la **rigueur** : documenter proprement sans divulguer les solutions
- Une **pratique régulière** en complément de la formation et de [TryHackMe](https://tryhackme.com/p/Dylanlpb)

---

<div align="center">

*Formation cybersécurité — BUT R&T, IUT d'Auxerre.*
Les write-ups détaillés restent **privés**, conformément à la charte Root-Me.

</div>
