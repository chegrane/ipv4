# L'adressage IPv4 — cours et laboratoire

Matériel d'un mini-cours d'introduction à l'adressage IPv4, suivi d'un laboratoire pratique de 30 minutes sous Windows et Cisco Packet Tracer.

- **Public :** étudiantes et étudiants de 2e session, sans connaissance préalable en réseau (base de Windows).
- **Auteur :** Ibrahim Chegrane — Cégep de Sherbrooke, Département d'informatique
- **Date :** 23 septembre 2026

## Objectifs

À la fin du cours, l'étudiant·e sait :

1. **Lire une adresse IPv4** : 4 octets de 8 bits = 32 bits, chacun de 0 à 255.
2. **Trouver le réseau grâce au masque** : avec `255.255.255.0`, 255 = la partie réseau (la rue), 0 = la partie hôte (la maison).
3. **Comprendre la passerelle par défaut** : la sortie vers les autres réseaux — un routeur, avec une adresse dans chaque réseau qu'il relie.

## Contenu du dépôt

| Fichier | Description |
|---|---|
| [Énoncé du laboratoire](laboratoire/enonce_lab_etudiant.pdf) | L'énoncé remis aux étudiants (1 page). |
| [Guide tutoriel pas à pas](laboratoire/guide_tutoriel_pas_a_pas.pdf) | Chaque étape dans Packet Tracer, avec captures d'écran, pour celles et ceux qui bloquent. |
| [Grille de vérification](laboratoire/grille_verification.pdf) | Ce qui est vérifié pour chaque partie (0, 1 et 2). |
| [Présentation (PDF)](presentation/Presentation-IPv4.pdf) | Les diapositives du cours. |
| [Fichier Packet Tracer — solution](packet-tracer/Lab1_Lab2_Solution.pkt) | La topologie complète et configurée. **À ouvrir après avoir fait le laboratoire.** |

Les fichiers `.html` du dossier `laboratoire/` sont les sources des PDF (avec leurs images dans `laboratoire/images/`).

## Installer Cisco Packet Tracer

Packet Tracer est **gratuit** ; il faut simplement un compte Cisco Networking Academy.

- Page officielle : <https://www.netacad.com/cisco-packet-tracer>
- Téléchargement : <https://www.netacad.com/resources/lab-downloads?courseLang=fr-FR>
- Cours d'introduction gratuit, en français — *Getting Started with Cisco Packet Tracer* : <https://www.netacad.com/fr/courses/getting-started-cisco-packet-tracer?courseLang=fr-FR>

## Pour aller plus loin

Prochains cours : le binaire et la notation /24 → les sous-réseaux → adresses privées et publiques.

---

*« There's no place like 127.0.0.1 »*
