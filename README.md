# BupoTFT — releases

Binaires autonomes de **BupoTFT**, un coach Teamfight Tactics qui s'affiche en overlay par-dessus le jeu et conseille en temps réel : compo méta à suivre, achats dans le shop, économie / niveau, items à crafter.

## Télécharger

Va dans **[Releases](../../releases)** → dernier `BupoTFT.exe`.

## Prérequis

- Windows 10/11 **64 bits** — aucun autre prérequis (Python, Qt et les modèles OCR sont embarqués dans l'exe).
- TFT en mode **fenêtré sans bordure**, idéalement en 1920×1080.

Au premier lancement Windows peut afficher « Windows a protégé votre ordinateur » (exécutable non signé) → **Informations complémentaires → Exécuter quand même**.

## Utilisation

1. Double-clique `BupoTFT.exe` — la fenêtre « En attente d'une partie » s'affiche (données du set et compos méta téléchargées une fois, ensuite en cache).
2. Lance TFT et entre en partie : l'overlay apparaît automatiquement — badges ACHETER / À VOIR / PASSER sur le shop, pastilles d'économie, panneau de compo à droite.
3. Raccourcis : `Alt+Shift+M` déplacer l'overlay · `Alt+Shift+C` replier le panneau · `Alt+Shift+H` masquer.
4. Fin de partie → la fenêtre d'attente revient. Quitter via son ✕ ou l'icône BupoTFT de la zone de notification.

Réglages, positions et cache : `%APPDATA%\bupotft`. Logs : `%APPDATA%\bupotft\bupotft.log`.

## Ce que fait (et ne fait pas) l'outil

- **Lecture d'écran + OCR uniquement** — aucune lecture mémoire, injection, ni action automatisée sur le jeu. L'overlay est en lecture seule.
- Données du set : Community Dragon ; compos méta : MetaTFT (API non officielle — peut changer).
- Comme tout outil tiers TFT, vérifie la [politique Riot en vigueur](https://support-developer.riotgames.com/) avant usage en ranked.

## Limites

- Calibré sur 1920×1080 ; d'autres résolutions peuvent nécessiter un recalage.
- Les unités du board sont déduites (traits), pas reconnues visuellement ; un objet inconnu s'affiche « ? ».
- En combat, le compte d'unités peut fluctuer brièvement.
