# Warp

## C'est quoi

Warp est **un terminal moderne**, qui remplace PowerShell ou Terminal. Il est gratuit pour
commencer. Pour toi, il a trois avantages :

- **Tu vois ton dossier** : un explorateur de fichiers est intégré.
- **Tu lis et modifies un fichier** sans ouvrir d'autre logiciel : il y a un petit éditeur intégré.
- **Claude Code tourne dedans** avec une barre d'outils : tu peux glisser une image, dicter, et
  voir les fichiers modifiés.

Warp a aussi sa propre IA. Tu n'en as pas besoin : on l'utilise comme terminal pour faire tourner
Claude Code.

## L'installer

Le plus simple, c'est de demander à Claude : « Installe-moi Warp. »

Sinon, une commande suffit :

| Système | Commande |
|---------|----------|
| Windows | `winget install Warp.Warp` |
| Mac | `brew install --cask warp` |

Tu peux aussi le télécharger sur https://www.warp.dev/download.

## Ta façon de travailler avec

1. Ouvre Warp.
2. Va dans le dossier de ton projet :

   ```powershell
   cd $HOME\Documents\mon-projet
   ```

3. Tape `claude`.
4. Ouvre l'explorateur de fichiers de Warp pour voir ton dossier pendant que Claude travaille.

C'est tout. Une fenêtre Warp = un projet = une session Claude.

## Pour aller plus loin

- Documentation : https://docs.warp.dev
- Lancer Claude Code dans Warp : https://docs.warp.dev/agent-platform/third-party-agents/overview
