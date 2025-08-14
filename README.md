# Tic‑Tac‑Toe+ (WebRTC • P2P)

Jeu Tic‑Tac‑Toe moderne, mobile‑first, thème auto, a11y, micro‑interactions, **mode en ligne sans serveur** via WebRTC (copier‑coller).

## Jouer en ligne (Maria 💜)
1. Ouvre la page GitHub Pages : `https://<user>.github.io/<repo>/`
2. **En ligne → Créer** (hôte, joue X) → *Créer une invitation* → *Copier code* → envoie à Maria.
3. Maria : **En ligne → Rejoindre** → colle le code → *Générer ma réponse* → *Copier* → te renvoie.
4. Hôte : colle la **réponse** → *Valider la réponse* → statut **Connecté** → c’est parti.

Liens rapides :
- Hôte : `?online=host`
- Invitée : `?online=join`

Ex. `https://<user>.github.io/<repo>/?online=host`

## Déploiement GitHub Pages
- Dépose `index.html`, `.nojekyll`, `assets/icon.svg`, `manifest.webmanifest`.
- **Settings → Pages** : *Deploy from a branch* → `main` / `(root)` → *Save*.
- URL verra le jour en ~1 minute : `https://<user>.github.io/<repo>/`.

## Détails techniques
- WebRTC DataChannel (STUN: `stun.l.google.com:19302`).
- Pas de serveur TURN (si NAT très strict : possible échec de connexion → jouer en local).
- Persistance : `localStorage` (scores, préférences, état en cours).
- Accessibilité : lecture d’état, `progressbar`, navigation clavier, focus trap modal.

## Licence
MIT