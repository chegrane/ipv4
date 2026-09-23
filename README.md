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

## Le laboratoire en bref (30 min)

| Partie | Durée | Environnement | Ce qu'on fait |
|---|---|---|---|
| **0** | 5 min | Windows | `ipconfig`, `ping 127.0.0.1`, `ping` l'ordinateur du voisin |
| **1** | 15 min | Packet Tracer | Un réseau local : 3 PC + 1 switch, adressage statique, `ping` entre les postes |
| **2** | 10 min | Packet Tracer | Un 2e réseau + un routeur, passerelle sur les 5 PC, `ping` d'un réseau à l'autre, puis on efface la passerelle pour voir ce qui se passe |

### Topologie et adressage (partie 2)

```
RÉSEAU A : 192.168.1.0                                         RÉSEAU B : 192.168.2.0
PC1, PC2, PC3 ── Switch 1 ── Gig0/0/0 [ ROUTEUR ISR4331 ] Gig0/0/1 ── Switch 2 ── PC4, PC5
                        192.168.1.1                   192.168.2.1
```

| Équipement | Adresse IPv4 | Masque | Passerelle par défaut |
|---|---|---|---|
| PC1 / PC2 / PC3 | 192.168.1.10 / .11 / .12 | 255.255.255.0 | 192.168.1.1 |
| Routeur — Gig0/0/0 | 192.168.1.1 | 255.255.255.0 | — |
| Routeur — Gig0/0/1 | 192.168.2.1 | 255.255.255.0 | — |
| PC4 / PC5 | 192.168.2.10 / .11 | 255.255.255.0 | 192.168.2.1 |

> ⚠️ **Le piège classique :** sur un routeur Cisco, les interfaces sont éteintes par défaut. Il faut cocher **Port Status : On** sur les deux interfaces, sinon les liens restent rouges.

## Installer Cisco Packet Tracer

Packet Tracer est **gratuit** ; il faut simplement un compte Cisco Networking Academy.

- Page officielle : <https://www.netacad.com/cisco-packet-tracer>
- Téléchargement : <https://www.netacad.com/resources/lab-downloads?courseLang=fr-FR>
- Cours d'introduction gratuit, en français — *Getting Started with Cisco Packet Tracer* : <https://www.netacad.com/fr/courses/getting-started-cisco-packet-tracer?courseLang=fr-FR>

## Pour aller plus loin

Prochains cours : le binaire et la notation /24 → les sous-réseaux → adresses privées et publiques.

---

*« There's no place like 127.0.0.1 »*
