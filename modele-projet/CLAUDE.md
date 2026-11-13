# [Nom du projet]

[Une phrase : ce que c'est, et pour qui.]

## À lire avant de travailler

- `docs/PRD.md` : ce qu'on construit, et quand c'est fini.
- `docs/marque/SOUL.md`, `VOICE.md`, `DESIGN.md` : qui est la marque, comment elle parle, à quoi
  elle ressemble. Tout visuel, texte ou vidéo les respecte.

S'ils n'existent pas encore, propose `/prd` ou `/charte` avant de produire quoi que ce soit.

## Règles

- Pas de vidéo, de page ni de code avant que le PRD soit relu et validé.
- Couleurs, polices et tailles : uniquement celles de `docs/marque/DESIGN.md`.
- Les textes, voix off et sous-titres suivent `docs/marque/VOICE.md`.
- Les fichiers fournis (logos, images, musiques, polices) sont dans `assets/`. N'en invente pas, et
  ne remplace pas un logo par un texte.
- N'invente jamais un chiffre, un avis ou un client.
- Pour une tâche de plus de quelques étapes, propose d'abord un plan.
- Réponds en français.

## Commandes

<!-- Remplace par les commandes de ton projet. Exemple pour une vidéo HyperFrames : -->
- `npx hyperframes preview` : prévisualiser la vidéo dans le navigateur
- `npx hyperframes render` : exporter en MP4

## Où sont les choses

- `docs/` : PRD et charte
- `assets/` : fichiers fournis
- `exports/` : les rendus finaux, nommés `AAAA-MM-JJ-sujet-format.mp4`
