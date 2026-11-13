---
version: alpha
name: "[Nom]"
description: "[Une phrase sur l'identité visuelle]"
colors:
  ink: "#RRGGBB"          # texte principal
  background: "#RRGGBB"   # fond
  surface: "#RRGGBB"      # cartes, encarts, bandeaux
  accent: "#RRGGBB"       # action principale ou mot clé, une fois par écran ou par plan
  on-accent: "#RRGGBB"    # texte posé sur l'accent
  muted: "#RRGGBB"        # texte secondaire
  success: "#RRGGBB"
  warning: "#RRGGBB"
  danger: "#RRGGBB"
typography:
  display:
    fontFamily: "[Police des titres]"
    fontSize: 48px
    fontWeight: 700
    lineHeight: 1.1
  body:
    fontFamily: "[Police du texte]"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.5
  caption:
    fontFamily: "[Police du texte]"
    fontSize: 13px
    fontWeight: 500
    lineHeight: 1.4
  subtitle-video:
    fontFamily: "[Police des sous-titres]"
    fontSize: 64px
    fontWeight: 700
    lineHeight: 1.15
rounded:
  sm: 4px
  md: 8px
  lg: 16px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 32px
  xl: 64px
components:
  button-primary:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.on-accent}"
    rounded: "{rounded.md}"
    padding: 12px
  lower-third:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.sm}"
    padding: 16px
---

# Design — [Nom]

> À quoi [Nom] ressemble. Ce fichier découle de `SOUL.md` (la personnalité) et de `VOICE.md` (le
> ton). L'en-tête donne les valeurs exactes ; le texte dit **pourquoi** et **comment** les
> utiliser.

<!--
MODE D'EMPLOI
- Format DESIGN.md de Google : l'en-tête YAML pour les machines, le texte pour comprendre. Vérification : npx @google/design.md lint DESIGN.md
- Pour une app ou un site, garder « Components » complet. Pour la vidéo, garder la section « Vidéo ». Pour une simple ambiance : Overview, Colors, Typography, Do's and Don'ts.
- Supprimer ces commentaires, les crochets et les sections non retenues.
-->

## Overview

**L'idée :** [d'où vient la direction, en une ou deux phrases : un métier, une matière, un lieu, une
époque, en lien avec SOUL.md].

**L'élément signature :** [le seul élément qu'on retient, et ce qu'il porte. Ex. « un trait jaune
sous le mot clé, comme un coup de surligneur »].

**L'ambiance :** [3 à 5 mots]. Références : [films, lieux, objets, marques, et ce qu'on leur prend].

## Colors

| Token | Rôle | Règle d'usage |
|---|---|---|
| `ink` | Texte principal | |
| `background` | Fond | |
| `surface` | Cartes, bandeaux | |
| `accent` | Action principale, mot clé | [ex. une seule fois par écran ou par plan] |
| `muted` | Texte secondaire | |
| `success` / `warning` / `danger` | Statuts | Toujours accompagnés d'un mot, jamais la couleur seule |

Contraste du texte : au moins 4,5:1 sur son fond.

## Typography

- **[Police des titres]** : [pourquoi elle, graisses utilisées].
- **[Police du texte]** : [pourquoi elle].
- Corps de texte : 16 px minimum sur écran. Chiffres tabulaires pour les prix et les heures.
- Casse de phrase partout : pas de titres entièrement en capitales.
- Les polices sont des fichiers dans `assets/fonts/`, avec leur licence.

## Layout

[Grille, marges, densité. Une seule échelle d'espacement : celle de l'en-tête. Largeur de lecture :
72 caractères au maximum.]

## Elevation & Depth

[Ombres, bordures ou tout à plat, et pourquoi.]

## Shapes

[Rayons, formes récurrentes, motifs, icônes : style et épaisseur de trait.]

## Components

[Pour chaque composant : son rôle et ses états (normal, survol, focus, désactivé).]

- **Bouton principal** : [règle].
- **Carte** : [règle].
- **Bandeau nom (lower third)** : [règle, pour la vidéo].
- **Logo** : [versions, taille minimum, zone de protection, fonds autorisés].

---

## Vidéo

| Sujet | Règle |
|---|---|
| Formats | 9:16 (1080 × 1920) pour les réseaux · 16:9 (1920 × 1080) pour YouTube et le site · 1:1 (1080 × 1080) |
| Zones de sécurité | Rien d'important à moins de [100] px des bords. En 9:16, garder libres le bas et la droite (boutons du réseau). |
| Texte à l'écran | [64] px minimum en 1080 × 1920 · [6] mots maximum par ligne · [1,5] s minimum à l'écran |
| Sous-titres | Token `subtitle-video` · position : [tiers inférieur] · [contour ou fond] · le mot prononcé passe en `accent` |
| Rythme | Plan moyen de [1,5 à 3] s · on coupe sur le temps fort de la musique |
| Mouvement | [ex. entrées courtes de 0,3 s, départ franc, pas de rebond] · Interdit : [zooms gratuits, transitions fantaisie] |
| Logo | [où, quand, combien de temps : ex. dernier plan seulement, 1,5 s] |
| Son | Musique : [ambiance, tempo] · Voix off : [qui, débit] |

### Prompt de style (générateurs IA)

À coller à la fin de chaque prompt Veo, Kling, Runway ou Higgsfield, pour que tous les plans se
ressemblent :

```
[Lumière : ex. lumière naturelle de fin d'après-midi, ombres douces.]
[Palette : ex. tons chauds, ocre et vert sapin, noirs profonds, pas de couleurs saturées.]
[Image : ex. grain léger de pellicule 35 mm, faible profondeur de champ.]
[Cadrage : ex. caméra à hauteur d'épaule, mouvements lents, plans serrés sur les mains.]
[Ambiance : ex. calme, concret, artisanal.]
[À éviter : ex. néons, rendu 3D brillant, texte généré dans l'image.]
```

---

## Do's and Don'ts

| À faire | À éviter |
|---|---|
| | |
| | |

### Garde-fous anti-générique

Avant de valider, vérifier que la direction n'utilise aucun de ces réflexes, sauf choix délibéré et
justifié :

- [ ] Fond crème avec un titre en serif et un accent terre cuite.
- [ ] Fond quasi noir avec un seul accent vert acide ou vermillon.
- [ ] Dégradé violet-bleu « tech ».
- [ ] Surtitre en capitales espacées au-dessus de chaque titre.
- [ ] Métadonnées séparées par des points médians (« A · B · C »).
- [ ] Gros chiffre en vedette avec un petit libellé, par défaut.
- [ ] Un seul mot du titre mis en couleur ou en italique, partout.
- [ ] Cartes identiques avec la même ombre grise.
- [ ] Polices par défaut (Arial, Inter, Georgia) sans raison.
- [ ] Vidéo : texte qui tremble, zoom lent permanent, transitions toutes différentes.

---

## Variantes

<!-- Une variante garde l'âme et la voix, et ne change qu'une dimension. Ne lister que ce qui change. -->

### [Nom de la variante] — [quand on l'utilise : mode sombre, été, TikTok, campagne X…]

| Ce qui change | Valeur |
|---|---|
| | |
