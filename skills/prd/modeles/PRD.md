# PRD — [Nom du produit] [version]

> [Une phrase : ce que c'est, pour qui.]
> Statut : [à construire / en cours / livré]. Document de référence pour Claude Code.
> [AAAA-MM-JJ] · relu par l'utilisateur : non

<!--
MODE D'EMPLOI
- Précis sur le quoi et le pourquoi, ouvert sur le comment.
- Ce qui est décidé s'écrit comme une règle. Ce qui est incertain s'écrit comme une option à justifier.
- Taille proportionnée : une vidéo, une page ou une tâche garde les sections 1 à 6 et 13, plus son module (logiciel ou vidéo). Un produit complet utilise tout ce qui sert.
- Sections non retenues : les supprimer, ne pas les laisser vides.
- Supprimer ces commentaires et les crochets avant de lancer la production.
-->

---

## 1. Phrase d'arrivée

**C'est fini quand** [qui] peut [action visible] [dans telle condition difficile], sans [ce qui doit disparaître].

<!-- Test : la scène est-elle observable ? Un acteur précis ? Réponse oui/non possible ? Une contrainte qui gêne ? -->

## 2. Critères de réussite globaux

1. [Test binaire n° 1, vérifiable en moins d'une minute]
2. [Test binaire n° 2]
3. [Test binaire n° 3]

<!-- Trois maximum. Si les trois passent, la version est livrable. -->

---

## 3. Problèmes à résoudre (classés par douleur)

| # | Problème | Conséquence concrète | Couvert dans cette version |
|---|----------|---------------------|----------------------------|
| P1 | [le plus douloureux] | [ce que la personne perd : temps, argent, client, sérénité] | Oui |
| P2 | | | Oui |
| P3 | | | Non, [version] |

<!-- Chaque fonctionnalité de la section 6 doit renvoyer à un problème de cette table. Sinon, elle sort. -->

## 4. Utilisateurs, rôles et moment d'usage

| Rôle | Qui | Besoin principal | Où et sur quel appareil |
|------|-----|-----------------|-------------------------|
| [Rôle 1] | | | |
| [Rôle 2] | | | |

**Moment d'usage typique :** [la scène réelle : où est la personne, ce qu'elle a dans les mains, combien de temps elle a].

### Permissions (si plusieurs rôles)

| Domaine | [Rôle 1] | [Rôle 2] | [Rôle 3] |
|---------|:-------:|:-------:|:-------:|
| [domaine] | ✅ | 👁 | ❌ |

Légende : ✅ complet · 👁 lecture seule · 🔒 limité (note) · ❌ aucun accès

## 5. Parcours principal (de A à B)

```
[Point A : la situation de départ]
  → [étape]
  → [étape]
  → [Point B : le résultat obtenu]
```

<!-- Tout ce qui ne sert pas ce parcours sort de cette version. -->

---

## 6. Périmètre

### 6.1 Dans cette version

**Indispensable (sans ça, pas de livraison)**
- [fonction] → répond à [P1]

**Souhaitable (si le calendrier tient)**
- [fonction] → répond à [Px]

### 6.2 Hors de cette version

| Fonctionnalité | Raison de l'exclusion | Version cible |
|----------------|----------------------|---------------|
| [fonction] | [pourquoi pas maintenant] | [V1.1 / V2 / jamais] |

## 7. Spécifications fonctionnelles

### F1 — [Module]

**Stories**
- En tant que [rôle], je [action] pour [bénéfice].

**États**

| État affiché | L'action qui y mène |
|--------------|---------------------|
| [état] | [story ou événement : « le client signe », « la date d'expiration passe »] |

<!-- Un état sans action est un trou : ajouter l'action, ou retirer l'état. -->

**Critères d'acceptation**
- [critère binaire]
- [état vide : ce qui s'affiche et l'action proposée]
- [erreur : ce qui s'est passé et comment corriger]

<!-- Répéter F2, F3… -->

## 8. Données de démonstration

| [Champ] | [Champ] | [Champ] | [Statut] |
|---------|---------|---------|----------|
| [valeur réaliste] | | | |
| | | | |
| | | | |

<!-- Des valeurs du vrai métier, jamais de « Lorem » ni de « Test 1 ». Elles servent à la fois de démo et de jeu de test. Pour une vidéo personnalisée : 3 vrais exemples de prospects. -->

## 9. Règles métier invariantes

- [règle qui ne doit jamais être violée, ex. un montant en centimes, un numéro sans trou, un document figé après émission]

## 10. Exigences non fonctionnelles

| Domaine | Exigence |
|---------|----------|
| Performance | |
| Mobile / terrain | |
| Accessibilité | |
| Données personnelles | |
| Langue et formats | |

## 11. Conformité et cadre légal

- [obligation applicable au domaine : droits d'image, droits musicaux, RGPD, mentions publicitaires…] — à valider par [expert concerné].

<!-- Supprimer si le domaine n'a pas d'obligation particulière. -->

## 12. Référence visuelle

La charte est dans `docs/marque/` (`SOUL.md`, `VOICE.md`, `DESIGN.md`). La direction retenue est **[nom]**, illustrée dans `docs/marque/[fichier].html`. Ce qui est produit reprend ses couleurs, ses polices, ses composants et son ton ; les mots s'adaptent à ce PRD.

---

## 13. Question avant construction

[La question dont la réponse peut changer le périmètre. Ex. : « Faut-il que deux personnes voient les mêmes données ? Si oui, il faut des comptes et une base de données. » Ou : « La vidéo est-elle regardée avec le son ? Si non, tout passe par le texte à l'écran. »]

<!-- On ne construit pas tant qu'elle n'a pas de réponse. -->

## 14. Risques et questions ouvertes

| Sujet | Risque ou question | Comment on le saura |
|-------|-------------------|---------------------|
| | | |

---

# Module logiciel

<!-- À garder uniquement pour un produit construit en code (app, site, outil). Ce module se réécrit quand la technique change ; le noyau au-dessus ne bouge pas. -->

## 15. Stack

| Couche | Choix | Pourquoi |
|--------|-------|----------|
| | | |

## 16. Modèle de données

```
[table]   [champs principaux]
```

## 17. Structure du projet

```
[arborescence]
```

## 18. Règles pour `CLAUDE.md`

- Lire le PRD et `docs/marque/` avant toute fonctionnalité.
- Les règles métier de la section 9 vivent dans [dossier], en fonctions pures testées.
- Couleurs, tailles et polices uniquement via les tokens de `docs/marque/DESIGN.md`.
- [règle propre au projet]

## 19. Jalons

| Jalon | Contenu | Fin de jalon = |
|-------|---------|----------------|
| J0 | | [scène démontrable] |
| J1 | | |

---

# Module vidéo

<!-- À garder uniquement pour une vidéo ou une série de vidéos. Le noyau dit à qui on parle et ce qui doit se passer après le visionnage ; ce module dit comment la vidéo est faite. -->

## 20. Format et diffusion

| Sujet | Choix |
|-------|-------|
| Où elle est vue | [LinkedIn, Instagram, TikTok, YouTube, e-mail de prospection, site…] |
| Format | [9:16 vertical · 16:9 horizontal · 1:1 carré] |
| Durée | [en secondes] |
| Son | [regardée avec ou sans le son → sous-titres obligatoires ou non] |
| Langue | |

## 21. Message

- **Une seule idée** : [ce que la personne doit retenir, en une phrase].
- **Accroche (0 à 3 s)** : [ce qui l'arrête de faire défiler].
- **Preuve** : [ce qu'on montre plutôt que ce qu'on promet].
- **Appel à l'action** : [verbe + objet : « Répondez à ce message », « Réservez un appel »].

## 22. Découpage

| # | Durée | À l'écran | Texte à l'écran / voix off | Source |
|---|-------|-----------|----------------------------|--------|
| 1 | 0–3 s | [accroche] | | [HyperFrames · générateur IA · capture d'écran · tournage · banque d'images] |
| 2 | | | | |
| 3 | | [appel à l'action] | | |

## 23. Personnalisation (si série)

<!-- Supprimer si la vidéo est unique. -->

- **Ce qui change d'une vidéo à l'autre** : [prénom, entreprise, logo, capture de son site, chiffre…]
- **D'où viennent les données** : [fichier CSV, liste, site] — 3 exemples réels en section 8.
- **Ce qui ne change jamais** : [structure, musique, durée, appel à l'action].

## 24. Production

| Sujet | Choix |
|-------|-------|
| Outil | [HyperFrames · Veo · Kling · Runway · montage…] |
| Fichiers fournis (`assets/`) | [logo, musique, voix, images] |
| Export | [résolution, nommage : `AAAA-MM-JJ-sujet-format.mp4`] |
| Validation | [qui regarde, sur quel appareil, avant envoi] |

| Jalon | Fin de jalon = |
|-------|----------------|
| V0 | Une vidéo validée de bout en bout |
| V1 | [la série, ou les déclinaisons de format] |

---

## Relecture avant envoi

- [ ] La phrase d'arrivée est observable, avec un acteur et une contrainte.
- [ ] Chaque fonctionnalité (ou chaque scène) renvoie à un problème classé.
- [ ] Chaque statut affiché peut être atteint par une action (aucun état orphelin).
- [ ] Chaque liste a un état vide, chaque formulaire a un message d'erreur.
- [ ] Les exclusions ont une raison et une version cible.
- [ ] Les données de démonstration viennent du vrai métier.
- [ ] Vidéo : l'accroche tient en 3 secondes et se comprend sans le son.
- [ ] La question avant construction a une réponse.

## Glossaire

| Terme | Définition dans ce produit |
|-------|----------------------------|
| | |
